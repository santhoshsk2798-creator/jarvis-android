# JARVIS Android v1 — phone-only setup

This is a static Progressive Web App. It works without an AI API key or server. It does NOT read Gmail or verify live application statuses.

## Publish using only Android and GitHub
1. Install Chrome and create a free account at https://github.com.
2. In Chrome open https://github.com/new and create a **private** repository named `jarvis-android`. Private repositories can be used with GitHub Pages only on qualifying paid plans; for free GitHub Pages use a **public** repository. The included source has no personal data or secrets, so a public code repository is okay, but never upload your exported application backup, OAuth credentials, or API keys.
3. Upload the four app files `index.html`, `manifest.webmanifest`, `icon.svg`, and `sw.js` using **Add file → Upload files** (in Chrome, enable Desktop site if necessary). Upload files individually if Android's file picker does not support selecting multiple files.
4. Go to **Settings → Pages → Build and deployment → Deploy from a branch**, choose `main` and `/ (root)`, and save. Pages may take a few minutes to publish.
5. Open `https://YOUR-USERNAME.github.io/jarvis-android/` in Chrome. Tap the Chrome menu → **Install app** or **Add to Home screen**. Install availability depends on browser and manifest compatibility.
6. Add your actual job applications manually. Export JSON backups regularly.

## Easier first test
Extract the ZIP with your Android Files app, then open `index.html` in Chrome. Some browser features (PWA install, service worker, microphone) may not work from a local file; hosting via HTTPS is recommended.

## Privacy
- Application data is stored locally in the browser using localStorage.
- No emails, Google credentials, or application data are transmitted by the app code.
- Browser speech recognition may send audio to the browser vendor's service.
- Data is not synced between phones and laptops. Clearing site data may delete it.
- Never put an OpenAI API key directly in the HTML or JavaScript. Add a secure backend in Phase 2.
