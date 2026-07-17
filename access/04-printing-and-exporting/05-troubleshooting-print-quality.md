---
title: "Troubleshooting Print Quality Issues"
---

{/* keywords: print quality, blurry badge, missing photo print, badge cut off, print not working, PDF badge, browser print tips, low resolution print */}
{/* category: Printing & Exporting Badges */}
{/* audience: Admins, Managers */}

This article covers common problems with badge printing and PNG exports, and how to resolve them.

---

## Badge Looks Blurry or Low-Resolution When Printed

**Cause**: The employee's profile photo was uploaded at low resolution.

**Fix**:

1. Open the employee record → **Profile** tab
2. Upload a higher-resolution photo — ideally at least **600 × 600 px**, recommended **1000 × 1000 px** or larger
3. The badge preview and export will automatically use the new photo

> **Source photo quality matters**: Badge exports use a 4× pixel ratio, which means a 150 × 150 px source photo will appear visibly soft when the badge is printed at card size. Always use photos of at least 600 px on the shortest side.

The badge template elements (colors, QR code, text) are vector/crisp at all sizes — only raster photos can appear blurry.

---

## Employee Photo Is Missing on the Printed Badge

**Possible causes and fixes:**

| Cause                                          | Fix                                                                                                                                           |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Photo not uploaded                             | Open employee record and upload a photo                                                                                                       |
| Photo upload still processing                  | Wait a few seconds and reload the Print Center                                                                                                |
| Photo URL blocked by CORS                      | The system auto-converts photos to base64 for export — if the photo was added via an external URL rather than uploaded, re-upload it directly |
| "Show Photo" toggle disabled in Badge Designer | Enable **Show Photo** in Badge Designer → Structure & Elements                                                                                |

---

## Company Logo Is Missing on the Printed Badge

**Possible causes:**

- Logo not uploaded in Settings → Branding, or in Badge Designer → Branding tab
- "Show Logo" toggle disabled in Badge Designer

**Fix**: Navigate to **Badge Designer → Branding tab** and upload or verify the logo. Ensure **Show Logo** is enabled in Structure & Elements.

---

## Badge Layout Is Cut Off or Clipped

**Cause**: Browser print margins are adding extra space, or the scale is too large.

**Fixes**:

1. In the browser print dialog, set **Margins** to **None** or **Minimum**
2. In the Print Center **Config** tab, reduce **Badge Scale** to 90% or 95%
3. Ensure **Page Size** in the Config tab matches the paper loaded in your printer
4. Disable **Fit to page** or **Scale to fit** in the browser print dialog — always use **100%**

---

## Colors Look Wrong or Washed Out When Printed

**Cause**: Browser is printing without background colors enabled.

**Fix**: In the browser print dialog, look for an option called:

- **Background graphics** (Chrome)
- **Print backgrounds** (Firefox)
- **Background colors and images** (Edge)

Enable this option before printing. Badge colors, gradients, and the QR code background all require background printing to be enabled.

---

## The Print Dialog Opens Blank or Shows No Badges

**Cause**: Browser blocked the `window.print()` call, or the badge rendering did not complete before printing started.

**Fixes**:

1. Click **Print Badge** again — sometimes browsers block the first popup
2. Allow popups for `access.essal.cloud` in your browser settings
3. Wait until the badge preview fully loads in the Print Center before clicking Print
4. If using a slow connection, wait a few extra seconds — the badge renderer needs photos and the logo to load first

---

## ZIP Export Stalls or Does Not Complete

**Cause**: One or more employee photos failed to load, or the browser tab became inactive.

**Fixes**:

1. Keep the browser tab active and visible during export — some browsers throttle background tabs
2. If progress stops (e.g. stuck at 5/20), refresh the page and try again with fewer employees
3. Check your internet connection — each photo needs to be downloaded during rendering
4. Try exporting in smaller batches (e.g. 25 at a time instead of all employees)

---

## Downloaded PNG Has No Photo or Broken Layout

**Cause**: The export ran before all images finished loading.

**Fix**: In the Print Center, select the employee and wait until you can see their photo in the badge preview panel before clicking **Download PNG**. The export uses the same rendering pipeline — if the preview shows the photo, the PNG will too.

---

## PDF Export Tips

Essal Access does not produce a PDF directly — it uses the browser's print-to-PDF feature. To save as PDF:

1. Click **Print Badge** or **Secure Download** (bulk)
2. In the browser print dialog, change the **Destination** / **Printer** to **Save as PDF**
3. Click **Save**

For best PDF quality:

- Set margins to **None**
- Enable background graphics
- Use **100% scale**
- Choose the same paper size as your Config tab setting

---

## Still Having Issues?

If none of the above resolves the problem, contact Essal Support with:

- A screenshot of the Print Center showing the issue
- The browser and version you're using (Chrome / Firefox / Edge / Safari)
- Whether the issue is with the browser print or the PNG/ZIP download
