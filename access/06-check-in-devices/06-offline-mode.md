---
title: "Offline Mode"
---

{/* keywords: offline mode, offline scanning, cache, no internet, disconnected, offline lock */}
{/* category: Check-In Devices */}
{/* audience: Admins, Security, Operators */}

The Essal Check-In App is designed to keep working even when the device loses internet connectivity. Employee and guest data is cached locally so that scans can be verified without a live connection.

---

## How Offline Mode Works

When the device is online, it continuously syncs data to a local database stored on the device:

- **On startup:** a full sync downloads all employees and guest badges for your organization
- **Every 5 minutes:** an incremental sync fetches any records updated since the last sync
- **Employee photos** are pre-fetched in the background so they appear on result cards even offline
- **Real-time updates** are received via a live database subscription when online

All sync data is stored in an on-device database (IndexedDB), keyed to your organization. Data from other organizations is never mixed in.

---

## Cache Freshness

| Threshold | Behavior |
|---|---|
| Data is less than **10 minutes old** | Used directly; no re-fetch attempted |
| Data is **10+ minutes old** but within 24 h | App tries to refresh from server; if offline, uses cached data with a "from cache" indicator on the result card |
| Data is **24+ hours old** | Returns an **Expired** result with denial reason "Cache expired" — the device must reconnect to refresh |

---

## Check-In Log When Offline

Scan events are **always recorded**, whether the device is online or offline:

- Every scan is saved immediately to the local database
- When the device comes back online, pending events are automatically flushed to the server
- Photo captures are also uploaded when connectivity is restored

No scan data is lost due to connectivity issues.

---

## Heartbeat and Online Status

The device sends a **heartbeat signal every 2 minutes** to the server while online. This updates the `last seen` timestamp visible in the admin panel.

The device also uses the heartbeat response to check its activation status:
- If the server reports the device has been **deactivated** by an admin, the app immediately shows an offline lock screen
- The last heartbeat time is stored locally so the app can calculate how long it has been offline

---

## Offline Warning and Lock

The app monitors how long it has been since the last successful server connection:

**Warning (amber banner):** Shown when the device has been offline for **2 hours less than the configured maximum** (e.g., warns at 22 hours if the limit is 24 hours). The app is still fully functional.

**Offline lock (📡):** Shown when the device exceeds the maximum offline duration (default: **24 hours**). Scanning is disabled until the device reconnects. The screen shows when the device last came online and a **Reconnect** button to retry.

**Revoked lock (🚫):** Shown when the admin has deactivated the device from the admin panel. This lock cannot be dismissed — the operator must sign out. To restore access, an administrator must reactivate the device from the admin panel and re-register it if necessary.

---

## Adjusting the Offline Limit

The maximum offline duration is configurable per device. By default it is **24 hours**. To change it, edit the `Max offline hours` setting in the **Settings** tab of the check-in app. Lower values are recommended for high-security environments.
