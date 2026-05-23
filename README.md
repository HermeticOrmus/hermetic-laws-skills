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
