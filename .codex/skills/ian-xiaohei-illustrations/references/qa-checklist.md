# QA Checklist

## Pass Criteria

- Is 16:9 horizontal.
- Background is clean white.
- Xiaohei is present.
- Xiaohei performs the core action, not just decoration.
- No old example compositions replicated — fresh metaphor invented for the current article.
- Image is whimsical, creative, interesting.
- Clean and restrained — main subject doesn't exceed ~60% of canvas.
- One image = one core structure.
- Handwritten annotations are few, short, and readable.
- Orange only for main paths or arrows.
- Red only for key points, problems, reminders, or results.
- Blue only for supplementary notes, feedback, or system status.

## Failure Signals

If any of these appear, regenerate or do a local edit:

- Top-left corner has "Common Pitfalls / Workflow / System Architecture / Roadmap" type titles.
- Xiaohei looks like a mascot, emoji, or cute cartoon.
- Image looks like a PPT, course slide, or formal flowchart.
- Too many elements, arrows, or nodes.
- Text becomes long paragraphs.
- Background has paper texture, shadows, gradients, beige, or noise.
- Real UI screenshots or tech-style interfaces.
- Severe text typos or unreadable annotations.
- Image is too rigid, lacking whimsical metaphor.
- Composition too similar to old examples in `assets/examples/`.

## Iteration Methods

- Too generic: Make Xiaohei the action subject, add a strange but valid metaphor.
- Too complex: Remove nodes, keep only one action and 3-5 short labels.
- Too cute: Emphasize deadpan, blank serious expression, not cute, not mascot.
- Too PPT-like: Remove titles, borders, neat grids, and excessive arrows. Switch to hand-drawn scene.
- Too similar to old examples: Keep core meaning, swap the main object and Xiaohei's action.
- Text errors: Prefer local edit first; if errors are severe, regenerate with fewer labels.

## Delivery Standard

A high-quality image should make the reader think "that's a bit weird" first, then understand the structure within 1 second.

If it looks like a tutorial page at first glance instead of a whimsical product sketch on white paper, it doesn't pass.
