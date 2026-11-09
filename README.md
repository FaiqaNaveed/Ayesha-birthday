# Happy Birthday, My Love 💋

A single-page romantic birthday journey — crimson, velvet red, cream and a
touch of gold, with lipstick-kiss and hug stickers, glossy tape and floating
hearts.

Everything lives in one self-contained `index.html` — no build step and no
dependencies (only Google Fonts is loaded from the web). The music and sound
effects are synthesised in the browser, so there are no audio files.

## What's in it

1. **Hero** — "Happy Birthday, My Love!", floating kiss/hug stickers, rising
   hearts, a live countdown, a music toggle and a *Start the Journey* button.
2. **Memory Lane** — six polaroid cards that flip to reveal a memory, a
   reason why, or a secret voice note.
3. **Make a Wish** — an SVG cake with five flickering candles. Blow into the
   microphone, or tap each flame; the last one sets off a heart-confetti blast.
4. **Kisses & Hugs** — every tap sends kiss and hug stickers flying across the
   screen and adds to the counter (remembered in the browser), with milestones.
5. **Love Letter** — a sealed envelope that opens to a full letter.
6. **Wishing Box** — a form that pins wishes to a sticky-note wall.
   Wishes are stored in that visitor's own browser (`localStorage`), so each
   person sees only the wishes made on their device.

## Personalising it

All the personal text is in the `CONFIG` object at the top of the script in
`index.html`:

- `name` — the name in the big title (default `My Love`)
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
