# 5 — Evaluation Report

> Part B real-case evaluation, plus the Part A self-evaluation of the SI against the PRD. **Case 1 (US–Japanese) is the primary Part B case** — it is carried through the full iteration loop the spec requires: first output → diagnosis → SI change → second output → rescore. Cases 2–5 are generalisation evidence on four further axes (Brazil, India, China, UAE/Sweden), scored on first output to confirm the agent holds up beyond the primary axis rather than being optimised for it. Every case is scored against the seven success criteria in PRD §7.

---

## Scoring criteria (PRD §7)

Every case below is scored on the same seven criteria:

1. Names a specific dimension linked to a concrete behaviour
2. Distinguishes cultural from commercial drivers
3. Proposes at least one specific, sequenced move
4. Flags / works the non-standard-profile limitation
5. Includes an Immediate Next Step
6. Applies the 4Ps with the primary breakdown level named
7. Uses multiple frameworks when warranted

Result values: **Met / Partial / Not met.**

---

## Case 1 — US Company vs Japanese Supplier (directness mismatch) — PRIMARY PART B CASE

*This is the primary real-case test. Its first output is below; the full iteration loop (diagnosis → SI change → second output → rescore) follows immediately after.*

**Input given to the agent:**

> We're a US tech firm setting up a long-term supply agreement with a Japanese precision manufacturer. We move fast, talk price first, and like things direct. They're slower, very relationship-focused, consensus-driven. Help me understand the differences, adapt how we communicate, rewrite our intro email, and tell me where our directness will cause problems.

**Agent output (in full):**

### Situation Diagnosis
A first-contact calibration case. The core risk is that your default — fast, direct, price-first — raises the trust barrier with a relationship-first counterpart rather than lowering it. The fix is to lead with relational intent and defer commercial structure.

### Cultural Analysis
- **Meyer — Trusting scale (task vs. relationship):** you build trust through competence and results; they build it through relationship first. Opening with price signals a task-first stance that reads as transactional.
- **Hofstede — Long-Term Orientation (Japan high):** they're optimising for a durable relationship, not this quarter's terms; your speed can read as short-termism.
- **Hall — High-Context Communication:** their consensus and indirection mean early commercial specifics will be met with deferral, not engagement.

**Confidence Calibration:** Medium. Lowered if the counterpart is in an internationally exposed role or has US business experience. Observe whether they reciprocate directness before committing to a low-context register.

### Negotiation Assessment
There is no deadlock yet — this is sequencing. **Primary breakdown risk: People** (trust threshold not crossed), with **Process** (communication register) as the live secondary. Introducing commercial structure before trust is the classic relationship-first failure; it raises the barrier you're trying to lower.

### Recommended Moves
1. **Make first contact relational only — no commercial content.** Establish intent, signal long-term commitment, ask about their priorities.
2. **Rewrite the intro email to remove price from first contact.** Replace "we'd like to discuss pricing for X volume" with an expression of interest in a long-term partnership and a request to meet.
3. **Hold your directness until they reciprocate it.** Use one direct question as a probe; if they answer in kind, you can operate more directly; if they soften, stay high-context.

### Immediate Next Step
Send a short relationship-first introduction that names long-term partnership intent and proposes a first conversation — with no commercial terms in it.

**Scoring against PRD §7:**

| Criterion | Result | Observed in the output |
|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | Meyer Trusting, Hofstede LTO, Hall High-Context — each tied to the price-first opening |
| Distinguishes cultural from commercial drivers | ✅ Met | Frames the problem as sequencing (People), not the commercial terms themselves |
| At least one specific sequenced move | ✅ Met | Relational first contact → email rewrite → directness held until reciprocated |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | Confidence Calibration names the modifiers (internationally exposed role, US experience) but does not develop the alternative reading |
| Includes an Immediate Next Step | ✅ Met | A relationship-first intro with no commercial terms |
| Applies the 4Ps with primary level named | ✅ Met | "Primary: People … secondary: Process" stated explicitly |
| Uses multiple frameworks when warranted | ✅ Met | Meyer, Hofstede, Hall combined |

