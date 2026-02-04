# SurMinus v4.0

**SurMinus** is an advanced cheat client for **Survev.io**, completely rewritten and optimized for performance, stealth, and stability.
This version (v4.0) introduces major core improvements, including a new build system, real latency monitoring, and an advanced predictive melee system.

---

## 🌟 Key Features

### Reworked Core & Build System
- **Fusion Build System**: Utilizes `Rollup` + `Terser` for aggressive minification and obfuscation.
- **Stealth Injection**: Runs within an isolated context using Shadow DOM/Iframe injection to bypass anti-cheat checks.
- **Developer Loader**: Restored `npm run dev` loader for rapid testing without rebuilding.

### ⚔️ Advanced Auto Melee (New in v4.0)
- **Predictive Lock**: Analyzes enemy velocity history to predict movement and land melee hits accurately.
- **Adaptive Range**: Automatically adjusts engagement distance based on the target's speed.
- **Hysteresis & Grace Period**: Prevents target loss when enemies briefly move out of range or behind obstacles.
- **Auto-Fire Integration**: Automatically attacks when a valid melee lock is acquired.

### 🎯 Aimbot "Savannah"
- **Linear Prediction**: Optimized for high-velocity targets and bullet drop.
- **High Velocity Support**: Automatically adjusts prediction for perks like "High Velocity" or "9mm Bonus".
- **Dynamic Smoothing**: Reduces jitter for a more "legit" look while maintaining accuracy.

### 📊 Visuals & HUD
- **Real Ping Display**: Hooks into the game's WebSocket to calculate and display **Real Round Trip Time (RTT)** (displayed as `Lat: XX ms` in green).
- **Armor HUD**: Displays exact Helmet and Vest protection percentages on the local player.
- **Clean ESP**: Optimized ESP lines, tracers, and skeletal rendering for better clarity.

### 🛠️ Quality of Life
- **Gun Overclock**: Configurable fire rate enhancements (Dual, Burst, etc.).
- **Infinite Zoom**: Unlocked view distance (with scroll wheel support).
- **Pan Hero**: Fixed logic for auto-blocking bullets with the Pan/Shield.
- **Menu**: Draggable, resizable, and styled with a modern "Glassmorphism" look.

---

## 🚀 Installation

### Option 1: Userscript (Recommended)
1. Install a userscript manager like **Tampermonkey** or **Violentmonkey**.
2. Drag and drop the `dist/SurMinus.user.js` file into your browser extensions tab (or create a new script and paste the content).
3. Navigate to [survev.io](https://survev.io) and play!

### Option 2: Chrome Extension
1. Go to `chrome://extensions`.
2. Enable **Developer Mode** (top right).
3. Click **Load unpacked**.
4. Select the `dist/extension` folder.
5. Navigate to [survev.io](https://survev.io).

---

## 💻 Development & Building

### Prerequisites
- [Node.js](https://nodejs.org/) (v16+)
- `npm`

### Setup
```bash
# Install dependencies
npm install
```

### Commands

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts the local dev server. Changes are reflected instantly (requires Loader script). |
| `npm run build` | Compiles the project into `dist/` (Userscript + Extension) using Rollup & Terser. |
| `npm run build:dev` | Compiles a non-minified version for debugging. |

---

## 📂 Project Structure

- `src/core`: Core injection, hooking, and state management logic.
- `src/features`: Individual hack features (Aimbot, ESP, AutoHeal, etc.).
- `src/ui`: Menu components (React-based) and styling.
- `src/utils`: Math helpers, geometry, and constants.

---

## ⚠️ Disclaimer
This software is for educational purposes only. Use at your own risk. The developers are not responsible for any bans or account suspensions.
