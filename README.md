# Royion Friend Edition

Royion is the friend-specific edition of the daily trivia dive, copied from the current [Shrimpion](https://github.com/GG-FLIPPER/shrimpion) base. The game loop, prompt data, scoring, themed packs, offline storage, and responsive interface remain functional while the friend-specific asset layer is prepared for later replacement.

The current copy intentionally keeps the base shrimp sprites and reactions as placeholders. No friend photos or reaction artwork are fabricated here. When those assets are available, replace the hardcoded buddy/sprite definitions in `app.js`; this edition has no public asset-upload or customization controls.

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

## Asset status

Friend-specific photos, reactions, and final branding artwork remain outstanding inputs. Until supplied, the copied Shrimpion assets are deliberately retained so the project remains runnable and testable.
