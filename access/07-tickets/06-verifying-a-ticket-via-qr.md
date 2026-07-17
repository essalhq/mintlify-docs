---
title: "Verifying a Ticket via QR"
---

{/* keywords: ticket verification, verify ticket, QR code ticket, ticket link, scan ticket, public ticket page */}
{/* category: Tickets */}
{/* audience: Admins, Security, Operators */}

Every ticket has a unique public verification link that can be opened or scanned by anyone — no login required. This is how security personnel or event organizers confirm that a ticket is genuine and currently valid.

---

## The Ticket Verification URL

Each ticket is accessible at:

```
https://idpage.link/ticket/{ticketId}
```

Where `{ticketId}` is a unique identifier in the format `TKT-A1B2C3D4E5`. This URL is permanent and always reflects the current status of the ticket.

---

## Copying the Ticket Link

To get the link for a specific ticket:

1. Navigate to **Tickets** in the admin panel
2. Find the ticket row
3. Click the **three-dot menu (⋮)**
4. Select **Copy Link**

The link is copied to your clipboard. You can share it via email, SMS, WhatsApp, or print it on a document. The link also contains an embedded QR code when the page is opened — this allows the recipient to present the page on their phone for scanning.

---

## What the Verification Page Shows

When someone opens a ticket link, they see a clean verification page with:

| Element | Details |
|---|---|
| **Organization logo** | Pulled from your whitelabel settings |
| **Status badge** | "Valid Ticket" / "Expiring Soon" / "Expired" / "Revoked" |
| **Ticket title** | The title entered when the ticket was issued |
| **Ticket type** | Colored dot + type name (e.g. "● Meal") |
| **Description** | Shown only if a description was entered |
| **Issued to** | Employee's full name and department |
| **Valid until** | The expiry date, or "Never expires" in green if no expiry was set |
| **Location** | Shown only if a location was entered |
| **Ticket ID** | Full ID in monospace format (e.g. `TKT-A1B2C3D4E5`) |
| **Language selector** | Lets the viewer switch the page language |

---

## Status Colors on the Verification Page

The accent stripe at the top of the ticket card and the status badge change color based on the ticket's current status:

| Status | Color | What it means |
|---|---|---|
| Valid (Active) | Your org's brand color | Ticket is valid — allow entry or access |
| Expiring Soon | Amber | Valid now but expires within 3 days |
| Expired | Amber | Validity window has passed — do not honor |
| Revoked | Red | Manually cancelled — do not honor |

---

## Language Support

The verification page automatically detects the viewer's browser language and displays content in the matched language. Supported languages:

- English
- Arabic (right-to-left layout)
- French
- Spanish  
- German

A **language selector** at the bottom of the page allows manual switching.

---

## Ticket Not Found

If the link is opened with an invalid or deleted ticket ID, the page displays an error card with a red icon and a "Ticket not found" message. This can happen if the ticket was **deleted** from the admin panel. Revoked tickets still have a visible page — they show the Revoked status rather than a not-found error.

---

## Using the Check-In App to Verify Tickets

Ticket QR codes can also be scanned using the Essal Check-In App (scan.idpage.link) in the same way employee badges are scanned. The result card will display the ticket holder's name and access result. See the Check-In Devices section for setup instructions.
