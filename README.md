# keep-asking / 追问

> **Don't define "good". Keep asking until "not good enough" reveals itself.**
> **不定义什么是"好"，追问出哪里"不够好"。**

---

## Why

We judge things every day — code, design, writing, decisions. And we struggle with the same question:

**"Is this good?"**

The problem is, "good" has no universal answer. No checklist, no rubric, no set of rules can define it once and for all. Every attempt to define "good" ends up either too vague to use or too rigid to fit new situations.

This project takes a different approach: **instead of defining what "good" looks like, we keep asking what's "not good enough" until nothing is left.** The closer you are to good, the harder it is to articulate why — but the easier it is to find what's still off.

**Keep asking. The answer is in the questions.**

---

## Quick Start

### I have a reference sample

1. **Find a target** — Find 3-5 excellent examples in the same domain. Analyze what makes them good.
2. **Run the funnel** — Ask through 5 layers of questions (logic → goal → comparison → boundary → gut feel).
3. **Stop when nothing's left** — Every layer has a clear stopping signal.

### I have no reference

1. **List non-negotiables** — What must absolutely not be violated?
2. **Find extremes** — What's the worst/best possible outcome?
3. **Build fast feedback** — What's the smallest thing you can ship to get real input?

---

## Core Framework

### Step 0: Find your target first

**Before you start working, find excellent examples. Don't build blind and compare after.**

Many "not good enough" outcomes come not from poor judgment, but from lacking a reference system to begin with.

| Step | Action | Output |
|------|--------|--------|
| ① Search | Find 3-5 well-regarded examples (same domain or analogous structure) | Candidate list |
| ② Analyze | Understand what makes them good — structure, standards, details | Analysis notes |
| ③ Set | Pick your primary target. Not to surpass it — to have a coordinate | Reference benchmark |

**Do this before starting.** It raises your threshold of "good enough" automatically.

