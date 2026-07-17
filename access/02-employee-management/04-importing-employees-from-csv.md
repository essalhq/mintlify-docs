---
title: "Importing Employees from CSV"
---

{/* keywords: CSV import, bulk import, import employees, employee spreadsheet, import wizard, column mapping, bulk add, HR export */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

The CSV import wizard lets you add many employees at once from a spreadsheet. This article walks through each step of the 4-step wizard.

Navigate to **Employees** in the sidebar, then click **Import CSV** in the top-right corner (or press `Alt+I`).

![CSV import wizard showing the file upload step](../screenshots/csv-import-wizard.png)

---

## Before You Start

Prepare your data:

- Export your employee list from your HR system as CSV, or fill in the downloadable template
- Make sure at least **First Name** and **Last Name** columns are present — these are the only required fields
- Dates should be in a standard format (e.g. `YYYY-MM-DD` or `MM/DD/YYYY`)
- Blood type values should be: `A+`, `A-`, `B+`, `B-`, `AB+`, `AB-`, `O+`, or `O-`

**Supported file formats**: `.csv`, `.tsv`, `.txt`

---

## Step 1 — Upload Your File

Drag your file onto the upload zone, or click anywhere in the zone to browse and select a file.

After the file is loaded, the wizard shows:

- **Row count** — the number of data rows detected
- **Column count** — the number of header columns
- **File size**
- **Detected Columns** — a list of all column headers found in the file

If you do not have a file ready, click **Download Template** to get a pre-formatted CSV with all the standard field headers filled in.

---

## Step 2 — Map Columns

Essal Access automatically maps your CSV columns to employee fields using AI-assisted inference. The mapping table shows:

| Column           | What it contains                                                              |
| ---------------- | ----------------------------------------------------------------------------- |
| **CSV Column**   | The header name from your file                                                |
| **Sample Value** | The first data value from that column                                         |
| **Confidence**   | A dot indicating mapping confidence: green (high), yellow (medium), red (low) |
| **Mapped To**    | The employee field this column will populate                                  |

Review the mappings and correct any that are wrong using the **Mapped To** dropdown. Options include:

- **Skip** — ignore this column entirely
- **Full Name → First + Last** — splits a single full-name column (e.g. `"Jane Smith"` → First: `Jane`, Last: `Smith`)
- All standard employee fields (see table below)
- Any custom fields defined in Settings → Custom Fields

### Standard Importable Fields

| Field                  | Required |
| ---------------------- | -------- |
| First Name             | **Yes**  |
| Last Name              | **Yes**  |
| Email                  | No       |
| Role / Job Title       | No       |
| Department             | No       |
| Phone Number           | No       |
| Address                | No       |
| City                   | No       |
| State / Province       | No       |
| Zip Code / Postal Code | No       |
| Nationality            | No       |
| Date of Birth          | No       |
| Blood Type             | No       |
| Bio / Description      | No       |

> **AI mapping notice**: If the AI service is unavailable, Essal Access falls back to keyword-based column matching. An amber notice is shown when automatic fallback was used — review the mappings carefully in that case.

---

## Step 3 — Preview and Validate

Before importing, the wizard validates every row. Three counters appear at the top:

- **Ready** — rows that passed validation and will be imported
- **Warnings** — rows with minor issues that will still import (e.g. unrecognized department name)
- **Errors** — rows that cannot be imported as-is

The preview table shows the first 10 valid rows and all error rows. Each row has a status pill:

- **OK** (green) — valid, will import
- **Warning** (amber) — will import with the issue noted
- **Error** (red) — will be skipped unless you choose to import anyway

### Handling Errors

Two options when errors exist:

1. **Fix the file** — click **Back**, correct the issues in your spreadsheet, and re-upload
2. **Skip errors and import anyway** — check the **Skip Errors** checkbox. Error rows are skipped; all valid rows are still imported
3. **Download Error Report** — exports a CSV listing each error row with the issue description, useful for correcting the source file

---

## Step 4 — Import

Click **Import** to start. A progress bar tracks the operation:

- **Imported** — rows successfully added so far
- **Failed** — rows that encountered an error during insert
- **Processed** — total rows handled so far
- **ETA** — estimated time remaining

The import runs in batches of 50 rows. You can click **Cancel Import** to stop after the current batch finishes — rows already processed are kept.

### After Import

When the import completes:

- A summary shows the final counts (imported, failed)
- Click **View Employees** to go to the employee list — a notification shows the import count and date
- Click **Undo Import** if you need to reverse it — a confirmation prompt appears, then all imported records are deleted one by one

---

## Common Import Errors

| Error                                       | Fix                                                           |
| ------------------------------------------- | ------------------------------------------------------------- |
| Duplicate email address                     | Remove duplicate rows or correct the email                    |
| Missing required field (First or Last Name) | Fill in the missing values                                    |
| Invalid date format                         | Use `YYYY-MM-DD`, `MM/DD/YYYY`, or `DD/MM/YYYY`               |
| Invalid blood type                          | Use exactly: `A+`, `A-`, `B+`, `B-`, `AB+`, `AB-`, `O+`, `O-` |
| Invalid custom field value                  | Check the allowed values for that custom field in Settings    |
