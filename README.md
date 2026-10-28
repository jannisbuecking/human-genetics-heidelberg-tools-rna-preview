# RNA tool portal — test website

Standalone preview of the horizontal RNA concept for the Institute of Human Genetics Heidelberg tool portal.

Website: https://jannisbuecking.github.io/human-genetics-heidelberg-tools-rna-preview/

Source branch: https://github.com/jannisbuecking/human-genetics-heidelberg-tools/tree/test/rna-horizontal

This repository contains only the standalone preview. GitHub Pages publishes the `preview` branch. The original repository’s `main` branch and live website are unchanged.

The original header, hero, animated terminal, descriptions, logos, and tool destinations are retained. The tools section uses a horizontal schematic RNA strand with the sequence layout AUG → aRgus → G C → MfAP → A U → MAMMOTH → C G → SYS → UAA. Tool panels are interface annotations; this is not a literal biological coding sequence.

The ribosome is a simplified 2D schematic using https://www.rcsb.org/structure/9RU8 as anatomical reference. It is not an atomic surface or a physical simulation of translation.

## Mobile scrolling correction

The layout now measures the stable CSS small viewport (`100svh`) instead of using the toolbar-dependent `window.innerHeight` to choose between the horizontal scene and the stacked fallback. Toolbar-only resize events no longer rebuild the scene. Width changes, orientation changes, and real changes to the stable viewport still update the geometry. The fitting threshold reserves 200 pixels beyond the heading and measured card, allowing the horizontal scene to fit a normal phone with its toolbar expanded. Very short windows retain the accessible stacked layout. Genuine geometry updates preserve the position within or below the scene.

Viewport unit reference: https://webkit.org/blog/12445/new-webkit-features-in-safari-15-4/

## Test website 2: vertical RNA

A separate vertical version is available at https://jannisbuecking.github.io/human-genetics-heidelberg-tools-rna-preview/vertical/ . Its source branch is https://github.com/jannisbuecking/human-genetics-heidelberg-tools/tree/test/rna-vertical . It keeps the same original top, tool information, colors, centered cards, and short sequence. It uses native vertical scrolling, upright labels, and the rotated translucent ribosome schematic. The horizontal website remains at the root URL.
