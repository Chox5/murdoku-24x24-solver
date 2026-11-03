# Murdoku 24×24 Interactive Solver — The Treasure Hunt

An interactive web-based solver for **Murdoku: The Treasure Hunt** (24×24 grid by Manuel Garand).

## 🌐 Live Demo (在线体验地址)

👉 **[https://chox5.github.io/murdoku-24x24-solver/](https://chox5.github.io/murdoku-24x24-solver/)**

---

## Features

- **Pixel-Accurate 24×24 Grid**: Overlaid on the glare-free official 24×24 map (`R1–R24`, `C1–C24`) with synchronized row/column crosshair highlighting.
- **Three Interaction Modes (`Draft` / `Confirm` / `Clear`)**:
  - **📝 Draft**: Toggle multiple candidate letters (`A–Z` excluding `V` and `X`, 24 suspects total) inside any cell.
  - **✅ Confirm**: Lock a cell to a specific suspect letter and **automatically eliminate that letter from all other cells in the same row and column**.
  - **🧹 Clear**: Clear all Draft/Confirm/X marks in the target cell.
- **Global 24-Letter Tracker**: View which suspects are confirmed (with exact `R#C#` coordinates) and click any letter to highlight all cells containing it across the board.
- **Keyboard Shortcuts**:
  - `Arrow Keys`: Move selected cell
  - `A–Z` (except `V`, `X`): Toggle Draft candidate in the selected cell
  - `Shift + Letter`: Confirm letter in the selected cell (and auto-prune row/column)
  - `X` or `Right Click`: Toggle manual elimination mark (`✕`)
  - `Backspace / Delete`: Clear selected cell
  - `Ctrl/Cmd + Z` / `Ctrl/Cmd + Y`: Undo / Redo (up to 80 steps)
- **Auto-Save**: Progress is saved automatically in `localStorage` and can be exported to JSON.

## Local Usage

Open `index.html` (or `murdoku_treasure_hunt.html`) directly in any modern browser. No server or build step required.
