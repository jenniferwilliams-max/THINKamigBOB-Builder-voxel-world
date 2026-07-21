# THINKer Bob rig-ready SVG set

Open `thinker-bob-rig.svg` to view the assembled character. The `layers` directory contains one SVG wrapper for each original artwork layer, and `assets` contains the linked transparent PNG artwork.

This package is portable as a directory: keep `thinker-bob-rig.svg`, `layers`, and `assets` together. The SVGs use raster artwork internally; they preserve the approved visual appearance but are not vector redraws.

## Browser animation

Inline the master SVG into the page so its named groups can be selected. Rotate a joint by setting its CSS custom property:

```js
const joint = document.querySelector('#right-shoulder');
joint.style.setProperty('--rotation', '-18deg');

const eyes = document.querySelector('#eyes');
eyes.style.setProperty('--blink', '0.08');
```

The joint coordinates were derived from the layer artwork and visually tuned through wave, walk, seated, and tool-holding tests. See `rig-manifest.json` for the complete pivot map.

## Tuned pose tests

`pose-tester.html` provides neutral, wave, two walk phases, seated, two-handed tool-holding, and blink checks. The pivot map was visually tuned against these poses so the transparent artwork remains centered at its shoulder, elbow, wrist, hip, knee, and ankle connections.
