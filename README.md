# Happy Birthday, My Love 💋

A single-page romantic birthday journey — crimson, velvet red, cream and a
touch of gold, with heart, rose and flower stickers, glossy tape and floating
hearts.

Everything lives in one self-contained `index.html` — no build step and no
dependencies (only Google Fonts is loaded from the web). The music and sound
effects are synthesised in the browser, so there are no audio files.

## What's in it

1. **Hero** — "Happy Birthday, My Love!", floating heart/rose/flower stickers, rising
   hearts, a live countdown, a music toggle and a *Start the Journey* button.
2. **Memory Lane** — six polaroid cards that flip to reveal a memory, a
   reason why, or a secret voice note.
3. **Make a Wish** — an SVG cake with five flickering candles. Blow into the
   microphone, or tap each flame; the last one sets off a heart-confetti blast.
4. **Love & Blessings** — every tap sends hearts, roses, flowers and gifts flying
   across the screen and adds to the counter (remembered in the browser), with milestones.
5. **Love Letter** — a sealed envelope that opens to a full letter.
6. **My Wishes for You** — three fixed wishes from Faiqa, pinned as sticky notes
   (edit them in `pinnedWishes` in `CONFIG`).

## Personalising it

All the personal text is in the `CONFIG` object at the top of the script in
`index.html`:

- `name` — the name in the big title (currently `Azhar`)
- `from` — how the letter and footer are signed
- `birthday` — `MM-DD`, drives the countdown (on the day itself it counts
  down the rest of the birthday)
- `memories` — the six cards. For a real photo, put the image in a `photos/`
  folder and set `photo: 'photos/our-first-date.jpg'`. For the voice card,
  set `audio: 'voice/note.mp3'` to play your own recording; without it the
  browser reads the note aloud.
- `letterGreeting` and `letter` — the letter, one string per paragraph

Colours are the CSS custom properties in `:root` plus the `PALETTE` array in
the script (confetti colours).

## Deploy

Static site, no framework. On Vercel: no build command, output directory `.`
(root). Pushing to `main` redeploys.

The microphone needs HTTPS, which Vercel provides; locally it works on
`localhost`.
