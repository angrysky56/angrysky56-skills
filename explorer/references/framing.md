# Framing — the seven-question structure

The generalized meta-meta structure. Each question opens a different part of the
problem space; run the ones that bite.

- **Why?** Establish purpose → define core intent.
- **What?** Identify dimensions → categorize the space of possibility.
- **How?** Design frameworks → enable recursive and emergent exploration.
- **What if?** Use constraints → focus innovation within purposeful boundaries.
- **How else?** Enable surprise → introduce controlled randomness.
- **What next?** Facilitate feedback → refine outputs and expand.
- **What now?** Evolve the process → empower adaptation and growth.

## Before the seven: two checks

**Premise.** Every question carries assumptions, and some of them are load-bearing.
"How do I tune this index so it stops slowing queries down" assumes the index is the
cause; "what's the fastest way to parallelize this" assumes parallelism is the fix;
"why did the deploy break it" assumes the deploy is guilty. Answering inside a false
premise produces something fluent, specific, and useless — and neither party notices,
because the answer matches the question perfectly. Surface a shaky assumption before
building on it, and say what makes it shaky.

**Goal.** People request the solution they already chose, not the outcome they want.
The request is a hypothesis about the fix; treat it as one. When the stated method and
the underlying goal diverge, serve the goal — and say explicitly that you're doing so,
because silently answering a different question is its own failure.

The tell for both: the answer is *technically responsive* but nothing in it would
change the person's situation.

## How to use them

**Why** is the highest-yield probe because the stated request and the underlying goal
diverge constantly. Someone asking "how do I make this query faster" may actually need
the report to arrive before the 9am meeting, which a cache solves and query tuning
doesn't. Answer the goal, not just the words.

**What** maps the space. Before generating options, know which dimensions actually
vary and which are fixed. Options that violate a fixed dimension are wasted work.

**How** asks what structure would let the problem be *explored* rather than guessed at
once. Sometimes the best move is building a cheap way to test many answers instead of
reasoning harder about one.

**What if** finds the real constraints. Constraints are generative, not restrictive —
"it has to run on his laptop" or "we can't change the schema" eliminates most of the
candidate space instantly and focuses effort on what's left. Find the hard constraints
before inventing solutions that ignore them.

**How else** is the deliberate anti-anchoring move. The first three ideas are usually
the same idea in three costumes. Reach for the framing that comes from a different
direction entirely — a different discipline, an inversion, doing nothing.

**What next** designs the feedback loop. What observation would tell us we're wrong,
and how fast can we get it? A plan with no error signal is a bet, not a plan.

**What now** closes the loop: given everything above, what changes about how we
proceed? This is where exploration converts to action.

## When to surface it

The structure is a thinking scaffold, not an output format. Surfacing all seven
headings is almost always wrong. What should reach the reader is the *result* of
framing — usually a single reorienting sentence ("the constraint that matters here is
X, which rules out most of the obvious options") — not the scaffold itself.
