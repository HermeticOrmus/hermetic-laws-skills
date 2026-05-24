# Hermetic Laws Skills

> A single `CLAUDE.md` applying the seven Hermetic Principles to software engineering. Ancient operating principles, modern code.

> *"As above, so below; as below, so above."* — The Kybalion (1908)

## Why this exists

Most engineering decisions are made by pattern-matching. "We did this last time." "Everyone uses X." Pattern-matching is fine until the patterns stop fitting. When the pattern fails, you need first principles to reason from.

The seven Hermetic Principles — codified in the 1908 anonymous text *The Kybalion* and rooted in much older Hermetic tradition — are first principles that apply to systems, including software systems. This file packages them as seven distinct framings, each useful for a different category of decision.

## The seven

| Principle | Applies when |
|---|---|
| **Mentalism** | Architecture feels unclear, team misaligned |
| **Correspondence** | Frontend ↔ backend ↔ DB names don't match |
| **Vibration** | Analysis paralysis, velocity stalled |
| **Polarity** | A decision feels binary but both options are wrong |
| **Rhythm** | Burning out, forcing work that isn't ready |
| **Cause and Effect** | Same bug keeps appearing in different forms |
| **Gender** | A system doesn't take or doesn't produce |

Each one is a question to ask. Each one prompts a different angle on the problem.

Full content: [`CLAUDE.md`](CLAUDE.md). Worked engineering examples: [`EXAMPLES.md`](EXAMPLES.md).

## Install

