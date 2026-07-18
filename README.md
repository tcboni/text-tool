# Text Tool

A character & string inspector. Paste any text — a letter, an emoji, a flag, a
ligature, an invisible control character — and it dissects it down to the bits.

**[→ Open Text Tool](https://tcboni.github.io/text-tool/)**

## What it shows

**Whole-string overview** — grapheme, code-point, UTF-8 byte, UTF-16 unit, word,
and line counts (via the browser's Unicode-aware `Intl.Segmenter`).

**Grapheme clusters** — the string split into user-perceived characters. Click any
cell to inspect it. Multi-code-point clusters (emoji, flags, accented letters) are
flagged so you can see how they're built.

**Per-code-point inspector**

- Identity: name, general category, script, and Unicode block.
- Code point in decimal, hex, octal, and binary.
- **UTF-8** bytes with each byte's bits colour-split into _structure_ bits and
  _code-point payload_ bits, so you can see the encoding at work.
- UTF-16 (with surrogate pairs) and UTF-32.
- Ready-to-paste escapes/references: HTML (decimal / hex / named), CSS,
  JavaScript (`\u` and ES6 `\u{}`), Python, URL percent-encoding, Base64.
- Case transforms and numeric value.
- Boolean Unicode properties (emoji, combining, whitespace, bidi control, …).

**String-level analysis** — a UTF-8 hex dump, bulk encodings, the four Unicode
normalization forms (NFC / NFD / NFKC / NFKD), and word/sentence segmentation.

**Emoji dissection** — ZWJ sequences, skin-tone modifiers, variation selectors,
and regional-indicator flags are each labelled by their role in the cluster.

**Hidden-character warnings** — flags zero-width, control, private-use, and
bidirectional control characters (the "Trojan Source" text-spoofing vector).

## Other features

- Hover any label for a plain-English tooltip explaining what it means.
- Hover a row to reveal a copy button that copies the raw value.
- Dark, keyboard-and-mouse-friendly, responsive.
