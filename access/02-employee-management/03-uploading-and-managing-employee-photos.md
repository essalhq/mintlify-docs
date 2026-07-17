---
title: "Uploading and Managing Employee Photos"
---

{/* keywords: employee photo, upload photo, profile picture, webcam, take photo, AI background removal, Claid, photo upload, badge photo */}
{/* category: Employee Management */}
{/* audience: Admins, Managers */}

Employee photos appear on their badge, public profile, and the employee portal. This article covers the three methods for adding a photo and how to manage it after upload.

Navigate to **Employees**, open the employee's record, and make sure you are on the **Profile** tab. The photo section is on the left side of the form.

![Employee modal Profile tab showing the photo upload area on the left side](../screenshots/employee-modal-profile.png)

---

## Method 1 — Upload from File

1. Click the **Upload Photo** button below the photo circle, or click directly on the photo circle itself
2. A file picker opens — select any image file (JPG, PNG, WEBP, GIF, etc.)
3. The photo is uploaded and the circle updates immediately

**File size limit**: 2 MB. If the selected file is larger, an error message appears and the upload is rejected.

**Recommended specs**:

- Minimum 400×400 px for a clear badge print
- Square crop works best — the badge displays the photo in a circle
- PNG or JPG for web; avoid animated GIFs

> **AI background removal**: If your tenant has the Claid photo enhancement API configured, the background is automatically removed from uploaded photos before they are stored. This gives badges a clean, professional appearance. The enhancement happens silently — you do not need to take any extra steps.

---

## Method 2 — Capture from Webcam

1. Click **Take Photo** below the photo circle
2. A full-screen camera view opens with an oval face guide
3. Position the employee's face within the oval
4. Click **Capture** (the large blue circle button) — the video pauses and shows a preview
5. Click **Use Photo** to accept it, or **Retake** to try again
6. The photo is uploaded and saved

> **Tip**: Use the webcam method when employees are present in the office — it is faster than asking people to send photos and ensures consistent framing.

---

## Method 3 — No Photo (Placeholder)

If no photo is uploaded, the badge and profile display a generic avatar placeholder. The employee's initials or a silhouette icon are shown instead.

You can add a photo at any time by editing the employee record — the badge updates immediately when the record is saved.

---

## Removing a Photo

When a photo is already uploaded, a **Remove Photo** link appears in red below the upload button.

Click **Remove Photo** to clear the image. The badge will revert to showing the placeholder avatar. This action takes effect when you click **Save**.

---

## Photo Display on the Badge

The badge template controls whether the photo is displayed and how large it appears:

- If **photo is enabled** in the Badge Designer, it appears in the configured position and size on the badge
- The photo is cropped to a circle on the badge by default (configurable in the designer)
- If **photo is disabled** in the Badge Designer template, the photo is still stored on the record but not shown on the printed badge

For photo placement and sizing options, see Configuring What Appears on the Front of the Badge.
