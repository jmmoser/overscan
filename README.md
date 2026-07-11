<div align="center">
  <h1>Overscan</h1>
  <p><strong>Turn any video into a light show.</strong></p>
  <p>Overscan syncs your smart lights to the colors and beat of whatever you're watching —
  YouTube, Twitch, music videos, gameplay, anything playing in your browser.</p>
</div>

---

## Download

Grab the file for your computer from the
[latest release](https://github.com/jmmoser/overscan/releases/latest):

| Your computer | Download |
|---|---|
| Mac with Apple silicon (M1/M2/M3/M4) | `overscan-macos-arm64.app.zip` |
| Mac with an Intel chip | `overscan-macos-x64.app.zip` |
| Windows | `overscan-windows-x64.exe` |
| Linux | `overscan-linux-x64` (or `overscan-linux-arm64` for ARM boxes like a Raspberry Pi) |

Then install the browser extension from the Chrome Web Store or Firefox
Add-ons, play a video, and your lights follow the picture. Staying current
is one click — the app checks this repo's releases once a day and offers
to update itself.

## How it works

1. The **browser extension** watches the video you're playing and extracts
   its dominant color and beat — everything is analyzed locally, nothing is
   recorded or uploaded.
2. It streams those tiny signals to the **Overscan desktop app** over a
   local WebSocket — nothing ever leaves your machine
   ([privacy policy](./PRIVACY.md)).
3. The desktop app finds your lights on the LAN — **LIFX**, **Philips Hue**,
   **WLED**, and **Govee** — and drives them in real time.

## Pro

The free tier syncs up to 2 lights. **Overscan Pro** is a one-time purchase
that unlocks unlimited lights and all Pro features: the room layout map
(place each lamp where it actually sits and it follows that part of the
picture), screen zones, edge-to-edge gradients on multizone strips
(LIFX Z/Beam, WLED), and everything Pro that ships later. The license key
activates offline — no account, no subscription.

Buy Pro from the app (menu → **Upgrade to Pro**) or contact
**getoverscan@gmail.com**. Commercial or business use (venues, events, paid
services) requires a commercial license — same address.

## Privacy

No accounts. No analytics. No data collection, period. The extension talks
only to the Overscan app on your own computer. Full policy:
[PRIVACY.md](./PRIVACY.md).

## About this repository

This repository hosts Overscan's **releases and documentation only**.
Overscan is proprietary, closed-source software — the source code is not
published here or anywhere else. Use of the software is governed by the
[EULA](./EULA.md).

Verify a download: each release ships a `SHA256SUMS` file, and each binary
an Ed25519 `.sig` the app itself uses to verify self-updates.

Found a bug or need help? [Open an issue](https://github.com/jmmoser/overscan/issues)
or email **getoverscan@gmail.com**.
