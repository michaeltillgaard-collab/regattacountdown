# Race Start Timer

Countdown timer for sailboat race starts, built for a phone: neon-red digits on pure black (OLED),
start time entry (hh:mm:ss), audio signals during the last 5 seconds plus a start gun, a green
"START!" flash, and Screen Wake Lock with a status indicator. No dependencies – plain HTML/CSS/JS.

## Host on GitHub Pages
1. Create a repository and put the files in the root (`index.html`, `manifest.webmanifest`, `sw.js`, `icon-*.png`).
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
3. Open `https://<username>.github.io/<repo>/` in Chrome on Android (HTTPS is required for Wake Lock and the service worker).
4. Chrome menu → **Add to Home screen** (or "Install app") to run fullscreen without the address bar.
   Open the page once with reception so it is cached for offline use.

## Usage
- Enter the start time and tap **Start countdown**.
- At zero, "START!" flashes green for 5 seconds, then the timer counts up (+mm:ss) since the start.
- **Hold to cancel**: press and hold the button for about 1 second.
- Adjust the signal settings in the constants at the top of the script (`START_SHOWN_MS`, `BEEP_LAST_SEC`).

The timer uses the phone's system clock – make sure "Set time automatically" is turned on.
