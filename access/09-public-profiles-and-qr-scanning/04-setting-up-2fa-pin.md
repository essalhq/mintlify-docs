---
title: "Setting Up a 2FA PIN for a Badge"
---
{/* category: Public Profiles & QR Scanning */}


A 2FA PIN adds a second layer of verification to an employee's badge. When enabled, anyone scanning the badge must enter a 4-digit PIN before the public profile is displayed. This is useful for high-security roles or sensitive areas.

## How It Works

When a badge with a PIN requirement is scanned:

1. The scanner sees a **PIN entry screen** instead of the public profile.
2. They enter the 4-digit code.
3. If the code is correct, the system records a verified scan event and the profile is displayed.
4. If the code is wrong, the attempt is logged. After 5 incorrect attempts, the PIN is locked and further attempts are blocked.

All verification attempts — successful and failed — are recorded in the audit log with device information and timestamp.

## Enabling a PIN for an Employee

1. Open the employee record (**Employees** → click the employee → **Edit**).
2. Check the **Require PIN (2FA)** option.
3. Enter a 4-digit PIN code in the **PIN Code** field.
4. Save the employee record.

From the next scan onwards, the PIN screen will appear before the profile is shown.

## The PIN Entry Screen

The visitor entering the PIN sees four individual digit boxes. The screen supports:

- **Auto-advance** — focus moves to the next box as each digit is typed
- **Backspace navigation** — deleting a digit returns focus to the previous box
- **Paste** — pasting a 4-digit code fills all boxes automatically and submits immediately
- **Enter key** — pressing Enter after the last digit submits

The screen uses the organization's primary brand color.

## Lockout Behavior

After **5 incorrect attempts** the PIN is locked. A locked PIN displays a "Too many attempts" error and will not accept further entries. Contact an administrator to reset or change the PIN.

## Disabling or Changing a PIN

To remove the PIN requirement:

1. Open the employee record.
2. Uncheck the **Require PIN (2FA)** option.
3. Save.

To change the PIN, update the **PIN Code** field with the new 4-digit value and save.
