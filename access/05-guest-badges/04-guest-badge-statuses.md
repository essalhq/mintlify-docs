---
title: "Guest Badge Statuses"
---

{/* keywords: guest badge status, active badge, expired badge, revoked badge, badge validity, badge states */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception, Security */}

Each guest badge has a status that determines whether access should be granted. This article explains what each status means and how it is set.

![Guest Badges list showing active, expired, and revoked badges with colored status pills](../screenshots/guest-badges-list.png)

---

## Status Overview

| Status | Color | Meaning |
|---|---|---|
| **Active** | Green | Badge is valid — the guest may be granted access |
| **Expired** | Amber | Validity window has passed — should not grant access |
| **Revoked** | Red | Manually cancelled by an admin — do not grant access |

---

## Active

A badge is **Active** when:
- Its database status is `active`, **and**
- The current time is within the `valid from` / `valid until` window

An active badge shows a **green** status pill in the admin list and a **blue** top bar on the public verification page.

> **Newly created badges** are active immediately unless you set a future `valid from` date.

---

## Expired

A badge is **Expired** when its `valid until` time has passed. Expiry is **automatic** — no manual action is needed.

- The expiry is calculated client-side on each page load
- The underlying database record remains as `active`; only the displayed status changes
- The public verification page also evaluates the `valid until` field and shows **Expired** to security guards

An expired badge shows an **amber** status pill in the admin list and an **amber** top bar on the verification page.

> **Important:** An expired badge cannot be reactivated. If a guest needs to extend their visit, create a new badge with an updated validity window.

---

## Revoked

A badge is **Revoked** when an admin explicitly cancels it before or after its validity window. This allows you to immediately block access even if the badge's `valid until` has not been reached yet.

When a badge is revoked:
- Its database status is set to `revoked`
- The name of the admin who revoked it and the timestamp are recorded (`revoked_by` and `revoked_at`)
- The verification page shows **Revoked Badge** in red to any guard who scans it

To revoke a badge:
1. Navigate to **Guest Badges**
2. Click the **three-dot menu (⋮)** on the badge row
3. Select **Revoke**
4. Confirm the action in the dialog

> **Note:** The Revoke option only appears for badges that are currently **Active**. Expired and already-revoked badges cannot be revoked again.

---

## What Security Guards See

On the public verification page, the status is communicated visually and textually:

| Status | Top bar color | Status pill text |
|---|---|---|
| Active | Blue | "Valid Badge" |
| Expired | Amber | "Expired Badge" |
| Revoked | Red | "Revoked Badge" |

If a guard scans a link that doesn't exist (the token is invalid or the badge was deleted), they see an error screen with an X icon and an explanatory message.

