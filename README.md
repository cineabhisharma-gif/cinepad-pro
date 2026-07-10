# CinePad Pro

CinePad Pro is a GitHub Pages-ready filmmaker workspace for iPad, MacBook, iPhone and desktop browsers.

## Files

- `index.html` — main application
- `manifest.webmanifest` — PWA install metadata
- `sw.js` — offline app shell service worker
- `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` — app icons

## GitHub Pages install

1. Create a new GitHub repository, for example `cinepad-pro`.
2. Upload all files from this folder to the repository root.
3. Open the repository Settings → Pages.
4. Under Build and deployment, choose Deploy from a branch.
5. Select branch `main` and folder `/root`, then save.
6. Open the Pages URL in Safari on iPad.
7. Tap Share → Add to Home Screen.

## Optional encrypted sync

CinePad Pro works locally without sync. To sync across devices:

1. Create a free Firebase project.
2. Add a Web App in Firebase and copy the Firebase config JSON.
3. Enable Authentication → Anonymous sign-in.
4. Create Firestore Database.
5. Paste the Firestore security rules shown inside CinePad Pro → Sync Setup.
6. In CinePad Pro, paste the Firebase config JSON, generate a Workspace ID, enter a strong sync passphrase and tap Save Sync Settings.
7. Tap Connect / Pull, then Push Now.
8. On another device, open the same GitHub Pages app and enter the same Firebase config, Workspace ID and passphrase.

Your workspace data is encrypted in the browser before upload. Keep the passphrase safe; if you forget it, cloud data cannot be decrypted.


## v1.1 Trash / Recently Deleted update

This update adds a Recently Deleted area. Deleted entries, tasks, voice notes, media and sections are moved to Trash first, where they can be restored or deleted forever. To update an existing GitHub Pages install, replace the existing repository files with this package, commit changes, then reopen the app. Existing local/Firebase data is preserved because the storage key is unchanged.