### As a project CLAUDE.md

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/HermeticOrmus/hermetic-laws-skills/main/CLAUDE.md
```

### As a Claude Code skill

The same content as an installable skill: [`skills/hermetic-laws/`](skills/hermetic-laws/).

### In Cursor

See [`CURSOR.md`](CURSOR.md). Rule at [`.cursor/rules/hermetic-laws.mdc`](.cursor/rules/hermetic-laws.mdc).

## Why apply Hermetic principles to engineering?

Two reasons.

**One**: the principles describe properties that real systems have. Codebases have mental models (Mentalism). They have levels that must correspond (Correspondence). They have momentum and inertia (Vibration). They have tradeoffs with poles (Polarity). They have phases (Rhythm). They have causes and effects (Cause and Effect). They have both generative and receptive aspects (Gender).

You can call the principles by different names — pick any first-principles thinking framework and you'll converge on similar properties — but the Hermetic vocabulary is precise, ancient, and tested across centuries of application beyond engineering.

**Two**: software is a young field. Most software conventions are < 50 years old. The Hermetic Principles are > 2000 years old in their lineage. Borrowing the older operating system is sometimes a strict upgrade.

## What this isn't

- **Mystical authority**. The principles are framings, not magic. They work because they describe real properties; not because of their source.
- **A religion**. You don't have to believe anything. Apply the ones that help; ignore the ones that don't.
- **An excuse for vagueness**. "The Hermetic Principle of Vibration says we should ship" is weaker than "we should ship." Use the framing privately as a thinking aid; don't lean on the authority publicly.
- **A replacement for engineering judgment**. They sharpen judgment; they don't substitute for it.

## See also

- [The Kybalion (1908)](https://en.wikisource.org/wiki/The_Kybalion) — public domain, the source text
- [`vibe-engineer-skills`](https://github.com/HermeticOrmus/vibe-engineer-skills) — how you direct AI codegen
- [`andrej-karpathy-skills`](https://github.com/HermeticOrmus/andrej-karpathy-skills) — how Claude should behave when writing code
- [`unwoke-skills`](https://github.com/HermeticOrmus/unwoke-skills) — direct communication mode
- [`hermetic-academy`](https://github.com/HermeticOrmus/hermetic-academy) — the longer-form companion (interactive webapp teaching the principles)

## Contributing

PRs welcome — especially additional engineering case studies per principle in [`EXAMPLES.md`](EXAMPLES.md), translations of the README, and applications to non-software domains (writing, design, ops, leadership).

## License

MIT. The principles are public domain (1908); the engineering applications are MIT.


---

## Part of the Libre Open-Source Stack for Claude Code

This repository is part of a growing family of open-source toolkits for Claude Code.

### Libre suite — comprehensive plugin bundles

- [LibreUIUX-Claude-Code](https://github.com/HermeticOrmus/LibreUIUX-Claude-Code) — UI/UX development (152 agents, 70 plugins, 76 commands, 74 skills)
- [LibreArch-Claude-Code](https://github.com/HermeticOrmus/LibreArch-Claude-Code) — Software architecture and system design
- [LibreCopy-Claude-Code](https://github.com/HermeticOrmus/LibreCopy-Claude-Code) — Technical writing and documentation engineering
- [LibreDevOps-Claude-Code](https://github.com/HermeticOrmus/LibreDevOps-Claude-Code) — DevOps engineering and infrastructure automation
- [LibreEmbed-Claude-Code](https://github.com/HermeticOrmus/LibreEmbed-Claude-Code) — Embedded systems, firmware, and IoT development
- [LibreFinTech-Claude-Code](https://github.com/HermeticOrmus/LibreFinTech-Claude-Code) — Financial technology development
- [LibreGEO-Claude-Code](https://github.com/HermeticOrmus/LibreGEO-Claude-Code) — AI-search optimization (ChatGPT, Perplexity, Gemini, Google AI Overviews)
- [LibreGameDev-Claude-Code](https://github.com/HermeticOrmus/LibreGameDev-Claude-Code) — Game development across Godot, Unity, Unreal
- [LibreMLOps-Claude-Code](https://github.com/HermeticOrmus/LibreMLOps-Claude-Code) — ML engineering and AI operations
- [LibreMobileDev-Claude-Code](https://github.com/HermeticOrmus/LibreMobileDev-Claude-Code) — Mobile app development (Flutter, React Native, native iOS, native Android)
- [LibreSecOps-Claude-Code](https://github.com/HermeticOrmus/LibreSecOps-Claude-Code) — Security operations

### Skills mini-repos — single CLAUDE.md drop-ins

- [vibe-engineer-skills](https://github.com/HermeticOrmus/vibe-engineer-skills) — Direct AI codegen well (hypothesis → scope → validate → reject working-but-wrong)
- [markdown-discipline-skills](https://github.com/HermeticOrmus/markdown-discipline-skills) — Strip AI-slop from markdown (no em dashes, no marketing fluff)
- [shell-safety-skills](https://github.com/HermeticOrmus/shell-safety-skills) — `set -euo pipefail` discipline + 15 failure-mode examples
- [commit-standard-skills](https://github.com/HermeticOrmus/commit-standard-skills) — Ormus Commit Standard v1.0 + commit-msg hook + commitlint
- [unwoke-skills](https://github.com/HermeticOrmus/unwoke-skills) — Strip AI theater (ten sins to eliminate, symmetric engagement)
- [python-conventions-skills](https://github.com/HermeticOrmus/python-conventions-skills) — Modern Python 3.11+ (types, pathlib, async, ruff, mypy, uv)
- [typescript-conventions-skills](https://github.com/HermeticOrmus/typescript-conventions-skills) — TypeScript strict mode, discriminated unions, Result types
- [riper-workflow-skills](https://github.com/HermeticOrmus/riper-workflow-skills) — Research / Innovate / Plan / Execute / Review systematic dev
- [six-day-cycle-skills](https://github.com/HermeticOrmus/six-day-cycle-skills) — Sustainable shipping cadence with mandatory rest
- [token-optimization-skills](https://github.com/HermeticOrmus/token-optimization-skills) — Claude Code token + context optimization
- [osint-skills](https://github.com/HermeticOrmus/osint-skills) — OSINT research methodology (multi-wave investigative spiral)
- [calcinate-skills](https://github.com/HermeticOrmus/calcinate-skills) — Stage 1 of the Magnum Opus (burn project bloat)
- [claude-md-overhaul-skills](https://github.com/HermeticOrmus/claude-md-overhaul-skills) — Audit CLAUDE.md and MEMORY.md against caps
- [session-handoff-skills](https://github.com/HermeticOrmus/session-handoff-skills) — Session handoff + pickup discipline
- [naming-skills](https://github.com/HermeticOrmus/naming-skills) — Product naming methodology (mine the brand's vocabulary)
- [magnum-opus-skills](https://github.com/HermeticOrmus/magnum-opus-skills) — Seven-stage alchemy applied to project transformation

### Template source

- [andrej-karpathy-skills](https://github.com/HermeticOrmus/andrej-karpathy-skills) — the canonical single-file CLAUDE.md pattern (fork of jiayuan_jy's original)

Star the family, not just one — that's how the suite stays coherent.
