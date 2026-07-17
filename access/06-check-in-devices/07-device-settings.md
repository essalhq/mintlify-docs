---
title: "Device Settings"
---

{/* keywords: device settings, app settings, auto dismiss, beep volume, vibration, theme, language, pin, sign out */}
{/* category: Check-In Devices */}
{/* audience: Operators, Admins */}

The **Settings** tab (gear icon) inside the check-in app lets operators and administrators configure how the device looks and behaves. Changes take effect immediately and are saved locally on the device.

---

## Appearance

| Setting | Options | Default |
|---|---|---|
| **Theme** | Dark / Light / System | Dark |

The Dark theme is recommended for dimly lit environments (warehouses, event venues). Light theme works better in well-lit offices.

---

## Language

| Setting | Options | Default |
|---|---|---|
| **Interface language** | English / Français / العربية | English |

Changing the language updates all labels in the app, including scan result cards. Arabic switches the entire interface to right-to-left layout.

---

## Device Information

These fields are editable and stored locally. They are displayed to admins in the **Check-In Devices** panel.

| Setting | Notes |
|---|---|
| **Device name** | A label for this device (e.g. "Main Entrance Tablet") |
| **Guard name** | The name of the operator (e.g. "Ahmed — Night Shift") |
| **Location** | A description of where the device is placed |

Click **Save** after making changes. These updates are stored locally and reflected in the device's identity within the check-in log.

---

## Scanner Behavior

| Setting | Range | Default | Notes |
|---|---|---|---|
| **Auto-dismiss delay** | 1 – 15 seconds | 4 seconds | How long the result card stays on screen before auto-dismissing |
| **Duplicate scan window** | 1 – 30 seconds | 5 seconds | During this period after a scan, the same badge code is ignored to prevent duplicate entries |
| **Beep volume** | 0 – 100% | 60% | Volume of the access granted / denied sound |
| **Vibration** | On / Off | On | Toggle haptic feedback. Turning on triggers a test buzz. |

---

## Data Cache

The data cache section shows how much data is stored locally for offline scanning:

| Counter | What it shows |
|---|---|
| Employees | Number of employee records cached |
| Guests | Number of guest badge records cached |
| Log entries | Total scan events stored locally |
| Unsynced | Events not yet pushed to the server |

**Force Sync** — immediately triggers a full data refresh from the server. Use this after making bulk employee changes in the admin panel, or after extended offline use.

**Clear Cache** — removes all locally cached employee and guest records. The device will re-download data on the next sync. Use this to free up storage or troubleshoot stale data.

---

## Security (PIN Lock)

If a security PIN has been configured for this device, the **PIN lock** section shows its status. When enabled:
- The app locks automatically when moved to the background or screen times out
- A PIN is required to resume scanning
- The PIN is stored as a hashed value (never in plain text)

PIN configuration is managed by the administrator from the admin panel.

---

## Other Settings

| Setting | Notes |
|---|---|
| **Install App** | Shows a button to trigger the browser's PWA install prompt (only visible if the app is not yet installed as a standalone app) |
| **Geolocation** | Request or view the status of the geolocation permission (used for location-tagged scan logs) |

---

## Signing Out

The **Sign Out** button at the bottom of Settings:
- Clears the device configuration from local storage
- Deletes the local offline cache (IndexedDB)
- Returns the app to the setup wizard

> **Warning:** Signing out permanently removes the device's local data and registration. The device will need to be re-registered. Before signing out, ensure that all pending offline scan events have synced (check the **Unsynced** counter in Data Cache).
