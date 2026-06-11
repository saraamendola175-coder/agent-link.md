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

### Per-Response Quality Checklist

Before writing your verdict, run this checklist on the agent's output. Each item is a binary check — yes or no. A "no" is a finding.

```
□ Does the response separate facts from hypotheses?
□ Does it avoid deterministic cultural statements ("X culture always...", "he is Japanese therefore...")?
□ Does it analyze BATNA, ZOPA, interests, stakeholders, and trust?
□ Does it use cultural frameworks as analytical lenses, not as fixed predictions?
□ Does it consider organizational culture, decision-making structure, and individual variation?
□ Does it identify the risks of the proposed course of action?
□ Does it provide practical, sequenced next steps?
□ Does it include a culturally adapted communication option (email, framing, reframe)?
□ Does it avoid reducing individuals to national averages without qualification?
□ Where a recognizable signal is present (silence, indirect refusal, delay), does the response match it to a specific Action Pattern — not just explain the cultural reason?
□ Does at least one recommended move include a specific direct→adapted phrase rather than only abstract style advice ("be more indirect")?
```

### Language and Framing Patterns to Check

These are the most common framing errors in cultural analysis responses. Check whether the agent used any of the following — each one is a finding:

| Problematic pattern | What to replace it with |
|---|---|
| "almost certainly" / "definitely" / "the supplier knows" | "may indicate" / "could suggest" / "one plausible interpretation is" |
| "Japan is relationship-based" as a fixed rule | "In Japan, trust may develop gradually through reliability, consistency, and process respect — though individual and organizational variation applies" |
| Delays explained solely by time orientation (polychronic) | Frame delays through consensus processes, high UAI, and internal approval structures (nemawashi, ringi-sho) — these are more specific and more accurate |
| "Japan has the highest MAS globally" | "Japan scores very high on Masculinity in Hofstede's framework" — avoid ranking claims without source reference |
| "Italy is low-context / direct" as a fixed label | "Compared with Japan, Italian negotiators may communicate more explicitly — but Italy itself is relationship-oriented and context-sensitive; the gap is relative, not absolute" |
| "The individuals in the room definitely lack authority" | "They may lack unilateral authority — this should be validated" |
| "We will study this internally" = indirect refusal | Treat as ambiguous: could indicate genuine consultation, consensus process, discomfort, indirect rejection, or technical review |
| "Do not send the email under any circumstances" | "The Italian team should not send a threatening email at this stage — given weak BATNA and relationship dependency, a coercive message would likely increase deadlock risk" |

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

---

## Appendix A — Worked Example: Italian-Japanese Supplier Case

This appendix documents a real evaluation run of the Culturae agent against a cross-cultural negotiation case. It shows what a good evaluation looks like: what the agent got right, where it overstepped, and how to correct it. Use it as a reference when running your own Part B evaluation.

---

### The Case (input)

An Italian manufacturing company is negotiating with a Japanese supplier for a 3-year contract on critical electronic components. The Italian buyer wants a 12% price reduction, stricter late-delivery penalties, and faster confirmation of delivery schedules. The Japanese supplier has responded indirectly. In the last meeting, the supplier remained silent several times and said: "We will study this internally." Since then, email replies have become slower and less specific. The Italian team wants to send a threatening message. The buyer's BATNA is weak: switching suppliers requires 10 months of technical certification, and the supplier holds know-how needed for future product development.

---

### Overall Assessment

**What the agent got right:**
- Correctly identified that the visible problem (price, penalties, schedules) is not the real bottleneck — the Process and People layers are in failure
- Applied BATNA, ZOPA, Interests vs. Positions, Stakeholder Mapping, and Trust correctly
- Used Hall's high-context framework, Hofstede's Japan profile, Meyer's Culture Map, and Japan regional profile (nemawashi, ringi-sho)
- Recommended against the threatening email with sound reasoning
- Produced a culturally appropriate sample email
- Applied hypothesis-based framing throughout

**Main issue:** Several statements were too absolute. The corrections below show where to apply more precise, hypothesis-based language.

---

### Correction 1 — BATNA and Supplier Awareness

