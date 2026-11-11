# Cosmic Commando website

The public website for Cosmic Commando by MrHateful Games: one static page (`index.html`,
`style.css`, `site.js`), no build step. GitHub Pages serves it straight from `main` (root folder),
so a push to `main` is live a minute later at https://michaeljburton.github.io/cosmic-commando-website/.

The game's own (private) repo keeps a copy in `website/`; this repo is the one that is published.

## Swapping art

Every picture is a file in `images/`. To replace one, save the new file **with the same name and
format** over the old one; no HTML changes are needed. Keep roughly the size listed so the
layout stays the same.

| File | Where it shows | Size | Current source |
|---|---|---|---|
| `images/title_art.jpg` | Hero background (top of the page) | 1920 x 1080, pilots and ship on the right, calm on the left | AI (Gemini, title_d_2: station hangar) |
| `images/mrhateful-games-wordmark.png` | Top-left of the header bar | about 600 x 200, transparent PNG | AI (Gemini, wide_a) |
| `images/mrhateful-games-logo.png` | Footer badge | about 512 x 512, transparent PNG | AI (Gemini, badge_a) |
| `images/commander.png` | Ship beside the intro text | 512 x 512, transparent PNG | Game art |
| `images/clip_battle.gif`, `clip_wave.gif`, `clip_dock.gif`, `clip_gate.gif` | "In action" section | 640 x 360 (16:9), under 5 MB each | Game recordings (placeholders) |
| `images/<name>.jpg` + `images/<name>_thumb.jpg` | Screenshot gallery (thumb in the grid, full size in the lightbox) | 1600 x 900 and 640 x 360 | Game screenshots |

Screenshot names: `battle`, `destroyer`, `combat`, `dock`, `station`, `galaxy`, `planet`,
`mainmenu`. To add, remove or reorder screenshots or GIFs, edit the `gallery` or `clips` block in
`index.html` (one line each; the caption is the `alt` / `figcaption` text).

To drop a picture entirely: delete its line in `index.html`. The header and footer logos can
also be swapped for plain text: replace the `<img class="brand-logo" ...>` line with
`<span class="brand-name">MRHATEFUL <b>GAMES</b></span>` (the style is already in `style.css`).

## Text

All words are in `index.html`: the hook line in the hero, the intro paragraph, the six feature
cards and the press kit facts.

## Steam link

When the store page exists, set `STEAM_URL` at the top of `site.js`. Every Wishlist / Steam link
then points there and the big button reads "Wishlist on Steam".

## Store page mock-up

`store-mockup/` is a planning mock-up of a store page (placeholder AI capsules in
`store-mockup/img/`, everything else from `images/`), at `/store-mockup/` on the live site, for
getting feedback. It is marked noindex and labelled as a mock-up; delete the folder when the real
store page exists.
