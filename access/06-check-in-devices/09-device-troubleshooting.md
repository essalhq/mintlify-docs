---
title: "Device Troubleshooting"
---

{/* keywords: device troubleshooting, scanner not working, offline lock, can't scan, device not connecting, fix check-in device */}
{/* category: Check-In Devices */}
{/* audience: Admins, Operators */}

This article covers the most common issues with check-in devices and how to resolve them.

---

## The device shows an "Offline Lock" screen

**Cause:** The device has not connected to the internet for longer than the configured offline limit (default: 24 hours).

**Fix:**
1. Ensure the device has a working internet connection (try opening a website in the browser)
2. Tap **Reconnect** on the lock screen
3. If the connection is successful, the app reopens to the scan screen

If the lock screen shows a **🚫 (Revoked)** icon instead of **📡**, the device has been deactivated from the admin panel — see the Revoked section below.

---

## The device shows a "Revoked" lock screen

**Cause:** An administrator has deactivated this device from the admin panel, or the device is connecting as a different tenant than expected.

**Fix (if deactivated by mistake):**
1. Log in to the admin panel
2. Go to **Check-In Devices**
3. Find the device and click **Reactivate**
4. The device will restore scanning on the next heartbeat (tap **Reconnect** to force it immediately)

**Fix (if the device should be permanently removed):**
1. The operator taps **Sign Out** on the lock screen
2. Re-register the device with a new code

---

## Camera won't open or shows a black screen

**Cause:** Camera permission denied, or another app is using the camera.

**Fix:**
1. Check that camera permission is granted — go to the device's **browser site settings** and allow camera access for `scan.idpage.link`
2. Close any other apps that might be using the camera
3. Refresh the app (pull to refresh or reopen from home screen)
4. On iOS, if permission is denied at the system level, go to **Settings → Safari → Camera** and allow access

---

## QR codes are not being detected

**Cause:** Poor lighting, camera focus, or the QR code is too small or damaged.

**Fix:**
- Ensure there is adequate lighting at the scan point
- Hold the badge 15–30 cm from the lens and keep it steady
- Clean the camera lens
- Try switching to **Manual** mode and entering the badge ID by typing or using the on-screen numpad
- If the badge QR code is printed, check whether the print quality is too low — see the Printing & Exporting Badges section for guidance

---

## Scans are giving "Not Found" results for valid employees

**Cause:** The employee data cache has not synced yet, or the employee's record is in a different tenant.

**Fix:**
1. Go to **Settings** → **Data Cache** → tap **Force Sync**
2. Wait for the sync to complete and try scanning again
3. Verify in the admin panel that the employee exists and their status is **Active**

---

## The same scan appears multiple times in the log

**Cause:** The duplicate scan window is set too short, or a USB barcode scanner fired the code multiple times.

**Fix:**
1. Open **Settings** → **Scanner** → increase the **Duplicate scan window** (e.g., from 5 to 10 seconds)
2. If using a USB/Bluetooth barcode scanner (Android app), check the scanner's own configuration for repeated-scan suppression

---

## The app is very slow or lagging

**Fix:**
1. Go to **Settings** → **Data Cache** → tap **Clear Cache**, then **Force Sync** to rebuild the database cleanly
2. If the device is old or has limited storage, consider reducing the employee photo pre-fetch by removing profile photos that are not strictly needed
3. Restarting the app (close and reopen from home screen) clears any lingering memory

---

## A device disappeared from the admin panel

**Cause:** The device was revoked (deleted) from the admin panel, or the database entry expired.

**Fix:** The device must be re-registered. Generate a new code from **Check-In Devices** and walk through the setup wizard on the device again. Previous scan logs for that device are preserved.

---

## "Cache expired" denial result

**Cause:** The device has been offline for more than 24 hours and its local data is stale. As a safety measure, the app denies access rather than using potentially outdated records.

**Fix:** Connect the device to the internet and tap **Force Sync** in Settings. Once the cache is refreshed (typically within a few seconds), scans will work correctly.
