---
title: "Configuring General Settings"
---

{/* keywords: settings, language, timezone, date format, time format, system name, general settings, localization */}
{/* category: Getting Started */}
{/* audience: Admins */}

This article walks through the **Settings → General** tab — where you configure the system language, date and time display, timezone, and the system name that appears throughout the interface.

Navigate to **Settings** in the sidebar, then make sure the **General** tab is selected (it is the default).

![Settings panel showing the General tab with language, system name, date format, time format, and timezone fields](../screenshots/settings-general.png)

---

## Language

The **Language** dropdown sets the interface language for all admin panel users in your tenant.

| Option       | Value |
| ------------ | ----- |
| English (US) | `en`  |
| Français     | `fr`  |

Changing the language affects all UI text, labels, and button names across the admin panel, the Employee Portal, and the check-in app. It does not affect the content of employee records or article text.

> **Note**: The language selection applies tenant-wide — all users in your organization will see the same interface language. Individual users cannot override this from their own profile.

---

## System Name

The **System Name** field sets a custom label for your instance of Essal Access. This name appears in:

- The browser tab title
- The top of the sidebar
- Email notifications sent to employees

Most organizations set this to their company name (e.g. _Acme Corp Access_) or a descriptive label (_Acme Security Portal_). It can be changed at any time without affecting any employee data or badge designs.

---

## Date Format

The **Date Format** dropdown controls how dates are displayed throughout the admin panel — in employee records, scan logs, audit logs, and ticket validity dates.

| Option       | Example    | Common usage                       |
| ------------ | ---------- | ---------------------------------- |
| `DD/MM/YYYY` | 18/03/2026 | Europe, most of the world          |
| `MM/DD/YYYY` | 03/18/2026 | United States                      |
| `YYYY-MM-DD` | 2026-03-18 | ISO 8601 — technical/international |

Choose the format your team is most familiar with. If your organization operates across multiple countries, `YYYY-MM-DD` is the most unambiguous.

---

## Time Format

The **Time Format** dropdown controls how times are displayed alongside dates in logs, schedules, and timestamps.

| Option        | Example |
| ------------- | ------- |
| `12h (AM/PM)` | 2:45 PM |
| `24h`         | 14:45   |

This setting affects the display of timestamps in the Scan Logs, Audit Logs, and anywhere a time of day is shown. It does not affect how access schedules are configured (those always use 24h input).

---

## Timezone

The **Timezone** dropdown sets the timezone used for all timestamps recorded in your tenant — scan events, audit log entries, employee record changes, and scheduled access windows.

Select the timezone that matches your facility's physical location. For organizations with multiple sites in different timezones, choose the primary headquarters timezone, or use UTC (`UTC+00:00`) for consistency.

> **Important**: Changing the timezone affects how all new timestamps are recorded and displayed. Historical entries already in the log are not retroactively converted — they retain the timezone offset they were recorded with.

---

## Saving Your Changes

All changes on the General tab are applied immediately when you click **Save**. There is no draft mode — clicking Save writes the settings to your tenant.

If you navigate away without saving, your changes are discarded.
