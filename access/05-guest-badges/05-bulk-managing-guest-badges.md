---
title: "Managing Guest Badges — Revoking & Deleting"
---

{/* keywords: revoke guest badge, delete guest badge, bulk revoke, bulk delete, manage visitor passes, cancel badge */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers */}

This article covers how to revoke or delete guest badges individually or in bulk, and how to filter the list to find what you need.

![Guest Badges list with multiple rows selected and the Actions dropdown open](../screenshots/guest-badges-list.png)

---

## Single-Badge Actions

For any individual badge, click the **three-dot menu (⋮)** at the end of its row to access:

| Action | When available | What it does |
|---|---|---|
| **View Badge** | Always | Opens the public verification page in a new tab |
| **Copy Link** | Always | Copies the badge URL to your clipboard |
| **Revoke** | Active badges only | Marks the badge as revoked (cannot be undone) |
| **Delete** | Always | Permanently removes the badge record |

### Revoking a Single Badge

1. Click **⋮** on the badge row
2. Select **Revoke**
3. Confirm in the dialog

The badge is immediately invalidated. The revocation is logged with your name and the current timestamp.

### Deleting a Single Badge

1. Click **⋮** on the badge row
2. Select **Delete**
3. Confirm in the dialog

The badge record and its link are permanently removed. Any guest who tries to open the link will see a "not found" error.

> **Revoke vs Delete:** Revoke keeps the badge record visible in the admin list (useful for audit trails). Delete removes it entirely.

---

## Bulk Actions

To manage multiple badges at once:

1. Click the **checkbox** on each row you want to select, or use the **header checkbox** to select all rows on the current page
2. The action bar at the top of the table changes to show **N selected** and an **Actions** button
3. Click **Actions** and choose:

| Bulk Action | Applies to | Behavior |
|---|---|---|
| **Revoke** | Selected **Active** badges only | Non-active badges in the selection are skipped |
| **Delete** | All selected badges | Deletes every selected badge regardless of status |

Both actions show a confirmation dialog before proceeding. Press **Escape** to cancel the selection without making any changes.

---

## Filtering the List

Use the status filter (above the table) to narrow the list to a specific status:

- **All** — shows every badge
- **Active** — currently valid badges
- **Expired** — past their validity window
- **Revoked** — manually cancelled badges

Filtering is useful when you want to:
- **Bulk-delete old expired badges** — filter by Expired, select all, delete
- **Find and revoke a specific active badge** — filter by Active, search by name
- **Audit who was on site** — filter by date range or status

---

## Pagination

The list shows **10 rows per page** by default. Use the rows-per-page selector (10 / 25 / 50 / 100) to show more badges at once, or navigate between pages using the page controls.

