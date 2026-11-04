# Inkstrument Xerif

**Version 1.1.0**

A custom cut of [Instrument Serif](https://github.com/Instrument/instrument-serif) by Rodrigo Fuenzalida, made for [albcantero.com](https://albcantero.com). Until 1.0.0 it was called *Instrument Serif Custom*.

## What changed

- **Lighter.** Every outline is inset by 6.6 units (of 1000), so stems and hairlines are thinner while each glyph keeps its original width and kerning. The letters keep their original vertical metrics: they sit on the baseline and reach the x-height, cap height, ascender and descender of Instrument Serif, with the same overshoots.
- **Higher contrast.** Insetting thin and thick strokes by the same amount makes hairlines lose about half their weight and stems about a fifth, so the contrast is noticeably higher than in the original.
- **Square dots.** The dots of `. : ; … ! ? ¡ ¿ i j`, the diaeresis and the dot above are squares instead of circles, centred where the round dots were and 92 % of their diameter, so they weigh about the same.
- **Straight marks.** The comma, the acute and grave accents and the quotes (`' " ‘ ’ “ ” ‚ „`) are redrawn as straight, sharp shapes that match the square dots. So are the comma below (`Ș Ț Ņ Ķ Ļ Ŗ…`), the turned comma above (`ģ`) and the apostrophe-like caron of `ď ť ľ Ľ`.
- **Tracking built in.** The -0.021em tracking it was designed with is baked into the advance widths, so it needs no `letter-spacing`.

## Stylistic sets

| Feature | Name | What it does |
| --- | --- | --- |
| `ss01` | (from Instrument Serif) | Sharp terminals instead of ball terminals in `a c d e g` and their accented forms. |
| `ss02` | Round dots and marks | Brings back the round dots, comma, quotes and curved accents of Instrument Serif, thinned like the rest of the font. The curved accents take the angle of the straight ones and sit at the same distance from the letter. |

They can be combined. On the web:

```css
.round { font-feature-settings: "ss02"; }
```

## Two families

| Family | Files | Notes |
| --- | --- | --- |
| **Inkstrument Xerif** | Regular, Italic | Hinted (ttfautohint). Meant for display sizes: the thinned hairlines get very fine in running text. |
| **Inkstrument Xerif Exposure** | Regular, Italic | The same, with the curves softened like an overexposed phototype print: rounded corners and ink pooling in the joints, without adding weight. Unhinted; meant for display sizes. The ogonek and the cedilla (`ą ę ş`) break slightly. |

Each comes as TTF (`fonts/ttf`) for desktop apps and WOFF2 (`fonts/webfonts`) for the web.

## Use on the web

```css
@font-face {
  font-family: 'Inkstrument Xerif';
  src: url('InkstrumentXerif-Regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Inkstrument Xerif';
  src: url('InkstrumentXerif-Italic.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
```

Use the Exposure files the same way under the family name `Inkstrument Xerif Exposure`.

## Changes

### 1.1.0

- The letters are back on the baseline and at their original heights (in 1.0.0 the inset left them 7 units above the baseline and 7 units short of each height).
- Square dots centred over the original round dots (three of them were 2 units off) and resized from 96 % to 92 % of the round dot.
- Acute and grave accents 14 % larger; on capitals, 24 units closer to the letter.
- The dot of `;` sits exactly over the head of the comma.
- New straight comma below, turned comma above and caron of `ď ť ľ Ľ`.
- New stylistic set `ss02`: round dots and marks.
- Hinting redone with ttfautohint; the Exposure family is baked again from the new regular cut.
- Renamed from Instrument Serif Custom to Inkstrument Xerif (family names and files).

### 1.0.0

- First release.

## License

[SIL Open Font License 1.1](OFL.txt), like the original. Instrument Serif is copyright 2022 The Instrument Serif Project Authors; the modifications are copyright 2026 Alberto Cantero Soriano.
