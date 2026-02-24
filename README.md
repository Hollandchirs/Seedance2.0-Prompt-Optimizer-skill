# Seedance 2.0 Video Prompt Skill

[中文](README-zh.md)

An [Agent skill](https://agentskills.io) for generating cinematic, platform-compliant video prompts for [Jimeng Seedance 2.0](https://jimeng.jianying.com/), ByteDance's multimodal AI video generation model. Works with Claude Code, Cursor, Cline, and other compatible agents.

Covers smart info collection before generation, 8 genre templates (action, xianxia, product ads, drama, transformation, dance/MV, lifestyle, sci-fi), SCELA formula structuring, copyright-safe character substitution, and @ reference syntax for images/videos/audio.

## Features

- **Info-first workflow** — collects duration (5s/10s/15s) and style before generating, no wasted attempts
- **8 genre templates (A–R)** — action/combat, xianxia/fantasy, product ads, short drama, transformation, dance MV, lifestyle vlog, sci-fi/mech
- **SCELA formula** — Subject · Camera · Effect · Light · Audio structured output
- **Copyright-safe substitution** — replaces IPs/celebrities while preserving visual similarity (color, costume, fighting style)
- **Clean output** — no trailing "Prohibited:" disclaimers, no unsolicited style tips
- **Language matching** — replies in whatever language the user writes in

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
| [references/compliance.md](references/compliance.md) | Copyright substitution rules and restricted content handling |
| [references/vocab.md](references/vocab.md) | Camera language, style terms, and audio vocabulary |

## How It Works

1. User describes their video idea
2. Skill asks for duration and style (one message, no back-and-forth)
3. Matches the closest genre template
4. Expands using SCELA formula with specific effects, camera moves, and audio
5. Checks compliance — replaces any IPs/brands/real people inline
6. Outputs a clean, ready-to-paste prompt

## Sources

Based on official ByteDance documentation:

- [Seedance 2.0 User Manual](https://bytedance.larkoffice.com/wiki/A5RHwWhoBiOnjukIIw6cu5ybnXQ) — Parameters, interaction methods, multimodal capabilities, and example prompts
- [Seedance 2.0 Real-world Cases](https://bytedance.larkoffice.com/wiki/LJXzwehluiFdzKkb1recZdfonZg) — Drama production, e-commerce ads, dance imitation, science education, AI MVs, and more

## License

[MIT](LICENSE)
