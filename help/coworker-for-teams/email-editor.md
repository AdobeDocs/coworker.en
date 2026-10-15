---
description: description.
title: Understand the email editor
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
---
# Understand the email editor {#email-editor}

The email editor lets you refine an AI-generated email directly on the campaign board. Edit the subject line and preheader, format text and images inline, or swap in a different template.

Selecting an email card on the campaign board opens the email editor as a side panel. From there, the user can edit the subject and preheader (with AI-suggested alternatives), click into the email body to select and format text or images, switch between AI-generated variants, swap the HTML template, check email-client compatibility, and send a test email to their own inbox. Changes save automatically, and past versions can be reviewed and restored.

## How to access

1. Open the desired campaign and click Open editor in the email card.

SCREENSHOT

1. Edit the **Subject** and **Preheader** fields directly, or click **Smart suggestions** next to either for AI-generated alternatives.
1. Click into the email body to select a text block or image, then use the floating toolbar that appears to format the text or manage the image.
1. Use **Switch HTML Template** to replace the email body with a different template.
1. Use **Send test email**, enter a recipient address, and click **Send** to email a live preview to that address.
1. Use the version history icon to preview and restore an earlier saved version.
1. Changes save automatically — no manual save step is required.

### Key behaviors

- Image uploads are capped at 10 MB; images over roughly 3 MB are automatically compressed, with a quality note recommending images under 3 MB.
- Subject and preheader fields have the option for a AI-generated alternatives via this ICON.
- Use Ctrl+z (CMD+z for Mac) to 'Undo' and reverse your last action. Use CTRL+Y (CMD+y for Mac) to 'Redo' and reverse your last Undo. KEITH CHECK STANDARD
- Past saved versions can be previewed and restored from a version history panel via this ICON.
- By default, we generate two variants per email; you can select the desired variant via their thumbnails on the right.

## What this feature does not do

- It isn't a drag-and-drop block builder — there's no block library, and content blocks can't be added, removed, or reordered; editing happens directly on the existing email HTML.
- It doesn't currently support inserting personalization/merge tags.
- It doesn't provide an alt-text field for images.
- It doesn't enforce a subject line, preheader, or other content-level checks before an email is considered "ready" — the only pre-launch checks are campaign-level (sending setup, a test email sent, a real audience), not checks on the email content itself.
- Desktop/mobile preview toggling isn't available in the standard campaign email editing view. [NEEDS INPUT to confirm scope]
- [NEEDS INPUT — to confirm with engineer: whether the editor becomes fully read-only (not just the sender field) once a campaign has been activated/launched.]
