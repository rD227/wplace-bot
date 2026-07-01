# wplace-bot

Auto-draw bot for [wplace.live](https://wplace.live). Tampermonkey userscript, forked from [Readixyee/wplace-bot](https://github.com/Readixyee/wplace-bot).

[中文文档](README_CN.md)

## New Features

- **Auto-draw loop** — check "Auto draw" and the bot automatically re-draws every cycle
- **Smart timer** — interval calculated from your charge cap (charges × 30s + 15s), adapts as you level up
- **One-click Paint** — all pixels previewed then a single Paint click confirms them

## Quick Install

1. Install [Tampermonkey](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
2. Open [dist.user.js](https://github.com/rD227/wplace-bot/raw/master/dist.user.js), click Install
3. `chrome://extensions` → Tampermonkey → Details → Allow User Scripts
4. Open wplace.live — the bot panel appears automatically

## Usage

1. Drag an image or `.wbot` file onto the panel
2. Drag image edges to position it
3. Optional: adjust color order, strategy, etc.
4. Check **Auto draw** to enable auto-loop
5. Click **Draw** to start

## Build

Requires [Bun](https://bun.sh):

```bash
bun install
bun start     # generates dist.user.js
```

After editing source files:

```bash
bun start && cp dist.user.js ~/Downloads/
```

## Update the Tampermonkey Script

After building, open Tampermonkey Dashboard → edit the script → paste `dist.user.js` → save.

Or wait for Tampermonkey to detect the `@updateURL` and prompt you.

## License

MPL-2.0 — inherited from [SoundOfTheSky/wplace-bot](https://github.com/SoundOfTheSky/wplace-bot)
