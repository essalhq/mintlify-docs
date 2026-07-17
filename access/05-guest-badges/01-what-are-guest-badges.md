---
title: "What Are Guest Badges?"
---

{/* keywords: guest badge, visitor badge, temporary badge, visitor access, QR code badge, guest pass */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception */}

Guest Badges are temporary, QR-code-based passes you can create for visitors, contractors, event attendees, delivery personnel, or anyone else who needs short-term access to your facility — without requiring them to have an employee account.

![Guest Badges list showing visitor passes with their status and validity period](../screenshots/guest-badges-list.png)

---

## How Guest Badges Work

When you create a Guest Badge, Essal Access generates a unique, shareable link in the format:

```
https://idpage.link/guest/{token}
```

This link (and its embedded QR code) can be:
- **Emailed** directly to the guest at the time of creation — Essal sends the invite automatically
- **Copied and shared** manually via any channel (SMS, WhatsApp, printed email, etc.)
- **Scanned at the entrance** by a security guard using any QR reader or check-in device

No app, account, or login is required for the guest to use the badge.

---

## What Makes Guest Badges Different from Employee Badges

| Feature | Employee Badge | Guest Badge |
|---|---|---|
| Requires an employee profile | ✓ | ✗ |
| Uses a custom badge design template | ✓ | ✗ |
| Has a validity period | ✗ (permanent) | ✓ (defined at creation) |
| Can be revoked manually | ✗ | ✓ |
| Public link for verification | ✗ | ✓ |
| Sent by email invite | ✗ | ✓ |

---

## When to Use Guest Badges

- **Site visits** — external clients, partners, or inspectors visiting the premises
- **Interviews** — job candidates arriving for on-site interviews
- **Meetings** — attendees for scheduled in-person meetings
- **Deliveries** — couriers or logistics personnel who need temporary access
- **Events** — participants at a conference, open day, or training session
- **Contractors** — short-term workers who don't need full employee accounts

---

## Key Concepts

- **Validity window** — each badge has a `valid from` and `valid until` timestamp. Guards can see this on the scanned page.
- **Access zones** — if your organization has defined access zones, you can specify which areas a guest is permitted to enter.
- **Automatic expiry** — badges past their `valid until` time automatically show as **Expired** without any manual action.
- **Revocation** — an admin can manually revoke a badge at any time, instantly invalidating it even if the validity window hasn't ended.

