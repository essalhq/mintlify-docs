---
title: "Health & Safety Records"
---

{/* keywords: health safety, emergency contact, allergies, medical conditions, disabilities, safety certifications, PPE, health records, employee health */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

The Health & Safety tab on each employee record stores sensitive data used for emergency response and workplace safety management. This article explains what data is stored, who can access it, and how to manage it.

Navigate to **Employees**, open an employee's record, and click the **Health & Safety** tab (or press `Ctrl+4`).

![Employee modal Health & Safety tab showing emergency contact, allergies, and certifications sections](../screenshots/employee-modal-health.png)

---

## What Is Stored

Health & Safety data is divided into six sections:

### Emergency Contact

| Field            | Description                                                       |
| ---------------- | ----------------------------------------------------------------- |
| **Name**         | Full name of the emergency contact person                         |
| **Phone**        | Contact phone number                                              |
| **Relationship** | Relationship to the employee (e.g. _Spouse_, _Parent_, _Sibling_) |

This information is shown to authorized admin users and can appear on the public profile if the Public Page Editor has that section enabled.

---

### Allergies

A list of allergens that apply to this employee (e.g. _Penicillin_, _Peanuts_, _Latex_).

To add an allergy:

1. Type the allergen name in the input field
2. Press **Enter** or click **Add**

To remove an allergy, click the × on its tag.

Duplicate entries are silently ignored.

---

### Medical Conditions

A list of relevant medical conditions (e.g. _Type 2 Diabetes_, _Asthma_, _Epilepsy_).

Same add/remove interaction as allergies.

---

### Disabilities / Additional Notes

A free-text field for recording disabilities, mobility considerations, or any additional safety-relevant notes. This is unstructured and can be as detailed as needed.

---

### PPE Requirements

A list of personal protective equipment that this employee must wear in their work area (e.g. _Hard Hat_, _Safety Vest_, _Steel-Toe Boots_, _Gloves_).

Same add/remove interaction as allergies.

This field is typically managed by admins and supervisors, not the employee themselves.

---

### Safety Certifications

A structured list of professional certifications relevant to safety (e.g. _First Aid_, _Forklift Operator License_, _HAZMAT Handling_).

Each certification record contains:

| Field | Notes |
|---|---|
| **Certification Name** | Required. Name of the certification or license. |
| **Cert Number** | Optional. Official certificate or license number. |
| **Issued Date** | The date the certification was granted |
| **Expiry Date** | The date the certification expires |

**Adding a certification:**

1. Click **Add Certification** to reveal the form
2. Fill in the Name (required) and any other fields
3. Click **Add Certification** to save it to the list

**Expiry alerts** are shown automatically:

- **Expiring Soon** (amber) — expiry is within 30 days
- **Expired** (red) — expiry date has passed

To remove a certification, click the trash icon on its card.

---

## Who Can View Health & Safety Data

Health & Safety data is visible to:

- **Admins** — full access to view and edit all fields
- **Managers** — full access to view and edit all fields
- **Security users** — can view the employee record but Health & Safety data visibility depends on your Public Page Editor configuration

The **PPE Requirements** and **Safety Certifications** sections are intended for admin use and are not shown to employees through the self-edit portal.

---

## Employee Self-Edit

Employees can update some of their own health and safety information through the Employee Portal if your organization has configured this:

- **Emergency Contact** — employees can update their own emergency contact
- **Allergies** — employees can add/remove their own allergies
- **Medical Conditions** — employees can add/remove their own medical conditions
- **Disabilities / Notes** — employees can update their own notes

**PPE Requirements** and **Safety Certifications** are admin-only and cannot be edited by employees.

For how to enable employee self-edit, see the Security Policy settings in Settings → Security Policy.

---

## Health & Safety Data on Public Profiles

Some health & safety data can be displayed on the employee's public QR code profile page. This is configured in the **Public Page Editor**:

- **Emergency contact** — can be shown (useful for on-site first responders)
- **Allergies** — can be shown
- **Medical conditions** — can be shown

If sensitive health data should remain private, ensure these sections are disabled in the Public Page Editor.
