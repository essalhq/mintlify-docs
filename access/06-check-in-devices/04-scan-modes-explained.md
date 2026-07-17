---
title: "Scan Modes Explained"
---

{/* keywords: scan mode, QR scanner, photo capture, AI face recognition, badge mode, camera mode */}
{/* category: Check-In Devices */}
{/* audience: Admins, Security, Operators */}

The check-in app supports three scan modes. You can switch between them using the mode selector at the top of the **Scan** tab. The last-used mode is remembered.

---

## Badge Mode (QR Scanner)

**Badge mode** is the primary and most commonly used mode. It activates the device camera as a live QR code reader.

**How it works:**
- The camera opens with a full-screen viewfinder
- A transparent scanning window sits in the center of the screen with corner brackets and an animated scan line
- Point the camera at any Essal badge QR code and the scan happens automatically — no button press needed
- Results appear immediately on screen

**What it can scan:**
- QR codes on printed employee badges
- QR codes on digital badges displayed on an employee's phone
- Guest badge links on a visitor's phone screen
- Raw badge IDs (e.g. `B-XXXXX`) entered via the Manual tab

**Best for:** Standard access control at entrances, turnstiles, and checkpoints where employees or guests present a badge.

**Android app only:** The Android version also supports **USB and Bluetooth barcode scanners** (HID keyboard emulation mode). The app intercepts rapid key input sequences and treats them as scanned codes, which means a physical scanner can be used at a fixed desk without pointing a camera.

---

## Photo Mode (Camera Capture)

**Photo mode** lets the operator take a photo of the visitor using the device camera. This is used for visitor logging and situations where a badge may not be present.

**How it works:**
1. Camera opens for capture
2. Operator takes the photo
3. Preview screen appears — optionally enter a reference ID (badge or employee ID) and a note
4. Tap **Confirm** to record the entry

**What it records:**
- The captured photo (stored locally and synced to the cloud when online)
- If a reference ID was provided, the full verification result (granted/denied/etc.) is recorded alongside the photo
- If no reference ID was provided, the entry is recorded as `photo_capture` with result `granted`

**Best for:** Visitor reception desks, situations where guests don't have a digital badge, or when visual identity verification is required alongside badge scanning.

---

## AI Face Mode

**AI face mode** uses artificial intelligence to recognize faces from the device camera and match them against registered employee photos.

- Configurable confidence threshold (default: 85%)
- Optional auto-approval when a match is found above the threshold
- Requires employees to have profile photos uploaded

> **Note:** AI face recognition is a premium feature. Availability depends on your organization's subscription plan.

---

## Switching Scan Modes

Tap the mode selector pill bar at the top of the **Scan** tab to switch between modes. The selected mode is highlighted and the corresponding scanner opens immediately. The app remembers your last-used mode and restores it on next launch.
