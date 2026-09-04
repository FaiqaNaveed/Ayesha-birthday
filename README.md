# Happy Birthday, Farwa 🎂

A one-page birthday surprise for Farwa (9 September), from Faiqa.

Single self-contained `index.html` — no build step, no dependencies, works offline.
Just open the file, or serve the folder statically.

## What's in it

- White + pink light theme with soft pink twinkles and floating balloons
- Three gift cards, each opening a different surprise:
  1. **Confetti storm** — canvas confetti burst + a flip-open envelope
  2. **Cake & candles** — tap each of the three flames to blow them out
  3. **Fireworks & letter** — a letter that types itself out
- A best-friend section, and a finale banner once all three are unwrapped

## Deploy

Static site, no framework. On Vercel: no build command, output directory `.`
(root). Everything lives in `index.html`.

## Editing the words

The personal wording is all in `index.html`:

- Envelope message and letter text — search for `Dear Farwa,`
- Best-friend cards — the `.bff-card` blocks
- Keepsake note — the `.bff-seal` block
