<div align="center">

# Dino Run

**Dino Run («Дино-бег») is a runner game in a single HTML page: jump over cacti and duck under birds. It runs in the browser with no server and no internet: open `index.html` or play it online.**

[**▶ Play online →**](https://alexalesha.github.io/DinoRun/) &nbsp;·&nbsp; [Русская версия этого файла](README.ru.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![CI](https://github.com/ALEXalesha/DinoRun/actions/workflows/ci.yml/badge.svg)](https://github.com/ALEXalesha/DinoRun/actions/workflows/ci.yml) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/DinoRun/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Code, tests and docs are written by Claude (Anthropic) in Claude Code. Ideas, testing and decisions - Alexey.

</div>

> Fan-made game. Not affiliated with the rights holder of the dinosaur game in a well-known browser.

The interface is in Russian.

![Menu](docs/screens/menu.png)

![A stage of the journey](docs/screens/play.png)

## What is in the game

- **Journey:** four stages to the finish at 10,000 m - desert, canyon at sunset, night steppe and a snowy pass, faster with each stage; the start of a stage is a checkpoint.
- **Endless run:** one life, day turns into night, the speed grows; the goal is a record.
- Birds fly high, middle and low: duck under the middle ones, jump over the low ones.
- Achievements and records, settings with key rebinding, gamepad support.
- Sprites are drawn by code, sounds and music are synthesised with WebAudio; no files from the internet.

## Controls

| Key | Action |
|---|---|
| Space, ↑, click or tap | jump (hold to jump higher) |
| ↓ or S | duck; in the air - fall faster |
| Esc | pause |

Keys can be changed in the settings where the game offers it; a gamepad works too where noted above.

## Run locally

Open `index.html` in Chrome, Edge or Firefox. Everything is in the repository; nothing is downloaded.

## Tests

The laws are Playwright tests in `tests/`. They open the page by its file address in headless
Chromium, one at a time:

```
npm install
npx playwright install chromium
npm test
```

Mouse capture in the tests is always a stub (a real `requestPointerLock` in headless Chromium on
Windows can clip the user's cursor).
The pictures above were made headless by the screenshot script of the Hub collection.

## History

The game was made in the [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) collection (folder `web/dino`), where it also runs in the Hub ([play there](https://alexalesha.github.io/)). This repository carries the game with its commit history.

## Licence

MIT, see [LICENSE](LICENSE).
