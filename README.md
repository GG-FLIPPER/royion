# Royion Friend Edition

Royion is a friend-specific edition of the daily trivia dive. It keeps the original game loop, daily and unlimited modes, themed packs, offline storage, and responsive interface, with seven hardcoded friend reactions and friend-photo mascots.

## What is inside

- **Daily Dive** — seven prompts in a fresh daily challenge.
- **Unlimited Ocean** — keep diving with an endless stream of prompts.
- **Themed Packs** — explore alternate prompt sets and visual worlds.
- **Shrimp Relay** — pass the keyboard around for same-device party play.
- **Answer tiers** — score from Plankton to **One in a Royion**.
- **Field guide and archive** — browse discovered answers and dive history.
- **Dive buddies** — unlock and equip illustrated or friend-photo companions.
- **Offline-first storage** — scores, settings, and progress stay in your browser.
- **Optional live lookup** — Wikipedia and Wikidata can help verify niche answers; disable it in Settings to keep play local.

## Reaction mapping

The friend photos are bundled locally in `assets/reactions/`. There is no public asset-upload or customization surface.

| Supplied photo | Reaction | Score |
| --- | --- | ---: |
| `IMG_20261116_081759_671.png` | Too Clever | +15 |
| `IMG_20261116_081756_008.png` | Plankton | +10 |
| `IMG_20261116_081749_897.png` | Schooler | +30 |
| `IMG_20261116_081721_144.png` | Rare | +60 |
| `IMG_20261116_081711_731.png` | Deep Cut | +85 |
| `IMG_20261116_081738_328.png` | One in a Royion | +100 |
| `IMG_20261116_081714_302.png` | Miss/timeout | 0 |

## How to play

1. Pick a mode from the menu.
2. Read the prompt and type the answer that feels right.
3. Submit before the timer expires.
4. Watch the depth meter reveal how rare your answer was.
5. Use the archive, wardrobe, and field guide to track your progress.

## Run locally

Royion has no build step or package dependencies.

```sh
git clone https://github.com/GG-FLIPPER/royion.git
cd royion
python3 -m http.server 4173
```

Open <http://localhost:4173/> in a browser. The same static files are deployed to GitHub Pages by `.github/workflows/pages.yml`.

## Project layout

```text
index.html   App shell and dialogs
app.js       Game state, prompts, rendering, audio, sprites, and interactions
styles.css   Pixel-inspired responsive visual system
```

## Privacy

Royion does not require an account or backend. Local progress is stored with `localStorage` in your browser. If Live Archive Search is enabled, the current prompt and submitted answer may be sent to the public Wikipedia/Wikidata APIs to check niche entries. Turning the setting off keeps play local.

## Attribution

Royion is a friend-specific edition of an independent daily trivia dive. The friend reaction photos are edition-specific assets and are not configurable through the game.
