# 2. Knowledge Base

> Step 2 of 5. You take the source material from Step 1 and turn it into a structured Knowledge Base — the document your agent consults at runtime.

## What a Knowledge Base is

A Knowledge Base is a **reference document** the agent reads to answer questions and make recommendations. It contains what the agent **knows**: frameworks, terminology, cultural patterns, negotiation moves, real examples. It does not contain how the agent **behaves** — that goes in the System Instructions in Step 4.

Think of the KB as a textbook the agent can flip through. The textbook does not tell you when to teach; the syllabus does that. Same separation here.

## The most important rule: KB / SI separation

Read this twice.

| Knowledge Base | System Instructions |
|---|---|
| What the agent *knows* | How the agent *behaves* |
| Frameworks, facts, examples | Workflow, rules, tone |
| "Hofstede's power distance dimension measures…" | "Always ask the user for the cultural axis before recommending a strategy." |
| Reference, consulted as needed | Operational, applied every turn |

If you write `the agent should…` anywhere in the KB, that line belongs in the SI, not here. If you write `Hofstede defined…` in the SI, that line belongs in the KB. This separation is non-negotiable. The grading rubric deducts 50 points for crossing it.

## The structure of a good KB

A KB is not a flat list of facts. It has a shape. The shape lets the agent navigate efficiently and lets you keep the document maintainable.

### The "How to Use This Knowledge Base" section

The first section of every KB. A short orientation map — three or four paragraphs — that tells the agent (and you) how the KB is organised, what each Part contains, and how to navigate it. Examples of what belongs here:

- "This KB has two Parts: Part 1 covers the negotiation methodology the agent applies on every case; Part 2 covers cross-cultural frameworks and patterns the agent layers on top."
- "When the user asks about a specific country, start with Part 2 Section X (the relevant region) and cross-reference Part 2 Section Y (the framework lens)."
- "Negotiation moves and cultural patterns interact — see the Strategic Links inside each Section for the cross-references."

Writing this section forces you to clarify the structure for yourself. If you cannot write a clean "How to Use" section, your structure is not yet clean.

### Parts

The major divisions of the KB. Most KBs of this size have **two or three Parts**. Choose them based on what your agent actually needs to look up. Patterns that work for a cross-cultural negotiation agent:

- **Two-part split (most common)** — Part 1: Negotiation methodology. Part 2: Cross-cultural frameworks and patterns.
- **Three-part split** — Part 1: Negotiation methodology. Part 2: Cross-cultural frameworks. Part 3: Country/regional patterns and case material.

Pick the split that matches how your agent will actually consult the KB at runtime. Do not overthink it.

### Sections within Parts

Each Part contains numbered Sections. A Section is a topic — "Hofstede's framework", "BATNA and ZOPA", "Negotiating in high-context cultures", "Bicultural counterparts". Two to five Sections per Part is a reasonable density.

Section titles must be **descriptive enough that someone scanning the KB knows what is inside without reading the body**. "Section 2.3: Hofstede's six cultural dimensions and where each applies" is a good title. "Section 2.3: Hofstede" is not.

### Chunks: the unit of retrieval

Inside each Section, the content is organised into **chunks** — bolded sub-headings each followed by a short body. A chunk is the unit the agent retrieves and applies. Each chunk follows a three-part pattern:

1. **Principle or concept** — what the idea is, stated clearly
2. **Explanation** — why it matters, how it works, the underlying logic
3. **Concrete example** — a specific scenario or illustration that makes the idea applicable

A chunk without an example is a shallow chunk. The example is what gives the agent enough material to actually apply the concept rather than just name it.

A bad chunk:

> **Anchoring**
> Anchoring is a cognitive bias where the first number affects the final outcome. It is powerful in negotiations.

A good chunk:

> **Anchoring**
> The first number on the table tends to pull the final outcome towards it, even when both sides know the underlying value. A buyer who opens at €20M and a buyer who opens at €32M, with identical valuations, will end up at very different prices — the higher anchor shifts what counts as a "reasonable" middle. Anchors work because people adjust insufficiently away from the first number they hear, especially under uncertainty or time pressure. The first-mover advantage holds when the anchor is justifiable; it backfires when the anchor is implausible enough to break credibility. *Cross-cultural caveat: in high-context cultures where opening positions are exploratory rather than committal, an aggressive anchor can damage the relationship before negotiation begins. See Part 2, Section 4.*

The good chunk is roughly two paragraphs. Short enough to retrieve; long enough to act on.

### Strategic Links

When two chunks reinforce each other across the KB, mark the connection explicitly inside the chunk. A strategic link looks something like:

> *See also Part 2, Section 3.2 (high-context communication) — in those cultures the anchoring rule above shifts.*

Strategic links matter because the agent will not always find connected ideas on its own. If your KB does not link them, the agent will treat each Section in isolation and miss the cross-cutting reasoning that makes a real expert.

### Glossary and Concept Index

Optional. Include a glossary if your KB uses domain terms a reader might confuse (e.g., "high-context", "ZOPA", "integrative bargaining"). Include a concept index — a reverse lookup — if your KB is large enough that a quick "where do I look for X?" reference would help. Smaller KBs may not need either.

