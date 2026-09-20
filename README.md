# Happy Birthday, Ayesha 🎂💜

A one-page birthday surprise for Ayesha (21 September), from her big sister Faiqa.

Single self-contained `index.html` — no build step, no dependencies, works offline.
Just open the file, or serve the folder statically.

## What's in it

- White + purple cute theme: rounded comic lettering, dashed chunky borders,
  wobbling headings and floating emoji sparkles (✨💜🦄🍭) with purple balloons
- Six gift cards, each opening a different surprise:
  1. **Confetti storm** — canvas confetti burst + a flip-open envelope
  2. **Cake & candles** — tap each of the three flames to blow them out
  3. **Fireworks & letter** — a letter that types itself out
  4. **Scratch card** — drag to scratch the purple foil off a hidden message
  5. **Fortune cookies** — tap for a random note, drawn without repeats
  6. **Balloon pop** — pop six balloons to spell out A-Y-E-S-H-A
- A little-sister section, and a finale banner once all six are unwrapped

## Deploy

Static site, no framework. On Vercel: no build command, output directory `.`
(root). Everything lives in `index.html`.

## Editing the words

The personal wording is all in `index.html`:

- Envelope message and letter text — search for `Dear Ayesha,`
- Fortune cookie notes — the `WISHES` array in scene `'5'`
- Scratch card message — the `.scratch-under` div in scene `'4'`
- Little-sister cards — the `.bff-card` blocks
- Keepsake note — the `.bff-seal` block

## Adding another surprise

Add a `<button class="gift gN" data-scene="N">` to the `.gifts` grid and a
matching `'N':function(){…}` entry in the `scenes` object. The progress counter
and the finale read the gift count from the markup, so nothing else needs
touching.

## Editing the colours

Every colour comes from the CSS custom properties in `:root` (`--purple`,
`--grape`, `--lilac`, `--line`, `--ink`…), plus the `PALETTE` array in the
script, which drives the confetti, fireworks and balloons.
