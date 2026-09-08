# Floor Log

Phone-first shift log for pipefitting. One screen, big buttons, times stamp themselves. Data stays on the phone.

## Use it

Open `index.html` in Chrome on Android.

Job # and piece # at the top. Tap:

- Start
- Locate QC
- QC done
- Grind and weld
- Drop at robot
- Looking for parts
- Next piece (same job, piece + 1, new block)
- Clock out

Times look like the handwritten notes (`500`, `109`, `1010`). Undo, copy day, switch job are under the buttons.

## Install on Android

Needs HTTPS (or localhost) for Add to Home Screen.

1. Open the page in Chrome.
2. Menu (three dots) → **Add to Home screen**.
3. It opens like an app. Works offline after the first load.

Opening the file from Downloads still works for logging (data in this browser). Add to Home Screen will not stick until it is served over HTTPS.

## Data

Saved in the browser (`localStorage`), keyed by date. No login. No server.

## Auto-write (notes-app style)

Every stamp (and typing in the log) auto-saves to the browser, then debounces a write of today's plain text file to Downloads as `floor-log-M-D-YY.txt` (same name updates through the day). Clock-out writes immediately. Manual **Save files** still exports `.txt` + HTML report.

