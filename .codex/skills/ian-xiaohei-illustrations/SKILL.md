---
name: ian-xiaohei-illustrations
description: Generate Ian-style bilingual article illustrations. Used when users request illustrations for articles, posts, blogs, Notion docs, workflow docs, methodologies, processes, structures, states, metaphors, or viewpoints; defaults to Xiaohei IP, pure white hand-drawn style, sparse red/orange/blue annotations, clean but whimsical visuals.
---

# Ian Xiaohei Whimsical Article Illustrations

## Core Purpose

Design and generate 16:9 horizontal article illustrations. The goal is not commercial illustration, PPT infographics, or cute cartoons — it's to turn key judgments, processes, structures, states, or metaphors from an article into a clean, whimsical, creative, readable (but not instructional) hand-drawn explanation.

The default visual IP is "Xiaohei": a small solid-black creature with white dot eyes, thin legs, and a blank expression, seriously performing an absurd but meaningful task. Xiaohei must participate in the core action of the scene, not just stand nearby as decoration.

## Read These References First

Load as needed by task — don't flood context all at once:

- `references/style-dna.md`: Visual DNA, colors, text rules, prohibitions.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action library, and restrictions.
- `references/composition-patterns.md`: Structure types, original metaphor generation method, and anti-copy rules.
- `references/prompt-template.md`: Single image generation prompt template.
- `references/qa-checklist.md`: Post-generation checks and iteration rules.
- `assets/examples/`: Low-frequency visual calibration only. Do not enter the default generation path. Do not copy compositions, objects, or annotations from these examples.

## Workflow

### 1. Digest the Content

Read the user's article, link, Notion page, Markdown file, or screenshot content. Extract:

- What is the core argument
- Which paragraphs contain cognitive turning points
- Which content is suitable for visual explanation
- Which parts are text-only and don't need illustrations

Don't distribute illustrations evenly. Prioritize "cognitive anchors" such as: core judgments, two breakpoints, input-output loops, branching, before/after comparisons, multi-use scenarios, handoff paths, common pitfalls, role state changes.

### 2. Output Illustration Strategy First

If the user only says "analyze where to add illustrations / think about what needs illustrations", provide a shot list first. For each image, specify:

- Which paragraph it follows
- Image theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested annotation words (in the target language)

Default 4-8 images. For short articles, 1-3 is fine. For long articles, don't exceed 9. Just enough — don't turn the article into a picture book.

### 3. Generate One by One

If the user explicitly requests "generate / output / create / help me generate", don't stop to ask for confirmation — use the built-in `image_gen` to generate each image individually. Don't combine multiple images into one.

Each image should convey only one core structure. The prompt must include:

- 16:9 horizontal article illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue handwritten annotations (in the target language)
- Large whitespace
- Xiaohei as the core action subject
- No PPT, commercial illustration, childish cute style, complex architecture, or top-left type titles

Don't replicate past examples. Examples only provide style density and Xiaohei's participation method — don't directly reuse known compositions (conveyor breakpoints / Xiaohei pulling wires / material fish / stamp toolbox / common pitfall paths) unless the user explicitly asks to replicate a specific image. Always invent a fresh, strange but valid metaphor from the current article.

### 4. Check and Iterate

After generation, check `references/qa-checklist.md`. If any of these issues appear, regenerate or do a local edit:

- Xiaohei is just decoration
- Scene is too crowded
- Looks too much like a PPT / flowchart
- Too much text or severe typos
- Top-left corner shows "Common Pitfalls / Workflow / System Architecture" type titles
- Style is too cute, childish, or rigid
- Background is not clean white

### 5. Save and Deliver

If the user is working within the workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Preserve original generated files. Don't overwrite existing assets unless the user explicitly requests replacement.

## Output Language

The skill instructions are in English, but the **output language for annotations is determined by the user's prompt**:

- English labels: Specify "Labels in English" or write the prompt in English
- Spanish labels: Specify "Etiquetas en español" or write the prompt in Spanish
- Mixed: Specify "Labels in English and Spanish"

If the user doesn't specify a language, default to the language of the prompt. If the prompt is in Spanish, generate Spanish annotations. If in English, generate English annotations.

## Output Format

Strategy output before generation should be short and precise. Post-generation deliverables should include:

- How many images were generated
- Purpose of each image
- Save paths
- Which images are most stable, which are optional

Don't write lengthy style theory explanations — let the images speak for themselves.
