# Examples

Each principle applied to a real engineering scenario.

---

## 1. Mentalism — the mental model precedes the code

**Scenario**: You inherit an authentication system. The code works but reading it produces no clear understanding of how. Comments say "DO NOT TOUCH" in several places. Every change breaks something distant.

**Without Mentalism**: keep patching. Each patch adds entropy. Eventually a refactor becomes necessary at the worst possible time.

**With Mentalism**:
1. Stop coding. Write one sentence describing what the auth system does (e.g., "exchanges credentials for a session token, validates that token on every request, refreshes it before expiry").
2. List the 5-7 entities (Credential, Session, Token, RefreshToken, User, Permission).
3. Map relationships (Credential → Session via login, Session contains Token + RefreshToken, Token → User via lookup, User → Permission via role).
4. Compare to the actual code. Note the mismatches.
5. The mismatches are the bug surface. Fix them one at a time, model-first.

The model usually takes 30 minutes. It saves weeks.

---

## 2. Correspondence — patterns flow through levels

**Scenario**: Your backend has Orders. Your frontend has "Purchases." Your database has `transactions`. New developers spend their first week confused about which is which.

**Without Correspondence**: each layer's vocabulary calcifies. Documentation contradicts code. Bug reports use different words than the code.

**With Correspondence**:
1. Identify all levels (domain → API → UI → DB).
2. Pick the canonical name at the highest level. "Order" is the business term used in customer conversations.
3. Audit each level: is it called "Order" everywhere?
4. Where it isn't, rename. Be ruthless. Two weeks of refactoring pays back over years of clarity.
5. Document the canonical name as a project decision.

Same pattern applies to: HTTP status codes that don't match domain semantics; database schemas that diverged from the entity model; URLs that reflect the file structure instead of the resource.

---

## 3. Vibration — ship to learn

**Scenario**: A team has been "designing the architecture" for three months. Nothing has shipped. Every design review surfaces new requirements that change the design. Velocity is zero.

**Without Vibration**: another design review. Then another. Eventually the team realizes the architecture doesn't matter as much as they thought.

**With Vibration**:
1. Define the smallest possible shippable unit. Not the "MVP" — the *minimum viable thing that runs in production for real users*.
2. Ship it in a week. Worst code you've ever written. Doesn't matter.
3. Observe what actually breaks. What users do. What the team learns.
4. Iterate.
5. The first version is wrong. That's fine — the second version is informed by reality, not whiteboards.

The momentum compounds. Each shipped iteration produces more signal than another design review.

---

## 4. Polarity — both poles are necessary

**Scenario**: The team debates: monolith or microservices? Half want monolith for simplicity. Half want microservices for scaling. The debate consumes a quarter.

**Without Polarity**: someone wins by exhaustion. The losing half is bitter; the winning half implements with the energy of revenge rather than conviction. The architecture has emotional baggage forever.

**With Polarity**:
1. Name both poles explicitly: simplicity vs. scalability.
2. Identify which pole serves the current goal. (Probably simplicity — you're not at scale yet.)
3. Acknowledge the cost of the other pole. (Microservices later will be expensive.)
4. Commit to monolith *for now* with a stated trigger condition for revisiting (e.g., "when we hit 10× current load, or when the codebase exceeds 100k LOC, or when we have 5+ teams contributing concurrently").
5. The team agrees because the decision isn't permanent — it's calibrated to the current pole.

Same pattern: tabs vs. spaces (within a project, pick one — across projects, doesn't matter). REST vs. GraphQL. SQL vs. NoSQL. Strict typing vs. dynamic.

---

## 5. Rhythm — phases are real

**Scenario**: You've been shipping features at high tempo for 4 months. Quality is degrading. Bugs are piling up. The team is exhausted but doesn't feel they can stop.

**Without Rhythm**: enforce the tempo. Burn out the team. Quality collapses. Six months from now, mass exodus.

**With Rhythm**:
1. Notice the current phase. The team is in feature-spike phase; the codebase is asking for maintenance phase.
2. Don't fight it. Schedule a 2-3 week explicit maintenance sprint.
3. During maintenance: pay down tech debt, fix latent bugs, refactor the painful areas, update dependencies, write the documentation that was skipped.
4. Plan the next feature spike before the maintenance ends — so the team has something to be excited about next.
5. Maintain the rhythm: feature spike → maintenance → feature spike. Both phases are productive; both are needed.

Same applies to individual work weeks: don't try to be productive every hour. Match the rhythm of the day.

---

## 6. Cause and Effect — find the cause, fix the cause

**Scenario**: A production bug appeared. You fixed it. A week later, the same class of bug appears in a different module. A week after that, again.

**Without Cause and Effect**: keep patching. Each patch makes the code more defensive in one place. The actual cause (a flawed pattern, a misunderstood library, a wrong abstraction) keeps producing new symptoms.

**With Cause and Effect**:
1. Notice that the bug is recurring, not new. This is the signal.
2. Trace each instance upstream. What was the immediate cause?
3. Look for what the instances have in common. A shared library? A copied pattern? A misunderstood API?
4. Fix the common cause. (Refactor the library. Rewrite the pattern. Document the API correctly.)
5. The downstream symptoms stop appearing.

Same applies to: recurring deploys that fail (root cause: CI is misconfigured, not "deploys are hard"); incidents that look different but trace to the same dependency; user complaints that vary in surface but share a theme.

---

## 7. Gender — both generative and receptive are needed

**Scenario**: You build a beautiful API. It's expressive, well-typed, well-documented. Nobody uses it. The team that consumes it complains it doesn't fit their workflow.

**Without Gender**: keep refining the API. Make it more expressive. More well-typed. Still nobody uses it.

**With Gender**:
1. Notice: the API is generative (produces interfaces) but not receptive (doesn't take feedback from consumers).
2. Identify the receptive channel. Is there one? Where do consumers report friction?
3. If no channel exists, build it: open a feedback issue tracker, schedule monthly consumer interviews, run usability tests.
4. Receive the feedback. Then change the API in response.
5. The pair (generative output ↔ receptive input) is now balanced. The system is alive.

Same applies to: a logging system that emits but isn't queried; a metrics dashboard that's built but never looked at; a documentation site that ships but doesn't accept PRs.

---

## How these compound

A single decision might benefit from one principle. Most decisions benefit from two or three.

**Example**: redesigning an API.

- **Mentalism**: What does this API actually do? One-sentence.
- **Correspondence**: Do the endpoint names match the domain entities? The database table names? The UI labels?
- **Polarity**: REST vs. GraphQL. Which pole serves the current consumer set?
- **Gender**: How do consumers feed back what they need from this API?

Four principles applied to one decision. Each one sharpened a different angle.

## How NOT to use these

- **Quoting them at colleagues** to win arguments. They're for thinking, not rhetorical authority.
- **Treating them as superstition**. They're framings, not mystical truths.
- **Applying all seven to every decision**. Overkill. Pick the ones that fit.
- **Ignoring them when convenient**. They work because they describe real properties of systems. The discomfort of applying them when convenient is the signal that they're working.

## Further reading

- [The Kybalion](https://en.wikisource.org/wiki/The_Kybalion) — the 1908 source text, public domain. Short. Worth reading once.
- [Hermetic Academy](https://github.com/HermeticOrmus/hermetic-academy) — interactive webapp teaching the seven principles with examples
- [Designing Data-Intensive Applications (Kleppmann)](https://dataintensive.net/) — engineering applies many of the same principles under different names; this book makes them explicit
- [The Pragmatic Programmer (Hunt & Thomas)](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/) — engineering aphorisms that overlap heavily with the Hermetic framings
