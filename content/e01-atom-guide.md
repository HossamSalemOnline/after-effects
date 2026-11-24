# Atom: the complete guide to an AI agent inside After Effects

<p align="center"><a href="https://tryatom.ai/after-effects-templates/minecraft-title-sequence"><img src="https://cdn.davey.design/templates/minecraft-title-sequence/video-thumb.jpg" width="720" alt="Minecraft title sequence, one-shot by Atom"></a><br><sub>A Minecraft-style title sequence Atom built from a single prompt (free template, link above)</sub></p>

> **Compiled from:** the official [tryatom.ai](https://tryatom.ai/) site and docs, 40 recent posts by its developer [@daveylovescode](https://x.com/daveylovescode), Jake In Motion's [After Effects 27 review](e02-after-effects-27-updates.md), School of Motion coverage and the Product Hunt launch. Full source list at the end.

## Contents
1. [What Atom is](#1-what-atom-is)
2. [Atom vs Adobe's own AI Assistant](#2-atom-vs-adobes-own-ai-assistant)
3. [Price and licence](#3-price-and-licence)
4. [Set it up in 5 minutes](#4-set-it-up-in-5-minutes)
5. [Which model to pick](#5-which-model-to-pick)
6. [How to prompt it](#6-how-to-prompt-it)
7. [Prompt library](#7-prompt-library)
8. [Skills: teach it your house style](#8-skills-teach-it-your-house-style)
9. [MCP Mode: drive AE from Claude Code, Codex or Cursor](#9-mcp-mode-drive-ae-from-claude-code-codex-or-cursor)
10. [Safety: checkpoints and security modes](#10-safety-checkpoints-and-security-modes)
11. [The best workflow: Atom + Design Mode](#11-the-best-workflow-atom--design-mode)
12. [Atom in Premiere Pro](#12-atom-in-premiere-pro)
13. [17 free Atom-built templates](#13-17-free-atom-built-templates)
14. [Davey's free tools (Motion Dock)](#14-daveys-free-tools-motion-dock)
15. [Best practices checklist](#15-best-practices-checklist)
16. [Sources](#16-sources)

---

## 1. What Atom is

Atom is an AI agent that lives in a panel inside **After Effects** and **Premiere Pro**. You type what you want, it writes and runs the ExtendScript and expressions, and the result appears in your comp as normal, editable layers.

| | |
|---|---|
| **Made by** | Davey ([@daveylovescode](https://x.com/daveylovescode)), also behind Davey Studio on YouTube and the [Motion Dock](https://motionfun.net) |
| **Launched** | Product Hunt, 27 Oct 2025 |
| **Runs on** | Your own **Claude Code**, **Codex** or **OpenCode** subscription. Atom doesn't proxy or resell AI usage, so there are no credits to buy. |
| **Can do** | Scenes and animation from a prompt, rigs and control layers, charts from CSV or PDF, expressions, ExtendScript, custom tool panels, versions, renders, image generation |

**What a "rig" means here.** Davey's term for a control surface: one master layer with a neat custom effect whose sliders and colour pickers drive properties across the whole scene (e.g. *Ring Color*, *Sun Size*). Atom builds these on the fly for everything it makes, so its output is a template you can adjust, not a flat render.

## 2. Atom vs Adobe's own AI Assistant

After Effects 27 (Nov 2026) ships Adobe's built-in AI Assistant. Davey's reply to Adobe's launch: upgrades to Atom stay free for life.

| | **Atom** | **Adobe AI Assistant** |
|---|---|---|
| Billing | Your existing Claude/OpenAI plan | Creative Cloud generative credits |
| Cost predictability | Your plan's normal limits | "No real way to predict" ([Jake In Motion](e02-after-effects-27-updates.md)). One forecast comp used 368 of 4,000 monthly credits. |
| Choice of model | Claude, GPT/Codex, OpenCode providers (Google subscription support in progress) | Adobe's choice |
| Custom skills | Yes, folders of SKILL.md plus .jsx | No |
| Use from outside AE | Yes, MCP Mode | No |
| Premiere Pro | Yes (separate or bundle licence) | Separate Adobe features |
| Price | One-off licence | Included, but credits run out |

**Verdict.** For occasional help the built-in assistant is fine. For daily use, Atom is cheaper and more flexible if you already pay for Claude or ChatGPT. Jake In Motion recommends it on camera with no affiliate deal.

## 3. Price and licence

| Licence | Black Friday | Normal |
|---|---|---|
| After Effects **or** Premiere Pro | **$77** | $99 |
| Both apps | **$111** | $149 |

- Black Friday pricing ends **27 Nov 2026**.
- Every licence includes a **7-day free trial** (no account needed), **lifetime updates**, use on **2 computers**, and a **7-day refund**.
- Atom adds no usage limits of its own. Limits are whatever your AI provider gives you.

## 4. Set it up in 5 minutes

1. Download from [tryatom.ai](https://tryatom.ai/) and install the panel ([installation docs](https://tryatom.ai/docs/getting-started/installation)).
2. Open it in After Effects. Start the **local 7-day trial**, or choose **I have an account**, enter your email and paste the six-digit code.
3. Connect a provider ([setup docs](https://tryatom.ai/docs/getting-started/setup)):

| Provider | Steps |
|---|---|
| **Codex (OpenAI)** | Click **Sign in with OpenAI** → finish in the browser → back to Atom. No CLI install needed, and it reuses an existing Codex setup. |
| **Claude Code** | Follow the [agent setup page](https://tryatom.ai/docs/getting-started/agent-setup); it uses your Claude subscription. |
| **OpenCode** | Choose OpenCode in the model selector → follow the setup card → on macOS install OpenCode and connect a provider in Terminal → **Check again**. Davey is moving OpenCode out of the panel; use it through [MCP Mode](#9-mcp-mode-drive-ae-from-claude-code-codex-or-cursor) instead. |
| **Google (Gemini)** | Not yet. Davey says he found a way to use a Google subscription and expects it in an update soon. |

4. **Save your project**, duplicate the comp you'll work in, and run your [first automation](https://tryatom.ai/docs/getting-started/first-automation).

> **Seat limit.** If both seats are in use, Atom lists your computers. Remove one and click **Use this computer**.

## 5. Which model to pick

From Davey's own replies:

- **Claude Opus 5.5** is the strongest for polished visual work and custom tool UIs: "if you use Atom with Opus 5.5, they absolutely can reach this level".
- **Codex** is strong on function and logic but historically weaker at UI design.
- In his "re-create Vice City in After Effects" benchmark, Fable, Opus and Sol all beat Astra 6.2.
- **Don't expect one-shots for complex builds.** Davey takes 5 to 10 back-and-forths to perfect each of his tools. Atom is tuned for speed, so ask it explicitly to "take a pass and really verify it" when quality matters.
- Use the [thinking modes](https://tryatom.ai/docs/reference/thinking-modes) setting for harder tasks.

## 6. How to prompt it

The [effective prompts guide](https://tryatom.ai/docs/guides/effective-prompts) comes down to five rules:

| Rule | ✗ Weak | ✓ Strong |
|---|---|---|
| **Name layers and comps** | "Animate the logo" | "Animate the **Logo** layer scale from 0% to 100% over 12 frames with ease-in" |
| **Give numbers** | "Make it faster" | "Shorten the intro to 2 seconds and keep the easing" |
| **Set the scope** | "Fix the colours" | "Only in the **Main** comp, change every text layer to #FFFFFF" |
| **Attach data** | "Make a chart of our sales" | "Attach **sales_data.csv** and create an animated bar chart showing quarterly growth" |
| **Say what's wrong** | "Fix it" / "Make it better" | "The bars overlap the title. Move the chart down 80 px and stagger each bar by 3 frames" |

**Attachments** ([docs](https://tryatom.ai/docs/reference/attachments)): CSV, PDF and images. Davey's infographic demo builds animated charts straight from an attached file.

## 7. Prompt library

The first four are verbatim from Atom's docs. The rest are starter prompts written for this guide; swap in your own layer names.

**Rigging and organising**
```text
Create a null called Master Controller with a slider named Intensity and link every layer starting with BG_ to that slider for opacity
```
```text
Build a control layer for this comp with grouped controls for every colour, the main text and the overall speed. Name each control clearly.
```
```text
Organise the project panel: folders for Comps, Precomps, Footage, Audio and Solids. Rename unnamed layers by what they contain.
```

**Animation**
```text
Animate the Logo layer scale from 0% to 100% over 12 frames with ease-in
```
```text
Stagger the entrance of every layer in the Cards comp by 4 frames, sliding up 60 px with an overshoot ease.
```

**Data and infographics**
```text
Attach sales_data.csv and create an animated bar chart showing quarterly growth
```

**Templates for editors**
```text
Turn this comp into a Motion Graphics template: expose the headline, subhead, brand colour and logo in Essential Graphics, with sensible ranges.
```

**Reuse what works**
```text
Create a skill from this animation style
```

**Quality pass**
```text
Take a full verification pass on what you just built: check every expression for errors, every layer for missing sources, and preview the whole comp. Fix anything broken and tell me what you changed.
```

More real examples are in [common workflows](https://tryatom.ai/docs/guides/common-workflows).

## 8. Skills: teach it your house style

A skill is a reusable instruction pack you call with a **/slash command** ([docs](https://tryatom.ai/docs/reference/skills)).

```text
acme-brand/
├── SKILL.md          ← required
├── apply-lower-third.jsx   ← optional script attachments
└── logo-sting.jsx
```

| Scope | Location |
|---|---|
| Global (every project) | `~/Library/Application Support/atom/skills/` |
| Project only | `atom/skills/` next to the project |

**SKILL.md template:**
```markdown
---
name: acme-brand
description: Apply ACME colours, fonts and motion rules to any comp
---

# ACME brand
- Colours: #0B1F3A navy, #FF6B35 orange, #F5F5F5 off-white
- Font: Inter Bold for headlines, Inter Regular for body
- Motion: 8-frame entrances, ease out 80%, no bounce
- Every comp gets a "Controls" layer with brand colour pickers
```

Keep the description around 100 characters (500 max). Docs examples: `acme-brand`, `smooth-reveal`, `wiggle-control`.

**Fastest way to make one:** get an animation right, then prompt *"Create a skill from this animation style."*

## 9. MCP Mode: drive AE from Claude Code, Codex or Cursor

[MCP Mode](https://tryatom.ai/docs/reference/mcp-mode) turns the open Atom panel into a local MCP server, so an external agent can control After Effects.

1. In Atom: **Settings → MCP Mode**.
2. Toggle the client you use: **Claude Code**, **Codex CLI** or **Cursor**.
3. The server runs at `http://127.0.0.1:{port}/mcp`, on your machine only.

Davey says this is "just as powerful" as the panel. It's also the supported route for OpenCode, and a natural fit for longer agent sessions that build on files in your repo.

## 10. Safety: checkpoints and security modes

- **[Checkpoints](https://tryatom.ai/docs/reference/checkpoints):** snapshots before changes, so you can roll back a bad run.
- **[Security modes](https://tryatom.ai/docs/reference/security):** control how freely Atom runs scripts without asking.
- **[Team AI setup](https://tryatom.ai/docs/reference/team-ai-setup):** for studios rolling it out across seats.
- Still **save and duplicate** before big jobs. Checkpoints don't replace a saved file.

## 11. The best workflow: Atom + Design Mode

Davey calls this "an unbelievably powerful After Effects workflow" (20 Nov 2026):

1. **Atom** builds an in-depth scene from your prompt.
2. **[Design Mode](https://jakeinmotion.com)** (Jake In Motion's vector-editing toolkit inside AE) lets you go in and art-direct it by hand.
3. Back to **Atom** to animate your tweaked design.

This keeps the AI on setup and motion and leaves the taste calls to you, the same split Jake recommends for Adobe's assistant.

## 12. Atom in Premiere Pro

Separate licence (or the $111 bundle). Typical jobs:
- Rough cuts from footage and a brief
- Filler-word and silence removal
- Captions
- Reframing for vertical and square formats

## 13. 17 free Atom-built templates

All built by Atom, free to download, **no plugins needed**. Open them to see how Atom structures scenes and rigs. Tap a thumbnail to open its page.

| | | |
|:---:|:---:|:---:|
| [![Sunset Rocket Launch](https://cdn.davey.design/templates/sunset-rocket-launch/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/sunset-rocket-launch)<br><sub>Sunset Rocket Launch</sub> | [![Golden Ratio Logo](https://cdn.davey.design/templates/golden-ratio-logo/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/golden-ratio-logo)<br><sub>Golden Ratio Logo</sub> | [![Chrome Sculpture](https://cdn.davey.design/templates/chrome-sculpture/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/chrome-sculpture)<br><sub>Chrome Sculpture</sub> |
| [![Flight Route](https://cdn.davey.design/templates/flight-route/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/flight-route)<br><sub>Flight Route</sub> | [![Sunlit App Screen](https://cdn.davey.design/templates/sunlit-app-screen/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/sunlit-app-screen)<br><sub>Sunlit App Screen</sub> | [![Neon City](https://cdn.davey.design/templates/neon-city/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/neon-city)<br><sub>Neon City</sub> |
| [![Kinetic Lyric](https://cdn.davey.design/templates/kinetic-lyric/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/kinetic-lyric)<br><sub>Kinetic Lyric</sub> | [![Robot Walk Cycle](https://cdn.davey.design/templates/robot-walk-cycle/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/robot-walk-cycle)<br><sub>Robot Walk Cycle</sub> | [![Lighthouse Storm](https://cdn.davey.design/templates/lighthouse-storm/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/lighthouse-storm)<br><sub>Lighthouse Storm</sub> |
| [![Solar Eclipse](https://cdn.davey.design/templates/solar-eclipse/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/solar-eclipse)<br><sub>Solar Eclipse</sub> | [![Koi Pond](https://cdn.davey.design/templates/koi-pond/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/koi-pond)<br><sub>Koi Pond</sub> | [![Aurora Borealis](https://cdn.davey.design/templates/aurora-borealis/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/aurora-borealis)<br><sub>Aurora Borealis</sub> |
| [![Minecraft Title Sequence](https://cdn.davey.design/templates/minecraft-title-sequence/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/minecraft-title-sequence)<br><sub>Minecraft Title Sequence</sub> | [![Shape Layer Fluid Simulation](https://cdn.davey.design/templates/shape-layer-fluid-simulation/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/shape-layer-fluid-simulation)<br><sub>Shape Layer Fluid Simulation</sub> | [![Mona Lisa Revealed](https://cdn.davey.design/templates/mona-lisa-revealed/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/mona-lisa-revealed)<br><sub>Mona Lisa Revealed</sub> |
| [![Pixel Matrix](https://cdn.davey.design/templates/pixel-matrix/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/pixel-matrix)<br><sub>Pixel Matrix</sub> | [![4D Tesseract Cube](https://cdn.davey.design/templates/4d-tesseract-cube/video-thumb.jpg)](https://tryatom.ai/after-effects-templates/4d-tesseract-cube)<br><sub>4D Tesseract Cube</sub> | |

<sub>The first 15 need After Effects CC 2026 or later. Pixel Matrix and 4D Tesseract Cube work from CC 2025.</sub>

## 14. Davey's free tools (Motion Dock)

Davey is releasing a free After Effects tool every day "until Adobe hires me". They all install together through the **[Motion Dock](https://motionfun.net)**. Recent drops:

| Day | Tool | What it does |
|---|---|---|
| 10 | **Retype** | Font swapper: click a font, pick a new one, and every layer using it changes |
| 11 | **Backdrop** | Puts a box behind any text and keeps it fitted when the copy changes |
| 12 | **Conga** | Lines layers up along a path in one click |
| 13 | Spellchecker | Reads every text layer in the project, precomps included, and fixes typos |
| 14 | Marker copier | Copies markers, which AE can't do natively |
| 15 | **Doohickey** | Pseudo-effect maker: pick properties from anywhere in the comp and get one tidy, grouped control effect |

**Doohickey vs Ditto (in Davey's words):** Ditto copies one layer's effect to many layers or links them to the first. Doohickey builds a new control panel for the whole scene. They work well together.

**Coming next:** a cloner/effector engine, and a more abstract, creative tool called Typhoon.

## 15. Best practices checklist

From the [best practices docs](https://tryatom.ai/docs/guides/best-practices) and Davey's replies:

- [ ] Save the project, then **duplicate the comp** before a big request
- [ ] **Name layers** properly; Atom reads names to find things
- [ ] Check **layer order** and **dependencies** (precomps, expressions) before structural changes
- [ ] Use **scope phrases** ("only in comp X", "only layers starting with BG_")
- [ ] Iterate in small steps; expect 5 to 10 rounds for anything complex
- [ ] Ask for a **verification pass** before you trust a build
- [ ] When something works, **turn it into a skill**
- [ ] Use **Opus 5.5** for visual/UI work, **Codex** for logic-heavy scripting
- [ ] Hit a problem? See [troubleshooting](https://tryatom.ai/docs/guides/troubleshooting) or ask in the [Discord](https://discord.com/invite/jAY6wWr)

## 16. Sources

| Source | Link |
|---|---|
| Official site | [tryatom.ai](https://tryatom.ai/) |
| Docs | [Installation](https://tryatom.ai/docs/getting-started/installation) · [Setup](https://tryatom.ai/docs/getting-started/setup) · [First automation](https://tryatom.ai/docs/getting-started/first-automation) · [Effective prompts](https://tryatom.ai/docs/guides/effective-prompts) · [Common workflows](https://tryatom.ai/docs/guides/common-workflows) · [Best practices](https://tryatom.ai/docs/guides/best-practices) · [Skills](https://tryatom.ai/docs/reference/skills) · [MCP Mode](https://tryatom.ai/docs/reference/mcp-mode) · [Usage limits](https://tryatom.ai/docs/reference/usage-limits) · [Pricing](https://tryatom.ai/docs/reference/pricing) |
| Free templates | [tryatom.ai/after-effects-templates](https://tryatom.ai/after-effects-templates) |
| Developer | [@daveylovescode on X](https://x.com/daveylovescode) · [Motion Dock](https://motionfun.net) · [Discord](https://discord.com/invite/jAY6wWr) |
| Key posts | [Atom + Design Mode workflow](https://x.com/daveylovescode/status/2123850149864915276) · [Opus 5.5 vs Codex advice](https://x.com/daveylovescode/status/2123818921489014860) · [MCP Mode with OpenCode](https://x.com/daveylovescode/status/2123665676334453008) · [Rigs explained](https://x.com/daveylovescode/status/2124919372875731123) · [Doohickey](https://x.com/daveylovescode/status/2124869026429927754) · [Vice City benchmark](https://x.com/daveylovescode/status/2123440146867749180) |
| Independent coverage | [Jake In Motion, AE 27 review](https://www.youtube.com/watch?v=RcNUE6lg3fE&t=163s) · School of Motion feature (Nov 2025) · Product Hunt launch (27 Oct 2025) |
| Alternatives | Adobe's built-in AI Assistant · Sagemode AI · motionvid.ai |
