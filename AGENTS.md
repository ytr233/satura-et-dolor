# Satura et Dolor — Folder Defaults

These instructions are the default for all work in this repository, especially new comic pages. Inspect representative existing pages in `src/assets/comics/` before generating or directing new artwork. Do not substitute a generic art direction.

## Comic format

- Every comic is one landscape page containing exactly six panels.
- The default and required layout is a clean 3-column by 2-row grid with thick, straight black gutters.
- Do not use vertical strip pages, inset panels, split panels, montage fragments, or more/fewer than six panels unless the user explicitly overrides the format.
- Comics are wordless. Do not place titles, dialogue, captions, verses, labels, sound effects, or other typography inside the artwork.

## House art direction

- Match the established collection: highly detailed hand-inked graphic-novel illustration, etched/crosshatched linework, tactile aged-paper grain, restrained realism, and dark luminous chiaroscuro.
- Favor antique gold, deep umber, muted moss, oxblood, smoke blue, and occasional faded coral. Adjust temperature to the story while keeping the page cohesive.
- Preserve expressive, dignified Black characters and careful rendering of faces and hands.
- Biblical, historical, symbolic, and contemporary settings should all feel like part of the same collection.
- Avoid glossy digital painting, generic fantasy concept art, soft watercolor-only rendering, photorealism, caricature, and generic white European biblical casting.
- Keep violence restrained and narratively meaningful. No explicit gore, sexualized nudity, or spectacle-first harm.

## Character variation

- Hairstyles change in every comic. Select a fresh, story-appropriate hairstyle for each new page instead of treating hair as a locked continuity feature.
- Keep a character's face, hairstyle, clothing, and distinguishing features consistent across the six panels of that one page.
- Do not infer that recurring biblical or symbolic figures must retain hairstyles from earlier comics.

## Storytelling

- Communicate through composition, gesture, expression, repeated visual motifs, and contrast rather than text.
- Favor moral and emotional ambiguity over literal explanation. Faces should carry mixed emotions when the story calls for them.
- Before generation, write a six-beat panel plan and verify that each beat maps to exactly one grid cell.

## Files and gallery metadata

- Use a concise Latin title consistent with the collection.
- Save artwork as a lowercase hyphenated slug in `src/assets/comics/<slug>.png`.
- Register it in `src/comics.js` with `page("<slug>", "<Latin Title>", scripture?)`.
- Scripture is optional metadata displayed by the gallery, never printed inside the comic image. Use the existing `{ reference, text }` structure and the collection's established translation style.
- Do not use Isaiah 46:10 unless a comic depicts it ironically in relation to there being no ending.
- After adding or replacing a page, run `npm run build` and verify that the generated asset is included.

## Image-generation workflow

- Load and visually inspect at least three representative existing comics before prompting a new one; for recurring themes, include the closest related pages.
- Use those inspected pages as style references while explicitly forbidding copied compositions.
- State `exactly six panels in a 3 × 2 grid` near both the beginning and end of the generation prompt.
- Inspect the result before installing it. Reject and regenerate if the grid, wordlessness, character dignity, or house rendering style is wrong.
