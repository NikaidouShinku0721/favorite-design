---
name: favorite-design
description: Design or refine illustrated game websites with art-led composition, expressive typography, staged reveals and story-linked interactions informed by FAVORITE and its official partner sites. Use for favorite-design requests or FAVORITE-inspired visual-novel sites, including narrow UI repairs and broader redesigns. Preserve original identity and meaningful density without enforcing a fixed template or minimalism.
---

# Favorite Design

Make a fictional place readable and inviting through its artwork, story and interactions. Simplify redundant containers while retaining meaningful density, expressive detail and the user's existing identity. A style is a set of relationships, not a mandatory material sheet or page order.

## Establish scope and evidence

1. Inspect the existing page and requested change. Preserve working features and custom interactions. A button repair stays local unless the user expands the scope. For an original/preview compromise, state the specific strengths to retain from each.
2. Read [design families](references/favorite-family-study.md) when choosing an art direction. FAVORITE includes seaside memory, night blossoms, star fields, snow/light ensembles and lively performances; do not impose one palette or feather motif on them all.
3. Use [recording evidence](references/recording-evidence.md) for observed motion and [source evidence](references/source-evidence.md) for provenance. Separate visible facts, verified source behavior and a new adaptation. Study supplied URLs directly. Recordings establish timing; their screenshots are not reusable game assets.
4. Inventory resources needed for the requested change before declaring one missing: relevant scenes, sprites, CG, native motifs or audio/script associations. Inspect all three sources when trilogy-wide content is requested; a local hover repair needs only its relevant motif. Do not invent a location or assign a voice by filename alone.
5. Size the plan to the task. Describe art/text relationships, stable control slots and feedback; add chapter variety and a motion/voice matrix when in scope. Produce and inspect a concrete preview before any required visual approval.

## Compose from content

- Let original art carry identity at a useful scale. Keep logos intact, inspect silhouettes and narrative landmarks, and find text-safe space before arranging the page. Choose a better scene when necessary rather than dimming every image with the same overlay.
- Give layers a purpose: environment, people, thematic detail, readable content and controls as needed. The layer count is not prescribed. Check actual stacking contexts; a large child z-index cannot escape its parent's context.
- A continuous outer world can contain changing local scenes. A character encounter updates setting, sprite and facts together; reading can use a quieter surface while retaining the world's atmosphere.
- Vary compositions by content: panoramic entrance, illustrated account, portrait stage, connected clues, compact archive or quiet message area. Do not turn every chapter into the same hero, card grid or sparse heading.
- Create density with real prose, scene thumbnails, relationships, original illustrations and useful links. Never manufacture statistics, dates, canon or filler labels.
- Develop project-specific spacing, shapes, paths and transitions. Repeated motifs support continuity without erasing distinctions between chapters or works.

## Preserve artwork and stable geometry

