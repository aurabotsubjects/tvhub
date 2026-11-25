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

## Waiting room (dot-to-dot)
While students wait for the teacher to start, their iPad shows a join-the-dots puzzle (dots 0 to 50, only the next few dots show). Each time it is a random one of 10 pictures, and the picture is only revealed when the last dot is joined.
- **ClassBoard** and **Guess Who??**: shown on the existing "You're in! Waiting for your teacher…" screen, and goes away when the teacher starts.
- **Buzzer**: students now wait here after picking their mascot and sound, until the teacher presses **Start game**. (The teacher now tells each student whether the game has started.)
- It is built into each app's `index.html` (one `<iframe>` near the end of the file), so each app is still one file.
- Originals from before this change are in `claude_auto/waitingroom-preview/backups/`. To rebuild after changing the puzzle, run `install_lobby.py` from that folder (it skips apps that already have it, so restore a backup first).
