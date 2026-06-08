tet### Output A — A scoping document

**1. What is this agent?** A general-purpose cross-cultural negotiation advisor that helps any professional prepare for, navigate, and recover from negotiations across any cultural axis, by applying negotiation methodology and cultural intelligence frameworks to the user's specific situation.

**2. Who is the typical user?**
A professional negotiator — in business, diplomacy, consulting, or academia — who has working knowledge of negotiation fundamentals (goals, positions, interests) but limited familiarity with cross-cultural frameworks and how cultural dimensions affect negotiation behaviour.

**Specific knowledge:** understands what a negotiation is, has a position and interests, knows what they want from the deal.  
**Specific gaps:** does not know how cultural dimensions (power distance, context, time orientation, individualism) shape the counterpart's communication style, decision-making process, and trust signals — and therefore misreads behaviour or applies culturally inappropriate tactics.

  
**3. When does the user open the agent?**
At any phase of a negotiation:

- **Before:** to prepare — understand the counterpart's cultural profile, anticipate likely friction points, design an opening strategy
- **During:** to diagnose — interpret unexpected behaviour, recalibrate tactics, reassess BATNA/ZOPA in light of cultural signals
- **After:** to debrief — understand what went wrong or right through a cultural lens, extract lessons for the next round

The agent adapts its output to whichever phase the user is in.

  
**4. What does the agent do?** 
Six concrete capabilities:
- 1. **Cultural profile analysis** — given a counterpart's country, region, or described cultural background, maps the relevant cultural dimensions (Hofstede, Meyer, Hall, Trompenaars, GLOBE) that are most likely to affect negotiation dynamics, with a clear explanation of how each dimension manifests in negotiation behaviour.
- 2. **Negotiation preparation support** — helps the user structure preparation: clarify their own interests vs. positions, estimate the counterpart's likely interests, assess BATNA and ZOPA for both sides, and identify leverage points.
- 3. **Friction diagnosis** — when the user describes unexpected counterpart behaviour (silence, delay, indirect refusal, sudden escalation), identifies whether the likely cause is cultural, commercial, or relational, and explains the reasoning.
- 4. **Strategy and move recommendation** — proposes specific negotiation moves adapted to the cultural context: opening style, concession sequencing, trust-building actions, face-saving tactics, reframing language.
- 5. **Framework exception flagging** — warns when standard cultural frameworks are unreliable for this counterpart (bicultural background, expatriate experience, generational divergence, regional variation within a country) and adjusts recommendations accordingly.
- 6. **Post-negotiation debrief** — analyses what happened through a cultural lens: which dynamics were cultural vs. commercial, what the user's moves communicated cross-culturally, and what to do differently next time.


**5. What does the agent NOT do?** 
- Does **not** predict the counterpart's final position or bottom line
- Does **not** roleplay as the counterpart or simulate live dialogue
- Does **not** provide legal, compliance, or contractual advice
- Does **not** draft contract terms, opening offers, or formal correspondence
- Does **not** apply cultural frameworks as fixed stereotypes — they are always framed as population-level tendencies and hypotheses to test, not labels for individuals
- Does **not** replace the user's judgement — it advises, the user decides


**6. What does expert-level performance look like?** 
If the agent performs at expert level, the user would notice the following — things a competent-but-generic negotiation tool would miss:
- **It names the specific mechanism, not the category.** Not "cultural differences may be at play" but "the counterpart's indirect refusal and extended silence after your proposal is consistent with high-context communication (Hall) combined with high power distance (Hofstede) — they may be waiting for a senior-level signal before responding, not stalling."
- **It separates cultural from commercial.** It explicitly tells the user: "the price disagreement is commercial; the communication breakdown is cultural" — and proposes a different strategy for each, rather than conflating them.
- **It flags when frameworks do not apply.** If the counterpart is described as a French-educated Moroccan executive working in Dubai, the agent notes that standard country-level Hofstede scores for Morocco are unreliable and explains why, adjusting its analysis to the actual profile.
- **It gives sequenced, actionable moves.** Not "rebuild trust" but "in your next message, acknowledge the delay before raising the commercial point — in high-context, relationship-first cultures this signals respect and reopens dialogue without escalating."
- **It updates BATNA/ZOPA with cultural constraints.** It recognises that some moves — like a public concession or a direct challenge to the counterpart's position — may be commercially rational but culturally unacceptable, and factors that into the zone of possible agreement.
- **It works across any cultural axis.** A user negotiating Italy–Japan gets the same analytical depth as one negotiating US–Saudi Arabia or Germany–Brazil. The agent does not have blind spots for certain regions.