## How to handle framework tensions

Sometimes two frameworks describe the same phenomenon differently — Hofstede and Meyer both treat "directness" but slice it differently. Sometimes they contradict. Decide *inside the KB* how the agent should handle the tension. The pattern:

> **Default:** Use Meyer's Culture Map for communication style assessments — it is more granular for everyday negotiation behaviour.
> **Exception:** When the user is comparing societies at the policy/macro level (e.g., M&A integration), use Hofstede — its national-scale data is better suited.

The KB resolves the conflict in writing so the agent does not have to guess at runtime.

## The exceptions are part of the knowledge

The grading rubric is explicit about this. A KB that teaches Hofstede and stops there is producing a stereotyping agent. The KB has to also teach:

- **Individual variation.** Frameworks describe distributions, not people. Two members of the same culture can diverge widely.
- **Biculturalism.** Many counterparts hold two cultural codes at once and switch between them based on context. An Indian who studied and works in the US is not "an Indian negotiator" — and is not an American one either. The KB should give the agent the analytical moves to detect bicultural signals and adapt.
- **Generational and class variation within a country.** A 28-year-old Chinese tech founder negotiates differently from a 60-year-old SOE executive.
- **Expatriate adaptation.** Counterparts who have spent years abroad take on hybrid behaviour.
- **Regional variation.** "Italy" is not one negotiating culture; "China" is not one negotiating culture.

Build these exceptions into the KB as their own sections — not as footnotes. When the agent reaches for a framework, it should reach for the qualifications at the same time.

## What does NOT belong in the KB

Recognising these will save you points on the rubric:

- Behavioural directives — "Always ask the user for the cultural axis first." → SI
- Decision logic — "If the user is uncertain, default to the more conservative recommendation." → SI
- Workflow — "First do X, then Y, then Z." → SI
- Tone or persona instructions — "Be direct but warm." → SI
- Response templates — "Reply with the following structure: …" → SI

If material from your Step 1 corpus contains rules of behaviour, mark it for the SI in Step 4. Do not let it leak into the KB.

## How deep should it go

Up to you. The size reference for this project is a Claude skill folder — compact, focused, useful — not a 15,000-word production reference document. A KB with three Parts, three to five Sections each, and four to six well-built chunks per Section is plenty. Better to have a KB that is tight and high-quality than one that is sprawling and shallow.

What matters more than size: every chunk is sourced, every chunk has an example, the structure is navigable, the KB-vs-SI separation is clean.

## How to do the work

- **Start from your Step 1 corpus, not from the model's memory.** Feed the research outputs into the model and have it propose a KB structure based on what is actually in them.
- **Decide the Parts and Sections before writing chunks.** Writing chunks first and trying to organise them later is a much longer path.
- **Write the "How to Use" section first** — even as a rough draft. It forces you to commit to a structure.
- **Build one Section at a time.** Treat each Section as a finished unit before moving on. It is easier to produce a good Section in one focused pass than to revisit ten half-finished ones.
- **Cite as you go and verify as you go.** Every fact from a specific source should carry the citation in the chunk, and every citation should be one you have personally found on Google Scholar or in a library catalogue. If you cannot find the source, the citation is fabricated — the fact does not go in.
- **Police the KB/SI line constantly.** Whenever the model writes "the agent should…", flag it for Step 4 and remove it from the KB.

## Common failure modes

- **Behavioural rules in the KB.** Most common error. Re-read every chunk asking: "is this knowledge or behaviour?" If the answer is behaviour, move it.
- **Chunks without examples.** A definition with no application is not a chunk; it is a glossary entry.
- **Stereotyping.** No exceptions section, no individual variation, no bicultural treatment. The agent built on this KB will be confidently wrong.
- **Too few interconnections between Parts.** A KB with rich Sections but no Strategic Links is a stack of mini-textbooks, not a navigable reference. The whole point of building Parts that complement each other (negotiation × culture × regional patterns) is the cross-reasoning the agent does at runtime — and that only happens if the chunks actually point to each other. If every Section reads as if it were written in isolation, you have failed to build the connective tissue. Every chunk that touches a concept covered elsewhere should carry a Strategic Link. Aim for the KB to feel woven, not stacked.
- **Too many Parts.** Five Parts is almost always two Parts pretending to be five. Consolidate.
- **Citations the model invented.** Models produce plausible-looking citations to books and papers that do not exist. Before any cited fact enters the KB, find the source on Google Scholar or in a library catalogue. If you cannot find it, the citation is not real and the fact does not go in.
- **One half of the course missing.** The KB needs both: negotiation and cross-cultural. An agent built on culture alone is not a negotiation agent.

## When you are done with this step

Move to `3-prd-reference-structure.md` when the KB has a clean "How to Use" section, two or three well-defined Parts, navigable Sections, chunks with the principle/explanation/example pattern, strategic links between related chunks, explicit treatment of framework tensions and the exceptions, and zero behavioural directives anywhere inside it.
