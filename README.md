# Cross-Cultural Negotiation 2026 — Student Project

> **Course:** Cross-Cultural Negotiation
> **Instructor:** Yadvinder S. Rana
> **Language:** English

## What you build

A **general-purpose AI agent** for cross-cultural negotiation — deployed as a Claude Project or a ChatGPT Project — that can support a user negotiating across *any* cultural axis covered in this course. The agent is general; the case you test it on is yours.

## How you build it

You follow a five-step methodology drawn from how production AI agents are designed. Each step has its own file in this folder:

1. **Brainstorming** — `1-brainstorming.md`
2. **Knowledge Base** — `2-knowledge-base-guide.md`
3. **PRD (Product Requirements Document)** — `3-prd-reference-structure.md`
4. **System Instructions** — `4-system-instructions-reference-structure.md`
5. **Evaluation** — `5-evaluation.md`

How deep you go inside each step is your decision. The materials teach you what each step is and what it produces; they do not script the work for you. Driving Claude or ChatGPT to produce each artefact is part of what you are learning.

The methodology you are using is a simplified version of an eight-stage process for developing AI agent system instructions. If you want to look behind the curtain after the project, ask me.

## What you submit

A folder with three things:

1. **A working agent.** Public link to your Claude Project or ChatGPT Project, plus any access notes.
2. **The artefacts you produced.** Knowledge Base, PRD, System Instructions — all in Markdown (see *File format* below).
3. **An evaluation report.** One round of self-evaluation against your own PRD; one round on a real cross-cultural negotiation case you bring. Done as a group.

Detailed submission notes are in `final-submission/`.

## Tools and group setup

You will deploy your agent as either a **Claude Project** or a **ChatGPT Project**. Both are environments where you paste System Instructions into a configuration field, upload your Knowledge Base as a file, and run the agent in chat. Claude Project comes with Claude Pro; ChatGPT Project comes with ChatGPT Plus. They are equivalent for this assignment — pick the one your group prefers.

You also need access to a **Deep Research feature**. Both Claude and ChatGPT include one. Deep Research is an automated mode where the model spends roughly ten to thirty minutes reading across many web sources, then produces a structured report with citations — you will use it heavily in Step 1 to gather your source material.

Pricing is around €20 per month per paid account. **Only one student per group needs the paid account** — the group shares it for the project. **Group size is around four students.**

## File format

All four submission pieces — Knowledge Base, PRD, System Instructions, and evaluation report — are submitted in **Markdown** (`.md`). PDF and Word are not accepted.

The reason is technical. The System Instructions get pasted into the Claude Project / ChatGPT Project configuration field — markdown or plain text only. The Knowledge Base gets attached as a file to the same Project — markdown gives the cleanest retrieval (PDFs are parsed lossy, Word loses structure). PRD and the evaluation report are markdown for consistency.

### Markdown in 30 seconds

Markdown is a plain-text format where light syntax produces structured documents. The methodology files in this folder are written in Markdown — open any one of them in a text editor to see the raw form. LLMs read and write it natively, which is why we use it.

**Where to write it (free):** VS Code, Typora, or Obsidian. All three render Markdown live as you type.

**The syntax you need:**

```
# Heading 1
## Heading 2
**bold** and *italic*
- list item
- another item

| Column A | Column B |
|---|---|
| value    | value    |

`inline code`
```

That covers everything you need. The official reference is at daringfireball.net/projects/markdown — you will not need more.

## Grading

Scored out of 500. Pass: 400. Distinction: 480+.

| Dimension | Weight | What I look for |
|-----------|--------|-----------------|
| **Domain rigour** | 100 | The KB is grounded in real frameworks from both halves of the course: **negotiation** (preparation, BATNA/ZOPA, leverage, value creation, concession strategy, and others taught in the course) and **cross-cultural** (Hofstede, Trompenaars, Meyer, GLOBE, Hall, and others). No hand-waving. No fabricated citations. |
| **Generalisation** | 100 | The agent genuinely supports any cultural axis a user might bring, not just the one in your test case. |
| **Coherence of design** | 100 | Knowledge Base, PRD, and System Instructions line up. No contradictions, no orphaned requirements, no behaviour leaking into the KB or knowledge leaking into the SI. |
| **Agent quality** | 100 | Tested on your real case and on at least one case outside its cultural axis, the agent performs at the level of a real cross-cultural negotiation expert. |
| **Evaluation honesty** | 100 | The evaluation surfaces real weaknesses. A polished agent with a thin eval scores lower than a rough agent with a sharp eval. |

**One automatic deduction:**
- Behaviour embedded in the KB, or knowledge dumped into the SI → **−50**

## Ground rules

- The agent is general. Your case tests it; it does not define it.
- **Cite real sources in your KB, and verify every citation.** Models routinely produce plausible-looking citations to books and papers that do not exist. Before any citation enters your KB, find the source on Google Scholar or in a library catalogue. If you cannot find it, the citation is fabricated — remove it. Fabricated citations are the fastest way to wreck your Domain rigour score.
- **This is a negotiation agent first, with cultural intelligence layered on top.** Cultural frameworks alone do not produce a negotiator. The agent must do the work of negotiation: preparation, leverage and BATNA/ZOPA analysis, value creation, concession sequencing, post-negotiation review. A culture commentary that names dimensions but never reaches a negotiation move is not what we are building.
- **Frameworks describe tendencies at a population level — not individuals.** Hofstede, Trompenaars, Meyer, GLOBE, Hall and the others give you statistical patterns across cultures. They are not a script for predicting any one person. An Indian who studied and lives in the US is not "an Indian negotiator." A bicultural counterpart may hold two cultural codes simultaneously and switch between them depending on context. Your KB must teach the frameworks *and* teach the exceptions: individual variation, biculturalism, generational shifts, expatriate adaptation, regional differences within a country. Your agent must apply frameworks as hypotheses to test, not as labels to apply.
- Use the model as a thinking partner, not a ghostwriter. I am evaluating *your* judgement.
- Iterate. First drafts of the PRD and SI will be incomplete.
- Bring drafts to office hours at any stage.
