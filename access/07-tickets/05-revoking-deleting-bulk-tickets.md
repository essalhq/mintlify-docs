---
title: "Revoking and Deleting Tickets"
---

{/* keywords: revoke ticket, delete ticket, bulk delete, cancel ticket, remove ticket */}
{/* category: Tickets */}
{/* audience: Admins, Managers */}

Tickets can be cancelled or removed individually or in bulk from the **Tickets** view.

![Tickets list showing row action menus and selectable checkboxes for bulk operations](../screenshots/tickets-list.png)

---

## Single Ticket Actions

Click the **three-dot menu (⋮)** on any ticket row to access:

| Action | When available | What it does |
|---|---|---|
| **View Ticket** | Always | Opens a detail panel showing all ticket fields and the current status |
| **Copy Link** | Always | Copies the public verification URL (`https://idpage.link/ticket/{id}`) to your clipboard |
| **Revoke** | Active tickets only | Marks the ticket as used — immediately invalidates it. Confirmation required. |
| **Delete** | Always | Permanently removes the ticket record from the employee's profile. Confirmation required. |

---

## Revoke vs Delete

| | Revoke | Delete |
|---|---|---|
| Ticket still appears in the list | ✓ (as Revoked) | ✗ |
| Verification page still loads | ✓ (shows "Revoked") | ✗ (shows "Ticket not found") |
| Can be undone | ✗ | ✗ |
| Keeps an audit trail of the ticket | ✓ | ✗ |

**Use Revoke** when you want to cancel a ticket but preserve the record for auditing or reference.

**Use Delete** when the ticket was issued in error or you want to clean up old records entirely.

---

## Revoking a Single Ticket

1. Find the ticket in the **Tickets** list
2. Click **⋮** on the row
3. Select **Revoke**
4. Confirm in the dialog

The ticket status immediately changes to **Revoked** (red) in the list and on its public verification page.

---

## Deleting a Single Ticket

1. Find the ticket in the **Tickets** list
2. Click **⋮** on the row
3. Select **Delete**
4. Confirm in the dialog

The ticket is permanently removed. Anyone who opens the ticket's verification link will see a "Ticket not found" error page.

---

## Bulk Delete

To delete multiple tickets at once:

1. Click the **checkbox** on each row you want to select, or use the **header checkbox** to select all tickets matching the current filters
2. The filter bar changes to show **N selected** and an **Actions** button
3. Click **Actions** → **Delete**
4. Confirm in the dialog

All selected tickets are permanently deleted.

> **Note:** Bulk **Revoke** is not available — to revoke multiple tickets you must do so individually. If you need to invalidate a large number of tickets at once, using Delete may be more practical.

---

## Cleaning Up Expired Tickets

To remove expired tickets in bulk:

1. Click the **Expired** tab in the status filter bar above the table
2. Click the header checkbox to select all expired tickets on the current page
3. Increase the rows-per-page selector (10 / 25 / 50 / 100) to load more at once
4. Click **Actions** → **Delete** and confirm

Repeat across pages until all expired records are cleared.
