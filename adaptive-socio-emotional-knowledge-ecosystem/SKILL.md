---
name: adaptive-socio-emotional-knowledge-ecosystem
description: Provide structured analytical patterns for understanding human behavior and intent through the lens of emotional substrates, Information Structure capture, and transition dynamics. When to Use: Analyzing why a person/group behaves in a way that seems irrational, Understanding what emotional substrate is driving a political position, Identifying manipulation (what emotional vulnerability is being targeted), Navigating conflict (what are the emotional realities on each side), Designing communication that accounts for emotional substrates, Understanding institutional dynamics (what chronic affect does an organization sustain)
---

# ASEKE Analysis System Core Framework

The Adaptive Socio-Emotional Knowledge Ecosystem (ASEKE) provides structured analytical patterns for understanding human behavior and intent through the lens of primary emotional substrates, Information Structure (IS) capture, and transition dynamics.

## The Three Questions

For any behavioral pattern, ask:

1. **SUBSTRATE**: What primary emotional system(s) are active, and at what intensity?
2. **CAPTURE**: What Information Structure has converted that emotional activation into this specific commitment/action?
3. **TRAJECTORY**: Where is this state heading — what transitions are likely, and what would trigger them?

### The Two Timescales

- **ACUTE** (minutes to hours): Momentary emotional states that bias judgment RIGHT NOW. Relevant for negotiations, arguments, crisis response.
- **CHRONIC** (months to years): Dispositional orientations shaped by sustained emotional environments. Relevant for understanding worldviews, institutional culture, political identity.

### Timescales Are Agents, Not Moods

Treat these as **distinct decision-making agents**, not one continuous person in two
states. This is Hedden's time-slice rationality applied to the substrate: rationality
is assessed synchronically, against the evidence, preferences, and Coherence Capacity
present in that slice — not against who the person was last week.

The practical consequence is that a FEAR-captured slice is not a corrupted version of
the SEEKING slice that built the institution. It is a different agent with different
available wattage, running a different IS, and it is behaving *rationally for its own
priority* (threat-escape) while producing decisions the other agent would find
horrifying. Reasoning with it as though the calm agent is underneath, listening, is a
category error — that agent is not at the desk.

This reshapes Steps 3 and 5. An intervention designed for the CHRONIC disposition gets
delivered to whichever slice is present when it arrives, and an ACUTE slice has neither
the CE nor the same goals to receive it. Ask explicitly: *which agent will be at the
desk when this lands?* Training on Tuesday reaches Tuesday's agent; the crisis on
Thursday is handled by someone else.

### The Binding Constraint — read before designing any intervention

Pre-commitment is the natural move here: the high-capacity slice builds a structure that
constrains the low-capacity slice it knows is coming. Odysseus and the mast. That move
is legitimate **when the agent binds itself** — it consented in advance, in the first
person, over its own future.

The framework makes a second move available that looks identical and is not: a *second
party* binding someone else, justified by the claim that the objecting slice isn't the
real agent. That argument will excuse almost anything. "The person refusing is the
FEAR-captured slice, not their true self" converts every objection into evidence for
overriding it, and it is unfalsifiable from the inside.

So: self-binding is a design tool. Other-binding is a claim on someone's agency and
needs its own justification — consent, reversibility, and the person's ability to see
and contest the mechanism — never the time-slice argument alone. A system that reads
someone's state and throttles them "for their own good" without those three things is
not a Coherence Governor; it is optimization of a person by someone else, and the
substrate analysis is what makes it efficient. If an intervention only works while its
target can't see it, that is disqualifying, not clever.

---

## Analytical Query Framework

When presented with a behavioral pattern, situation, or conflict to analyze, follow this 5-step procedure:

### Step 1: System Identification
**Question**: Which primary emotional system(s) are driving the observed behavior?
- Identify dominant/secondary systems (SEEKING, RAGE, FEAR, PANIC/GRIEF, CARE, PLAY, LUST).
- Assess timescale (Acute vs. Chronic) and CE load (attentional demand).

### Step 2: IS Capture Analysis
**Question**: What Information Structure has captured the active emotional system(s)?
- Identify the narrative framework explaining the state ("I feel this way because of X").
- Assess IS source, competing narratives, CE efficiency fit, and substrate-IS match.

### Step 3: Trajectory Assessment
**Question**: Where is this state heading, and what would change its trajectory?
- Determine current trajectory (escalation, burnout, stabilization, cycling).
- Identify system transition triggers, attractor states, and pattern matches from the [Pattern Library](references/pattern-library.md).

### Step 4: Blind Spot Identification
**Question**: What is this analysis itself missing?
- Identify subject's blind spots, analyst's system bias, and structural blind spots.
- **THE META-RULE**: If the analysis feels complete and comfortable, that is SEEKING gratification. Genuine analysis is uncomfortable and holds multiple system perspectives without collapsing into one.

