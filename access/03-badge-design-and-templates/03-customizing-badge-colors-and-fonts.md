---
title: "Customizing Badge Colors and Fonts"
---

{/* keywords: badge colors, primary color, accent color, badge font, brand colors, color picker, badge branding, hex color */}
{/* category: Badge Design & Templates */}
{/* audience: Admins */}

The **Branding** tab in the right panel of the Badge Designer controls your badge's color scheme and typography. This article explains each setting and how it affects the badge.

Navigate to **Badge Designer** in the sidebar, then find the **Branding** tab in the right panel.

![Badge Designer showing the Branding tab with color pickers for Primary and Accent colors](../screenshots/badge-designer.png)

---

## Primary Color

**Primary Color** is the most prominent color on the badge. It controls:

- Header bars and sidebar panels (Corporate, Modern)
- Role pill backgrounds and text accents (most layouts)
- The vertical accent strip (Conference)
- QR code backgrounds in some layouts
- Logo text color when no logo image is uploaded
- Accent elements on the badge back

To change it:

1. Click the color swatch next to **Primary Color**
2. Use the native color picker to select a color
3. Or type a hex code directly in the text input next to the swatch (e.g. `#1d4ed8`)

The badge preview updates in real time as you pick.

> **Tip**: Import your exact brand colors automatically using BrandFetch — see Using BrandFetch to Import Your Logo and Brand Colors.

---

## Accent Color

**Accent Color** is the secondary color used for:

- Footer stripe (Corporate layout)
- Second gradient stop (Gradient layout — the badge flows from primary to accent to primary)
- Badge back default background color (when no custom background is set)

The accent color is typically a complementary or contrasting color to the primary. A common pairing is a deep blue primary with a purple accent.

---

## Logo

The **Logo** section lets you upload your company logo image.

1. Click **Upload Logo** (or the logo preview area)
2. Select any image file — PNG, SVG, JPG, or WEBP
3. The logo appears on the badge in the logo position defined by the layout

When no logo is uploaded, the badge displays your **Company Name** as text in the primary color, optionally with a colored dot circle.

> **Logo tip**: Use a PNG or SVG with a transparent background for the cleanest result on all badge layouts. White logos work best on dark-themed layouts (Tech, Executive).

The same logo is used on both the badge front and back.

---

## Background Image (Front)

You can place an image behind the badge content on the front face:

1. Under **Background Image** in the Branding tab, click the upload area
2. Select an image (maximum **2 MB**)
3. The image renders as a background layer behind all badge content

When a background is active, a small thumbnail preview appears with a red **Clear** button to remove it.

> Background images are stored encoded within the badge configuration. Keep file sizes under 2 MB for best performance.

---

## Font

Three font families are available for badge text:

| Option                   | Style                       | Best for                                               |
| ------------------------ | --------------------------- | ------------------------------------------------------ |
| **Sans-serif** (default) | Clean, modern               | Most organizations — excellent legibility              |
| **Serif**                | Traditional, editorial      | Law firms, financial institutions, conservative brands |
| **Monospace**            | Technical, coding aesthetic | Tech companies, developer teams                        |

The font applies to all text on the badge — name, role, department, and all field labels.

> **Note**: The font selector is applied automatically by the AI Theme Generator when available. The default font for new templates is Sans-serif.

---

## How Colors Work Per Layout

Different layouts use the primary and accent colors differently:

| Layout     | Primary color used for        | Accent color used for |
| ---------- | ----------------------------- | --------------------- |
| Modern     | Left sidebar, role pill       | —                     |
| Corporate  | Header bar, accent stripe     | Footer stripe         |
| Tech       | Last name text, Badge ID chip | —                     |
| Conference | Left strip, role pill         | —                     |
| Minimal    | Name underline bar            | —                     |
| Gradient   | Gradient start + end          | Gradient middle stop  |
| Executive  | Amber replaces primary        | —                     |

Use the live preview to see exactly how your color choices look before saving.

---

## Saving Your Changes

Click **Save** in the top-right of the right panel to persist your color and logo changes. All employee badges update to the new design immediately after saving.
