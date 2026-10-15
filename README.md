# Tic-Tac-Toe — Paper & Ink

A 3×3 tic-tac-toe that looks like a notebook page: textured paper, X and O drawn as pen strokes, and a score that lives in your browser.

Live: https://aditiaangga.github.io/tictactoe/

## Features

- **Three modes.** 2 Players to share a screen, Easy AI picks random cells, Hard AI runs minimax and cannot be beaten. The best result against it is a draw.
- **Six achievements.** First win, three in a row, a win inside five moves, a draw against Hard AI, ten wins, and trying all three themes. They unlock on their own and are never revoked, even after you reset the score.
- **Three themes.** Paper & Ink (default, light), Wood (dark and warm), and Chalk (dark green). Names from the earlier version are mapped over, so old scores are not lost.
- **Rename the players.** Click a name on the scoreboard, type, press Enter. When an AI mode is on the opponent is named "Computer".
- **Share the score by link.** The score and names are written into the URL, for example `?x=3&o=1&d=2&xn=Adit`. The "Share link" button copies it.
- **Play without a mouse.** Arrow keys and Home/End move across the board, `R` starts a new round, Esc closes the popup or the Desk panel.

## Running locally

```bash
# Open index.html straight in a browser — nothing to install
start index.html     # Windows
open index.html      # macOS

# Or serve the folder with a small static server
python -m http.server 8000
# then open http://localhost:8000
```

## Technical notes

- **Hard AI is minimax.** `minimax()` scores a position from O's point of view across every remaining branch, then `getBestMove()` takes the highest one. With only 9 cells it is instant without alpha-beta pruning.
- **Logic is split from the DOM.** The `GAME LOGIC` and `AI (minimax)` sections touch no `document`, no `localStorage` and no UI variable, so they can be run straight from Node without a browser.
- **The win line is drawn by hand.** Coordinates are derived from the winning combo on a 0–100 viewBox and drawn as an `<line>` with a `stroke-dashoffset` animation. Both ends deliberately overshoot the marks a little so it reads as a pen stroke rather than a tidy rule.
- **Scores live in localStorage, not on a server.** Score, names, theme, mode, sound and achievements each keep their own key (`ttt_scores`, `ttt_names`, and so on). Every access is wrapped in `try/catch` so nothing breaks when a browser blocks storage, private mode for instance.
- **Accessibility is built in, not bolted on.** Cells are `<button>` elements with an Indonesian-free `aria-label` ("Row 1 column 1, empty"), the turn indicator uses `role="status"`, and the result popup is a `role="dialog"` that traps focus and hands it back on close. A `prefers-reduced-motion` block switches off the stroke and popup animations.

## Limitations

- No online mode. Scores stay in the local browser, so they cannot be compared across devices.
- Sound is synthesised through the Web Audio API, with no audio files at all.
- The headings use Fraunces and IBM Plex Mono from Google Fonts. Offline they fall back to system fonts and look slightly different.

## Structure

```
tictactoe/
├── index.html   # HTML + CSS + JavaScript in one file, no build step
└── README.md
```

## Licence

Built for learning and portfolio purposes — Aditia Angga Perdana.
