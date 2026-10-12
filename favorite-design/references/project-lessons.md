# Lessons from a continuous illustrated page

Read this reference for asynchronous scene/profile interactions and integration. These lessons came from a trilogy-themed personal site reviewed on 2026-10-12. After preview approval and local integration, [the website](https://nikaidoushinku0721.github.io/) was published at [commit `e1851af`](https://github.com/NikaidouShinku0721/NikaidouShinku0721.github.io/commit/e1851afd4e8d8d1d00f2850e88da4793637037a0); GitHub Pages deployment #59 succeeded. Local interaction evidence and online delivery checks are distinguished below. The reusable skill package preserves these evidence boundaries and distributes original guidance rather than the site's game assets.

## Commit identity and reveal together

A related-person link may move the reader into a character chapter before the new artwork loads. Keep the requested identity separate from the displayed identity. The old scene can remain usable while loading; it must not be narrated as the new person.

On a successful commit, coordinate scene, sprite, name, facts, selection, local reveal and context voice. If the reader is still viewing this chapter, restart the new encounter at commit time and stop any old-identity voice. If the reader has left, update stored content without restarting an offscreen reveal or interrupting another chapter's narration. Failed preloading preserves the coherent previous state.

```mermaid
sequenceDiagram
    participant R as Reader
    participant C as Controller
    participant A as Artwork
    participant V as View and voice
    R->>C: Request person B
    C->>A: Preload B; record request version
    Note over V: Person A remains coherent
    A-->>C: Ready
    alt B is still the latest request and chapter is visible
        C->>V: Commit B scene, sprite and facts
        C->>V: Restart B reveal; stop A voice
        C->>V: Schedule verified B line
    else Reader has left or request is stale
        C->>V: Store valid content or discard stale result
        Note over V: Preserve current chapter narration
    end
```

A local controller simulation reproduced a 1.5-second associated-person image load, then checked the full new reveal window and old-voice stop. A separate case verified that a late profile did not stop a message chapter's diary line. These are controller/model observations, not proof of actual CSS animation, listening quality or a real slow network.

## An anchor expresses intent, not final geometry

An initial `#people` or story anchor can resolve before asynchronous chapters acquire their final height. Restore the initial valid target once necessary content is committed, only if the reader has not acted and the hash still matches. Cancel restoration on new navigation or scrolling intent. Do not repeatedly pull the reader to an old anchor.

Pointer, wheel, touch, navigation keys and history changes can signal changed intent. A scroll caused by layout alone does not establish it. Explicit allowed anchors and listener cleanup make this easier to reason about.

The project's visible-browser check observed a fresh `#people` load reaching the intended chapter at a tested desktop width, near the fixed header's lower edge and without horizontal overflow. That observation covers that state; it is not a blanket promise about all anchors, widths or frameworks.

## Dwell starts at a coherent state

Five-second automatic cycling without a manual selector was a requirement of this particular project. For another site, follow its requested cadence and controls. A preload should not consume the next state's display window. Define a resumed window after returning from another chapter, a hidden tab or an opening film.

A complete automatic voice needs its full duration plus a startup allowance within the remaining relevant dwell. If it cannot fit, defer rather than shortening the original line or carrying it into an unrelated theme. Keep longer introductions for portrait or story interactions.

The local model checked deadline scheduling, hidden/film pauses, load failure, last-request wins and complete short-line selection. Source extraction and full decoding proved the origin and integrity of the project's 19 selected clips. Browser playback observations, careful listening and public deployment are separate evidence; a model pass does not prove them.

## Transfer principles, preserve choices

The user's corrections exposed reusable decisions:

- Place complete ornament contours below live labels with enough visual space.
- Use the requested full-body sprite and verify visible feet rather than enlarging a half portrait.
- Keep shared UI slots stable while content changes.
- Preserve meaningful prose and art; refinement does not require empty minimalism.
- Verify original plot, speaker and scene association before designing narrative triggers.
- Make narrow repairs stay narrow; broaden the design only with the user's expanded request.

Feathers, seaside blue, automatic themes and implicit original voice fit this site. Other design families may call for stars, snow, theatrical rhythm or quieter feedback. None of these examples mandates the same assets, controller or page sequence.

## Integrate with the existing site

### Compare computed geometry across hosts

Identical markup and shared CSS do not guarantee identical boxes. A blog theme can supply inherited letter spacing, line height or font rules, and its scrollbar can change the available layout width. Compare the same controls at the same CSS viewport and state, then correct the actual cause within the component's scope.

In this integration, Fluid's inherited `letter-spacing: 0.32px` subtly shifted navigation compared with the standalone scene. Explicitly resetting the shared text properties and aligning the project's 6 px scrollbar treatment resolved the first observed difference. A visible-browser comparison at 1440 CSS px then found zero `x/y/width/height` difference for the checked header, brand and navigation slots between homepage and archives. A separate static audit checked declared sizes at twelve widths; that static result does not establish actual browser geometry at every width.

A later long/short-route comparison exposed another issue: the long homepage had a 6 px scrollbar, while the short blog index had none. Equal scrollbar styling did not reserve equal layout space, so the navigation could still differ by 6 px. The project reserves the same vertical-scroll space with `html { overflow-y: scroll; }` in both hosts. Actual local-browser retests at 375, 768 and 1440 CSS px found zero `x/y/width/height` difference for all compared header, brand and navigation boxes between homepage and short blog. The 375 px width was confirmed from `innerWidth`, and that case had no horizontal overflow. This is a project-specific implementation, not a requirement to force permanent scrollbars on every design. The transferable check is scrollbar **presence and reserved space**, including short routes, not only its declared width. Neither `0.32px` nor `6px` is a recommended constant for other projects.

### Transform content without losing meaning

Keep useful blog functions such as actual article links, prose, code, search, reading navigation and existing comments. Simplifying repeated chrome should not discard them. Inspect the resulting semantic structure, not only its colors and borders.

An integration loop moved nodes while iterating a live `children` collection, skipping the blog title. Snapshotting the nodes before moving them fixed the omission. Heading/entry assertions in the transformed output help catch this class of error; a good-looking screenshot alone does not prove that the title or article links survive.

A second issue left two sidebar directories because the intended direct-child navigation was not selected and replaced. Locate the exact existing node and replace it, rather than adding another navigation block after an unsuccessful broad selector. Verify the final count, destinations and accessible labels. For this project, a static DOM regression retained prose, code, TOC, search, scroll controls and comments in a sample future-post fixture. It was a transformation check, not proof of browser interaction for every future article.

### Preserve canonical comment and route identity

A comment service's key may depend on a canonical path that differs from the visible route. Moving a message page into a homepage section should preserve that key when the old discussion is meant to continue. Confirm the configured identity before initializing a new widget; do not silently create an empty replacement thread.

The local integration reused Waline's existing `/message/` key and read 12 existing comments. Editing Markdown and displaying its preview were checked without posting a new public comment. This proves the observed local read/preview behavior, not a successful comment submission or production deployment.

Legacy URLs can map to the appropriate section while preserving useful fragment intent. Local browser checks reached the intended chapters for the former about, message, links, world-archive object and picturebook entries. The mapper also preserves unrelated external URLs in static regression. These aliases serve this site's history; another project needs its own route inventory.

### Separate production output from research

Before publication, inspect generated output as well as source. Remove preview diagnostics, inspector scripts/data, local server paths, unused inspection images and unneeded source manifests from the production bundle. Keep the separate inventory that explains what is used and why; use it to prune after confirming the actual consumers rather than deleting by extension alone.

The public skill package contains original instructions, original diagrams and official reference links. It excludes the site's game images/audio, full official-page captures, extraction material and local QA data. The website's asset inventory and the skill's reusable instruction package have different purposes.

### Bound local interactions and deployed delivery separately

The local visible-browser pass observed nine person-entry and nine portrait-click interactions reaching actual playback. It establishes those playback starts with the verified speaker/context mapping; it does not claim every line was listened to completion. Blog search and the legacy entries were restored and checked locally, while the comment read/Markdown preview kept its original identity.

The opening-film modal was also checked locally at 375 CSS px: its dialog covered a 375×900 viewport; the media reached readyState 4 with `paused` false. Skip cleared the media source, paused playback, released the scroll lock and restored focus to the opening trigger. This is actual local UI/media-state evidence, not a claim of an online full-video viewing.

The deployed [website](https://nikaidoushinku0721.github.io/) corresponds to [commit `e1851af`](https://github.com/NikaidouShinku0721/NikaidouShinku0721.github.io/commit/e1851afd4e8d8d1d00f2850e88da4793637037a0), with Pages deployment #59 successful. An independent online HTTP pass completed 62/62 checks: 59 complete resources returned HTTP 200 and matched local generated-output SHA-256; three opening-video Range requests returned HTTP 206 with correct ranges and matching first 1024 bytes. The full resources comprised the homepage, eight blog routes, five compatibility entries, eleven CSS/JS resources, two JSON files, two Waline vendor files, nineteen original voice clips and eleven key images. This verified selected delivered bytes, not a full video download or browser execution of redirects.

An actual online browser accessibility-tree check exposed the new title and all chapter content. That check and the resource audit do not repeat every local animation, portrait interaction, voice ending or live comment-service operation online. Browser automation-interface delays limited that additional online interaction pass; do not relabel the local results as a complete online end-to-end acceptance. Record any later online check separately.

## Report evidence at its actual level

| Evidence | Supported claim |
| --- | --- |
| Exact archive/scenario association and full decoding | Resource origin and technical integrity |
| Timer/class/media simulation | Controller decisions in the modeled cases |
| Visible browser states and interaction records | Particular geometry, animation and playback states observed |
| Careful listening and user preview approval | Different parts of perceived and accepted quality |
| Successful deployed-page acceptance | The published site's checked result |

Keep these claims distinct in a final report. A good screenshot or a passed fixture should not become an assertion that every interaction, every line or the final deployment is complete.