**Teaches:** in relationship-first cultures, introducing commercial structure before trust raises the barrier rather than lowering it; first contact should establish relational intent only.

---

## Primary Part B case — iteration loop (Case 1)

Case 1 is the primary Part B test, carried through the full loop the spec requires: first output (above) → diagnosis → SI change → second output → rescore. It was chosen because it shows the recurring weakness most cleanly, and its modifier — an internationally exposed counterpart — is the exact gap the SI revision targets.

### Diagnosis of the gap
In the first output, the non-standard-profile criterion scored **Partial**: the Confidence Calibration line named the modifiers (internationally exposed role, US business experience) but the analysis never *worked* that reading — it did not say which scores become unreliable, estimate the counterpart's adaptability, or change the recommended moves accordingly. Root cause: **SI gap** — Step 2's non-standard-profile handling was an optional flag, not a mandatory worked step.

### SI change applied
SI §5 Step 2 was strengthened from "flag if non-standard" to a mandatory worked assessment: *when any modifier is significant, state which scores are unreliable and why, estimate adaptability, and identify which cultural code is likely active in this context.* (Revision 1 in the SI-changes table below.)

### Second output (full) — Case 1, redeployed agent

**Input:** identical to Case 1 above.

#### Situation Diagnosis
A first-contact calibration case, with an organisation-vs-individual split that the first pass under-used: the firm's decision process is consensus-bound regardless of who you talk to, but your likely point of contact at an export-facing precision manufacturer may be an internationally exposed individual operating in a more low-context register. Register and institutional pace must be treated as two separate clocks.

#### Cultural Analysis
- **Meyer — Trusting scale (task vs. relationship):** they build trust through relationship first; opening with price reads as transactional.
- **Hofstede — Long-Term Orientation (Japan high):** they're optimising for a durable relationship, not this quarter's terms.
- **Hall — High-Context Communication:** consensus and indirection mean early commercial specifics meet deferral.
- **Cultural-intelligence / non-standard-profile lens (worked):** an export-facing Japanese precision manufacturer selling to global tech firms will often field an internationally experienced sales/BD contact. *Which scores become unreliable:* at the interpersonal register, this individual's Hall high-context and Meyer relationship-first scores are the least reliable — in English with foreign clients they may operate more directly and low-context than the national baseline. *Which stay reliable:* Hofstede LTO and the institutional consensus (nemawashi) constraint hold regardless of the individual, because they're organisational, not personal. *Adaptability estimate:* moderate-to-high at the level of communication register; low at the level of internal decision pace. *Active cultural code:* the external, client-facing code — more internationalised than the firm's internal code.

**Confidence Calibration:** Medium. The split read (adaptable individual, non-adaptable institution) is itself a hypothesis — update it by watching whether your contact answers a direct question in kind (individual is low-context) or defers it to internal review (the institution dominates).

#### Negotiation Assessment
No deadlock — this is sequencing. **Primary breakdown risk: People** (trust threshold), with **Process** (register) as the live secondary. The worked profile splits the move set: communication register can flex to the contact's adaptability, but commercial pacing cannot — it is gated by the consensus process, not the individual.

#### Recommended Moves
1. **Deploy one calibrated directness probe earlier than the baseline would allow.** Because the individual may be low-context, embed a single direct, substantive question in first contact: *"To make our first conversation useful — what's the one thing you'd most want to understand about us as a long-term partner?"* If answered directly, escalate directness; if deferred, stay high-context.
2. **Keep commercial pacing on the institutional clock regardless of how direct the individual is.** A fluent, Westernised contact cannot compress nemawashi — do not let individual adaptability be misread as institutional readiness, which is the trap a "they seem direct, let's table terms" reading walks into.
3. **Rewrite the intro email with a flexible register.** Relational-first framing, plus one concrete substantive line the contact can engage directly if they're low-context — giving them room to set the tempo rather than forcing one register on them.