- Record source and usable image regions. Inspect alpha, native proportions and embedded text. Use official files or verified game resources when original locations/people are required.
- Preserve a decoration's entire intended contour. Place the work-appropriate ornament beneath live text/UI and give it room; use feathers when they serve the requested work. Do not repair a wrong layer by clipping its ends. Separating a complete state from a sprite sheet is valid extraction. Reject neighboring fragments and contaminating baked text.
- Frame scenery around narrative landmarks. A requested full-body encounter retains the whole sprite, including feet; inspect nontransparent bounds and stage space. Choose cover/contain by image role, not universally.
- Extend scenery behind atmospheric headers. Shared navigation, logo slots, click targets and text slots keep their position/size across themes/routes/states. Fit different aspect ratios without stretching.
- Hover/focus/selection must not move the click target. Measure recurring UI at the same viewport; unexplained differences greater than 1 CSS px require correction.
- When the same shell spans a standalone scene and a blog/theme host, compare computed inheritance as well as declared CSS: typography and scrollbar presence can shift identical markup. Compare both long and short routes at the same viewport; matching scrollbar widths alone does not reserve the same layout space. Scope corrections to shared components. See [integration lessons](references/project-lessons.md#integrate-with-the-existing-site) for geometry, semantic content and comment identity.

## Typography and interaction

- Match type to the work: expressive Mincho/Song narrative text with a clear small-text companion where appropriate. Original title art remains central; a large neutral headline is not a substitute for its identity.
- Glow needs sharp glyphs and restrained light. Check bright clouds and dark scenery. Reading needs suitable line length, leading and a deliberate surface.
- For a requested RE:BIRTH-like menu, combine borderless glowing live text with a complete diagonal feather beneath it on hover/focus. The source is a flat image state; separate layers and smooth drift are adaptations. Do not infer particles or 3D from that evidence.
- Keep labels accessible, decoration noninteractive and keyboard focus visible. Touch works without hover. Inputs, filters and portrait selectors may retain functional boundaries.
- Contextual voice follows meaning: scene entry, story clue or portrait encounter → verified relevant line → actual speaker and readable subtitle. For narration/easter eggs, do not replace this design with a speaker button.
- Respect audio unlock and keep one foreground voice. Verify requested people/works; attribute narration honestly for an unvoiced protagonist. Avoid hover spam and playback after leaving its context. Provide an appropriate stop/mute method consistent with the presentation; preserve readable captions on failure.

## Motion as a relationship

Choose movement for what changes. Staged entrances, scene crossfades, hover light and ambient motion have different jobs.

| Situation | Useful relationship | Required invariant |
| --- | --- | --- |
| Page arrival | Loaded art, phrase, logo and actions reveal deliberately; a short light curtain may fit | No repeated entrance after final state or theme change; page navigation remains available |
| Portrait | Information can precede the sprite; local scene coordinates with the encounter | Full silhouette, fixed common stage, last request wins |
| Scene/theme | Preload, commit one coherent state, then crossfade | No blank frame or stale asynchronous writeback; keep usable state on failure |
| Ornament feedback | Complete work-appropriate detail softly reveals below the label | No clipping, blocked input or layout shift |
| Ambient | Sparse thematic particles or restrained sprite drift | Calm reading; pause while hidden/in video; remove ongoing movement for reduced motion |

- Verify timing against source when claiming fidelity. New durations/paths are creative choices, not official constants. Do not blindly copy particle counts or old timer loops.
- Automatic cycling is project-specific. Follow requested cadence and controls; keep reading stable, pause while hidden/in video, start dwell at committed state and handle return explicitly. Use a deadline rather than coarse tick counts.
- A complete automatic voice must fit the remaining contextual dwell, including startup margin. Otherwise defer to a later visit; do not cut it or let an unrelated theme inherit it.
- Use cancellation/version tokens and check requested identities alongside committed ones. Slow associated links, rapid clicks and failed playback must not select old content or permanently suppress retries.
- For asynchronous continuous-page interactions, consult [project lessons](references/project-lessons.md) for commit-time reveals and initial-anchor restoration. These are failure-derived examples, not a prescribed controller or page structure.
- A fullscreen opening film is a separate modal interaction: it may cover page navigation but needs immediately usable Skip. Closing/ending/cancellation stops media, clears source, releases scroll lock and restores focus.
- Natural scrolling may connect chapters. Do not infer snapping from a recording; long reading remains controllable. Reduced motion removes drift/delays while preserving final content and requested functionality.

## Canon, sources and reusable output

Distinguish original plot, translated/paraphrased plot and site-original fiction. Label original site writing explicitly. Keep scene attribution separate from event attribution: an illustrative location alone does not prove a character visited it. Record exact audio/script bindings; do not infer canon from decoration, silent recordings or shortened lines.

Keep research assets separate from a public skill package. Publish reusable instructions/code and original diagrams with source links; inspect permissions before bundling third-party images, audio, script text or website source. Educational use is not a blanket asset license. See [source evidence](references/source-evidence.md).

## Inspect each stage

1. Compare original, reference and preview: art scale/color, silhouette/text relationship, purposeful density, chapter variety and motion sequence. Border removal alone is not success; neither maximal ornament nor empty minimalism fulfills the brief.
2. Inspect full decorative contours and alpha on real backgrounds, plus shared UI geometry across themes/routes.
3. When verification is requested, inspect affected components on desktop, intermediate widths and phone. Check relevant overflow, sprites, hover/focus, keyboard/touch and retained custom interactions. For work involving voice/media, cover its contextual clips, rapid requests, failures, Skip and reduced motion. Match inspection to the scope; a narrow repair does not authorize a whole-site redesign.
4. Use actual browser interaction for visual/media acceptance. Logic tests complement it; they do not establish listening or visual quality. Fix failures and repeat affected checks before advancing.
5. When integrating or publishing, retain useful blog behavior and canonical comment identity. Inspect built output for duplicate navigation, missing semantic headings, debug/QA state, private paths and unused research assets; keep a source inventory separate from the public bundle. This publishing check does not expand a local repair's scope.
6. Report evidence and remaining limits. Do not invent an AI percentage or call an unapproved preview production-complete. Present screenshot/preview proof for required approval; publish only at the authorized stage.

Retain frontend-design's intentional composition, coherent type/color tokens, accessibility, responsiveness, CSS discipline and self-critique within the requested scope. These principles do not authorize changing unrelated colors, type or layouts. Apply restraint to meaningless ornament and redundant containers while preserving the original world's emotional identity.
