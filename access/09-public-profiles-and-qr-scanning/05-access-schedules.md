---
title: "Access Schedules"
---
{/* category: Public Profiles & QR Scanning */}


An access schedule restricts when an employee's badge can be scanned. Scans outside the configured time window are blocked and the visitor is shown the allowed hours, rather than the employee's profile.

## When to Use Access Schedules

Use access schedules for employees whose badge should only validate during working hours — for example, contractors with fixed shifts, or temporary staff with limited site access.

## Configuring a Schedule

1. Open the employee record (**Employees** → click the employee → **Edit**).
2. Find the **Access Schedule** section and enable it.
3. Set the **Start time** and **End time** (24-hour format).
4. Choose which days the badge is valid:
   - **Allowed days** — select individual days of the week (Sunday through Saturday)
   - Or use **Weekdays only** to allow Monday through Friday automatically
5. Save the employee record.

The schedule takes effect immediately on the next scan.

## What Happens Outside the Schedule

When someone scans the badge outside the allowed hours or days, they see an **Outside Work Hours** message instead of the profile. The screen displays:

- The allowed time window (e.g. "08:00 – 17:00")
- The allowed days, highlighted in a row of day abbreviations
- A note explaining that access is limited to these hours

The scan is recorded in the audit log with a `denied` status and the reason `outside_schedule`.

## Disabling a Schedule

To remove a schedule from an employee:

1. Open the employee record.
2. Find the **Access Schedule** section.
3. Disable (toggle off) the schedule.
4. Save.

Badge scans for that employee will no longer be restricted by time.

## Time Zone

Schedules are evaluated server-side using the time zone configured for the organization. Make sure your organization's time zone is set correctly in **Settings → General** to ensure schedules match local working hours.
