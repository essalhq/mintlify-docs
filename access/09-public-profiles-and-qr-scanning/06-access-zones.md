---
title: "Access Zones"
---
{/* category: Public Profiles & QR Scanning */}

Access zones are named areas within your facility — such as "Lobby", "Server Room", or "Floor 2". You can assign zones to employees and guest badges to indicate which areas they are authorized to enter. Zones are visible on the public profile when the **Access Level** field is enabled.

## Creating Access Zones

Zones are defined at the organization level in **Settings → Access Zones** (or **Settings → Departments & Zones**, depending on your version).

For each zone, you can set:
- **Name** — the label used throughout the system (e.g. "Restricted Lab")
- **Description** — optional notes about the zone
- **Color** — a color used when displaying the zone as a badge/chip in the UI

## Assigning Zones to an Employee

1. Open the employee record (**Employees** → click the employee → **Edit**).
2. Find the **Access Zones** field.
3. Select one or more zones from the list.
4. Save.

The selected zones are stored on the employee record and shown on their public profile (if **Show access level** is enabled in the Public Page Editor).

## Zones on the Public Profile

When **Show access level** is turned on in the Public Page Editor, a scanner viewing the employee's badge profile can see which zones the employee is authorized for. Each zone appears as a colored chip.

## Zones on Guest Badges

When creating a guest badge, you can specify which access zones the guest is permitted to enter. These zones are shown prominently on the guest verification page along with the guest's name and validity dates.

## How Zones Relate to Check-In Devices

Check-in devices are associated with a physical **location** (configured when the device is registered). Zones and device locations are separate concepts — zones define what an employee is authorized for, while device location records where a scan happened. Combined, they provide a full picture in the scan logs of who was scanned where and whether they were authorized.
