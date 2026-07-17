---
title: "The Guest Verification Page"
---

{/* keywords: guest verification page, badge scan page, guard view, visitor badge page, QR scan result, badge public page */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Security, Reception */}

The Guest Verification Page is the public-facing page that guests and security guards see when a badge link is opened. No login is required.

---

## What the Page Shows

The verification page is designed to give a guard all the information they need in a single glance.

### Visual Elements (Top to Bottom)

1. **Organization logo** — pulled from your whitelabel settings
2. **Status bar** — a full-width colored bar at the top indicating the badge status at a glance
3. **Status pill** — text label ("Valid Badge", "Expired Badge", or "Revoked Badge")
4. **Guest name** — displayed as the main heading
5. **Guest company** — shown below the name (if provided), with a building icon

### Detail Rows

| Icon | Field | Shown when |
|---|---|---|
| Tag | **Purpose** | Always |
| User | **Host** | Always (shows `host_name`) |
| Calendar | **Valid Until** | Always |
| Map Pin | **Permitted Zones** | Only if access zones were assigned |
| Map Pin | **Address / Location** | Only if an address was added; links are clickable (opens maps) |

> **Note:** Guest email addresses are never displayed on the public verification page. Only the information a guard needs is shown.

---

## Status Colors

The color of the top bar and the status pill text changes based on badge status:

| Status | Bar color | Pill text |
|---|---|---|
| Active (within validity window) | Blue | "Valid Badge" |
| Expired (past `valid until`) | Amber | "Expired Badge" |
| Revoked (cancelled by admin) | Red | "Revoked Badge" |

Security personnel should **only grant access** when the bar is **blue** (Valid Badge).

---

## Language Support

The page automatically detects the visitor's browser language and displays the content in the matching language. Supported languages:

- English
- Arabic (right-to-left layout)
- French
- Spanish
- German

A **language selector** is available at the bottom of the page if the guest or guard wants to switch manually.

---

## Invalid or Deleted Badges

If the badge URL contains a token that doesn't exist (e.g., the badge was deleted or the link was altered), the page displays an error state:

- An X-circle icon with an error message
- No badge information is shown

Guards should treat this result the same as a **Revoked** badge — access should not be granted.

---

## Branding

The verification page uses your organization's branding from the **Whitelabel Settings**:
- Company logo
- Company name (also used in the page's SEO title: *"\{Status\} — \{Guest Name\} — \{Company Name\}"*)

This ensures the page looks professional and trusted to guests and security staff.

---

## What Guests See vs What Guards See

Both guests and security guards open the same URL. The page is designed for both audiences:

- **Guests** can see their visit details to confirm the badge is correct
- **Guards** can confirm the badge is valid, check the access zones, and verify the guest's name matches their ID

Neither guests nor guards can modify the badge from this page.

