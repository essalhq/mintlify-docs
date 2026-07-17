---
title: "Ticket Status and Validity"
---

{/* keywords: ticket status, active ticket, expired ticket, expiring soon, revoked ticket, ticket validity */}
{/* category: Tickets */}
{/* audience: Admins, Managers, Security */}

Each ticket has a status that reflects its current validity. Statuses are automatically calculated from the ticket's expiry date and its stored state — no manual updates are required.

![Tickets list showing tickets with various statuses including active, expiring soon, and expired](../screenshots/tickets-list.png)

---

## Status Overview

| Status | Color | Meaning |
|---|---|---|
| **Active** | Green | Ticket is valid and within its validity window |
| **Expiring Soon** | Amber | Ticket is valid but expires within the next 3 days |
| **Expired** | Gray | The validity window has passed — the ticket is no longer valid |
| **Revoked** | Red | The ticket was manually cancelled by an administrator |

---

## Active

A ticket is **Active** when:
- Its stored status is `active`, **and**
- Either it has no expiry date, or the current time is before the `valid until` date

Active tickets are fully valid and the verification page will show an access confirmation in your organization's brand color.

---

## Expiring Soon

A ticket is **Expiring Soon** when it is still active but its `valid until` date is **within 3 days** of today. This status helps administrators identify tickets that need to be renewed before they expire.

The verification page shows an amber status badge for expiring-soon tickets.

---

## Expired

A ticket is **Expired** when its `valid until` date has passed. Expiry is automatic — no admin action is required.

- The ticket row in the admin list is shown with reduced opacity and a gray background
- The verification page displays an **Expired** badge in amber
- Expired tickets cannot be revoked (the Revoke action is hidden for them)

> **Note:** Expiry is calculated client-side at display time. The stored ticket record keeps `status: "active"` in the database — only the displayed status changes to Expired.

---

## Revoked

A ticket is **Revoked** when an administrator has manually cancelled it using the **Revoke** action. Revoking sets the ticket's stored status to `used`, which immediately invalidates it.

- The verification page shows a **Revoked** badge in red
- The `valid until` date is shown with a strikethrough
- Revoked tickets cannot be revoked again

**When to revoke:**
- The employee no longer needs the pass before its expiry
- The ticket was issued in error
- The employee was terminated or suspended

---

## Tickets That Never Expire

If a ticket was created with the **Ticket expires** checkbox unchecked, it has no `valid until` date. These tickets remain **Active** indefinitely until they are manually **Revoked** or **Deleted**.

On the verification page, the validity field shows **"Never expires"** in green text.

---

## Filtering by Status

In the **Tickets** list, use the status tab bar above the table to filter:
- **All** — shows every ticket regardless of status
- **Active** — only currently valid tickets (includes Expiring Soon)
- **Expiring soon** — tickets that expire within 3 days
- **Expired** — tickets whose validity window has passed