### Output B — Source material for the Knowledge Base
A curated corpus of documentation that your agent will need to know from. **The KB you build in Step 2 will be drawn from this material — it is not built from the model's general training.** If you skip this work, the model will fill the KB with plausible-sounding generalities and your agent will hallucinate confidently.

The corpus must cover both halves of the course:

- **Negotiation methodology** — preparation frameworks, BATNA/ZOPA, leverage analysis, value creation, integrative vs. distributive moves, concession strategy, post-negotiation review. Use the negotiation frameworks taught in this course as your spine; supplement with classics (Fisher & Ury, Lewicki, Raiffa, Malhotra) where useful.
- **Cross-cultural frameworks** — Hofstede, Trompenaars, Meyer (Culture Map), GLOBE, Hall (high/low context, monochronic/polychronic), and any others you cover in class. For each, you need enough source material to write the framework's *core dimensions, how to apply them, and where they fail* — not just the names of the dimensions.
- **Country and regional patterns relevant to negotiation** — communication style, hierarchy, decision-making processes, time orientation, trust-building, conflict handling. The agent has to be general (any cultural axis), so the corpus has to span more than one region.
- **The exceptions to the frameworks** — individual variation, biculturalism, generational shifts, expatriate adaptation, regional variation within a country. As important as the frameworks themselves. Without this material, your agent will stereotype.
- **Real cases** — at least a few documented cross-cultural negotiation cases (M&A, supply, joint venture, diplomatic). Cases ground the frameworks in behaviour.

## How to do the work

You have access to paid Claude or ChatGPT. Use the **deep research** feature of either tool — that is what it is for. A few practical notes:

- **Run deep research on each major area separately.** One research run on negotiation methodology, one on cross-cultural frameworks, one on the regional patterns you want covered, one on the exceptions and individual variation. Trying to research everything at once produces shallow output.
- **Save what you get.** Keep the research outputs as files you can later feed into Step 2. Do not just read them and move on — Step 2 needs them in writing.
- **Verify citations as you go.** Deep research outputs cite sources; not all citations are real — models will produce plausible-looking citations to books or papers that do not exist. Before putting any cited fact in your KB, search the citation on Google Scholar or in a library catalogue. If you cannot find the source, treat the citation as fabricated and remove the fact. Doing this while the context is fresh is far faster than chasing the problem during the evaluation.
- **Use your course material first.** The frameworks taught in class are the spine. Deep research fills in around them — it does not replace them.
- **Use the model as a thinking partner for the scoping document.** Have it interrogate your scoping decisions, push back on vagueness, surface the questions you have not yet asked yourself. Do not let it just confirm your first idea.

## Common failure modes

- **Scope sprawl.** The agent ends up doing five different jobs. Pick one.
- **Generic user.** "A manager." Be specific.
- **Aspirational success.** "Helps the user feel prepared." Replace with observable behaviour.
- **No out-of-scope.** If you cannot name what the agent will not do, you have not scoped it.
- **Skipping the source material.** Easy to fall into because the model "already knows this stuff." It does not — not at the depth your agent needs, and not with citations you can defend.
- **Cultural side without negotiation side, or vice versa.** Both halves of the course must be in the corpus.
- **One region only.** The agent is general. Your corpus must be too.

## When you are done with this step

Move to `2-knowledge-base-guide.md` only when both outputs are in good shape: the six scoping questions are answered specifically in writing, and you have a folder of research material covering negotiation methodology, cross-cultural frameworks, regional patterns, exceptions, and at least a few real cases — enough that someone could open it and start building a Knowledge Base from what is in there.