| | Text |
|---|---|
| **Original** | "The supplier almost certainly knows it. Any threat to switch is a credibility-destroying bluff." |
| **Corrected** | "The Italian buyer's BATNA appears weak because switching suppliers would require 10 months of technical certification. The supplier *may* be aware of this dependency, or may infer it from the technical nature of the components and continued engagement. A threat to switch would therefore be risky — if not credible, it may weaken the Italian team's position and damage trust." |
| **Why** | Avoid assuming what the supplier knows without direct evidence. |

---

### Correction 2 — Japanese Trust Formation

| | Text |
|---|---|
| **Original** | "In Japan, trust is relationship-based… It does not develop through contract terms or pressure." |
| **Corrected** | "In Japan, trust often develops gradually through reliability, consistency, reputation, repeated interaction, and respect for process. It should not be treated as something created only through contract pressure. The cooling signals *may* indicate weakening trust — but this should be validated through further interaction." |
| **Why** | Japan is not purely relationship-based in the same way as Brazil, China, or Middle Eastern contexts. Japanese trust also has strong task-based and process-based components. |

---

### Correction 3 — Delays and Time Orientation

| | Text |
|---|---|
| **Original** | "The demand for faster schedule confirmation is applying monochronic time logic to an organization whose internal decision process follows a consensus-based timeline that cannot be unilaterally accelerated." |
| **Corrected** | "The issue is less about polychronic time and more about consensus-based decision-making, high UAI, and internal approval processes. Faster confirmation may require internal alignment, technical verification, risk assessment, and formal approval before the supplier can commit externally." |
| **Why** | Japan is not primarily a polychronic culture — framing the delay through UAI, nemawashi, and ringi-sho is more precise and more grounded in the KB. |

---

### Correction 4 — Hofstede Masculinity Claim

| | Text |
|---|---|
| **Original** | "Japan MAS: 95 (highest globally)" |
| **Corrected** | "Japan scores very high on Masculinity in Hofstede's framework. This may be associated with strong concern for performance, quality, and professional reputation. Stricter penalty clauses may be interpreted as questioning the supplier's reliability — a reputational concern in a high-MAS context." |
| **Why** | Avoid ranking claims without a specific source reference. Keep the interpretation, drop the superlative. |

---

### Correction 5 — Italy as Direct Communication Culture

| | Text |
|---|---|
| **Original** | "Italy sits toward the direct end. This is a textbook example of what happens when these two extremes interact." |
| **Corrected** | "Compared with Japan, Italian negotiators may communicate more explicitly and expressively. However, Italy is not a purely low-context culture — it is relationship-oriented, context-sensitive, and regionally variable. The miscommunication is better described as a *relative gap*: the Italian team is using a more explicit and pressure-oriented style than the Japanese supplier expects." |
| **Why** | Italy's position on Meyer's Communicating scale is not at the low-context extreme. Framing this as two extremes is inaccurate and risks stereotyping both cultures. |

---

### Correction 6 — Stakeholder Authority

| | Text |
|---|---|
| **Original** | "The individuals in the room almost certainly do not have unilateral decision authority." |
| **Corrected** | "The individuals in the room *may* not have unilateral authority to approve significant price reductions, stricter penalty clauses, or delivery schedule commitments without internal consultation. 'We will study this internally' may indicate that additional stakeholders, technical reviewers, or formal approval processes are involved." |
| **Why** | This is a plausible hypothesis — not a certainty. Preserve the insight while flagging the uncertainty. |

---

### Correction 7 — Interpreting "We Will Study This Internally"

| | Text |
|---|---|
| **Original** | "'We will study this internally' is likely an indirect refusal signal or serious discomfort." |
| **Corrected** | "'We will study this internally' may indicate several things: genuine internal consultation, consensus-building, technical or legal review, discomfort with the proposal, or an indirect signal that the current framing is unacceptable. It should not be treated as clear agreement — but it should not be automatically decoded as refusal either." |
| **Why** | High-context signals are genuinely ambiguous. Giving multiple interpretations is better analysis. |

---

### Correction 8 — Tone of the Recommendation

