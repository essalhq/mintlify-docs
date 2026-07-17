---
title: "Setting Up Your Company Branding"
---

{/* keywords: branding, company name, logo, colors, tagline, BrandFetch, whitelabel, primary color, badge branding */}
{/* category: Getting Started */}
{/* audience: Admins */}

This article explains how to configure your company's identity in Essal Access — the name, tagline, logo, and brand colors that appear on badges, public profiles, and throughout the admin interface.

Navigate to **Settings** in the sidebar, then click the **Branding** tab.

![Settings panel showing the Branding tab with company name, logo upload, and color pickers](../screenshots/settings-general.png)

---

## Company Name and Tagline

At the top of the Branding tab you'll find two fields under **Company Info**:

**Company Name** — The name of your organization. This is used on:

- All employee badges (in the company name position, if enabled in the badge template)
- The admin panel sidebar header
- Public profile pages
- Email notifications

**Tagline** — An optional short phrase shown on badges below the company name (e.g. _"Securing your workplace"_, _"Building 3 — North Wing"_). Leave it blank if you don't need one.

> **Tip**: The Company Name and Tagline fields here are linked to the badge template. Saving a new name or tagline immediately updates what appears on all employee badges — no need to re-open the Badge Designer.

---

## Logo

Under the **Logo** section, click the upload zone (or drag a file onto it) to upload your company logo.

**Supported formats**: PNG, JPG, SVG, WEBP  
**Maximum file size**: 5 MB  
**Recommended**: PNG or SVG with a transparent background so the logo looks clean on any badge color

Once uploaded, the logo appears:

- In the admin panel sidebar
- On employee badges (if **Show Logo** is enabled in the Badge Designer)
- On public profile and verification pages
- On the Employee Portal

To replace the logo, click the upload zone again and select a new file. To remove it entirely, click the **Remove logo** link that appears below the upload zone after a logo is set.

> **Logo not showing on badges?** Open the Badge Designer and check that **Show Logo** is toggled on in the front or back configuration panel. The branding settings upload the logo file — the badge template controls whether and where it appears.

---

## Brand Colors

Under **Brand Colors**, you can set two colors:

**Primary Color** — The main accent color used throughout the admin panel, the Employee Portal, and the check-in app. It also becomes the default badge primary color for new badge templates. Click the color swatch to open a color picker, or type a hex code directly (e.g. `#2563eb`).

**Secondary Color** — A lighter complementary color used for backgrounds and highlights in the interface. Usually a lighter tint of the primary color (e.g. `#eff6ff` for a blue primary).

Changes to brand colors apply immediately across the interface as soon as you save. Both colors also flow into the default badge template — you can always override them independently in the Badge Designer.

---

## BrandFetch — Import Your Brand Automatically

If your company has a public website, the **BrandFetch** feature can automatically import your company name, logo, and primary color palette in one step.

1. Enter your company's website URL in the **Website URL** field (e.g. `essal.cloud`)
2. Click **Fetch Brand**
3. Essal Access queries the BrandFetch database and fills in your company name, logo, and brand colors automatically
4. Review the imported values and click **Save**

BrandFetch works for most companies with an established web presence. If your domain isn't found, you'll see an error — upload your logo and set colors manually in that case.

> BrandFetch imports are a starting point — you can freely edit any imported values after the fetch.

---

## Saving Changes

Click **Save** in the top-right area of the Settings panel to commit your changes. Company name and tagline updates apply to badges immediately. Logo and color changes are visible across the interface as soon as the save completes.
