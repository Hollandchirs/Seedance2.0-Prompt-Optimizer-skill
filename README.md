# Seedance 2.0 Video Prompt Skill

[中文](README-zh.md)

An [Agent skill](https://agentskills.io) for generating cinematic, platform-compliant video prompts for [Jimeng Seedance 2.0](https://jimeng.jianying.com/), ByteDance's multimodal AI video generation model. Works with Claude Code, Cursor, Cline, and other compatible agents.

Distilled from **400+ real high-scoring prompts** into 18 production-ready templates across 8 genres. Just describe your idea in one sentence — get a production-grade prompt instantly.

## Why This Skill

| | Without skill | With skill |
|---|---|---|
| Input | Detailed prompt engineering | One sentence of intent |
| Output | Hit-or-miss results | Production-grade prompts |
| Platform pass rate | ~60–70% | **~99%** |
| Copyright handling | Manual | Auto-substituted, visually faithful |
| Restricted words | Triggers blocks | Auto-routed around Seedance's filter list |

## Features

- **One sentence in, production prompt out** — describe your idea casually, get a fully structured SCELA prompt ready to paste
- **~99% platform pass rate** — built-in routing around Seedance's restricted word list; compliant constraints are embedded inline, never appended as visible disclaimers
- **400+ prompts distilled into 18 templates (A–R)** — action/combat, xianxia/fantasy, product ads, short drama, transformation, dance MV, lifestyle vlog, sci-fi/mech
- **SCELA formula** — Subject · Camera · Effect · Light · Audio structured output
- **Copyright-safe substitution** — replaces IPs/celebrities while preserving visual similarity (color palette, costume style, fighting moves)
- **Info-first workflow** — confirms duration (5s/10s/15s) and style before generating; no wasted attempts
- **Language matching** — replies in whatever language the user writes in
- **Clean output** — no trailing "Prohibited:" disclaimers, no unsolicited style tips

## Install

### Option A: Manual copy (recommended)

Clone or download this repository, then copy the skill folder to your Claude skills directory:

```bash
git clone https://github.com/Hollandchirs/seedance2.0.git
cp -r seedance2.0 ~/.claude/skills/seedance-bot
```

### Option B: Via skills CLI

```bash
npx skills add Hollandchirs/seedance2.0
```

Then ask your agent:

> "Create a 10s sci-fi mech battle video prompt"

## Skill Files

| File | Description |
|---|---|
| [SKILL.md](SKILL.md) | Main skill — workflow, SCELA formula, output rules |
| [references/prompt-templates.md](references/prompt-templates.md) | 18 genre templates (A–R) with real high-scoring examples |
| [references/compliance.md](references/compliance.md) | Restricted word routing and copyright substitution rules |
| [references/vocab.md](references/vocab.md) | Camera language, style terms, and audio vocabulary |

## How It Works

1. User describes their video idea in one sentence
2. Skill confirms duration and style (single message, no back-and-forth)
3. Matches the closest of 18 genre templates, distilled from 400+ real prompts
4. Expands using SCELA formula with specific effects, camera moves, and audio
5. Routes around Seedance's restricted word list — compliance embedded inline, never shown to user
6. Outputs a clean, ready-to-paste production-grade prompt

## Sources

Based on official ByteDance documentation:

- [Seedance 2.0 User Manual](https://bytedance.larkoffice.com/wiki/A5RHwWhoBiOnjukIIw6cu5ybnXQ) — Parameters, interaction methods, multimodal capabilities, and example prompts
- [Seedance 2.0 Real-world Cases](https://bytedance.larkoffice.com/wiki/LJXzwehluiFdzKkb1recZdfonZg) — Drama production, e-commerce ads, dance imitation, science education, AI MVs, and more

## License

[MIT](LICENSE)
