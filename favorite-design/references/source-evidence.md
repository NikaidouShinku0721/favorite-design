# Source evidence and public-package boundaries

Read this reference when deciding what a visual reference proves or which files can belong in a reusable skill.

## Three different forms of evidence

| Evidence | Establishes | Does not establish |
| --- | --- | --- |
| Original website file | Source URL, image bounds/alpha, declared styles and implementation | Successful runtime state or a grant to redistribute the file |
| Clean browser capture | Visible composition at the observed viewport and state | Transparent asset bounds, motion duration or unobserved mobile behavior |
| Recording | Order and motion within the recorded interval | Earlier actions, all interactions or underlying rendering technology |

Use an original file when implementing an authorized artwork requirement, a live page to study composition, and a recording to study timing. Do not label a recording crop as an original transparent asset. Do not treat a new static capture as proof of an older recording's timestamp.

## Primary sources

| Study | Official page | What was checked |
| --- | --- | --- |
| Night-sakura arrival and chapter rhythm | [ENTERGRAM さくら、もゆ。](https://www.entergram.co.jp/sakuramoyu/) | Declared `js/common.js?0202` and `css/style.css?230222` separate a light curtain, phrase, logo and actionable information. The declared `img/sakura.png` is used for 2D petals. |
| Full feather boundaries and contextual profiles | [FAVORITE Sekai HD](https://www.favo-soft.jp/soft/product/WorldsEndHD/index.html) | Original separators and profile backgrounds serve distinct roles. Compare dimensions and transparent contours before choosing how each should be framed. |
| Fixed serif menu and selected/hover states | [dramatic create WORLD](https://dramaticcreate.com/world_re/world.html) | Declared `css/navigate.css` and [menu sprite](https://dramaticcreate.com/world_re/menu/menu.png): a 720×100 sheet with 120×50 state cells. This is a flat image state, not proof of an animated particle burst. |
| Character information and near-scene composition | [dramatic create CHARACTER](https://dramaticcreate.com/world_re/character.html) | Selected menu, profile and character composition. A selected-state screenshot alone does not prove successful hover behavior. |
| Design-family coverage | [FAVORITE catalog](https://www.favo-soft.jp/soft/product.html) | A bounded survey on 2026-10-12: 24 then-listed entries, with a separate WORLD page and deeper study of the three references above. Entries include remasters and bundles; this is not a count of unrelated visual languages. |

The original research kept downloaded documents and file hashes locally. Those documents, recordings, game resources and full official-page screenshots are not part of this package. Links above let readers inspect the primary pages. Pages and declared file URLs may change after the recorded study date; recheck them for a new project.

## Keep facts and adaptations separate

- **Observed:** a menu's feather appears underneath its word; profile text precedes the sprite; a page uses a pale curtain before a logo.
- **Source-verified:** fixed sprite-cell geometry; declared delay values; 2D canvas petal implementation.
- **Adapted:** editable glowing text above a separately layered ornament; newly chosen drift paths; portrait or story-linked voice; a five-second cycle requested for one project.

A clean capture can still show only a horizontal part of the PC site's fixed-width layout. Record that limitation instead of concluding that its art is cropped or that it supports phones. Record page, selected item, scroll position and CSS viewport for future captures. Saved image dimensions are not automatically CSS viewport dimensions.

## Source records for a new project

For each resource relevant to the requested change, retain the official page or game/archive association, retrieval date, dimensions, role and hash as useful. For voice, retain actual speaker, source scenario association and complete-line duration. Mark unknown or unverified fields explicitly. This record belongs to the implementation project; a narrow UI repair does not require an unrelated whole-game inventory.

## Redistribution

Source availability and educational intent do not provide a blanket redistribution license. Consult the [FAVORITE guideline](https://www.favo-soft.jp/soft/guideline.html) and the particular site's notice before bundling its art, audio, script text or code. This skill uses original explanatory writing, diagrams and official links. Its MIT license covers the repository's own work and does not license the referenced games or websites.
