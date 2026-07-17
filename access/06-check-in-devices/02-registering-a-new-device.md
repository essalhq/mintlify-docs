---
title: "Registering a New Device"
---

{/* keywords: register device, setup check-in device, add scanner, registration code, device registration */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers */}

Registering a device links it to your organization and allows it to access your employee and guest data. Registration takes a few minutes and only needs to be done once per device.

![Check-In Devices list showing the Generate Code button and registered device entries](../screenshots/checkin-devices-list.png)

---

## Before You Begin

- The device must have a browser that supports camera access (Chrome recommended)
- The device must be able to reach `https://scan.idpage.link`
- You will need an administrator account in the Essal Access admin panel to generate the registration code

---

## Step 1 — Generate a Registration Code

1. Log in to the Essal Access admin panel
2. Navigate to **Check-In Devices** in the sidebar
3. Click **Generate Code**
4. A 6-character code appears (e.g. `A3F7B2`) with a countdown timer
5. The code is valid for **15 minutes** — the timer turns red when less than 60 seconds remain
6. Click the copy icon to copy the code, or read it aloud to the person setting up the device

> If the code expires before it is used, click **Generate Again** to get a new one immediately.

---

## Step 2 — Open the Check-In App on the Device

1. On the device, open a browser and go to **`https://scan.idpage.link`**
2. If prompted to install the app, follow the **Add to Home Screen** instructions (optional but recommended)
3. The setup wizard launches automatically on first open

---

## Step 3 — Complete the Setup Wizard

The wizard walks through the following steps:

**1. Choose language** — select English, French (Français), or Arabic (العربية). The app interface and results will be shown in this language.

**2. Install app (optional)** — if the browser shows an install prompt, click **Install** to add the app to the home screen for easier access. Tap **Continue in browser** to skip.

**3. Enter registration code** — type the 6-character code from the admin panel. The code is automatically converted to uppercase as you type. Tap **Confirm** — Essal verifies the code with the server and links the device to your organization.

**4. Enter device details:**
- **Guard name** (required) — the name of the operator using this device (e.g. "Main Gate Security")
- **Device name** (required) — a label for this device (e.g. "Main Entrance Tablet")
- **Location** (optional) — a description of where the device is placed

**5. Confirm** — the app saves the configuration locally and opens the scan screen.

---

## What Happens After Registration

- The device appears immediately in the admin panel's **Check-In Devices** list
- The device's employee and guest data cache begins syncing in the background
- The device sends a **heartbeat every 2 minutes** so the admin panel can show its online status
- All scan events are logged and visible in the **Scan Logs** view

---

## Editing Device Details Later

Device name, guard name, and location can be edited later from the **Settings** tab inside the check-in app. These changes are saved locally on the device and do not require re-registration.
