---
title: "Inviting Your First Users"
---

{/* keywords: invite user, create user, system user, admin account, manager account, security account, suspend, delete user, user management */}
{/* category: Getting Started */}
{/* audience: Admins */}

This article explains how to create system user accounts so your team can log in to the Essal Access admin panel. Only **Admins** can create, suspend, and delete other users.

Navigate to **System Users** in the sidebar (or **Settings → Users**).

![System users list showing team members with their roles and last login times](../screenshots/system-users.png)

---

## Creating a New User Account

1. Click **Add User** in the top-right corner of the System Users page
2. Fill in the form:

   | Field         | Notes                                                                       |
   | ------------- | --------------------------------------------------------------------------- |
   | **Full Name** | The person's name — displayed in the admin panel and in email notifications |
   | **Email**     | Their work email address — this is their login username                     |
   | **Role**      | Choose Admin, Manager, or Security (see below)                              |

3. Click **Create User**

Essal Access creates the account and sends a **magic link email** to the address you entered. The new user clicks the link to sign in for the first time — no password setup is required unless they choose to set one later.

> **Employee role not available here**: The Employee role is assigned automatically when you link a system user to an employee record. You cannot select it in the Add User form. To give an employee portal access, create their employee record first and link a portal account to it.

---

## Choosing a Role

| Role         | Who to assign it to                                                              |
| ------------ | -------------------------------------------------------------------------------- |
| **Admin**    | IT managers, system owners — full access including user management               |
| **Manager**  | HR staff, office managers — can manage employees and badges, cannot manage users |
| **Security** | Guards, receptionists — can view employees, guest badges, and scan logs only     |

For a detailed breakdown of what each role can and cannot do, see Understanding User Roles.

Keep Admin accounts to a minimum. Most day-to-day staff should be Manager or Security.

---

## What the New User Receives

When you create a user account, Essal Access automatically sends an invitation email containing:

- A welcome message with your company name
- A sign-in link (magic link) to access the admin panel
- The URL for the admin panel (`access.essal.cloud`)

Magic links expire after **10 minutes**. If the new user misses the link, they can request a new one from the login page by entering their email and clicking **Continue** — a new magic link will be sent immediately.

---

## Linking a User to an Employee Record

If the person is also an employee with a badge, you can link their system user account to their employee record. This connects their admin identity to their badge, QR code, and employee portal access.

To link after creation:

1. Go to **Employees**, find the employee record
2. Open the employee modal → **Security** tab
3. Under **Linked System User**, select the matching user account from the dropdown and save

Once linked, the user's name and photo in the admin panel pulls from the employee record, and their Employee Portal (`portal.access.essal.cloud`) becomes active.

---

## Suspending a User

Suspending a user blocks them from signing in without deleting their account. Use this when someone is on leave, their role changes, or you need to temporarily remove access.

1. In the System Users list, find the user
2. Click the **suspend icon** (the user-with-X icon) in their row
3. Confirm the action

A suspended account shows an **amber "Suspended" badge** in the users list. The user will see an error if they try to log in. Their account data and history are preserved.

To **unsuspend**, click the same icon again (it becomes a user-with-checkmark icon when the account is suspended).

> You cannot suspend your own account. The suspend action is only available for other users.

---

## Deleting a User

Deleting permanently removes the user's account and their login access. This cannot be undone.

1. In the System Users list, find the user
2. Click the **trash icon** in their row
3. Confirm the deletion in the prompt

Use deletion for former employees or accounts created in error. For temporary removal, prefer **suspension** — it keeps the account history intact and is reversible.

> Only Admins can delete users. You cannot delete your own account.

---

## Viewing Last Login

The System Users list shows each user's **last login time**. This is useful for identifying:

- Accounts that have never been used (invitation not accepted)
- Inactive accounts that can be suspended or removed
- Unexpected recent logins that may need investigation
