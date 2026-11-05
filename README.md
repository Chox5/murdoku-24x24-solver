# Murdoku 24×24 Interactive Solver — The Treasure Hunt (v2)

An interactive web-based solver and solution walkthrough recorder for **Murdoku: The Treasure Hunt** (24×24 grid by Manuel Garand), built on the official contest PDF (`murdoku-contest1-treasurehunt-EN.pdf`).

## 🌐 Live Demo (在线体验地址)

👉 **[https://chox5.github.io/murdoku-24x24-solver/](https://chox5.github.io/murdoku-24x24-solver/)**

---

## Key Features (v2 Iteration)

1. **Streamlined Single-Line Top Toolbar & Pure Keyboard Input**:
   - Single-row compact top header (`44px`) housing the unified **Mode Switcher (`📝 Draft` / `✅ Confirm` / `🧹 Clear`)**, a collapsible **`🚫 排除显示 ▾`** dropdown menu, **`📸 记录步骤`**, Zoom/Opacity sliders, Undo/Redo, and JSON Import/Export.
   - Removed the redundant floating cell popover and duplicate mode tabs; clicking a cell selects it cleanly without obstructing the map.
2. **Collapsible Sidebars & Compact Clue Cards**:
   - Left **24 Suspects & Clues Drawer** can be collapsed/expanded anytime via `◀ 收起`, the top bar button, floating edge tab, or `[` key. Includes a **`↕ 折叠已定位`** toggle to collapse solved suspects into single-line bars.
   - Right **Inspector & Steps Sidebar** can also be collapsed via `▶` or `]` key, and deduplicates controls into two clean tabs: **`🧭 盘面高亮与追踪`** and **`📓 解题过程`**.
3. **Smart Confirm Auto-Elimination**:
   - Confirming a suspect letter `L` at `(R#, C#)` automatically:
     1. Removes `L` from `drafts` across the **entire 24×24 board**.
     2. Clears existing `drafts` on all other unconfirmed cells in the same row and column, and marks them with a **solid red `✕` (`manualX = true`)**.
     3. Displays the confirmed letter badge directly inside the row (`R#`) and column (`C#`) coordinate headers.
     4. Pushes the entire state transition onto the Undo stack so `Ctrl/Cmd + Z` restores all affected cells in one step.
4. **Solution Process Recorder & Replay Timeline (`📓 解题过程`)**:
   - Capture board snapshots + reasoning notes (`StepUnit`) at any point (`➕ 保存为新步骤` or `Cmd/Ctrl + S`).
   - Automatically calculates diff summaries against the previous step (`+Confirm`, `+Draft`, `+✕`) and highlights changed cells on the board during step replay.
   - Full timeline management: click any step to load/preview its board slice, step backward/forward (`⏮ / ◀ / ▶ / ⏭`), edit notes, overwrite snapshots with the current board, insert steps in between, reorder (`⬆ / ⬇`), delete, or export a full **Markdown Walkthrough Report (`📋 导出报告`)** and JSON bundle (`📂 导入` / `💾 导出`, backward-compatible with v1 progress JSON files).
