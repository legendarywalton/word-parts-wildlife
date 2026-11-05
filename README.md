# Word Parts Wildlife

A silly study game for a word-parts quiz: prefixes, suffixes, and roots from the class flashcards. Get one right and a creature drops in like a stamp to say something encouraging. Get one wrong and it goes on the trouble list for a Challenge Round.

Single file, no build step, no dependencies beyond Google Fonts (falls back to system fonts offline).

## Play it

Open `index.html` in any browser, or serve it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

## Modes

| Mode | What it drills |
|---|---|
| Flashcards | Flip, then self-grade |
| Meaning Match | Word part → meaning |
| Backwards Bear | Meaning → word part |
| Word Detective | Real word → the part hiding inside |
| Speedy Sorter | Prefix, suffix, or root? |
| Match Up | Drag 3 parts onto 3 meanings, like the paper sheet |
| Challenge Round | Mixed questions drawn only from past misses |

Misses are counted per word part and saved in the browser (`localStorage`), so the Challenge Round and best streak are per device.

## Editing the word list

All content lives in the `PARTS` array near the top of the `<script>` in `index.html`. Each entry:

```js
{id:'sub', type:'Prefix', label:'sub-', forms:['sub'], meaning:'under or below',
 examples:[['submarine','a vessel that travels under water'], ...]}
```

`forms` lists the spellings Word Detective looks for inside example words. Suffixes may also carry `pos` (part of speech) which shows on the flashcard back.