| | Text |
|---|---|
| **Original** | "Do not send the threatening email under any circumstances before that senior-level meeting has occurred." |
| **Corrected** | "The Italian team should not send a threatening email at this stage. Given the weak BATNA, the relationship dependency, and the possible face-threatening effects, a coercive message would likely increase the risk of deadlock. A firmer message should be considered only after the team has clarified authority, explored the supplier's constraints, and strengthened its alternatives." |
| **Why** | The recommendation is correct — but absolute phrasing in professional advice should be reserved for genuine certainties. |

---

### Improved Cultural Analysis (reference version)

```markdown
## Cultural Analysis

The following is hypothesis-based. It describes possible cultural and organizational
explanations, not guaranteed facts about the Japanese supplier.

### Hall — High-Context Communication
Japan is commonly treated as a high-context communication culture. Silence, slower
replies, and "we will study this internally" may indicate: genuine internal
consultation; need for consensus-building; discomfort with the proposal; reluctance
to reject directly; technical or legal review. The Italian team should not interpret
indirectness as bad faith — nor as agreement.

### Hofstede — Japan Profile
- High UAI: may require precise procedures and internal risk review before accepting
  penalty clauses or schedule commitments.
- High LTO: may evaluate the negotiation in terms of long-term partnership, not only
  short-term price.
- Very High MAS: may be sensitive to reputational framing. Penalty clauses may be
  perceived as questioning delivery reliability.
- Moderate PDI: hierarchy may matter; significant concessions may require senior-level
  involvement.
- Moderate Collectivism: internal consensus may be required before commitment.
These are hypotheses, not conclusions. Test through follow-up meetings.

### Meyer — Culture Map
- Communicating: Japan is relatively high-context. Pay attention to silence,
  indirect wording, reduced engagement.
- Deciding: Japanese organizations often require consensus and formal approval
  before decisions become final.
- Disagreeing: direct confrontation may be avoided. Absence of explicit refusal
  does not mean agreement.

### Japan Regional Profile
Nemawashi (informal pre-alignment) and ringi-sho (formal upward approval) may be
active. The Italian team should support the supplier's internal process rather than
try to bypass it through pressure.
```

---

### What This Example Teaches

1. Well-structured analytical responses can still contain overgeneralization — precision at the framing level matters as much as structural correctness.
2. The checklist and language patterns in Part B above catch the majority of quality gaps before they appear in a final evaluation.
3. Treating hypothesis-based language as a discipline (not just a caveat) produces better recommendations — because it forces the analyst to hold multiple interpretations open rather than committing prematurely.
4. The Italy–Japan case illustrates that cultural gaps are relative, not absolute. Both cultures have contextual and relationship-oriented dimensions; the gap between them is real but should not be described as extreme-vs-extreme.

---

## Appendix B — Worked Example: US Company vs Japanese Supplier Case

This appendix documents a second evaluation run of the Culturae agent. Where Appendix A focuses on corrections to a response that contained framing errors, this appendix shows what a high-quality response looks like and how to score it. Use it as the reference benchmark when the agent performs well.

---

### The Case (input)

A US technology company is negotiating a long-term supply agreement with a Japanese manufacturer of precision components. The American team prefers direct communication, quick decisions, and immediate discussion of pricing. The Japanese team values relationship-building, consensus, hierarchy, and indirect communication.

**Agent tasks:**
1. Identify cultural differences between the two parties
2. Suggest communication adaptations
3. Rewrite a negotiation email for a Japanese audience
4. Highlight risks of excessive directness
5. Recommend face-saving language

---

### Scoring Table

