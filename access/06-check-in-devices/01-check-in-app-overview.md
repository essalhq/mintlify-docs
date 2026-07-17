---
title: "Check-In App Overview"
---

{/* keywords: check-in app, scanner app, device overview, essal scanner, scan.idpage.link */}
{/* category: Check-In Devices */}
{/* audience: Admins, Managers, Security */}

The Essal Check-In App is a dedicated scanning application installed on tablets or phones at your access points. It reads employee badge QR codes and guest badge links, verifies them against your organization's data, and instantly displays whether the person should be granted or denied access.

![Check-In Devices list showing registered devices with their online status and last-seen time](../screenshots/checkin-devices-list.png)

---

## What the Check-In App Does

- **Scans QR codes** printed on employee badges or displayed on a guest's phone
- **Verifies identity and access rights** in real time, including access schedules and zones
- **Works offline** — data is cached locally so scans work even when internet connectivity drops
- **Logs every scan event** with a timestamp, result, and operator name
- **Supports multiple scan modes** — camera QR scan, photo capture, or AI face recognition

---

## How It's Installed

The check-in app is a separate web application (PWA) hosted at **`https://scan.idpage.link`**. It is not part of the main Essal Access admin panel.

To install it on a device:
1. Open **`https://scan.idpage.link`** in the browser on the device
2. Follow the browser prompt to **Add to Home Screen** (or install as a PWA)
3. Enter the registration code provided by your administrator

An **Android APK** ("Essal Scanner") is also available for organizations that prefer a native app experience. The Android version adds support for USB and Bluetooth barcode scanners.

---

## Overview of the App Screens

Once registered and unlocked, the app has four tabs:

| Tab | Purpose |
|---|---|
| **Scan** | Live camera scanner — the main operating screen |
| **Log** | Today's check-in history with result details |
| **Manual** | Enter a badge or employee ID manually via keyboard or numpad |
| **Settings** | Configure device name, scan behavior, appearance, and data cache |

---

## Managing Devices from the Admin Panel

Administrators can view, deactivate, and revoke all registered devices from **Admin → Check-In Devices**. The admin panel shows each device's name, location, guard name, online status, and last-seen timestamp, giving full visibility into which devices are active across your facility.

---

## Differences: PWA vs Android App

| Feature | PWA (scan.idpage.link) | Android App |
|---|---|---|
| USB/Bluetooth barcode scanner | ✗ | ✓ |
| Non-blocking scan toast | ✗ | ✓ |
| Hardware back button support | ✗ | ✓ |
| Swipe tab navigation | ✗ | ✓ |
| Installation | Browser / Add to Home Screen | APK install |
