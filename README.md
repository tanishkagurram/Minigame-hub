# Mini Games Hub 🎮

A collection of five small, self-contained browser games with a single
landing page that links them all together. No build step, no backend, no
dependencies — every game is a standalone HTML file that runs by just
opening it in a browser.

## What's included

| Game | File | What it is |
|---|---|---|
| ⭕ Tic Tac Toe | `code (1).html` | Classic 3×3 grid game with **2‑player** and **vs. Computer** modes, score tracking, and a simple AI opponent. |
| 🎯 Hangman | `hangman1.html` | Word-guessing game with a canvas-drawn gallows, 20 words across categories (Music, Animal, Fruit, Weather, etc.), clues and two extra hints per word, and a **Computer** mode plus a **Multiplayer** mode where one player sets the word for another. |
| ✂️ Rock Paper Scissors | `rock-paper-scissors.html` | Classic hand-game against the computer with animated choices, a running score board, and a first-to-5 match format. |
| 🏴‍☠️ Treasure Hunt | `tresurehunt_uadate/mini project/game/tresure.html` | A meme-driven, choice-based "Gen Z vibe check" adventure — each stage presents a prompt with a correct answer and several joke "trap" answers that send you back to start, with sound effects and background music. |
| 🔢 Number Guessing Game | `number_game/number_game/guessing-game-html.html` | Guess a mystery number across 5 difficulty levels (Easy → Master), each with 5 trivia-flavored mystery numbers, an optional hint system (hints cost points), and a scoring/next-level flow. |

## How to run it

No installation or server required.

1. Unzip the project (if it isn't already).
2. Open **`mini/index.html`** in any modern browser (Chrome, Edge, Firefox, Safari).
3. Pick a game from the hub — each card's **Play Now** button opens that
   game in the same tab.

That's it — everything runs client-side.

> **Note:** the Treasure Hunt game loads a few meme images directly from
> `imgflip.com` over the internet, so an internet connection is needed for
> those specific images to load (the local images/audio in its `game/`
> folder still work offline).

## Project layout

```
mini/
├── index.html                                  Landing page — the "Mini Games Hub"
├── code (1).html                                Tic Tac Toe
├── hangman1.html                                Hangman
├── rock-paper-scissors.html                     Rock Paper Scissors
├── number_game/
│   └── number_game/
│       ├── guessing-game-html.html              Number Guessing Game
│       └── .vscode/launch.json                  Editor launch config (not needed to play)
└── tresurehunt_uadate/
    └── mini project/
        ├── Untitled-1.js                        Scratch/leftover script file
        └── game/
            ├── tresure.html                      Treasure Hunt game
            ├── correct-choice-43861.mp3          Correct-answer sound effect
            ├── fail-144746.mp3                    Trap/wrong-answer sound effect
            ├── gta_mission_passed.mp3             Victory sound effect
            ├── ddlj.mp3                            Background music for one stage
            ├── ddlj.jpg                            Stage image
            ├── dating.jpg                          Stage image
            └── crpto.webp                          Stage image
```

## How each game works

- **Tic Tac Toe** — choose "2 Players" or "vs Computer" from the mode
  selector; the computer opponent moves automatically after a short delay.
- **Hangman** — pick "Computer Mode" to get a random word with clues and up
  to two extra hints, or "Multiplayer Mode" where one player types a
  secret word for the other to guess; you have 6 wrong guesses before the
  hangman drawing is complete.
- **Rock Paper Scissors** — click Rock, Paper, or Scissors; the game tracks
  wins/losses/ties on a scoreboard as you play toward 5 wins.
- **Treasure Hunt** — read each prompt and pick from several answers; one
  answer advances you to the next stage, the rest are "traps" that restart
  the run with a joke penalty message.
- **Number Guessing Game** — guess the hidden number for the current level;
  each level has 5 rounds tied to a trivia fact (dates, jersey numbers,
  famous constants, etc.), and revealing a hint costs points off your score.

## Technical notes

- Every game is plain **HTML, CSS, and vanilla JavaScript** — no frameworks
  or build tools involved.
- All game logic runs in a single `<script>` block per file, so each game
  can be copied out and used independently of the hub.
- The `.vscode/launch.json` and `Untitled-1.js` files are editor/workspace
  leftovers from development and aren't required to play the games.

## Limitations / possible improvements

- File and folder names are inconsistent (spaces, mixed casing, a
  duplicated `number_game/number_game` and `tresurehunt_uadate/mini project`
  nesting) — flattening these would make the project easier to navigate.
- The Treasure Hunt game depends on external image URLs for some memes,
  so it isn't fully offline-capable as-is.
- No shared styling or scoring system across games — each one reimplements
  its own theme and UI from scratch.
- Could add a shared "back to hub" link inside each game, and a persistent
  high-score/leaderboard across games using `localStorage`.