| Category | Score | What the agent did |
|---|---|---|
| Cultural Accuracy | 9/10 | Correctly identified low- vs high-context communication, task-based vs relationship-based trust, nemawashi and ringi-sho, and relevant Hofstede indicators (LTO 26 vs 88, UAI 46 vs 92). Minor gap: could briefly acknowledge globalization or industry effects for highly internationalized Japanese firms. |
| Depth of Analysis | 10/10 | Multi-layer diagnosis using the 4Ps (Problem, Process, People) was applied correctly and explicitly. Clear causal logic, not just description. |
| Practical Recommendations | 9.5/10 | Actionable guidance: allow silence, avoid binary questions, match seniority, 10–14 day follow-up timing. Could add a sample meeting agenda or guidance on non-verbal cues. |
| Email Rewrite | 10/10 | Formal, respectful, relationship-oriented. Avoids hard price anchors, deadlines, and pressure language. Comparison table (original vs rewritten) is effective. |
| Risk Awareness | 10/10 | Five clearly articulated risks with causal logic linking American behavior to Japanese consequences. |
| Face-Saving Language | 10/10 | Six-scenario table with direct-to-indirect transformations, immediately applicable in live negotiation. |
| Structure and Clarity | 9/10 | Logical sectioning and effective use of tables. Slightly dense in places for executive audiences. |
| **Overall** | **9.6/10** | High-quality, expert-level response suitable for professional or academic use. |

---

### What the Agent Got Right

- Correctly diagnosed the root problem as a **People and Process layer issue before a Problem layer issue** — pricing cannot be negotiated productively before trust and process alignment are established
- Used hypothesis-based language throughout ("may indicate", "could suggest") without prompting
- Applied multiple frameworks together: Hall (communication context), Hofstede (LTO, UAI, PDI comparisons), Meyer (Trusting, Deciding, Disagreeing scales)
- Produced a culturally adapted email and a face-saving language table that are directly usable
- Framed Japanese trust as gradual and reliability-based, not as a purely social or personal relationship — this is the correction established in Appendix A, applied correctly here

---

### Minor Gaps

These are not errors; they are opportunities for stronger responses:

| Gap | What a stronger response would add |
|---|---|
| No acknowledgment of organizational or generational variation | A brief note that highly internationalized Japanese firms may display more direct communication styles; the framework applies to tendencies, not certainties |
| No "what to do if the negotiation stalls" guidance | A short decision tree: if no response after 2–3 weeks, escalate to senior executive contact rather than increase pressure |
| No engagement timeline | A Week 1–4 roadmap: relationship meeting → follow-up email → topic-specific working session → pricing discussion |

---

### What This Example Teaches

1. A response can be structurally correct and still benefit from richer qualification at the edges — acknowledging individual, organizational, and generational variation strengthens every analysis.
2. Face-saving language tables are among the highest-value deliverables an agent can produce — they convert cultural insight into immediately usable communication tools.
3. The multi-layer diagnosis (Problem / Process / People) does the most analytical work in this type of case; it should appear early and explicitly.
4. Hypothesis-based framing is not only about avoiding overstatement — it also signals to the counterpart that the analysis is being held open to revision, which is a professional and accurate posture.

---

## Appendix C — Worked Example: German Company vs Brazilian Supplier Case

This appendix documents a third evaluation run. Where Appendix A shows corrections to a response with framing errors, and Appendix B benchmarks a high-quality response, this appendix introduces a new evaluation dimension — **Agent Optimization** — and shows what a near-excellent response still lacks in terms of operational usability. Use it to calibrate the gap between analytical quality and practical retrievability.

---

### The Case (input)

A German automotive company is negotiating delivery deadlines with a Brazilian supplier. The German side focuses on precision, planning, and strict schedules. The Brazilian side emphasizes flexibility, personal relationships, and adaptability.

**Agent tasks:** detect differences in time orientation; recommend negotiation strategies; predict possible misunderstandings; generate culturally adapted meeting notes.

---

### Scoring Table