- Have direct examples? Use the best one as target.
- No direct examples but analogous structures? Cross-domain reference works.
- Truly nothing to compare? Skip to the [No Reference](#no-reference-scenario) path.

---

### 5-Layer Funnel (with reference)

Ask in order. You don't always need all 5 layers — start where it feels right, but follow the sequence.

#### P0 — Logical Consistency

**Question:** Does this output contradict itself?

| When | What to ask |
|------|-------------|
| Claims relate to each other | "Does this claim contradict an earlier one?" |
| Multiple standards coexist | "Are the criteria used for A and B the same?" |
| Long causal chain | "What premises does this conclusion require? Are they all valid?" |

**Stop when:** Every claim is consistent under the same standard. No "X because Y, but here notY because Z" loops.

---

#### P1 — Goal Alignment

**Question:** Does this actually solve the original problem?

| When | What to ask |
|------|-------------|
| Solution has taken shape | "What problem were we solving? Does this actually solve it?" |
| Multiple goals | "Are these goals in conflict? Which one takes priority and why?" |
| Unclear audience | "Who is this for? What do they care about?" |

**Stop when:** Every major part of the output can clearly answer "which goal does this serve?" No "I added this because it felt right" without a link to a goal.

---

#### P2 — Comparison Coverage

**Question:** What alternatives were excluded, and is the exclusion justified?

| When | What to ask |
|------|-------------|
| A solution was chosen | "Why A over B? What's the exclusion reason for B?" |
| Appears to be the only way | "Is there really only one approach? What did you implicitly rule out?" |
| Clear trade-off | "What did you lose by choosing A? Can you live with that?" |

**Stop when:** Every excluded option has an explicit, repeatable reason. Not "A felt better," but "Because X, Y, Z, A fits better than B for this scenario."

---

#### P3 — Boundary Check

**Question:** Does this hold up under extreme conditions?

| When | What to ask |
|------|-------------|
| Input has limits | "If input is much larger/smaller/messier than expected, what happens?" |
| Assumptions matter | "What assumptions does this rely on? What if they break?" |
| Robustness | "Which part is most likely to fail? Is there a fallback?" |

**Stop when:** You can list 3+ potential failure points, each with either a contingency plan or an explicit "we accept this risk."

---

#### P4 — Gut Feel

**Question:** Strip away all reasoning. Does the result itself feel right?

| When | What to ask |
|------|-------------|
| Aesthetic judgment | "Forget the justification — do you feel comfortable with this?" |
| Vague unease | "Is there something that feels 'off' but you can't articulate why?" |
| Gestalt | "Put it next to excellent peers. Does it stand out as out of place?" |

**Stop when:** Zero residual unease. Note: P4 is the only layer without a logical stopping condition — it relies on your own feeling. If something still feels off, go back to P0-P3 to find the concrete cause.

---

### No-Reference Scenario

**When P2 (comparison) finds nothing to compare against**, switch to this path.

Core shift: from **"compared to what"** to **"what must hold true"**.

#### A — Non-Negotiables

**Question:** What must this output absolutely not violate?

| When | What to ask |
|------|-------------|
| Truly new territory | "If failure is not an option, what conditions must be met?" |
| Unclear constraints | "Which are hard constraints (must not violate) vs soft (can compromise)?" |
| Fuzzy goals | "Even if everything else is bad, what's the one thing we can't get wrong?" |

**Stop when:** You have a list of non-negotiables, each with a clear answer to "what happens if we violate this?"

#### B — Extreme Positioning

**Question:** Between worst and best, where do we stand?

| When | What to ask |
|------|-------------|
| No coordinates | "What's the worst possible outcome? The best, ignoring cost?" |
| Limited resources | "Given current constraints, which point between extremes is most reasonable?" |
| Decision paralysis | "If I lean left vs right, what do I gain/lose?" |

**Stop when:** You can draw a "worst ↔ reasonable ↔ best" axis with your position marked and justified.

#### C — Fast Feedback Loop

**Question:** What does the real world say?

| When | What to ask |
|------|-------------|
| No samples | "What's the smallest verifiable version? Fastest way to get first feedback?" |
| Too many assumptions | "If this assumption is wrong, how quickly can we verify?" |
| Direction unclear | "How many independent feedback signals do we need to confirm direction?" |

**Stop when:** After 2-3 independent feedback signals, you can clearly say "this direction works / this doesn't."

**Order matters:** A → B → C, don't skip.

- **A clears the minefield** — prevents obvious mistakes
- **B finds direction** — avoids wandering aimlessly  
- **C validates with reality** — turns assumptions into facts

If you jump to C without A, you're testing blind — you don't know what you're measuring. If you jump to C without B, your feedback gets anchored to a random starting point.

---

## Interactive Tool

**→ [Try the Keep-Asking Funnel](https://YOUR_USERNAME.github.io/keep-asking)**

A step-by-step web tool that guides you through the funnel:
- Choose your scenario (with/without reference)
- Answer layer-by-layer questions
- Track progress with clear stopping signals
- Export your findings as an improvement checklist

*Built with vanilla HTML/CSS/JS. No dependencies. Zero tracking.*

---

## Use Cases

| Scenario | Suggested Path |
|----------|---------------|
| Code review | P0 (consistency) → P3 (edge cases) → P2 (alternatives) |
| UI/UX design | Pre-find target → P4 (gut feel) → P2 (compare) → P1 (goals) |
| Writing/editing | P1 (audience) → P4 (flow) → P0 (logic) |
| Decision making | Pre-find target → P2 (alternatives) → P3 (risks) |
| New concept (no reference) | A (non-negotiables) → B (extremes) → C (feedback) |

---

## FAQ

**Q: Why not just set rules for what "good" is?**
A: Because quality is context-dependent. Rules that work for one situation fail in another. The funnel adapts to any context.

**Q: This feels like a lot of questions. Do I always need all layers?**
A: No. Pick the layers that match your scenario. A quick code review might only need P0+P3. A major design decision might need all 5 + pre-work.

**Q: What if I don't have 3-5 reference examples?**
A: Use cross-domain examples (similar structure, different field). If truly nothing exists, use the No-Reference path.

**Q: What if P4 (gut feel) says something is wrong but P0-P3 all pass?**
A: Then something is wrong that your logical layers can't capture. Go back and re-examine each layer more carefully. Sometimes the problem is in the assumptions, not the logic.

**Q: Is this for individuals or teams?**
A: Both. Individuals use it as a mental checklist. Teams use it as a structured review format.

---

## License

MIT — see [LICENSE](./LICENSE).

---

## Contributing

Keep-asking is a living methodology. If you have:

- New questioning angles for specific domains (code, design, writing, etc.)
- Real-world examples of the funnel in action
- Improvements to the web tool
- Translations

Open an issue or PR. See [CONTRIBUTING](./CONTRIBUTING.md) for guidelines.
