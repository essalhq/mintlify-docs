---
title: "How Public Badge Scanning Works"
---
{/* category: Public Profiles & QR Scanning */}

Every employee badge contains a QR code. When someone scans it, they are taken to a public verification page that shows the employee's profile — no login required. This article explains the full flow from scan to display.

## What Happens When a Badge Is Scanned

1. The scanner (a phone camera, a check-in device, or a browser) opens the URL encoded in the QR code.
2. The system looks up the badge ID and retrieves the employee's record.
3. A series of checks runs to determine whether access should be granted, blocked, or limited.
4. The appropriate page is displayed to the scanner: a full public profile, a business card, a restricted-access screen, a PIN entry screen, or an invalid-badge page.

The entire flow happens automatically and requires no action from the employee or an administrator.

## Entry Points

| URL pattern | What it verifies |
|---|---|
| `/{badgeId}` | Employee badge (subdomain or main domain) |
| `/public/{badgeId}` | Employee badge (explicit public path) |
| `/guest/{token}` | Guest badge |
| `/ticket/{ticketId}` | Event ticket |

## The Verification Checks

When an employee badge URL is opened, the system works through the following checks in order:

1. **Badge lookup** — the badge ID is matched to an employee record. If no match is found, the visitor sees the Invalid Badge page.
2. **Tenant check** — if the URL is on a company subdomain, the badge must belong to that company. A mismatch shows the Invalid Badge page.
3. **Blocked status** — if the badge or employee is suspended, lost, deactivated, expired, or terminated, the visitor is shown a Restricted Access page explaining why.
4. **Public verification setting** — if the organization has disabled public badge scanning, the scan is blocked (or redirected to the business card, if that option is enabled).
5. **Maintenance mode** — if the system is under maintenance, all public scans are blocked.
6. **Authenticated scanners only** — if this employee's badge requires a logged-in scanner, the visitor must be signed in to an account in the same organization.
7. **Access schedule** — if the employee has restricted hours, scans outside those hours show a "Outside Work Hours" message.
8. **2FA PIN** — if a PIN is required for this employee's badge, the visitor must enter the correct 4-digit code before the profile is shown.

Once all checks pass, the employee's public profile is displayed.

## Guest Badge and Ticket Scanning

**Guest badges** are verified at `/guest/{token}`. The system checks the token and displays the guest's name, company, visit purpose, host name, authorized access zones, and validity dates. The badge can show as Valid, Expired, or Revoked.

**Tickets** are verified at `/ticket/{ticketId}`. The system derives the ticket's current state and displays it as Active, Expiring Soon, Expired, or Revoked.

## Scan Logging

Every scan — successful or not — is recorded automatically. Successful employee badge views are logged with the scanner's device type, browser, and IP address. Blocked scans are logged with the reason. See Scan Logging for details.
