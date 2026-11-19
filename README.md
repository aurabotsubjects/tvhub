# Class HQ 🚀

One folder, one landing page, three classroom apps.

```
hub/
  index.html        <- the Class HQ landing page (open this one)
  classboard/       <- live student whiteboards
  buzzer/           <- quiz buzzer
  guesswho/         <- Draw & Guess + Bingo
```

## Deploy
Put the whole `hub` folder in one GitHub repo (e.g. `classhq`) and turn on GitHub Pages (main / root). The landing page is then `https://<you>.github.io/classhq/` and each app lives under it.
Each app is still a normal standalone app: a QR code opens that app's own page, so students go straight in and never see the landing page.

## Landing page
- Click a window (or press **1 / 2 / 3**, or use arrow keys + Enter) to launch an app with a warp transition.
- A green **Room open** badge shows on an app if you already have a teacher room running in it on this computer. **Last used** marks the app you launched most recently.
- 🔊 button mutes the little sounds.
- Every app's teacher/student start screen has a **🏠 Class HQ** button to get back.

## Updating one app
Replace that app's `index.html` inside its folder. To keep the back-to-hub button, the only addition in each app is one `<a class="hubback">` line under its landing element and a small `<style>` block just before `</head>`.
