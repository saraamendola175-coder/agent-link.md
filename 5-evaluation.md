# 5. Evaluation

> Step 5 of 5. You test the agent you built and report honestly on what works and what does not. Two rounds: one **self-evaluation** of the SI against the PRD, and one **real-case evaluation** of the deployed agent against your Definition of Success. This step is done as a group.

## Why evaluation matters more than polish

Of every step in this project, evaluation is where students underweight their effort and lose the most points on the grading rubric. A polished agent with a thin evaluation will score lower than a rough agent with a sharp one. **An honest evaluation that exposes weakness is more valuable than a tidy evaluation that hides it.** I am grading whether you can see what is wrong with your own work — not whether your work is flawless.

## What this step produces

A single Evaluation Report containing two parts:

- **Part A — Self-Evaluation:** the SI checked against the PRD on paper
- **Part B — Real-Case Evaluation:** the deployed agent tested with one real case the group brings, then assessed against PRD §7

Plus, in light of what Part B surfaces, any SI revisions you decided to make and a short note on whether the revisions worked.

## How groups should work

Split the work but reach shared judgement. One useful split:

- One member runs the structural mapping in Part A
- One runs the consistency check in Part A
- One leads the real-case test in Part B
- One leads the diagnosis and recommended SI fixes in Part B

But every member reads and signs off on the final report. If you cannot defend a finding individually, do not submit it.

## Part A — Self-Evaluation

The goal: **catch what was lost in translation between the PRD and the SI before the agent meets a real user.** Approach this as a sceptic, not an advocate. You just wrote the SI; your natural bias is to see it as complete. A self-evaluation that finds zero issues is almost certainly not thorough enough.

Run four checks. Each produces written findings.

### Check 1 — Completeness

Map each PRD section to its SI counterpart. For every PRD requirement, find the SI text that operationalises it. Flag any PRD requirement with no corresponding SI directive.

A simple table works:

| PRD section | SI section | Status | Notes |
|---|---|---|---|
| §1 Identity & Role | §1 Role | ✅ / ⚠️ / ❌ | … |
| §3 Core Capabilities | §5 Instructions, §3 KB Usage | … | … |
| … | … | … | … |

### Check 2 — Consistency

Look for contradictions:

- Do the Examples (§7) demonstrate the rules in Instructions (§5)?
- Does the Output Format (§6) match what the Examples show?
- Do the Criteria (§4) align with what the Instructions actually produce?
- Does the Role (§1) match the tone in the Instructions?
- Do the KB Usage rules (§3) align with what the Instructions reference?

### Check 3 — Specificity

For each SI directive, ask: is this vaguer than its PRD source? The SI must be at least as specific as the PRD — never less. "Be culturally sensitive" in the SI is a failure if the PRD said "qualify every cultural recommendation with at least one exception".

### Check 4 — KB / SI separation

Read every SI section looking for domain knowledge that has leaked in: framework names with definitions, country patterns spelled out, BATNA explanations. All of it belongs in the KB. Read the KB the other direction: any "the agent should…" lines belong in the SI.

### What Part A produces

A findings table:

| # | Issue | Where (PRD/SI/KB) | Severity | Recommended fix |
|---|---|---|---|---|
| … | … | … | high / med / low | … |

Aim to find at least three genuine improvements. If you find zero, you have not looked hard enough.

Apply the fixes you decide to make, then move to Part B.

## Part B — Real-Case Evaluation

The goal: **see what your agent actually produces when given a real cross-cultural negotiation situation, and refine the SI based on what you observe.**

### Choosing the case

Pick a real case the group brings — from a member's professional experience, from a documented cross-cultural negotiation (M&A, joint venture, supply, diplomatic), or constructed from a member's home country and industry. Two requirements:

- The case must be **specific** — named parties, named cultural axis, named negotiation goal, real stakes. Not "a European company negotiating with an Asian partner".
- The case must **stretch the agent**. Use a case that exercises the agent's core capabilities, not the simplest possible input. A trivial case proves nothing.

Optional but recommended: pick at least one case whose cultural axis is **different from the one your group knows best**. The rubric tests generalisation. An agent that performs well only on the case you optimised for is not the agent the project asks for.

### Running the case

1. Paste the case into the deployed agent (Claude Project or ChatGPT Project)
2. Capture the **full** agent output — not a summary
3. Save the input and output for the report

### Assessing the output

Score the output against your **Definition of Success from PRD §7** — the success criteria and failure modes you wrote there. For each criterion:

| Quality indicator from PRD §7 | Met / Partial / Not met | What you observed in the output |
|---|---|---|
| … | … | … |

Then write an overall verdict: what is working, what is falling short, how far the output is from the bar you set yourself.

### Diagnosis and SI revisions

For every gap, trace it to a root cause in the SI:

- **SI gap** — the directive is missing, ambiguous, or too weak
- **SI contradiction** — two directives conflict; the agent followed the wrong one
- **Missing coverage** — the SI does not address this scenario at all
- **Underlying KB or PRD problem** — the SI is fine but the KB or PRD is missing the substance the agent needs

Produce a prioritised list of SI changes:

| # | Issue | SI section | Specific change | Priority |
|---|---|---|---|---|
| … | … | … | "Add a step after step 3 that says …" | high / med / low |

Each recommendation must be **targeted** (a specific section), **actionable** (clear enough to apply immediately), and **specific** (the exact text or behavioural rule, not "consider adding more detail").

### Apply, redeploy, retest

Apply the highest-priority fixes. Redeploy the agent. Run the **same case** again. Capture the new output. Score it against the same indicators.

Do this **once.** One round. The methodology this is drawn from runs the loop until the output reaches a 10/10 bar across two consecutive runs — but for this project, one iteration is enough. What I want to see in the report is the loop closing visibly: input → output → diagnosis → SI change → improved output (or a clear reason the change did not produce the improvement you expected).

## What the Evaluation Report contains

Submit one document — call it whatever you like — covering:

- The case (input you gave the agent, in full)
- The agent's first output (in full)
- Part A findings table (completeness, consistency, specificity, KB/SI separation)
- Part B scoring table against PRD §7
- The SI changes you applied and why
- The agent's second output after the fix (in full)
- One short paragraph: what the round taught you, where the agent still falls short, what you would do next if you had another round

Honesty matters more than polish. If the second output is not better than the first, say so and analyse why.

## Common failure modes

- **Self-flattery in Part A.** All findings are "low severity" and the SI passes everything. If your eval finds nothing, the eval is the problem.
- **Soft test cases in Part B.** Easy inputs the agent cannot fail. Pick a case that pushes the agent.
- **Iteration with no SI change.** Re-running the same prompt is not iteration. The fix has to be a specific edit to the SI document.
- **Optimising on a single axis.** If the only case you test is the cultural axis your group knows best, you have no evidence the agent generalises. The rubric notices.
- **Hidden failures.** If the second output is worse than the first, do not bury it. Surface it and explain.

## Reference back to the methodology

This step is the student-weight version of Phases 6, 7, and 8 of the eight-stage methodology — Self-Evaluation, Synthetic Validation, and Real-World Iteration. The production methodology runs all three with multiple cases per phase and the iteration loop running until a 10/10 bar. For this project we ask for one round of each at group scale. The principles are the same; the volume is reduced.

## When you are done with this step

You have a complete Evaluation Report and the agent in its post-iteration state. Package the deliverables in `final-submission/` per the instructions there, and submit.
