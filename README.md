# Xiaohei Illustrations — English/Spanish Edition

> **Fork of [ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)** by [Ian](https://github.com/helloianneo). Adapted for English and Spanish content.

> Turn the judgments, processes, states, and metaphors in articles into clean, hand-drawn, whimsical article illustrations on white backgrounds.
>
> 16:9 Horizontal | Xiaohei IP | Pure White Hand-Drawn | Sparse Red/Orange/Blue Annotations | Codex Skill

> **En español:** Convierte los juicios, procesos, estados y metáforas de un artículo en ilustraciones limpias, hechas a mano, caprichosas, sobre fondos blancos. **Genera etiquetas en inglés O español** — solo indica el idioma en tu prompt.

---

## What This Repository Is

Xiaohei Illustrations (EN/ES) is a **Codex Skill** — a set of instructions that guides an AI agent (OpenAI Codex) to generate article illustrations for English and Spanish articles, posts, blogs, Notion docs, and methodology content.

This is a **fork** of the original Chinese-only [ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) repo by Ian. All skill files, prompts, and references have been translated to English. The visual style, Xiaohei IP character, and workflow remain identical to the original.

**You choose the output language.** The skill instructions are in English, but when you generate images you can specify:
- **English labels**: "Labels in English"
- **Spanish labels**: "Etiquetas en español"
- **Mixed**: "Labels in English and Spanish"

It's not a generic illustration prompt, nor a PPT infographic template. Its core goal is: first understand the cognitive anchors in an article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanation.

---

## Requirements

> **This skill requires a paid subscription or API key to run.**

This is a Codex Skill — it runs inside [OpenAI Codex CLI](https://github.com/openai/codex). You need one of:

| Option | Cost | Details |
|--------|------|---------|
| **ChatGPT Plus** | $20/month | Run `codex`, sign in with your ChatGPT account |
| **ChatGPT Pro** | $200/month | Same, with access to advanced models |
| **ChatGPT Business/Enterprise** | Team plan | Organization-level subscription |
| **OpenAI API Key** | Pay-per-use | Set `OPENAI_API_KEY` env variable (~$0.08-$0.12 per generated image) |

**There is no free tier.** The skill files are free (MIT licensed), but the AI model that powers them requires a paid OpenAI account.

---

## Installation

### Prerequisites

- **Node.js 22+** (use [mise](https://mise.jdx.dev/) or [nvm](https://github.com/nvm-sh/nvm) for version management)
- **OpenAI account** with one of the plans listed above

### Setup

```bash
# 1. Clone this repo
git clone https://github.com/Bllq21/xiaohei-illustrations-en-es.git
cd xiaohei-illustrations-en-es

# 2. Install dependencies (local, not global)
npm install

# 3. Enable skills feature
mkdir -p .codex
cat > .codex/config.toml << 'EOF'
[features]
skills = true
EOF

# 4. Copy the skill
cp -R ./skill .codex/skills/

# 5. Run
npx codex
```

Then in Codex:
```text
Use $xiaohei-illustrations to generate a whimsical article illustration about "the difference between knowledge and wisdom".
```

### Isolated Setup (mise + direnv)

```bash
# .mise.toml is included — just run:
mise trust
direnv allow
npx codex
```

---

## How to Use

### Illustration Planning Only

```text
Use $xiaohei-illustrations don't generate images yet.
Please analyze the following article and identify where illustrations would be valuable. Output a shot list of about 5 images.
For each image, specify: which paragraph it follows, theme, core meaning, structure type, what Xiaohei is doing, suggested labels.

<paste article>
```

### Generate Article Illustrations

```text
Use $xiaohei-illustrations generate 4 whimsical article illustrations for the following article.
Requirements: 16:9 horizontal, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten annotations.

<paste article>
```

### Single Concept Illustration

```text
Use $xiaohei-illustrations generate one article illustration for: "Trust isn't shouted — it's paved one piece of evidence at a time."
The scene should be whimsical but clean. Xiaohei must perform the core action.
```

### Edit: Remove Title or Fix Text

```text
Use $xiaohei-illustrations help me edit this image. Remove the "Workflow" title from the top-left corner, keep everything else the same.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Visual Style

This skill uses Ian's "Xiaohei Whimsical Article Illustration" style:

- Pure white background — no paper texture, beige, shadows, gradients
- Black hand-drawn line art — thin lines, slight wobble
- Lots of whitespace — subject occupies ~40%-60% of frame
- Sparse red, orange, blue handwritten annotations
- One image = one core action, structure, state, or metaphor
- Xiaohei must participate in the core action, not just be decoration
- Whimsical, creative, clean — not childish, not cute

---

## Example Results

These images are from the original Chinese version. They are style calibration samples, not composition templates.

![Two Breakpoints](examples/images/01-two-breakpoints.png)
![Sort by Purpose](examples/images/02-sort-by-purpose.png)
![One Fish Many Uses](examples/images/03-one-fish-many-uses.png)
![Handoff Path](examples/images/04-handoff-path.png)

---

## Credits

This is a fork of [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) by [Ian](https://github.com/helloianneo).

All original work (visual style, Xiaohei IP character, composition patterns, workflow design) belongs to Ian. This fork translates the skill files to English for use with English/Spanish content.

Original author:
- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)

---

## License

MIT License. See [LICENSE](LICENSE).
