[🇹🇷 Click here for Turkish](README.tr.md)

# Öncelikli Geçiş — Baggage Logistics Center

This repository contains a **browser-based puzzle game** inspired by classic “block sliding” logic puzzles.  
Your mission is to move the **yellow priority luggage** through the grid and **deliver it to the exit gate** (the red laser on the right).

The game is implemented primarily as a **single-page HTML** experience (no build step required for the standalone version).  
A **React + Vite** version also exists under `src/`.

---

## Gameplay

- The board is a **6×6 grid**
- Blocks can move only along their axis:
  - **Horizontal blocks** move left/right
  - **Vertical blocks** move up/down
- Goal: move the **priority block** (yellow, “ÖNCELİKLİ”) to the **exit** on the right side

---

## Features

### 1. Levels
- Includes **5 handcrafted levels**
- Each level has a “terminal” theme (e.g., Istanbul, London, New York…)

### 2. Smooth Drag Controls
- Drag blocks with **mouse**
- Works on **touch devices** (mobile/tablet)
- Movement is constrained to valid grid steps (prevents jumping through blocks)

### 3. Move Counter & Progression
- Move counter per level
- Win modal shows your move count
- “Next terminal” button to advance
- Completion screen shows **total moves** and a simple **performance rating**

### 4. UI / Visuals
- Built with **Tailwind CSS** (CDN in standalone HTML)
- Uses **Lucide icons**
- Clean “logistics control panel” style theme

---

## Project Structure

### Standalone (runs by opening a single file)
- `index.html` — the standalone version (HTML + Tailwind CDN + game logic in an inline `<script>`)

### React + Vite version (optional)
- `src/App.jsx` — React implementation of the same game mechanics
- `src/main.jsx` — React entry
- `src/index.css` — Tailwind import + base styles
- `vite.config.js`, `package.json` — Vite tooling

---

## Getting Started

### Option A — Run standalone (recommended for quick play)
1. Clone the repository:
   ```bash
   git clone https://github.com/miyigun/my_luggage_game.git
   cd my_luggage_game
   ```
2. Open `index.html` in your browser.

> Tip: If your browser blocks some features when opening local files, run a local server.

Example (Python):
```bash
python -m http.server 8000
```
Then open:
- `http://localhost:8000`

### Option B — Run React + Vite version (development)
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start dev server:
   ```bash
   npm run dev
   ```
3. Build:
   ```bash
   npm run build
   ```
4. Preview build:
   ```bash
   npm run preview
   ```

---

## 🛠️ Technologies Used

- HTML / JavaScript
- Tailwind CSS
- Lucide Icons
- (Optional) React + Vite (for the `src/` version)

---

## 📌 Notes

- The win condition is when the priority block reaches the exit line on the right side (same row as the target).
- The repo currently contains **two implementations** (standalone HTML and React). You may choose one to maintain long-term.

---

## 📜 License

MIT License (see `LICENSE`).