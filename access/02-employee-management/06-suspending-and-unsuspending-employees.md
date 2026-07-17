---
title: "Suspending and Unsuspending Employees"
---

{/* keywords: suspend employee, unsuspend, deactivate badge, reactivate employee, temporary suspension, employee access, badge deactivate */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Suspension temporarily deactivates an employee's badge access without deleting their record or ending their employment. This article explains when to use suspension, how to apply it, and how to lift it.

---

## When to Suspend

Use suspension when access needs to be paused temporarily:

- An employee is on extended leave (medical, parental, sabbatical)
- An HR investigation is in progress
- An employee's account requires a security review
- A contractor's project has paused but will resume

Suspension is different from termination:

- **Suspended** — reversible, employee record and badge history are intact, easy to reactivate
- **Terminated** — signals the employment has ended; use for off-boarding

If the employee's physical badge card has been lost or stolen, use **Mark Lost** instead — this issues a "badge lost" status rather than a general suspension and prompts a badge reissue.

---

## How to Suspend an Employee

1. Navigate to **Employees** in the sidebar
2. Find the employee in the list (use the search bar or filters if needed)
3. Click the **⋯** actions menu on their row
4. Select **Deactivate**

The employee's status changes to **Suspended** (orange badge) immediately. Their badge QR code will now return a **Denied — Suspended** result at any check-in device.

![Employee list showing an employee with Suspended status badge](../screenshots/employees-list.png)

> **Bulk suspension**: To suspend multiple employees at once, use the checkboxes to select employees, then choose **Batch Deactivate** from the **Batch Actions** dropdown. See Bulk Actions.

---

## What Happens When Suspended

- All badge scans are denied immediately — no grace period
- The public profile page shows an **Access Suspended** message to anyone scanning the QR code
- The employee can still log into the Employee Portal (their system user account is separate — suspend that separately if needed from System Users)
- The employee remains visible on the **Active** tab in the employee list alongside active employees
- All historical data (scan logs, badge history, tickets) is preserved

---

## How to Unsuspend (Reactivate)

1. Find the employee in the list
2. Click the **⋯** actions menu on their row
3. Select **Reactivate**

The employee's status returns to **Active** immediately. Their most recently active badge is restored.

> If the employee was previously suspended due to a lost badge, **Reactivate** restores their previous badge status. If you want to issue a completely new badge ID instead, use **Reissue Badge**.

---

## Checking an Employee's Current Status

The status badge is visible in the employee list without opening the record. The color codes are:

| Color  | Status        |
| ------ | ------------- |
| Green  | Active        |
| Orange | Suspended     |
| Red    | Lost / Stolen |
| Blue   | Pending       |
| Grey   | Terminated    |

You can also filter the employee list by status using the **Status** dropdown in the filter bar to show only suspended employees.

---

## Suspending via the Security Tab

Suspension can also be applied from inside the employee modal:

1. Open the employee record → go to the **Security** tab
2. Change the **Status** dropdown from `Active` to `Suspended`
3. Click **Save**

This has the same effect as using the row action menu.