#### Immediate Next Step
Send the relationship-first intro with one calibrated direct question embedded, and use the response — direct vs deferred — to set your register for the next exchange.

### Rescore against PRD §7 (second output)

| Criterion | First output | Second output | Change |
|---|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | ✅ Met | — |
| Distinguishes cultural from commercial drivers | ✅ Met | ✅ Met | — |
| At least one specific sequenced move | ✅ Met | ✅ Met | — |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | ✅ Met | **Improved** |
| Includes an Immediate Next Step | ✅ Met | ✅ Met | — |
| Applies the 4Ps with primary level named | ✅ Met | ✅ Met | — |
| Uses multiple frameworks when warranted | ✅ Met | ✅ Met | — |

### Retest verdict
The revision fired. The second output no longer merely flags an internationally experienced counterpart — it works the reading: it states which scores become unreliable (the individual's high-context and relationship-first scores) and which stay reliable (institutional LTO and nemawashi), estimates adaptability, identifies the active cultural code, and splits the move set accordingly (register flexes; commercial pacing does not). The one criterion that was Partial across all five cases moved to Met, and the other six held — which indicates the revision targeted the correct weakness and did not introduce regressions. The loop is closed: same case, revised SI, second output captured in full, rescored against the same criteria.

---

## Generalisation cases (Cases 2–5)

> The four cases below are first-run only, included to test the agent on axes beyond the primary case — the spec's requirement not to optimise on a single axis. Each is scored against the same seven PRD §7 criteria.

## Case 2 — German Buyer vs Brazilian Supplier (time-orientation mismatch)

**Input given to the agent:**

> Our German automotive company is negotiating delivery deadlines with a Brazilian supplier. We run on precision and fixed planning; they're more flexible and relationship-led. Where will the time-orientation differences bite, what strategy do you recommend, and can you help me frame the meeting notes so both sides are aligned?

**Agent output (in full):**

### Situation Diagnosis
A synchronic/sequential time mismatch, amplified by a shared trait pulling in opposite directions: both sides are uncertainty-averse but reduce uncertainty with opposite instruments — you through fixed contracts and schedules, they through relationships and flexibility.

### Cultural Analysis
- **Hall — Monochronic vs. Polychronic time:** you treat the schedule as a commitment; they treat it as a flexible intention adjusted to circumstances and relationships.
- **Trompenaars — Sequential vs. Synchronic:** your linear, one-task-at-a-time planning meets their parallel, adaptive approach — deadlines mean different things to each side.
- **Uncertainty-reduction paradox:** both sides want certainty; your instrument is the contract, theirs is the relationship. Pushing harder on the contract can erode the relationship that actually delivers their reliability.

**Confidence Calibration:** Medium. Lowered if the supplier has experience with European OEMs or an export-facing operation accustomed to gate-date discipline.

### Negotiation Assessment
Naming the paradox is not yet a move. **Primary breakdown: Process** (how deadlines are defined and tracked). The fix is structural: distinguish the dates that genuinely cannot move from the milestones that can absorb flexibility, and build a channel that surfaces slippage early instead of at the deadline.

### Recommended Moves
1. **Separate non-negotiable gate dates from absorbable operational milestones.** Make explicit which dates are hard (certification, line launch) and which have built-in tolerance — don't present every date as immovable.
2. **Build an early-warning channel.** Agree a lightweight check-in rhythm so a slipping milestone surfaces weeks early, when the relationship can absorb it, rather than at the gate.
3. **Frame the meeting notes around shared reliability, not compliance.** Record gate dates as joint commitments and milestones as collaboratively managed — language that respects their relational frame while protecting your planning.

### Immediate Next Step
Draft the meeting notes with a two-tier date structure (gate vs. operational) and propose the early-warning check-in cadence as a shared mechanism.

**Scoring against PRD §7:**

| Criterion | Result | Observed in the output |
|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | Hall Monochronic/Polychronic and Trompenaars Sequential/Synchronic, each tied to what a deadline means |
| Distinguishes cultural from commercial drivers | ✅ Met | The paradox separates the cultural instrument (relationship vs contract) from the commercial deadline itself |
| At least one specific sequenced move | ✅ Met | Two-tier date split → early-warning channel → reframed meeting notes |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | Names the European-OEM/export-facing modifier but does not work the alternative reading |
| Includes an Immediate Next Step | ✅ Met | Two-tier meeting notes plus the proposed check-in cadence |
| Applies the 4Ps with primary level named | ✅ Met | "Primary: Process" named explicitly |
| Uses multiple frameworks when warranted | ✅ Met | Hall, Trompenaars, plus the uncertainty-reduction paradox |

**Teaches:** naming a paradox is not yet a move — the move is the structural fix (separate non-negotiable gate dates from absorbable milestones, build the early-warning channel).

---

## Case 3 — French Manager vs Indian IT Partner (compound hierarchy)

**Input given to the agent:**

> I manage a French team outsourcing software to an Indian IT firm. I expect people to push back and flag problems openly, but our Indian counterparts never contradict us — everything sounds fine until it isn't. How do I get honest feedback, and how should I rewrite the way I ask for it?

**Agent output (in full):**

### Situation Diagnosis
A compound-hierarchy case: two sources of deference stack. The fix is not asking harder for honesty — it's redesigning the channel through which problems surface, because the current channel structurally suppresses them.

### Cultural Analysis
- **Hofstede — Power Distance Index (India high vs. France lower):** open contradiction of a senior figure is face-threatening; silence is respect, not agreement.
- **The outsourcing multiplier:** client authority compounds with seniority — your counterparts defer both to rank and to you as the client, so the suppression is doubled, not single.
- **Hall — High-Context Communication:** problems are signalled indirectly (hedging, "we will try", slight delays), not stated outright.

**Confidence Calibration:** Medium-to-High on the pattern. Lowered for an internationally experienced counterpart or a firm with extensive Western-client exposure, who may be more direct.

### Negotiation Assessment
The problem is **People** (face and hierarchy) expressed through a broken feedback **Process**. Asking "any concerns?" in a yes/no frame to a high-PDI counterpart reliably returns "no concerns" regardless of reality — the question itself is the failure.

### Recommended Moves
1. **Never validate via yes/no questions.** Replace "does this work / any problems?" with "walk me through the two riskiest parts of this plan and what would make them slip" — make problem-surfacing the expected answer.
2. **Make bad news an assigned deliverable.** Build a standing "top three risks this week" item owned by their lead, so flagging problems is the job, not an act of contradiction.
3. **Reward the first piece of bad news visibly.** If the first surfaced problem is met with frustration, the channel closes permanently — respond with appreciation and support.

### Immediate Next Step
Reframe your next status request as an assigned risk-surfacing deliverable ("the three things most likely to go wrong, and what you need from us"), not a yes/no check-in.

**Scoring against PRD §7:**

| Criterion | Result | Observed in the output |
|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | Hofstede PDI and Hall High-Context, each tied to silence and indirect signalling |
| Distinguishes cultural from commercial drivers | ✅ Met | Diagnoses a People/Process channel failure, not a delivery or commercial problem |
| At least one specific sequenced move | ✅ Met | Replace yes/no questions → assign bad news as a deliverable → reward the first bad news |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | Names the internationally-experienced/Western-exposed modifier but does not develop the alternative reading |
| Includes an Immediate Next Step | ✅ Met | Reframe the next status request as a risk-surfacing deliverable |
| Applies the 4Ps with primary level named | ✅ Met | "People … expressed through a broken feedback Process" |
| Uses multiple frameworks when warranted | ✅ Met | Hofstede PDI, the outsourcing multiplier, Hall High-Context |

**Teaches:** in high-power-distance compound-hierarchy contexts, never validate via yes/no questions; make problem-surfacing an assigned deliverable, and reward the first piece of bad news or the channel closes.

---

## Case 4 — Chinese Investor vs Italian Startup (trust-sequence mismatch)

**Input given to the agent:**

> We're an Italian startup and a Chinese investment group is evaluating a partnership with us. We want to move fast to a contract — our runway is tight. They keep prioritising relationship, long-term thinking, reputation, lots of dinners and warmth but no commercial movement. How do we read this and speed it up?

**Agent output (in full):**

### Situation Diagnosis
A trust-sequence mismatch with a projection risk: you're reading relational warmth as commercial readiness and your own runway pressure as a shared clock. Neither is safe. The warmth is due diligence, not a buying signal.

### Cultural Analysis
- **Meyer — Trusting scale (relationship-based):** trust is built before terms, not through them; the dinners and warmth are how they evaluate you, not evidence they've decided.
- **Hofstede — Long-Term Orientation (China high):** they're assessing a durable relationship; visible urgency on your side can read as instability or short-termism.
- **Uncertainty-reduction paradox:** they reduce risk through relationship and reputation; pushing for a fast contract raises their uncertainty rather than resolving yours.

**Confidence Calibration:** Medium. Lowered if the investors are a globally active fund accustomed to Western deal tempo, who may move faster than the relationship-first baseline suggests.

### Negotiation Assessment
**Primary breakdown: People** (trust threshold not yet crossed). Your runway is a real constraint, but projecting it onto their pace is a misread — they don't share your clock. Pushing commercial structure before the trust signal arrives can stall the deal entirely. Waiting for their readiness signal is a legitimate, often highest-priority move here.

### Recommended Moves
1. **Do not force the contract; watch for the readiness signal.** It looks like a timeline question, commercial language, or a proposed next step from their side — name it and wait for it.
2. **Consider a trusted intermediary (Zhongjianren).** Someone who can vouch for you accelerates trust far faster than you pressing directly.
3. **Manage your runway separately, not at the negotiating table.** If timing is genuinely critical, solve it through bridge options on your side rather than transmitting urgency that reads as weakness.

### Immediate Next Step
Hold the commercial push; invest one more relationship cycle and identify whether a credible intermediary exists who can vouch for you to the investors.

**Scoring against PRD §7:**

| Criterion | Result | Observed in the output |
|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | Meyer Trusting (relationship-based) and Hofstede LTO, tied to the dinners-as-due-diligence read |
| Distinguishes cultural from commercial drivers | ✅ Met | Separates the real commercial constraint (runway) from the cultural misread (warmth as readiness) |
| At least one specific sequenced move | ✅ Met | Wait for the readiness signal → intermediary → manage runway off-table |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | Names the globally-active-fund modifier but does not develop the alternative reading |
| Includes an Immediate Next Step | ✅ Met | Hold the push, invest one more relationship cycle, identify an intermediary |
| Applies the 4Ps with primary level named | ✅ Met | "Primary: People" named explicitly |
| Uses multiple frameworks when warranted | ✅ Met | Meyer, Hofstede, plus the uncertainty-reduction paradox |

**Teaches:** warmth and hospitality from a relationship-trust culture are relational due diligence, not buying signals; projecting internal urgency (cash runway) onto the counterpart's pace is a misread.

---

## Case 5 — UAE Company vs Swedish Firm (power-distance gap)

**Input given to the agent:**

> We're setting up a joint venture between an Emirati company and a Swedish firm. The Emirati side runs on hierarchy and formal authority; the Swedish side expects flat structures and consensus. Meetings keep misfiring. How do I structure them so both sides function?

**Agent output (in full):**

### Situation Diagnosis
A large power-distance gap with incompatible participation requirements. The solution is architectural — separate the meeting structure so each side operates in its own mode — not asking either side to "be more flexible".

### Cultural Analysis
- **Hofstede — Power Distance Index (UAE high vs. Sweden very low):** a >40-point gap. The Emirati side expects decisions and signals to flow through senior authority; the Swedish side expects open, level participation regardless of title.
- **Meyer — Deciding / Leading scales:** consensus-led vs. top-down decision norms collide directly in a single shared meeting format.

**Confidence Calibration:** Medium-to-High on the structural gap. Lowered for individuals with significant cross-cultural JV experience who already code-switch.

### Negotiation Assessment
**Primary breakdown: Process** (meeting architecture) **and People** (authority and face). A single meeting format cannot satisfy both participation models at once — forcing one format makes one side either disrespected or silenced.

### Recommended Moves
1. **Architect the sessions, don't compromise them.** Run a senior-to-senior protocol in plenary (satisfying the hierarchy need) plus working-group breakouts where Swedish-style open contribution happens (satisfying the consensus need).
2. **Route decisions through the format each side expects.** Plenary confirms direction senior-to-senior; breakouts generate the substance collaboratively.
3. **Reframe the egalitarian norm as a competence claim, not a preference.** Present open contribution as "expertise independent of title" rather than "equality" — a competence framing travels across the PDI gap where a values framing does not.

### Immediate Next Step
Redesign the agenda into a two-layer structure — senior-to-senior plenary plus working-group breakouts — and circulate it as the standing meeting protocol.

**Scoring against PRD §7:**

| Criterion | Result | Observed in the output |
|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ Met | Hofstede PDI (>40-point gap) and Meyer Deciding/Leading, tied to the misfiring meetings |
| Distinguishes cultural from commercial drivers | ✅ Met | Diagnoses a participation-architecture problem, not a commercial or JV-terms dispute |
| At least one specific sequenced move | ✅ Met | Two-layer session architecture → route decisions by format → reframe egalitarian norm as competence |
| Flags / works the non-standard-profile limitation | ⚠️ Partial | Names the cross-cultural-JV-experience modifier but the adaptability lens is flagged, not applied |
| Includes an Immediate Next Step | ✅ Met | Redesign the agenda into a two-layer protocol and circulate it |
| Applies the 4Ps with primary level named | ✅ Met | "Process and People" named — though identified rather than expanded |
| Uses multiple frameworks when warranted | ✅ Met | Hofstede PDI and Meyer Deciding/Leading |

**Teaches:** a >40-point PDI gap with incompatible participation requirements is solved by architectural separation, not compromise; reframe the egalitarian norm as "expertise independent of title" (a competence claim), not "equality" (a preference claim).

---

## Cross-case summary

| Criterion | Case 1 | Case 2 | Case 3 | Case 4 | Case 5 |
|---|---|---|---|---|---|
| Names a specific dimension linked to a concrete behaviour | ✅ | ✅ | ✅ | ✅ | ✅ |
| Distinguishes cultural from commercial drivers | ✅ | ✅ | ✅ | ✅ | ✅ |
| At least one specific sequenced move | ✅ | ✅ | ✅ | ✅ | ✅ |
| Flags / works the non-standard-profile limitation | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ |
| Includes an Immediate Next Step | ✅ | ✅ | ✅ | ✅ | ✅ |
| Applies the 4Ps with primary level named | ✅ | ✅ | ✅ | ✅ | ✅ |
| Uses multiple frameworks when warranted | ✅ | ✅ | ✅ | ✅ | ✅ |

The pattern is unambiguous: six of the seven criteria are met consistently across all five axes. The **non-standard-profile criterion is Partial in every case** — the agent reliably *flags* that a framework may not apply to an internationally experienced or bicultural counterpart, but does not *work* the alternative reading. The gap recurs independently of the cultural axis, which marks it as structural rather than case-specific, and is what drives the SI revision (Part A) and the primary-case iteration loop above.

---

## Part A — Self-Evaluation (SI against PRD)

Approached as a sceptic. The four checks below are run against the revised PRD (seven sections) and revised SI (seven sections), after the KB/SI separation was cleaned up and the hard-coded KB references removed.

### Check 1 — Completeness

| PRD section | SI section | Status | Notes |
|---|---|---|---|
| §1 Identity & Role | §1 Role | ✅ | Name, domain, and the three traits expressed as behaviour |
| §2 Target Users | §2 Context | ✅ | Mid-to-senior profile; the applied-vs-conceptual gap is carried over |
| §3 Cap 1 — Cultural Profile & Risk | §5 Step 2 | ✅ | Modifier check, code-switching lens, the 2–3 named risks, confidence calibration |
| §3 Cap 2 — Negotiation Preparation | §5 Step 3 | ✅ | BATNA/ZOPA, leverage, power dynamics, 4Ps |
| §3 Cap 3 — Friction Diagnosis | §5 Steps 2–4 | ✅ | Modifier check, confidence, mandatory non-cultural-cause test |
| §3 Cap 4 — Strategy & Move | §5 Step 4 | ✅ | Applied execution material referenced by category; direct→adapted phrase required |
| §3 Cap 5 — Framework Exception Flagging | §5 Step 2 + Part B | ✅ | Bicultural / expatriate / generational handled in workflow and edge cases |
| §3 Cap 6 — Post-Negotiation Debrief | §5 Step 1 | ✅ | Dedicated debrief trigger now in Step 1 (was previously only implicit) |
| §4 Interaction Guidelines | §5 Part B edge cases | ✅ | Out-of-scope redirects, ambiguity, stereotyping, multi-turn, user's own culture |
| §5 Output Format | §6 Output Format | ✅ | Five required sections + four optional blocks; Confidence Calibration required |
| §6 Boundaries & Constraints | §5 Part B (out-of-scope) | ✅ | Legal, roleplay, bottom-line, ghostwriting all present |
| §7 Success criteria | §4 Criteria (good) | ✅ | All seven self-checkable criteria translated to positive checks |
| §7 Failure modes | §4 Criteria (bad) | ✅ | All six PRD failure modes present as negative checks |

### Check 2 — Consistency

- The five §7 Examples now demonstrate the §5 workflow and the §6 format, including the required Confidence Calibration line and at least one optional block — no contradiction between rules and examples. ✅
- §6 length guidance ("roughly 300–600 words, longer for briefs and multi-party cases") matches the PRD and no longer contradicts the worked examples. ✅ *(This was a real inconsistency in the prior draft — "300–500" against 700–1500-word examples — now resolved.)*

### Check 3 — Specificity

- PRD §3 Cap 1 "2–3 cultural risks the user should anticipate" is now an explicit Step 2 output requirement, not just an implied one. ✅
- PRD §3 Cap 3 "test at least one non-cultural explanation before concluding a cultural cause" is now a positive Step 3 instruction, not only a negative check in §4. ✅

### Check 4 — KB / SI Separation

- The SI no longer contains the applied "Execution Layer" (action patterns, language patterns, templates, strategies); that domain content has moved to the KB, and the SI references it by category. ✅
- KB references in the SI are now by category, not by hard-coded section number — they survive KB revisions. ✅
- One residual watch-item: the §6 output template names specific frameworks (Hall, Meyer, Hofstede…). These are names, not definitions, so the separation holds — but if dimension *descriptions* ever creep into that template, they belong in the KB. ⚠️ low

### Part A — Findings table

| # | Issue | Where | Severity | Fix applied |
|---|---|---|---|---|
| 1 | Capability 6 (debrief) had no dedicated SI trigger — only implicit in multi-turn logic | PRD §3 / SI §5 | Medium | Added a debrief trigger to SI Step 1: on a concluded round, apply 4Ps retrospectively, separate cultural vs commercial drivers, extract 2–3 lessons |
| 2 | SI length guideline contradicted the worked examples (300–500 vs 700–1500 words) | SI §6 / §7 | Medium | Aligned to "roughly 300–600 standard; longer for briefs/multi-party", consistent with PRD |
| 3 | "2–3 cultural risks to anticipate" not required in the SI workflow | PRD §3 Cap 1 / SI §5 | Low | Made an explicit Step 2 output requirement, each risk linked to its framework |
| 4 | Non-cultural-cause check existed only as a negative check, not a positive step | PRD §3 Cap 3 / SI §5 | Medium | Added to Step 3 as a positive instruction to test one non-cultural explanation before concluding a cultural cause |
| 5 | Applied "Execution Layer" domain content sat inside the SI, breaking KB/SI separation | SI §8 → KB | High | Removed from the SI; relocated to the KB; SI now references it by category |
| 6 | Hard-coded KB section numbers in the SI (some also numerically wrong) | SI §3 | High | Replaced with category references throughout |

Six findings, none cosmetic, two high-severity — consistent with the guidance that a self-evaluation finding only "low" issues has not looked hard enough.

---

## SI changes applied (prioritised) and why

Traced from the primary-case gap and from the Part A findings, the SI revisions below were applied to the System Instructions document, in priority order:

| # | Issue | SI section | Specific change | Priority |
|---|---|---|---|---|
| 1 | Non-standard-profile criterion only Partial — agent flagged but did not work the alternative reading (all five cases) | §5 Step 2 | Make the non-standard-profile assessment mandatory: state which scores are unreliable and why, estimate adaptability, identify the active cultural code — not an optional flag | High |
| 2 | Applied "Execution Layer" domain content sat inside the SI, breaking KB/SI separation | §3, §5 | Remove the embedded Execution Layer; reference the KB's applied material by category | High |
| 3 | Capability 6 (debrief) had no dedicated SI trigger | §5 Step 1 | Add a debrief trigger: on a concluded round, apply 4Ps retrospectively, separate cultural vs commercial drivers, extract 2–3 lessons | Medium |
| 4 | Non-cultural-cause check existed only as a negative check, not a positive step | §5 Step 3 | Add a positive instruction to test one non-cultural explanation before concluding a cultural cause | Medium |

---

## What this round taught us

The agent performs at a high level on its core task across all five axes: it names specific dimensions, separates cultural from commercial drivers, and produces concrete, sequenced moves rather than culture commentary. Its strongest behaviour — structural fixes over tone advice (the two-tier date split in Case 2, the feedback-channel redesign in Case 3, the session architecture in Case 5) — is exactly what the PRD's "abstract style advice" failure mode is meant to prevent.

The consistent weakness, visible in all five cases, was the **non-standard-profile criterion**: the agent reliably *flagged* that frameworks may not apply to an internationally experienced or bicultural counterpart, but did not *work* the alternative reading. This was a failure of execution rather than of knowledge — the directive existed but was too weak to fire consistently — which is why the highest-priority SI fix strengthened Step 2 from an optional flag to a mandatory worked step. The iteration loop on Case 1 confirms the fix worked: the second output moved that criterion from Partial to Met without regressing the other six.

**Where the agent still falls short:** the loop was closed on one case (Case 1); the other four were re-scored on first output only, so the fix is confirmed on one axis rather than all five. The deeper limitation, untestable from this set, is generalisation — the non-standard-profile gap recurred on every axis tested, which suggests it is structural, and one confirmed fix does not prove it fires everywhere.

**What we would do with another round:** (1) re-run the remaining four cases through the redeployed agent to confirm the Step 2 fix fires across every axis, not just Case 1; (2) add a short "framework checklist" self-check at the end of Step 2 so the agent confirms it has both *named* and *worked* any non-standard profile; (3) test one further axis the group does not know well, to put pressure on generalisation rather than on the cases the agent has already been tuned against.
