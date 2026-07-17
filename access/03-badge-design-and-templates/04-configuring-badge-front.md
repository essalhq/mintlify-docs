---
title: "Configuring What Appears on the Front of the Badge"
---

{/* keywords: badge front, badge elements, show photo, show QR code, badge fields, employee ID on badge, role on badge, department on badge, badge ID, blood type, logo on badge, slogan */}
{/* category: Badge Design & Templates */}
{/* audience: Admins */}

The **Elements** section of the left panel controls which fields are shown on the front face of the badge. All changes update the live preview instantly.

Navigate to **Badge Designer** in the sidebar. Make sure the **Front** side is selected in the canvas toolbar. The **Elements** section appears below the Templates section in the left panel.

![Badge Designer showing the Elements section with toggle switches for each badge field](../screenshots/badge-designer.png)

---

## Available Front Fields

Nine fields can be toggled on or off. Each is a pill-shaped switch that turns blue when enabled.

| Field           | What it displays                                                                   |
| --------------- | ---------------------------------------------------------------------------------- |
| **Photo**       | The employee's profile photo (or silhouette placeholder if none is uploaded)       |
| **Role**        | The employee's job role/title (e.g. _Security Officer_, _HR Manager_)              |
| **Department**  | The employee's department name                                                     |
| **Employee ID** | The unique employee identifier (e.g. `EMP-A3F7K2`)                                 |
| **Badge ID**    | The physical badge card identifier (e.g. `BDG-X7K2M9`)                             |
| **Blood Type**  | The employee's blood type (e.g. `A+`, `O-`) — useful for first-responder scenarios |
| **QR Code**     | The scannable QR code that links to the employee's public profile                  |
| **Slogan**      | Your company tagline as set in Settings → Branding                                 |
| **Logo**        | Your company logo (or company name text if no logo is uploaded)                    |

---

## "Show title label" Sub-Toggles

Five fields have an optional **"Show title label"** sub-toggle that appears indented below the field when the field itself is enabled. Enabling it prepends the field name to the displayed value on the badge:

| Field       | Without label       | With label                |
| ----------- | ------------------- | ------------------------- |
| Role        | `Software Engineer` | `Role: Software Engineer` |
| Department  | `Engineering`       | `Dept: Engineering`       |
| Employee ID | `EMP-A3F7K2`        | `ID: EMP-A3F7K2`          |
| Badge ID    | `BDG-X7K2M9`        | `Badge ID: BDG-X7K2M9`    |
| Blood Type  | `A+`                | `Blood Type: A+`          |

Labels improve clarity when multiple IDs appear on the same badge, or when the badge is used in a security context where field identification matters.

---

## Field Rendering by Layout

Not every layout renders every field in the same position or the same way. The layout determines placement — toggling a field on means it will be shown wherever that layout places it.

- **Photo** — displayed as a circle in all layouts; size varies (large in Modern and Conference, medium in Corporate and Minimal)
- **QR Code** — positioned in a corner or beside the photo; always has a white background for reliable scanning
- **Logo** — shown in the header, corner, or top area depending on the layout
- **Role pill** — some layouts render the role inside a colored pill (Modern, Conference, Corporate); others render it as plain text
- **Blood Type** — rendered as smaller text, typically below department or role

Use the live preview and switch between layouts to see how your field selection looks in each one.

---

## Recommended Combinations

**Minimal badge** (fastest to print, most readable at a glance):

- Photo ✅ · Name (always shown) · Role ✅ · QR Code ✅ · Logo ✅
- Turn off: Department, Employee ID, Badge ID, Blood Type, Slogan

**Full identification badge** (maximum information):

- All fields on, with labels enabled for Role, Department, Employee ID, Badge ID

**Security / access control badge**:

- Photo ✅ · QR Code ✅ · Employee ID ✅ · Badge ID ✅ · Role ✅ · Department ✅
- Blood Type optional depending on your safety policy

**Event / conference badge**:

- Photo ✅ · Role ✅ · Department or Company ✅ · QR Code ✅
- Turn off: Employee ID, Badge ID, Blood Type (not relevant for visitors)

---

## Name Fields

The employee's **First Name** and **Last Name** are always displayed on the badge — there is no toggle to hide the name. The name is the primary identifier and is part of every layout's core structure.

---

## QR Code Behavior

The QR code on the badge links to the employee's public verification profile at `idpage.link/public/{badgeId}`. The URL:

- Uses the employee's most recently issued active badge ID
- Updates automatically when a new badge is issued to that employee
- The page it links to can be configured in **Public Page Editor** — see Configuring the Public Profile Page

If **Public Profile Enabled** is turned off for an employee (Security tab), their QR code is still on the badge but scanning it shows a blocked/restricted message.
