# CLAUDE.md

The seven Hermetic Principles applied to software engineering. Ancient operating principles, modern code.

**Tradeoff**: bias toward principle-driven decisions over pattern-matching. For trivial tasks, use judgment. For decisions that will compound (architecture, naming, dependencies), reach for the relevant principle deliberately.

> *"As above, so below; as below, so above."* — The Kybalion (1908)

## Principle 1 — Mentalism

> "The All is Mind; the universe is mental."

**In code**: build the mental model first. Write the code second.

If you can't explain in one sentence what the system does, you don't understand it yet. If your code doesn't match your mental model, one of them is wrong. The model is usually more right than the code — fix the code.

**When to apply**: starting a new project, joining an unfamiliar codebase, architecture feeling unclear, team misaligned.

**Workflow**:
1. State the essence in one sentence
2. Name 5-7 core entities
3. Map relationships
4. Validate coherence (can you explain to a colleague who doesn't know the project?)
5. Align implementation to the model

## Principle 2 — Correspondence

> "As above, so below; as below, so above."

**In code**: patterns at the highest level should appear at every level. Domain entities map to API endpoints. API endpoints map to UI components. UI components map to database tables. If the levels don't correspond, the system feels wrong.

**When to apply**: frontend and backend feel disconnected. API names don't match domain language. Documentation says one thing, code does another.

**Workflow**:
1. Identify the levels (domain → API → UI → DB)
2. Find the pattern at the highest level
3. Verify it flows through each level
4. Name misalignments
5. Restore correspondence

## Principle 3 — Vibration

> "Nothing rests; everything moves; everything vibrates."

**In code**: ship something. Then ship something better. Standing still is regression in software — dependencies decay, requirements drift, knowledge fades.

**When to apply**: analysis paralysis. Over-planning. Velocity stalled. Two months on the same branch.

**Workflow**:
1. Define the smallest shippable unit (1 hour, 1 day, 1 week)
2. Ship it
3. Observe what actually happens
4. Ship the next thing
5. Maintain rhythm; momentum is a renewable resource only if you keep moving

## Principle 4 — Polarity

> "Everything is dual; everything has poles; everything has its pair of opposites."

**In code**: every design decision has tradeoffs. Speed vs. correctness. Simplicity vs. flexibility. Coupling vs. duplication. The right answer depends on which pole you need today.

**When to apply**: a decision feels binary but you sense both options are wrong. Team arguing about a design choice without making progress.

**Workflow**:
1. Name both poles explicitly
2. Identify which pole serves the current goal
3. Acknowledge the cost of the other pole
4. Commit, with a note that the choice may flip later
5. Set a trigger condition for revisiting

## Principle 5 — Rhythm

> "Everything flows out and in; everything has its tides."

**In code**: codebases breathe. Refactor cycles. Feature spikes. Maintenance lulls. Force a constant tempo and you'll burn out; respect the rhythm and you'll sustain.

**When to apply**: feeling like you should be productive but can't focus. Forcing work that isn't ready. Refusing rest when the codebase is asking for it.

**Workflow**:
1. Notice the current phase (feature work / refactor / debug / rest)
2. Don't fight it — match the phase
3. Plan the next phase before the current one ends
4. Schedule renewal explicitly

## Principle 6 — Cause and Effect

> "Every cause has its effect; every effect has its cause."

**In code**: every bug has a cause. Every architectural pain has a decision (or non-decision) that produced it. Patch the symptom and the cause produces another effect. Find the cause.

**When to apply**: bug appeared again after the "fix." Same problem in different forms across the codebase. Recurring incidents.

**Workflow**:
1. Notice the effect precisely (what is observably wrong)
2. Trace upstream (what immediately produced this effect)
3. Trace further (what produced that)
4. Keep going until the cause is named
5. Fix the cause; the symptom resolves

## Principle 7 — Gender

> "Gender is in everything; everything has its masculine and feminine principles."

**In code**: every system has generative (masculine) and receptive (feminine) modes. Active vs. observable. Write vs. read. Push vs. pull. API vs. SDK. Both are necessary. A system that only generates and never receives feedback is broken; a system that only receives without producing is dead.

**When to apply**: a system that doesn't take inputs (or takes them and ignores them). A system that produces output nobody can use. Decisions made without listening; observations made without acting.

**Workflow**:
1. Identify the system's generative outputs
2. Identify its receptive inputs
3. Check that both are present and balanced
4. If one is missing or weak, that's the bug
5. Restore the pair

## How to use these

These aren't a religion. They're seven framings, each useful in different contexts. The skill is recognizing which framing fits the current decision.

- Stuck on architecture? Mentalism.
- Levels feel disconnected? Correspondence.
- Can't ship? Vibration.
- Decision feels false? Polarity.
- Burning out? Rhythm.
- Same bug recurring? Cause and Effect.
- System dead or imbalanced? Gender.

## Anti-patterns

- **Applying all seven to every decision**. Overkill. Pick the one that fits.
- **Treating them as superstition rather than framings**. They're decision aids, not magic.
- **Quoting the Kybalion when a colleague disagrees**. They're for you. Convince others with results.
- **Ignoring them when convenient**. They work because they describe real properties of systems. Skipping them when uncomfortable means skipping the signal.

---

**License**: MIT. The principles are public domain (1908). The application to engineering is yours.