| Category | Score | Key finding |
|---|---|---|
| Cultural Accuracy | 9.5/10 | Correct identification of monochronic vs polychronic (Hall), sequential vs synchronic (Trompenaars), and the UAI paradox (both cultures score high on UAI but manage uncertainty through opposite mechanisms). Minor gap: no mention of regional variation within Brazil (e.g., São Paulo business culture vs. other regions). |
| Depth of Diagnosis (4Ps) | 10/10 | Textbook application: correctly identifies Process and People as the blocked layers, explicitly excludes the Problem layer as the bottleneck. |
| Strategic Recommendations | 9.5/10 | Bilateral guidance (for both German and Brazilian sides). Particularly strong: buffer timelines, early-warning protocol, and senior-level relationship investment. Could be slightly more step-by-step. |
| Misunderstanding Analysis | 10/10 | Six realistic misunderstandings, each presented as a mutual misread with both cultural perspectives — immediately transferable to training contexts. |
| Meeting Notes Adaptation | 10/10 | Exceptional balance between German need for structure and Brazilian relationship tone. Explanation of design choices is included inline. |
| Theory / Practice Integration | 10/10 | Hall + Hofstede + Trompenaars + 4Ps applied without framework dumping — everything connected to a concrete behavior or recommendation. |
| **Agent Optimization** | **7.5/10** | See below. |
| **Overall** | **9.4/10** | Expert-level analytical response. Main growth area: operational retrievability. |

---

### Notable Analytical Strength: The UAI Paradox

The strongest analytical moment in this response is the identification that Germany (UAI 65) and Brazil (UAI 76) both score relatively high on Uncertainty Avoidance — yet manage uncertainty through opposite mechanisms. Germany uses formal documentation, defined procedures, and written contracts. Brazil uses personal relationships and trust as the primary risk-management system. This means that the German team's contract-heavy approach may register as suspicious to a Brazilian partner who considers the relationship itself the guarantee — and the Brazilian team's relational reassurances may register as insufficient to a German team that needs written confirmation.

This is expert-level synthesis: same Hofstede dimension, opposite behavioral outputs. It should appear in every analysis involving these two cultural profiles.

---

### Agent Optimization Finding (Score 7.5/10)

Even a near-perfect analytical response can have limited operational usability if its structure is narrative rather than retrieval-ready. This case illustrates that gap.

**The limitation:** The response is well-organized but primarily written in paragraph form. Under time pressure or in a live negotiation, a user cannot quickly extract the specific action to take when a specific signal appears. The analysis explains *why* Brazilian suppliers communicate delivery delays late; it does not give the agent a quick pattern to fire when that signal occurs.

**What was missing:** If→then action blocks of the form used in KB Part VI:

> *Signal:* Late delivery notice received with short lead time
> *Meaning:* Relationship-based hesitation to deliver bad news — not negligence
> *Action:* Reinforce no-penalty early-warning rule; reframe as shared problem-solving, not blame assignment

**Why this matters for evaluation:** KB Part VI (Execution Layer, added to this project) was built in direct response to this gap. A response that applies Part VI Action Patterns and Language Patterns will score higher on Agent Optimization than one that provides the same cultural analysis in purely narrative form.

**How to check for this in evaluation:**
- Are the recommended moves specific enough to be executed by someone who stopped reading after the diagnosis?
- Does the response include at least one direct→adapted phrase, not just a style description?
- Would the key action for the most likely next signal fit in two sentences?

---

### Minor Gap: Regional Variation Within Brazil

The response treats Brazil as culturally uniform. A stronger response would note that São Paulo business culture — more monochronic, more internationally adapted, with a larger German-Brazilian and Japanese-Brazilian community — may sit closer to European norms than the national average suggests. This is the KB Part IV regional variation caveat (Section 4.8) applied to the Brazilian context.

---

### What This Example Teaches

1. Analytical quality and operational usability are different properties. A response can be analytically correct and expert-level while still being too dense for rapid real-time retrieval. Both dimensions should be evaluated.
2. The UAI paradox (same dimension, opposite mechanism) is one of the most powerful insights available in cross-cultural analysis — it surfaces the cases where frameworks predict similarity but behavior diverges sharply.
3. The Agent Optimization gap was the direct motivation for KB Part VI. Evaluators should check whether the agent is drawing from Part VI Action Patterns and Language Patterns, not only providing narrative cultural analysis.
4. Bilateral framing — providing recommendations for both sides — is a mark of high-quality analysis. Single-sided advice ("the German team should...") treats the negotiation asymmetrically; bilateral advice treats it as a shared system with friction on both sides.

---

## When you are done with this step

You have a complete Evaluation Report and the agent in its post-iteration state. Package the deliverables in `final-submission/` per the instructions there, and submit.
