# Studio Ghibli: The World of Words

A self-contained, asset-free classroom PWA for magical student selection and balanced group generation. The visual style is original storybook-inspired CSS/SVG scenery; no film artwork, external images, audio files, libraries, or backend are required.

## Files
Upload these files directly to the repository root:
- `index.html`
- `style.css`
- `script.js`
- `manifest.webmanifest`
- `sw.js`
- `README.md`

## Deploy from Android
1. In GitHub, create a new repository.
2. Open the repository, choose **Add file → Upload files**.
3. Upload the six files above directly (do not upload a containing folder).
4. Commit the files to the `main` branch.
5. Open **Settings → Pages**.
6. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
7. Wait for GitHub Pages to publish. Open the Pages URL in Chrome on Android.
8. In Chrome, tap the three-dot menu and choose **Install app** or **Add to Home screen**.

## Updating
Edit or upload changed files to the same root paths and commit. The service worker caches core files for offline use. After a deployment, reload the app online once so the new service worker can install. If an old version remains, close the installed app, open the site in Chrome, reload, and clear site storage only if needed (this clears locally saved classroom data).

## Classroom use
- Manage roster: add names, paste a line-separated list, search, edit, delete, shuffle, or export CSV.
- Name picker: one selection per roster entry each round, with saved progress and history.
- Groups: select number of groups or members per group; assignments are balanced and students are distributed across groups. Group names can be edited, group locks are available, and arrangements can be saved/restored/exported/printed.
- Settings: class and teacher labels, motion, synthesized sound, volume, and fullscreen.

## Privacy and storage
All roster, selection, arrangement, and settings data is stored locally in this browser using `localStorage`. It is not uploaded. Avoid using sensitive student details; first names or classroom-safe labels are recommended. Export a CSV backup before clearing browser storage.

## Troubleshooting
- **Install option missing:** GitHub Pages must be served over HTTPS; open the published URL in Chrome rather than a file preview.
- **Offline not available:** visit the published site online once, then reload after service worker installation.
- **Stale version:** update `CACHE` in `sw.js` when changing app versions, commit, then revisit online.
- **GitHub Pages path:** all app paths are relative (`./`) so the app works from a repository Pages subpath.
