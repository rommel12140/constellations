# Sky atlas rebuild of the meeting tasks hero

Mode: Refine, using the `design-review` skill from rommel12140/skills. Scope: the hero scene of `docs/spec/exo-meeting-tasks.html`. The story, data, honesty labels, workflow, inspector, why, cost and coverage sections are unchanged.

## What changed

- The SVG constellation is replaced by a canvas chart drawn like a printed sky atlas: a night chart in dark mode and a paper atlas in light mode, all colours from tokens.
- Stars are stages; filled when visited, open circles when this run did not reach them. Planets are what EXO holds, shaded by their star and coloured by outcome.
- The 15-minute wait is a dial of minute ticks. The approved-people shield is the only smoke: a translucent wash that planets part as they pass and that ripples when Jordan's item strikes it.
- Each item's route is drawn as a dashed track with time marks.
- The timeline is a continuous scrubber; the camera follows playback and flies in when a stage is opened, where moons orbit the chosen planet and a card lists its evidence.
- Removed: glow halos, pulsing, nebula blobs, cursor glow and frosted glass (catalog M3, C3, K2).
- The page header is shorter so the chart reaches the first screen at 1280 by 800.

## Measured

| Check | Before (published version 3) | After |
| --- | --- | --- |
| Idle sample, 5 s, no input, 1440x900 | 600 frames | 0 frames |
| Throttled phone, 4x CPU, 390x844 at DPR 3, 14 s of playback, frames over 25 ms | median 60 (48 to 61), three runs | median 20 (19 to 21), three runs |
| Horizontal overflow at 2560, 1440, 1280, 1024, 768, 390, 320 and after resizing back | 0 px everywhere | 0 px everywhere |
| Lowest text contrast in the hero | not measured | 6.61 dark, 4.75 light |
| Page HTML bytes | 80,023 | 102,176 |

The phone keeps a sharp canvas and drops to 1x resolution if frames run long during motion. Captures are in this folder: 1280x800 and 1440x900 dark, 1440x900 light, 390x844 dark and light at DPR 3, and 320 after a wide-to-narrow resize.

## Not checked

- Real devices; all phone numbers are Chromium emulation with CPU throttling.
- Cold-load medians for first and largest paint.
- Keyboard and screen-reader walkthrough beyond the controls being real buttons and a slider with values.
- `voice.md` does not exist in this repo or in EXO, so the visual-language gate (X1) is unchecked; the space concept is the owner's direction.

## Accepted exception

Glowing nodes on a dark field are banned by the catalog (M3, C3). The owner asked for a constellation with planets, moons and a smoky barrier, and the product is named Constellations, so the concept stays; every element carries meaning and the decorative glow is gone.
