# Royion Friend Edition

Royion is the friend-specific edition of the daily trivia dive, copied from the current [Shrimpion](https://github.com/GG-FLIPPER/shrimpion) base. The game loop, prompt data, scoring, themed packs, offline storage, and responsive interface remain functional with a hardcoded friend reaction set.

The friend photos are bundled locally in `assets/reactions/`. There is no public asset-upload or customization surface, so this special edition cannot be changed through the UI.

## Reaction mapping

| Supplied photo | Reaction | Score |
| --- | --- | ---: |
| `IMG_20261116_081759_671.png` | Too Clever | +15 |
| `IMG_20261116_081756_008.png` | Plankton | +10 |
| `IMG_20261116_081749_897.png` | Schooler | +30 |
| `IMG_20261116_081721_144.png` | Rare | +60 |
| `IMG_20261116_081711_731.png` | Deep Cut | +85 |
| `IMG_20261116_081738_328.png` | One in a Shrimpion | +100 |
| `IMG_20261116_081714_302.png` | Miss/timeout | 0 |

## Run locally

Royion has no build step and no package dependencies.

```sh
git clone https://github.com/GG-FLIPPER/royion.git
cd royion
python3 -m http.server 4173
```

Open <http://localhost:4173/> in a browser. A local server provides the most consistent browser behavior.

## Included base functionality

- Daily Dive, Unlimited Ocean, party relay, and themed prompt packs.
- Tiered scoring and depth-meter feedback.
- Offline-first progress, settings, archive, wardrobe, and field guide storage.
- Optional Wikipedia/Wikidata lookup, disabled from Settings when desired.
- GitHub Pages deployment through `.github/workflows/pages.yml`.

## Project layout

```text
index.html   App shell and dialogs
app.js       Game state, prompts, rendering, audio, sprites, and interactions
styles.css   Pixel-inspired responsive visual system
```

## Privacy

Royion does not require an account or backend. Local progress is stored with `localStorage` in the browser. If Live Archive Search is enabled, the current prompt and submitted answer may be sent to the public Wikipedia/Wikidata APIs to check niche entries. Turning the setting off keeps play local.

## Build and install

There is no compile step and no package dependency. To install locally, clone the repository and serve the project directory with any static HTTP server:

```sh
git clone https://github.com/GG-FLIPPER/royion.git
cd royion
python3 -m http.server 4173
```

Open <http://localhost:4173/> in a browser. The same static files can be deployed to GitHub Pages using the included `.github/workflows/pages.yml` workflow.
