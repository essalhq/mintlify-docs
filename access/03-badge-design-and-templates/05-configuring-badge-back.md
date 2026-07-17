---
title: "Configuring the Back of the Badge"
---

{/* keywords: badge back, back side, badge reverse, enable back side, contact info, legal text, accent bars, back background, badge QR back */}
{/* category: Badge Design & Templates */}
{/* audience: Admins */}

Essal Access badges can optionally have a printed back side. This article explains how to enable and configure it.

Navigate to **Badge Designer** in the sidebar, then click **Back** in the **Front / Back** segmented control in the canvas toolbar. The left panel switches to show the back side controls.

![Badge Designer showing the back side view with back-side controls in the left panel](../screenshots/badge-designer-back.png)

---

## Enabling the Back Side

At the top of the left panel (when Back is selected), the **Enable Back Side** card is shown. Toggle it on to activate the back side of the badge.

When enabled:

- The canvas preview switches to show the back face
- The Back Elements section appears in the left panel
- The back side is included when printing (Print Center renders both sides)

When disabled, the back of the badge is blank — nothing prints on the reverse.

---

## Back Side Elements

Five content elements can be toggled on or off for the back face:

| Element          | What it displays                                                                                                           |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Accent Lines** | A thin color bar at the top edge and another at the bottom edge, in your primary color. Adds a polished frame to the back. |
| **Logo**         | Your company logo (or company name text if no logo image is uploaded), centered on the back.                               |
| **Tagline**      | Your company tagline (as configured in Settings → Branding), centered below the logo.                                      |
| **QR Code**      | The employee's QR code, centered on the back — useful when the front QR is too small or partially covered.                 |
| **Contact Info** | A line of free-text contact information (see below).                                                                       |

---

## Contact Text

When **Contact Info** is enabled, a text input appears:

- Enter any contact information you want printed on the back — typically an email address, phone number, or helpdesk URL
- Example: `contact@company.com | +1 555 0000`
- The text is rendered in a small font near the bottom of the back face

This field is free-text — you can include any combination of contact details.

---

## Legal / Disclaimer Text

A **Legal / Disclaimer** textarea is always visible when the back side is enabled. Use this for:

- "If found, please return to Security at [address]"
- A confidentiality notice
- Authorized personnel only statements
- Any compliance-required disclaimer

The text renders in a very small font at the bottom of the back face, in your primary color at reduced opacity. Leave it blank if not needed.

---

## Background Color

The back side has its own **Background Color** setting:

1. Click the color swatch next to **Background Color**
2. Pick a color or enter a hex code

The default background color is your **Accent Color**. Changing it here only affects the back — the front background is not changed.

> **Tip**: A light background with your primary color elements works well for formal organizations. A full-color back (using your primary color as the background) creates a bold two-sided look.

---

## Background Image (Back)

You can also upload a background image specific to the back side:

1. Under **Background Image** in the left panel (back side controls), click to upload
2. Select an image (maximum 2 MB)
3. The image renders behind all back content

Click **Remove Image** to clear it.

---

## Printing the Back Side

When the back side is enabled, the Print Center automatically includes it in all print jobs. The badge is rendered as two pages (front and back) or as a two-sided layout depending on your print settings.

See Bulk Printing Multiple Badges for print layout options.

## Saving Your Changes

Click **Save** in the top-right of the right panel to save your back side configuration along with all other badge settings.
