# Class HQ 🚀

One folder, one landing page, four classroom apps.

```
hub/
  index.html        <- the Class HQ landing page (open this one)
  classboard/       <- live student whiteboards
  buzzer/           <- quiz buzzer
  guesswho/         <- Draw & Guess + Bingo
  ourspace/         <- Our Space: students add shapes, post-its, balloons or fish to a shared screen
```

## Deploy
Put the whole `hub` folder in one GitHub repo (e.g. `classhq`) and turn on GitHub Pages (main / root). The landing page is then `https://<you>.github.io/classhq/` and each app lives under it.
Each app is still a normal standalone app: a QR code opens that app's own page, so students go straight in and never see the landing page.

## Landing page
- Click a window (or press **1 / 2 / 3 / 4**, or use arrow keys + Enter) to launch an app with a warp transition.
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

## Our Space
Students add drawings and notes to one shared screen (the teacher's screen). Students join with the QR code like the other apps, and they see the same space on their iPad, so they can tap things and move post-its too.
Pick one activity per room (you can change it any time from **Settings**; each activity keeps its own things):
- **Random shapes**: a random 2D shape to draw or write on. They float around.
- **3D shapes**: a random 3D shape wrapped in their drawing. Floats and spins. (Loads the three.js library from a CDN when first used.)
- **Post-its**: draw on a post-it, then place it anywhere. Tap to zoom in, or drag to move it. Only one person can hold a post-it at a time.
- **Back & front**: like a post-it with a front and back. Flip button when zoomed in.
- **Balloons**: float up off the top and come back at the bottom. Double-tap pops one (it comes back at the bottom).
- **Fishing**: write on a fish. Fish swim with the message hidden. Tap in the sky above the water to cast a hook. Catch a fish and it flips to show the message.
Teacher controls: entries per student (counted on screen), auto-remove timer, show/hide names, pause adding, clear, remove a student's things or kick them. Tapping any thing zooms it in (it comes towards the camera). The teacher can remove anything from the zoomed view; students can take down their own.
The room and its contents are kept if the teacher reloads the page. Originals from before this change: `hub/backups_ourspace/`.
