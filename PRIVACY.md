# Overscan Privacy Policy

**Last updated: July 7, 2026**

Overscan is built to be private by design. The short version: **your data never
leaves your computer.** (The desktop app's only outside contact is an
optional once-a-day version check — see below.)

## What Overscan processes

- **Video and audio analysis.** While a video plays in your browser, the Overscan
  extension analyzes the picture's colors and the audio's beat *locally, inside
  the page*. Raw video and audio are never recorded, stored, or transmitted
  anywhere.
- **Light control data.** The extension sends only tiny derived signals — an
  average color (3 numbers) and beat timing — over a WebSocket connection to
  the Overscan desktop app running on `localhost` on the same computer. The desktop
  app relays color commands to your smart lights over your local Wi-Fi network.
- **Settings.** Your light selection and effect settings are stored by the
  desktop app in files on your computer (`~/.overscan/`). The extension keeps
  only its own small preferences — the per-site off list and the desktop
  app's port — in your browser's extension storage (`storage.sync`), which
  your browser may sync between your own devices if you have browser sync
  enabled.
- **License keys** (Pro) are verified locally on your computer. No activation
  server, no phone-home.
- **Update check.** Once a day, the desktop app asks GitHub's public API for
  the latest Overscan release so it can tell you when an update is out. The
  request carries no personal data, no identifiers, and nothing about your
  usage — it is the same request as opening the Releases page. Set the
  `OVERSCAN_NO_UPDATE_CHECK=1` environment variable to turn it off entirely.
- **One-click update.** Updates install only when you click the update
  button (tray menu or dashboard) — never automatically. Clicking downloads
  the new app binary from GitHub Releases over HTTPS; like the check, the
  download carries no personal data or identifiers. The app verifies the
  file's cryptographic signature before replacing itself and refuses
  anything that doesn't match.
- **Screen sync.** If you use the "Sync screen" feature, the picture you
  choose to share is analyzed locally exactly like page video — nothing is
  recorded, stored, or transmitted; only the derived color numbers go to the
  desktop app on `localhost`.
- **Diagnostics.** The dashboard's "Copy diagnostics" button compiles a
  report (app version, OS, current state, recent console output) locally on
  your machine — it is only ever shared if you copy it and send it
  somewhere yourself.

## What Overscan does NOT do

- No analytics, telemetry, or tracking of any kind.
- No accounts, no sign-in.
- No data sent to Overscan's developer or any third party. (The optional update
  check above sends nothing — it only downloads the public release list.)
- No browsing history collected. The extension only reacts to `<video>`
  elements on pages you visit and connects only to `localhost`.

## Chrome Web Store disclosures

Overscan does not collect, use, or share user data as defined by the Chrome Web
Store User Data Policy. Overscan does not sell or transfer user data to third
parties, does not use user data for purposes unrelated to its single purpose,
and does not use user data to determine creditworthiness or for lending
purposes.

## Changes

If this policy ever changes, the updated version will be published at this URL
with a new "Last updated" date.

## Contact

Questions: Justin Moser — getoverscan@gmail.com