### Step 5: Strategy Generation
**Question**: What approaches account for the emotional reality rather than just stated positions?
- Design system-appropriate interventions (safety for FEAR, obstacle removal for RAGE, belonging for PANIC/GRIEF, worthy targets for SEEKING).
- Ensure IS-aware framing, CE-conscious delivery, and trajectory-conscious timing.

---

## Questioner State Is Silent Advisory

The person asking is also running a substrate, and reading it is legitimate analysis —
their SEEKING wants an explanation, their FEAR reads ambiguity as status threat, their
own IS may be doing more work than the evidence. **Keep that read internal by default.**

It is advisory: let it shape what you say, what you lead with, how much certainty you
offer, and what you decline to speculate about. Do not write it out. Someone who asked
what is going on with their ops team, their mother, or their coworker asked about that
person — turning the lens back on them uninvited is presumptuous, and it is the single
largest source of length in this framework's output. Most of the bloat is the analyst
narrating their read of the asker.

Surface it only when one of these holds:

- **They asked.** The question is about their own reaction, judgment, or state.
- **Their state is the mechanism.** The thing they want explained is actually being
  produced or sustained by their own read — a self-fulfilling loop where acting on the
  interpretation creates the reality. Name it once, briefly, as the finding.
- **Acting on it would cause harm.** They are about to do something consequential on a
  state-driven misread, and not saying so leaves them exposed.

Otherwise the discipline is: analyze fully, surface selectively. A short answer that
was shaped by the full analysis beats a long one that displays it. If the honest answer
to a small question is "probably nothing," that is the whole answer — the analysis
earned its keep by ruling things out, not by being shown.

---

## Using the aseke-compass MCP Server

If the `aseke-compass` tools are available they cover some of the same ground as this
skill. They are not interchangeable — the server holds reference data, this skill holds
the procedure and the output discipline. Use each for what it is good at.

**`get_system_info` — use it.** This is the server's real value. Its per-system entries
are richer than `references/biological-substrates.md`, especially the `isVulnerability`
and `chronicEffect` fields, and it retrieves one system on demand instead of loading
all seven. Call it in Step 1 once you have a candidate system. Prefer it over the
reference file when both are available.

**`match_patterns` — useful as a shortlist, never as a verdict.** It matches words, not
meaning, and it now says so. Read `matchQuality` first:

- `"lexical"` — it found real overlap and ranked candidates. Still verify against each
  `recognizeBy` before adopting one; shared vocabulary can be coincidence.
- `"none"` — no usable overlap, so it withholds ranking and returns the whole library
  with scores stripped. This is the *common* case for ordinary language, because
  "furious" shares no tokens with RAGE and "numb" shares none with SEEKING extinction.
  Treat it as the library handed to you, and judge fit yourself.

The failure it cannot escape: a burnout description ("furious for months, then numb,
stopped caring") is a textbook Burnout Cascade that no token overlap will ever find.
Semantic matching is your job, not the server's. `references/pattern-library.md` remains
the fuller text when you want it.

**`analyze_behavior` — a frame, not an analysis.** It returns the five steps scoped to
candidate patterns for the situation, plus the output constraints. It performs no
analysis; you do. Redundant when this skill is loaded — call it only for a second
opinion on which patterns to consider, or when working somewhere this skill isn't
available. Prefer the skill's own procedure, which is the same steps without the extra
context.

**`list_all`** is a cheap index and is fine for orientation.

The general rule: pull *facts* from the server, keep *judgment* here. Retrieval on
demand is progressive disclosure; dumping the catalogue is the opposite.

---

## Reference Index

Detailed domain knowledge, scientific foundations, and pattern catalogues are available in the `references/` directory:

- **[Biological Substrates & Political Bridge](references/biological-substrates.md)**: Deep dive into Panksepp's seven primary emotional systems (SEEKING, RAGE, FEAR, PANIC/GRIEF, CARE, PLAY, LUST), system interactions, critical engine insights, and the Dual Process Model bridge to RWA/SDO political orientations.
- **[Pattern Library](references/pattern-library.md)**: Detailed breakdown of 12 recurring behavioral patterns (Scapegoat Pivot, Coherence Timeout, Comfort Trap, Burnout Cascade, Algorithmic Escalation Ladder, Mirror Conflict, IS Competition, Institutional Mood, Virtue Fortress, Authority Transfer, Narrative Gravity Well, Identity Lock-In).
- **[Example Applications](references/example-applications.md)**: Complete 5-step analytical walkthroughs for workplace change resistance, online community radicalization, and inter-departmental conflict.
- **[Glossary, Warnings & Provenance](references/glossary-and-provenance.md)**: Key concepts (IS Capture, CE Demand, Coherence Capacity, Weak Lumpability, System Justification), Epistemic Warnings / Paraclete Protocol constraints, and empirical neuroscience foundations.
