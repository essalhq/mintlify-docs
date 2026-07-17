---
title: "Managing Devices from the Admin Panel"
---

{/* keywords: manage devices, deactivate device, reactivate device, revoke device, device list, admin panel devices */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers */}

The **Check-In Devices** section in the admin panel gives you full visibility into all registered devices across your facility — and the ability to deactivate or permanently remove them.

![Check-In Devices list showing registered devices with status indicators and action menus](../screenshots/checkin-devices-list.png)

---

## The Device List

Each row in the device list shows:

| Column | Description |
|---|---|
| **Status dot** | **Green** = online (seen within the last 5 minutes); **Gray** = offline or stale; **Red** = deactivated |
| **Device name** | The label assigned during setup (e.g. "Main Entrance Tablet") |
| **Location** | The location tag set on the device |
| **Guard name** | The operator name assigned to this device |
| **Last seen** | How long ago the device last sent a heartbeat ("just now", "5m ago", "2h ago") |
| **Deactivated badge** | A red pill shown only when the device has been deactivated by an admin |

---

## Device Actions

Click the **three-dot menu (⋮)** on any device row to access:

### Deactivate

Temporarily prevents the device from scanning. The device receives the deactivation signal on its next heartbeat (within 2 minutes) and is immediately locked with a **Revoked** lock screen. The operator cannot bypass this — they must sign out.

- The device record is retained; no data is lost
- You can **reactivate** the device at any time
- **Use this when:** a device is lost, stolen, or temporarily taken out of service

### Reactivate

Re-enables a previously deactivated device. The device will resume scanning normally on its next heartbeat. The operator may need to tap **Reconnect** on the lock screen.

### Revoke

Permanently removes the device from your organization. The device is deleted from the system — it cannot be reactivated and must be re-registered from scratch if needed again.

- A confirmation dialog is shown before deletion
- All scan logs from the device remain in your **Scan Logs** history
- **Use this when:** a device is permanently decommissioned, replaced, or the app has been reinstalled

---

## Registering a New Device

The top of the Check-In Devices page contains the registration tools:

- **Generate Code** — creates a 6-character one-time code (valid for 15 minutes) that the operator enters during device setup
- **Send Setup Email** — emails a no-expiry registration code and setup instructions to an operator

See the Registering a New Device article for a step-by-step walkthrough.

---

## Monitoring Device Health

The `last seen` timestamp tells you whether each device is actively sending heartbeats:

- **"Just now"** or **"Xm ago" (< 5 min)** — device is online and operational
- **"Xm ago" (5+ min)** — device may have lost connectivity; check the location
- **"Xh ago"** or a date — device has been offline for an extended period; investigate

A device that has been offline for its configured maximum duration (default 24 hours) will show a lock screen to its operator and require a reconnection before scans can resume.
