# Murdoku 24×24 Interactive Solver — The Treasure Hunt

An interactive web-based solver for **Murdoku: The Treasure Hunt** (24×24 grid by Manuel Garand), built on the official contest PDF (`murdoku-contest1-treasurehunt-EN.pdf`).

## 🌐 Live Demo (在线体验地址)

👉 **[https://chox5.github.io/murdoku-24x24-solver/](https://chox5.github.io/murdoku-24x24-solver/)**

---

## Features

- **Official 300 DPI PDF Map (Scheme A)**: Overlaid on the official PDF Page 2 map (`R1–R24`, `C1–C24`), including the corrected **Cabin A door between `(C5, R3)` and `(C5, R4)`**.
- **24 Suspects & Clues Drawer (PDF Page 1 Integration)**:
  - High-resolution cropped avatars (`A–Z` excluding `V` and `X`, where `T = Treasure`), visual trait tags (`🎩 Hat` [5], `🏴‍☠️ Eyepatch` [3]), and full English clues.
  - One-click trait/status filters (`All`, `🎩 Hat`, `🏴‍☠️ Eyepatch`, `⏳ Unplaced`, `✅ Placed`), manual read/done check-offs, and interactive clue chips that directly highlight matching **Items** or **Areas** on the board.
  - Includes a `📄 原版线索图` modal to view the original full-page PDF Page 1 clue sheet anytime.
- **Interactive Item & Door Highlighter (`17 Items + 4 Doors`)**:
  - Highlight any occupiable furniture (`bed`, `chair`, `hammock`), unoccupiable obstacle (`fire`, `tree`, `flowers`, `shark`, `sack`, `pig`, `tombstone`, `crate`, `rope`, `barrel`, `shelf`, `shrub`, `table`, `boulder`), or `door`.
  - Optional **"Beside / In front of" Candidate Overlay**: Automatically outlines valid orthogonally adjacent occupiable cells **within the same Area** (or the 2 cells directly in front of each door).
- **Interactive Area Highlighter (`17 Areas + 3 Clue Groups`)**:
  - Highlight any of the 17 distinct Areas (`Woods`, `Cavern`, `Beach`, `Dock`, `Cliff`, `Clearing`, `Cabin A/B/C`, `Tavern`, `Water`, `Frigate A/B`, `Sloop A/B/C`, `Galleon`) or clue groups (`All Cabins`, `All Ships`, `All Sloops`).
  - Displays total vs. occupiable cell counts and highlights the **Top Row** of the selected Area (assisting with Griselda's clue).
- **Master & Granular `❌` Elimination Toggles**:
  - Master toggle (`🚫 显示排除❌`) + 3 independent toggles for **Unoccupiable Items (96 cells)**, **Row/Column Auto-Eliminated (`×`)**, and **Manual Eliminations (`✕`)**.
  - Selecting `T (Treasure)` automatically reveals unoccupiable item cells since the Treasure can be buried beneath an unoccupiable object.
- **Three Interaction Modes (`Draft` / `Confirm` / `Clear`) + Undo/Redo + Auto-Save**:
  - Full keyboard navigation (`Arrow Keys`, `A–Z`, `Shift + Letter` to Confirm, `X` or `Right Click` to toggle manual `✕`, `Esc` to clear highlights, `Ctrl/Cmd + Z/Y` for 80-step Undo/Redo) and `localStorage` persistence.

## Local Usage

Open `index.html` (or `murdoku_treasure_hunt.html`) directly in any modern browser. Everything is self-contained in a single HTML file with zero external network dependencies.
