---
title: "Creating Custom Ticket Types"
---

{/* keywords: custom ticket type, ticket type, add ticket type, ticket color, manage ticket types */}
{/* category: Tickets */}
{/* audience: Admins, Managers */}

Essal Access includes six built-in ticket types, but you can add your own to match your organization's specific needs — each with a custom name, color, and optional description.

![Tickets list showing the variety of ticket types available](../screenshots/tickets-list.png)

---

## Default Ticket Types

The following types are available out of the box:

| Type | Color |
|---|---|
| Access | Blue |
| Meal | Green |
| Event | Purple |
| Parking | Amber |
| Transport | Cyan |
| Voucher | Pink |

---

## Adding a Custom Ticket Type

1. Navigate to **Tickets** in the sidebar
2. Click **New Ticket** (or **+ Issue Ticket**) to open the Create Ticket modal
3. In the **Ticket Type** section, click **Manage types**
4. The Ticket Type Manager panel opens

### In the Type Manager:

| Field | Required | Notes |
|---|---|---|
| **Name** | ✓ | The display name of the type (e.g. "Gym Access", "Library Card") |
| **Color** | ✓ | Pick any color using the color picker (defaults to blue) |
| **Description** | Optional | Internal note about when this type should be used |

5. Click **Add** (or the **+** button) to save the new type
6. It immediately appears in the ticket type selector grid and is available for all future tickets

---

## How Ticket Type IDs Work

The type's internal `id` is automatically generated from the name — spaces are replaced with dashes and all characters are lowercased (e.g. "Gym Access" → `gym-access`). This ID is stored on every ticket issued with that type.

---

## Deleting a Ticket Type

1. Open **Manage types** from the Create Ticket modal
2. Find the type to remove and click the **delete** (trash) icon next to it
3. Confirm the deletion in the dialog

> **Note:** Deleting a ticket type does not affect already-issued tickets. Existing tickets retain their type ID, but the type name and color will no longer resolve on the verification page — the ticket will show the raw type ID instead of the name. It is recommended to revoke or delete all tickets of a type before removing the type itself.

---

## Where Ticket Types Are Stored

Custom ticket types are stored in your organization's settings and are available to all administrators. Changes are applied immediately — any admin who opens the Create Ticket modal will see the updated type list.
