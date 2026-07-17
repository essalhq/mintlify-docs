---
title: "Custom Fields — Creating and Managing Attributes"
---

{/* keywords: custom fields, custom attributes, employee attributes, extra fields, custom data, field types, required fields, badge field, self-edit */}
{/* category: Employee Management */}
{/* audience: Admins */}

Custom fields let you add organization-specific data fields to every employee record. This article explains how to create, configure, and manage custom attribute definitions.

Navigate to **Settings** in the sidebar, then click the **Custom Fields** tab.

![Settings Custom Fields tab showing existing custom fields and the new field form](../screenshots/settings-custom-fields.png)

---

## What Custom Fields Are For

The standard employee profile covers common fields (name, email, role, department, phone, etc.). Custom fields extend this with data specific to your organization, such as:

- **Employee number** (if your HR system uses a different ID format)
- **Floor or desk location**
- **Vehicle registration plate** (for parking access)
- **Uniform size**
- **Security clearance level**
- **Canteen meal plan type**

Custom field values are stored per employee and can be shown on badges and public profiles.

---

## Creating a Custom Field

1. In the **Custom Fields** tab, find the **New Custom Field** form
2. Set the **Field Name** — this is the label shown on the employee form (e.g. _Desk Number_, _Security Level_)
3. Choose a **Field Type** (see options below)
4. Configure the **Options** (for select fields — see below)
5. Set any additional toggles (Required, Show on Badge, Show on Public Profile, Allow Employee Self-Edit)
6. Click **Add Field** to save

The field immediately appears in the **Custom Fields** section at the bottom of every employee's Profile tab.

---

## Field Types

| Type       | Input shown on employee form     | Use for                                                 |
| ---------- | -------------------------------- | ------------------------------------------------------- |
| **Text**   | Single-line text input           | Short free-text values                                  |
| **Number** | Numeric input                    | Quantities, scores, IDs                                 |
| **Date**   | Date picker                      | Certification dates, review dates                       |
| **Email**  | Email input with validation      | Secondary email addresses                               |
| **Phone**  | Phone number input               | Extension numbers, second phone                         |
| **URL**    | URL input with validation        | Personal website, LinkedIn                              |
| **Select** | Dropdown with predefined options | Fixed-value choices like clearance levels or meal plans |

---

## Select Field Options

For **Select** type fields, a list of allowed values must be defined:

1. Type each option in the **Options** text area, one per line
2. The employee form will show a dropdown with exactly these options
3. CSV imports must use one of the listed values exactly — other values cause a validation error

---

## Field Configuration Options

| Option                       | What it does                                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| **Required**                 | Marks the field with a red asterisk and prevents saving the employee record until it is filled in |
| **Show on Badge**            | Makes the field value available in the Badge Designer to place on the badge face                  |
| **Show on Public Profile**   | Displays the field value on the employee's public verification profile                            |
| **Allow Employee Self-Edit** | When the employee portal self-edit is enabled, employees can update this field themselves         |

---

## Field Order

Custom fields appear in the order they were created. To reorder them, use the drag handle (if available) or delete and re-create them in the desired sequence.

---

## Editing a Custom Field

Click the **Edit** icon next to a custom field. You can change:

- The field name
- The field type (note: changing type may affect existing data if values become incompatible)
- Options (for select type)
- All configuration toggles

---

## Deleting a Custom Field

Click the **Delete** icon next to a field. This permanently removes:

- The field definition
- **All employee data stored in that field across every employee record**

> Deletion is irreversible. Export employee data before deleting a field if you need to preserve its values.

---

## Custom Fields in CSV Import

Custom fields appear in the **Mapped To** dropdown in the CSV import wizard. Map your CSV column to the custom field to populate it during bulk import.

For select-type fields, CSV values must exactly match one of the defined options.
