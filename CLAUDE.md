# Pack the Truck — instructions for Claude

## Who you're working with
- Owner: Industrial Engineering student, new to programming. Explain decisions in plain language.
- After each task, add 3–5 lines to LEARNING.md: what changed and the concept behind it.

## What we're building
A mobile browser puzzle game about bin packing: drag and rotate boxes into a truck grid;
score = fill rate. Levels come from a config file. Playable on a phone in portrait.

## Stack
Phaser 3, Vite, plain JavaScript, Vitest. PWA manifest so it installs to the home screen.
Hosted on GitHub Pages from /docs on the main branch, and as an HTML5 zip on itch.io.

## Commands
- Install: npm install   (run at the start of every session)
- Tests:   npm test
- Build:   npm run build   (output goes to /docs)

## Layout
- src/main.js: Phaser config and scenes
- src/logic/grid.js: pure game logic (fits, place, rotate, fill rate), no Phaser imports, fully tested
- src/levels.json: level definitions
- public/: assets and manifest
- tests/: Vitest

## Rules
- Keep game logic in src/logic/ separate from Phaser so it can be unit-tested.
- Touch first: tap to rotate, drag to place; it must also work with a mouse.
- Simple shapes and colors drawn in code; no copyrighted assets.
- One feature per session; show a plan first if more than one file changes.
- Ask before adding a dependency.
- End every session by updating PROGRESS.md: done, next, open questions.

## Definition of done
Tests pass, the build succeeds into /docs, and the game runs without console errors on a phone-sized screen.
