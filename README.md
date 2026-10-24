# Copperwing

A tap-to-flap bird game tuned to the classic 2013 flap physics.

This is the release build: classic physics, graphics from the `assets` folder, sounds from `assets/sounds`, and a sound on/off button. There's no settings panel.

## Add your own graphics

1. Open the `templates` folder. It has three blank, transparent PNGs at the game's sprite sizes:

   | File | Game size | File size |
   |---|---|---|
   | `bird.png` | 34 × 24 | 136 × 96 |
   | `pipe.png` | 52 × 320 | 208 × 1280 |
   | `background.png` | 288 × 512 | 576 × 1024 |
   | `title.png` | 220 × 60 | 440 × 120 |
   | `gameover.png` | 220 × 50 | 440 × 100 |
   | `panel.png` | 220 × 120 | 440 × 240 |
   | `medal-bronze.png`, `medal-silver.png`, `medal-gold.png`, `medal-platinum.png` | 48 × 48 | 192 × 192 |

2. Draw your design on each one. The files in `templates/guides` show the frame, center lines, the pipe's cap area, and where the ground strip covers the background. Put a guide on a layer under your drawing for reference, then hide it before exporting.
3. Export as PNG with the same names and save them in the `assets` folder. The title artwork replaces the game's name on the opening screen. On the post-game screen, the heading replaces the "Grounded" text, the panel is the board behind your score, and each medal shows at 10, 20, 30 and 40 points. The score numbers and medal name are drawn on top of the panel, so leave room for them (the panel guide shows where).
4. Draw the pipe upright, with the cap at the top. The game flips it for the top pipe.

You don't have to use the templates. Any PNG or JPG named correctly works. The game smart-crops it to the right size when it loads, removes a solid background color from everything except the background, and extends short pipes to fill. Transparent backgrounds give the cleanest result.

Any file you leave out uses the built-in art.

## Add your own sounds

Save sound files in `assets/sounds`, named for when they play:

| File name | Plays when |
|---|---|
| `flap` | Every tap |
| `point` | Clearing a pipe |
| `hit` | Crashing |
| `fall` | Dropping after a pipe hit |
| `swoosh` | Starting a new run |

Use `.mp3`, `.wav`, `.ogg` or `.m4a` (for example `flap.mp3`). Short clips work best, since the flap sound plays on every tap. Any you leave out use the built-in sounds, and the sound button turns all of them on or off.

## Put it on GitHub Pages

1. Create a new repository on GitHub.
2. Upload everything in this folder (`index.html`, `assets`, `templates`, `README.md`), keeping the folder structure.
3. In the repository, go to **Settings → Pages**. Under "Build and deployment," set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. After a minute or two, your game is live at `https://<your-username>.github.io/<repository-name>/`.

To play it like an app on iPhone, open that link in Safari, tap **Share**, then **Add to Home Screen**.

## Notes

- The `assets` folder only loads when the game is served from a website, such as GitHub Pages. Opening `index.html` straight from your computer skips it and shows the built-in art, because browsers block reading nearby files there.
- A GitHub Pages site is public. Anyone with the link can play it and see the images and sounds in `assets`, so only use artwork and audio you made or have the rights to share.
- After you replace an image, the browser may keep showing the old one for a bit. Reload the page to pick up the change.
