# MCRN Personal Field Terminal — MK-VII

Unofficial fan-made Expanse-inspired PWA for the Motorola moto g power (2025).

## Included functions
- Live clock, date, time zone, online/offline status
- Battery percentage when the browser exposes the Battery Status API
- GPS position with accuracy and a Google Maps handoff
- Device compass/orientation where Chrome exposes the sensor
- Quick links to Phone, SMS, Maps, Calendar, Mail and web search
- Local task list and notes (stored in this browser on this device)
- Offline app shell after the first successful load

## Install on the phone (recommended: GitHub Pages)
A PWA must be served from HTTPS (or localhost) for installation and service-worker features.

1. On a computer, sign in to GitHub and create a new **public** repository named `mcrn-terminal`.
2. Upload the contents of this folder to the repository root (not the ZIP itself).
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-USERNAME.github.io/mcrn-terminal/`.
6. On the Motorola, open that URL in **Chrome**. Tap the three-dot menu → **Install app** (or **Add to Home screen**) → Install.
7. Launch **MCRN Terminal** from the app drawer. For the full-screen look, open Android Settings → Display → Display size and text if you want to tune scaling.

## Phone setup
- Set Chrome as the browser used to open the hosted terminal.
- When prompted, allow Location only when you tap POSITION FIX.
- Tap COMPASS and grant sensor permission if prompted. Keep the phone away from magnets; compass readings can be affected by interference.
- Add the terminal to the home screen and move it to your primary home-screen position.
- Optional: use Android Settings → Display → Dark theme and set brightness to taste.

## Important limits
- This is a web app, not a privileged Android system app. It cannot replace the lock screen, notification shade, launcher, or system status bar.
- Battery telemetry may be hidden by some Chrome/Android versions; if so, the battery tile reports that it is unavailable.
- Compass access depends on browser sensor support and permission. GPS requires HTTPS and user permission.
- Flashlight is not directly controlled; use Android Quick Settings.
- Notes and tasks use browser localStorage. They are not encrypted or synced. Clearing Chrome site data can erase them. Do not store passwords, financial credentials, or sensitive information here.
- Calls and SMS links open Android's installed apps; the dashboard does not read messages or call logs.
- Weather opens a web search; no API key or tracking backend is included.

## Updating
Upload revised files to the same GitHub repository. Reopen the app while online. If an old version persists, close the app completely and reopen it; the service worker updates the cache.
