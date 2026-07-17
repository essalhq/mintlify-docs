---
title: "Understanding Scan Results"
---

{/* keywords: scan result, access granted, access denied, badge expired, badge revoked, not found, result card */}
{/* category: Check-In Devices */}
{/* audience: Security, Operators, Admins */}

After each scan, the check-in app displays a result card that tells the operator whether to allow or deny entry. Each result has a distinct color and label so the decision can be made at a glance.

---

## Result Types

### Access Granted — Green

The person's badge is valid and they are permitted to pass.

This result appears when:
- The employee's status is **active** and the current time is within their configured access schedule
- The guest badge is **active** and within its `valid from` / `valid until` window

**Feedback:** A single beep and a short vibration (80 ms).

---

### Access Denied — Red

The person should not be permitted to pass.

This result appears when:
- The employee's status is `suspended`, `terminated`, or `lost badge`
- The employee's account is in `pending` state (not yet active)
- The current time is outside the employee's permitted access hours
- A guest badge's `valid from` time has not yet been reached

The result card shows the **denial reason** so the operator understands why access was denied (e.g., "Outside access hours", "Account suspended").

**Feedback:** A denial sound and a triple vibration burst.

---

### Badge Expired — Amber

The badge was valid but is no longer current.

This result appears when:
- A guest badge's `valid until` time has passed
- The device's locally cached employee data is more than **24 hours old** and the device cannot reach the server to refresh it — in this case, the denial reason shows "Cache expired" and the operator should check internet connectivity

**Feedback:** A denial sound and a triple vibration burst.

---

### Badge Revoked — Orange

The badge has been manually cancelled by an administrator.

This result appears when a guest badge has been explicitly revoked from the admin panel. The person should not be allowed to enter regardless of what they claim.

**Feedback:** A denial sound and a triple vibration burst.

---

### Not Found — Gray

The scanned code does not match any employee or guest in the system.

This result appears when:
- The QR code is not an Essal badge (wrong app, corrupted code, or a badge from a different organization)
- The badge ID has been deleted from the system
- The scan was attempted from a device registered to a different organization

**Feedback:** A denial sound and a triple vibration burst.

---

## The Result Card

After every scan, a result card slides up from the bottom of the screen showing:

- The person's **photo** (from cache or their profile; falls back to a person icon if unavailable)
- **Full name**, role, and department
- The **result label** (ACCESS GRANTED / ACCESS DENIED / etc.)
- **Denial reason** (if denied)
- **Access zones** they are permitted to enter (as chips)
- For guests: **host name**, **purpose**, and **valid until** datetime
- A **"from cache"** indicator if the data was served from the local offline cache

The card **auto-dismisses** after a configurable delay (default: 4 seconds). Tap anywhere on the card to dismiss it manually. On the Android app, a non-blocking 2-second toast is shown instead, keeping the camera active for continuous high-throughput scanning.

---

## View Profile (Employees)

Active employee result cards include a **View Profile** button that opens a full profile modal with additional details. When the profile modal is open, the auto-dismiss timer is paused so the operator has time to review.
