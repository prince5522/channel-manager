# Channel Studio — starter project

A beginner-friendly, local-first PWA starter for managing written stories, episodes, posting reminders, channel links, promotions, themes, and downloadable backups.

## Run it
1. Extract this folder.
2. Upload the **contents** of this folder to a new GitHub repository, or open it with a local static server.
3. For PWA installation and service-worker/offline features, use HTTPS (GitHub Pages is suitable).
4. Open `index.html` / your GitHub Pages URL.

## Included
- Separate HTML pages for the main features.
- Local browser storage with guarded reads/writes and basic storage-error handling.
- PDF selectable-text extraction through PDF.js CDN when online. Scanned PDFs require OCR, not included.
- 13-episode splitter with editable previews.
- Tasks and basic in-app/browser notification attempts while the app is running.
- Channel links, hype drafts, theme settings, backup export/restore.
- Image/video Media Library with previews, downloads, deletion, and IndexedDB storage (35 MB per file limit).
- PWA manifest, generated 192/512 app icons, and offline app-shell cache.
- Complaint records and channel reviews saved locally on this device.

## Important limitations
- No Supabase credentials are included. Cloud sync/backup is not enabled yet. Media files stay in this browser/device and are not included in JSON backups. Complaints and reviews are local-only until a secure backend and moderation flow are connected.
- The starter cannot guarantee reminders while fully closed/offline. Reliable push needs a push service and server worker.
- It does not automatically publish to WhatsApp Channels. Regular WhatsApp account linking does not provide an official general Channel-posting API. Saved links and manual handoff are supported.
- Do not put service-role secrets in frontend files. Cloud integration needs proper server-side access control.

## Suggested next steps
1. Test each page and save a sample story/task/channel.
2. Export a backup and test restore.
3. Add IndexedDB for large stories and PDF originals.
4. Configure Supabase Auth/Storage/database with restrictive access policies.
5. Add a push-notification backend if supported by your hosting.
6. Verify WhatsApp publishing integration availability before promising automatic posting.
