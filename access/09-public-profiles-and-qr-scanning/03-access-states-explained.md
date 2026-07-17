---
title: "Access States Explained"
---
{/* category: Public Profiles & QR Scanning */}

When a badge is scanned, the result shown to the visitor depends on the current state of the badge and employee record. This article describes every possible outcome and what triggers it.

## Employee Badge States

### ✅ Active — Profile Shown

All checks pass. The visitor sees the employee's public profile with the information configured in the Public Page Editor.

This state requires:
- The employee status is **Active**
- The badge status is **Active**
- Public verification is enabled
- No access schedule restriction applies at the current time
- No PIN is required (or the correct PIN has been entered)

### 🔒 Badge Reported Lost

The badge has been reported as lost or stolen, either by the employee through the portal or by an administrator.

The visitor sees a **Badge Reported Lost** message with an amber warning icon. The scan is logged as `badge_lost`.

### ⚠️ Badge Suspended

The employee or their badge has been temporarily suspended by an administrator.

The visitor sees a **Badge Suspended** message. This is a temporary state — the badge can be reactivated.

### ✗ Badge Deactivated

The badge has been permanently deactivated. This differs from suspended in that deactivation is not intended to be reversed.

The visitor sees a **Badge Deactivated** message with a slash icon.

### ⏱ Badge Expired

The badge has reached its expiration date.

The visitor sees a **Badge Expired** message.

### ✗ Employment Ended

The employee record has a **Terminated** status. The visitor sees an **Employment Ended** message.

### 🔒 Public Verification Disabled

The organization has turned off public badge scanning in settings. All scans for all employees are blocked.

If **Business Card Mode** is also enabled, the visitor sees the employee's business card instead of this error.

### 🔒 Profile Deactivated

An administrator has disabled the public profile for this specific employee. Other employees' profiles continue to work normally.

### 🔔 System Maintenance

The system is under maintenance. All public scans are temporarily blocked and visitors see a maintenance notice.

### 🛡 Restricted Access (Authenticated Scanners Only)

This employee's badge is configured to require an authenticated scanner — meaning the scanner must be signed in to an account within the same organization.

An unauthenticated visitor (such as someone pointing a phone camera) sees a **Restricted Access** message and is prompted to log in.

### 🕐 Outside Work Hours

This employee has an access schedule configured, and the scan is happening outside the allowed time window. The visitor is shown the allowed hours and days so they know when to return.

### ❓ Invalid Badge

No employee, guest badge, or ticket matches the scanned identifier — the badge ID does not exist in the system. The visitor sees an **Invalid Badge** page on a dark background with a red X icon.

---

## Guest Badge States

| State | What the visitor sees |
|---|---|
| **Active** | Green checkmark — "Valid Badge" |
| **Expired** | Amber clock — "Expired Badge" |
| **Revoked** | Red X — "Revoked Badge" |
| **Not found** | Red X — invalid badge error |

## Ticket States

| State | What the visitor sees |
|---|---|
| **Active** | Green checkmark |
| **Expiring soon** | Amber clock — expires within 3 days |
| **Expired** | Amber clock |
| **Used / Revoked** | Red X |
