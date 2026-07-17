---
title: "Sharing a Guest Badge Link"
---

{/* keywords: share guest badge, copy badge link, guest badge URL, send badge link, QR code guest */}
{/* category: Guest Badges */}
{/* audience: Admins, Managers, Reception */}

Every guest badge has a unique, permanent link that can be shared with the guest and scanned by security personnel.

![Guest Badges list with action menu showing Copy Link and View Badge options](../screenshots/guest-badges-list.png)

---

## The Badge URL Format

Every guest badge is accessible at:

```
https://idpage.link/guest/{token}
```

Where `{token}` is a unique UUID generated at the time of creation. This URL is:
- **Public** — no login required to open it
- **Permanent** — the link does not change or expire (the badge status does)
- **Unique** — each badge has a different token; links cannot be guessed

---

## How the Invite Email Is Sent

When you click **Send Invite** (or **Send N Invites**), Essal Access automatically emails the badge link to each guest's email address. The email includes:
- The badge link and a QR code image
- The visit details (purpose, validity window, host name, access zones)
- Your organization's branding (logo and name)

No further action is needed on your part.

---

## Copying the Link Manually

If you need to re-share the link after the initial invite (or if the email bounced), you can copy it from the admin panel:

1. Navigate to **Guest Badges**
2. Find the badge row in the list
3. Click the **three-dot menu (⋮)** at the end of the row
4. Select **Copy Link**

The badge URL is copied to your clipboard and a confirmation notification appears. You can then paste it wherever you need — SMS, WhatsApp, Slack, a printed email, etc.

---

## Viewing the Badge Page

To preview exactly what the guest will see when they open the link:

1. Find the badge row in the **Guest Badges** list
2. Click the **three-dot menu (⋮)**
3. Select **View Badge**

The public verification page opens in a new browser tab.

---

## For Security Guards

Guards do not need to log in to verify a badge. When a guest arrives and presents their QR code on their phone screen, the guard can:

1. Open any QR scanner (including the camera app on a smartphone)
2. Scan the QR code on the guest's phone
3. The badge page opens in the browser, showing the guest's name, purpose, validity, and access zones

The top bar of the page is color-coded so the status is visible at a glance:
- **Blue** → Active / valid
- **Amber** → Expired
- **Red** → Revoked

