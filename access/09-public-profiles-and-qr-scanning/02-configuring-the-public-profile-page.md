---
title: "Configuring the Public Profile Page"
---
{/* category: Public Profiles & QR Scanning */}

The Public Page Editor lets administrators control exactly what information appears when an employee's badge is scanned. You can toggle individual fields on or off, set the brand color, upload a cover photo, and control global scanning permissions.

![Public Page Editor](../screenshots/public-page-editor.png)

## Opening the Editor

Go to **Settings** → **Public Page Editor** in the admin navigation, or navigate directly to `/public-page-editor`. A live preview on the right updates as you make changes.

## Branding

**Primary color** — sets the accent color used for the cover strip at the top of the profile and for buttons. Click the color swatch to open a color picker, or type a hex value directly.

## Visibility Toggles

Use the toggles to show or hide each section of the public profile:

| Toggle | What it controls |
|---|---|
| **Cover** | Colored header bar at the top of the profile |
| **Profile photo** | Employee's uploaded photo |
| **Job information** | Role, department |
| **Nationality** | Employee's nationality field |
| **Access level** | The employee's assigned access zones |
| **Tickets** | Any active tickets linked to the employee |
| **Custom attributes** | Any custom fields marked as visible on the public profile |
| **Bio** | Employee bio / summary text |

**Contact section:**
- **Show contact info** — master toggle for all contact details
- **Show email** — employee's email address (requires contact toggle on)
- **Show phone** — employee's phone number (requires contact toggle on)
- **Show location** — city and address

> Showing email and phone makes that data publicly visible to anyone who scans the badge. Use these toggles carefully.

**Health & Safety** (shown separately):
- Blood type, emergency contact, allergies, medical conditions, safety certifications

## Global Access Controls

These settings are found in the main **Settings** page but directly affect public scanning:

| Setting | Effect |
|---|---|
| **Allow public badge verification** | Master on/off switch. When disabled, all badge scans are blocked |
| **Business card mode** | When enabled alongside disabled public verification, blocked scans show the business card instead of an error page |

## Saving Changes

Changes in the editor are applied immediately to the live preview. Click **Save** to apply changes to all public profiles site-wide.
