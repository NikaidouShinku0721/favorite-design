# Recording evidence

Read this reference when selecting a reveal relationship or comparing a proposed animation with the source. The study combined user-provided desktop recordings with the official sites below. Recordings are not distributed here. Times begin at each recording's first frame; browser chrome and translation overlays are excluded from design observations.

The observations were reviewed on 2026-10-12. They describe particular recorded intervals, not every possible state of those websites or their current behavior.

## ENTERGRAM: night artwork and separate reveal moments

Primary page: [さくら、もゆ。](https://www.entergram.co.jp/sakuramoyu/)

A 34.00-second desktop recording showed night-sakura artwork already present, a disappearing pale curtain, softly glowing vertical phrases, then the original logo and release/action information. Its first frame did not include the start of loading.

- At about 6–13.8 seconds, three illustrated story compositions alternate large images and substantial prose, with selective plot-word color and image edges blending into a reading surface.
- At about 13.8–19.5 seconds, nine circular avatars lead to a stable profile stage: facts on the left, a large sprite on the right and a vertical signature line. Three observed changes take about 0.8–0.95 seconds; text precedes the new sprite by about 0.3–0.45 seconds.
- The remaining interval shows a dense CG gallery, illustrated special entries, product artwork and compact credits/specifications.
- Petals continue across dark and light chapters. The recording alone does not establish their rendering technology.

A separate 3.20-second complete-entry supplement was sampled at 10 fps. An opaque white curtain is visible around 0.15–0.85 seconds, dissolves into the artwork around 0.95–1.55 seconds, then a phrase and logo become legible at different moments. These times include actual loading, with roughly 0.1-second sampling precision.

The site's declared source independently specifies window load → 300 ms delay → 800 ms curtain fade. Phrase, logo and release-information delays are 0.5, 1.0 and 1.5 seconds, with an 0.8-second fade. The petals use 2D canvas images. The short supplement is effectively silent; it establishes no voice behavior.

**Transfer:** separate loaded artwork, phrase, identity and action into deliberate reveal moments. Choose new timings that fit the project. These exact values, blossoms, art and chapter order are not universal skill defaults.

## FAVORITE: a continuous sky around changing near-scenes

Primary page: [いろとりどりのセカイ HD Re:GENERATION](https://www.favo-soft.jp/soft/product/WorldsEndHD/index.html)

A 28.23-second desktop recording showed original character art and sky from its first frame, followed by a phrase and logo. Fine navigation is already usable.

- At about 4–13 seconds, large irregular feather illustrations connect remaster information, illustrated entries and story. White reading paper, translucent panels and scenery-native text have different densities.
- At about 13.25–21.25 seconds, ten avatars, a large sprite, vertical quote and rich profile form a character encounter. The near-scene changes with the character while the outer sky and navigation persist. Observed coordinated crossfades last roughly 0.2–0.4 seconds.
- The final interval shows a tight three-column CG gallery and compact two-column specifications.

The recorded initial feathers are substantially static. The recording is effectively silent and does not establish voice/BGM interaction. It provides no evidence of 3D models, gallery-opening behavior or whether an avatar transition came from a click or hover.

**Transfer:** maintain a coherent external world while a local character encounter changes scene, sprite and facts together. Preserve complete decorative contours. Do not imitate old fixed-width geometry as a modern responsive recipe.

## dramatic create: a word and a complete feather

Primary page: [WORLD’S END -RE:BIRTH- WORLD](https://dramaticcreate.com/world_re/world.html)

A 6.47-second recording begins with the page already open. It demonstrates menu hovering, not site arrival. Six serif labels lack enclosing button frames or opaque fills. A bright diagonal feather appears behind a hovered word. WORLD retains its selected feather independently of another item's hover.

The source separately verifies a flat 720×100 menu sprite with fixed 120×50 cells: normal row at y=0, hover/selected row at y=50. A background-position change performs the feedback. This supports the stable slot and complete artwork state; it does not establish CSS animation timing or a particle burst.

**Transfer:** keep new functional text editable, above a complete work-appropriate ornament. Keyboard focus should offer comparable feedback. Separate live layers, soft drift and extra text glow are new adaptations, not behavior proven by the sprite source.

## Evidence limits

These recordings do not prove WebGL/3D, fullscreen opening/Skip, contextual voice semantics, custom-cursor implementation, mobile responsiveness or forceful scroll snapping. Those may be useful project choices; label them as additions. Consult [source evidence](source-evidence.md) for primary references and [design families](favorite-family-study.md) before treating a seaside motif as the style of every FAVORITE work.
