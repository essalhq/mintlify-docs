---
title: "Exporting Badges as PNG/ZIP"
---

{/* keywords: export badge, download badge PNG, badge ZIP, bulk export, download all badges, badge image export, zip download */}
{/* category: Printing & Exporting Badges */}
{/* audience: Admins, Managers */}

Essal Access can export badge images as high-resolution PNG files — either one at a time or as a ZIP archive for multiple employees. This is useful when sending badges to a print shop, importing into another system, or archiving.

![Bulk print tab showing Download ZIP button with employee selection](../screenshots/print-bulk.png)

---

## Exporting a Single Badge as PNG

1. Go to **Print Center → Individual** tab
2. Select an employee from the left panel
3. Click **Download PNG**
4. The badge renders at high resolution — a spinner shows while processing (2–5 seconds)
5. The file downloads automatically to your browser's default download folder

**File details:**

- Format: PNG (lossless)
- Resolution: ~1720 × 2720 px at 4× pixel density (suitable for high-quality print)
- File name: `{FirstName}_{LastName}_{BadgeID}.png`

---

## Exporting Multiple Badges as a ZIP

1. Go to **Print Center → Bulk** tab
2. Select the employees you want to export (use search and department filter to narrow the list)
3. Click **Download ZIP (N)** where N is the number of selected employees
4. A **Security Verification** dialog appears — click **Authorize**
5. A progress indicator appears on the button: `{done}/{total}` as each badge is rendered
6. When complete, a single ZIP file downloads automatically

**ZIP file details:**

- File name: `badges_export_{YYYY-MM-DD}.zip`
- Contents: one PNG per selected employee
- Individual file names inside: `{FirstName}_{LastName}_{BadgeID}.png`
- Compression: DEFLATE (standard ZIP compression)

> **Performance note**: Badges are rendered one at a time to avoid memory issues. Exporting 50 employees typically takes 60–90 seconds. Do not close the browser tab while the export is running.

---

## What's Included in the Export

Each exported badge PNG includes everything visible on the badge front:

- Employee photo (if enabled and uploaded)
- Name, role, department, and other enabled fields
- QR code (if enabled)
- Company logo (if enabled)
- Colors and layout from the Badge Designer template

**Back side**: The individual PNG download and ZIP export only include the badge **front**. To print the back side, use the browser print flow (Bulk → Print All) which includes back pages automatically.

---

## Cross-Origin Images

Employee photos, logos, and background images hosted on external URLs are automatically converted to embedded data for export. This ensures images appear correctly in the PNG even if the CDN applies access restrictions.

If a photo fails to load during export, the badge will render without the photo rather than failing entirely. Check that the employee's photo is uploaded in their record.

---

## Use Cases

| Scenario                                      | Recommended method                                       |
| --------------------------------------------- | -------------------------------------------------------- |
| Sending badges to a commercial print shop     | Bulk ZIP export — send the ZIP with individual PNG files |
| Creating digital ID cards for a system import | Bulk ZIP export                                          |
| Printing in-house on a printer                | Browser print (Individual or Bulk Print)                 |
| Archiving a specific employee's badge         | Individual PNG download                                  |
| Sending a badge to an employee digitally      | Individual PNG download, attach to email                 |
