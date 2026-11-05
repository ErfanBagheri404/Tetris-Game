# Tetris (HTML canvas)

Classic Tetris in vanilla JavaScript. Seven tetrominoes on a 10x20 canvas grid
with rotation, hard/soft drop, line clears, score and a falling speed that
increases as you clear lines.

## Controls

| key | action |
|---|---|
| `ArrowLeft` / `ArrowRight` | move |
| `ArrowUp` | rotate |
| `ArrowDown` | soft drop |
| `Space` | hard drop |

## How it works

- `Tetromino` class holds the cell coordinates, colour, current position and the
  board matrix; `static BLOCK_SIZE = 28`, `DELAY = 400 ms`.
- A tick loop drops the piece; the delay shrinks as lines clear.
- Scoring is `[40, 100, 300, 1200]` for 1-4 rows at once; full rows are spliced
  out of the matrix and new rows unshifted on top.
- Score and lines are rendered into `#score` and `#lines`.

## Run

```bash
git clone https://github.com/ErfanBagheri404/Tetris-Game.git
cd Tetris-Game
```

Open `index.html` in a browser.

## Files

| file | role |
|---|---|
| `index.html` | canvas, score/lines labels, background |
| `index.js` | tetromino definitions, board, input, tick loop |
| `style.css` | layout and colours |
