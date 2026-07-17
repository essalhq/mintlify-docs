---
title: "Employee Status Explained"
---

{/* keywords: employee status, active, suspended, lost badge, pending, terminated, badge status, status change */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Every employee record has a **status** that controls whether their badge is valid and what they can access. This article explains what each status means and how to change it.

![Employee list showing employees with different status badges](../screenshots/employees-list.png)

---

## The Five Statuses

### Active

The employee's badge is valid. Badge scans at check-in devices are processed normally according to the employee's access zones, schedule, and PIN settings.

- Shown as a **green** badge in the employee list
- The employee appears on the **Active** tab (default view)
- New employees start as Active after being saved (unless the approval workflow is enabled)

---

### Suspended

The employee's badge is temporarily deactivated. Scans at any device show a **Denied — Suspended** result. The badge QR code still works to display the public profile, but access is blocked.

- Shown as an **orange** badge in the employee list
- The employee appears on the **Active** tab (still visible alongside active employees)
- Suspension is reversible — use **Reactivate** from the row action menu to restore Active status

Use suspension when an employee is on extended leave, during an investigation, or when access needs to be temporarily paused without permanently ending their employment.

---

### Lost / Stolen

The employee's badge has been reported as lost or stolen. Badge scans show a **Denied — Badge Lost** result. The badge is deactivated immediately when this status is set.

- Shown as a **red** badge in the employee list
- The employee appears on the **Active** tab
- To restore access, use **Reissue Badge** (generates a new Badge ID) or **Found** (reactivates without a new ID) from the row action menu

> **Lost vs Suspended**: Suspended means access is paused at an admin's discretion. Lost means the physical badge card is compromised — a new badge should be issued.

---

### Pending

The employee record has been created but not yet approved. Their badge is not active and scans will be denied.

- Shown as a **blue** badge in the employee list
- The employee appears **only** on the **Require Approval** tab — they are hidden from the main Active tab
- To activate, use **Approve** from the row action menu, or use **Batch Approve** to approve multiple employees at once

The Pending status is only used when the **Require approval to issue badge** toggle is enabled on the employee's Security tab, or when a new employee record is created with that setting turned on.

> If you do not see a **Require Approval** tab in your employee list, the approval workflow is not enabled on your tenant.

---

### Terminated

The employee has left the organization. Their badge is permanently revoked. Scans show a **Denied — Terminated** result.

- Shown as a **grey** badge in the employee list
- The employee appears **only** on the **Archived** tab — they are removed from the Active view
- Termination can be reversed — use **Reactivate** from the row menu on the Archived tab if needed
- Employee data is retained after termination for audit and reporting purposes

Use termination (not deletion) when an employee leaves so their badge history, scan logs, and records are preserved. See Revoking All Access — Termination Checklist for the full off-boarding process.

---

## Status Summary

| Status     | Badge color | Tab              | Scans                   | Reversible |
| ---------- | :---------: | ---------------- | ----------------------- | :--------: |
| Active     |    Green    | Active           | Granted (if rules pass) |     —      |
| Suspended  |   Orange    | Active           | Denied                  |     ✅     |
| Lost       |     Red     | Active           | Denied                  |     ✅     |
| Pending    |    Blue     | Require Approval | Denied                  |     ✅     |
| Terminated |    Grey     | Archived         | Denied                  |     ✅     |

---

## How to Change an Employee's Status

Status changes are made from the **employee list row actions** — not from inside the modal.

1. Find the employee in the list
2. Click the **⋯** actions menu on their row
3. Select the appropriate action:

| Action            | Result                        |
| ----------------- | ----------------------------- |
| **Deactivate**    | Active → Suspended            |
| **Mark Lost**     | Active → Lost (immediately)   |
| **Terminate**     | Any → Terminated              |
| **Approve**       | Pending → Active              |
| **Reactivate**    | Suspended → Active            |
| **Reissue Badge** | Lost → Active (new badge ID)  |
| **Found**         | Lost → Active (same badge ID) |

> Status can also be changed from the **Status** dropdown on the **Security tab** of the employee modal — but only between Active, Suspended, and Lost. Pending and Terminated are only set through the list actions.

---

## Status and the Employee Portal

When status changes, the effect on the Employee Portal is immediate:

| Status     | Portal access                                                     |
| ---------- | ----------------------------------------------------------------- |
| Active     | Employee can log in and view their badge                          |
| Suspended  | Employee can log in but badge shows as suspended                  |
| Lost       | Employee can log in but badge shows as lost                       |
| Pending    | Employee can log in but no active badge is shown                  |
| Terminated | Employee account is also typically suspended — contact your admin |
