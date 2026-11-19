# Guess Who?? 🕵️

A classroom drawing-and-guessing game. Same style and hosting as Buzzer: one static file (`index.html`), students join by QR code, no server of your own.

## Deploy
Put `index.html` in a GitHub repo (e.g. `guesswho`) and turn on GitHub Pages, exactly like Buzzer. HTTPS is fine for everything here.

## Activity 1: Draw & Guess
**Teacher:** Open hub → pick the activity → type what everyone should draw (e.g. "Draw your favourite animal") → choose drawing / guessing times, default big-screen view and options → **Open room**.
1. Show the QR code. Players appear as chips (a ⚠️ means two players share a first name).
2. **Start drawing.** The timer runs. Names and drawings stay secret on the big screen.
3. **Start guessing.** Pictures are shuffled and numbered. Pick the big-screen view: **All** (everything on screen), **Slideshow** (near full screen, changes every 3-12s, Space pauses) or **Gallery** (you control it with ◀ ▶ or the arrow keys).
4. **Finish round** when everyone has pressed "I'm finished".
5. Results tabs: **Player scores** (most correct guesses), **Most guessed** (each picture, the artist and who guessed it), **Podium** (3rd, 2nd, then the winner with fanfare). Ties share a step.
6. **Play again** keeps the players and lets you change the topic.

**Students:** scan the QR code, type your real first name, draw (colours, 3 brush sizes, rub out, undo, clear), press **Send drawing**. Then type who drew each numbered picture (your own is marked ⭐). Press **I'm finished**.

## Activity 2: Bingo 🎱
Pick **Bingo** in setup. Everyone draws as normal (needs **25+ drawings**), then each player gets their own shuffled 5×5 card of other players' drawings.
- No picture repeats on a card and nobody gets their own. If there are exactly 25 drawings, your own picture is a free pre-ticked square.
- Cards are filled so every drawing appears about the same number of times across the class.
- A student taps a square and types who drew it. The teacher's screen checks the name (same marking rules as below). A wrong answer means a short wait (you choose 0-20s) so nobody can guess names at random.
- First to complete the chosen number of lines (default **4**; rows, columns and diagonals all count) is 1st. The game stops after the chosen number of finishers (default **4th place**), or when the bingo timer ends, or when you press **End game**.
- Results tabs: **Podium** (1st-3rd, 4th listed underneath), **Standings** (lines and squares for everyone), **Pictures** (how often each drawing was spotted).

## Marking
Capitals, spaces, accents and punctuation are ignored. "Ella" matches "Ella Smith". Optional (on by default): one typo is forgiven for names of 5+ letters. Points = number of pictures you correctly named.

## Notes
- If time runs out while drawing, every device sends whatever it has automatically.
- Teacher can refresh the page and keep the room; students reconnect and re-send their drawing and guesses.
- Drawings are 800x600 JPEGs; students receive smaller copies of the others' pictures.
- TURN server option for strict school Wi-Fi is at the top of the script, same as Buzzer.

## Two drawers per iPad
With 'Let two students share one iPad' ticked (on by default), after the first person sends their drawing a **➕ Pass the iPad** button appears. The second person draws and types their own name. Each drawing is its own picture; the iPad guesses (and plays Bingo) as one team and never has to guess its own two pictures. Teacher screens show the pair as 'Ella & Ben'.
