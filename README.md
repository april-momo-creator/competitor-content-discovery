# Competitor Content Discovery

A Codex skill for building an evidence-based competitor map before analyzing social content.

Most competitor research starts too late: people search a few familiar brand names, collect viral posts, and then try to explain why those examples matter. This skill makes the upstream reasoning explicit. It moves from product understanding to competitor discovery, competitor layering, positioning, differentiation, social search design, and finally a traceable pool of content candidates.

The skill covers the **front half of competitor content research**. It is designed to answer:

- What does the product actually compete with?
- Which competitors deserve research attention, and why?
- Which products compete for the same purchase, solve the same pain differently, or simply communicate better to the same audience?
- What should be searched on each platform before content collection begins?
- How can every candidate, judgment, and content reference remain traceable to evidence?

## Research Architecture

```mermaid
flowchart LR
    A[Product intake] --> B[Candidate discovery]
    B --> C[Pool layering]
    C --> D[Positioning cards]
    D --> E[Differentiation hypotheses]
    E --> F[Owned social map]
    F --> G[Social search map]
    G --> H[Content candidate pool]
```

Each stage creates a structured input for the next. The workflow prevents downstream content research from being driven by familiar names, random platform browsing, or unsupported assumptions.

## Core Reasoning

### 1. Understand the product through six lenses

Product understanding is not a feature summary. The skill builds an initial keyword map from six different sources:

| Lens | What it reveals |
|---|---|
| Product functions | The formal category and capability language |
| User problems | How people describe the pain before knowing the solution |
| Use cases | The situations in which the product becomes relevant |
| Target users | Persona-specific language, needs, and buying context |
| Known alternatives | Existing comparison and substitution paths |
| Platform habits | Native phrases people actually search, post, and discuss |

Using all six lenses expands the research surface beyond products with similar features. It makes it possible to find direct competitors, indirect substitutes, attention competitors, and content references that would be invisible in a category-only search.

### 2. Discover candidates from five evidence environments

Candidate discovery is intentionally broad and defers classification. Every plausible candidate is recorded with the evidence line and source that surfaced it.

| Discovery signal | What it contributes to the map |
|---|---|
| Official comparison, alternative, pricing, and FAQ pages | Commercial competitors actively used in purchase decisions |
| Search results and repeated third-party lists | Category consensus and mainstream market players |
| Social platforms and attention pools | Brands and accounts competing for audience attention |
| Reviews, comments, stores, and community complaints | Real objections, substitute paths, and unmet needs |
| Products with overlapping personas | Aspirational examples of mature content, UGC, or community expression |

Together, these signals create a more complete competitor map across **commercial competition, category consensus, attention competition, substitution behavior, and audience culture**.

### 3. Layer the pool before deep research

A candidate is kept when it passes at least three of five gates:

1. **Problem relevance:** it addresses a core problem.
2. **User relevance:** it serves likely users, buyers, or influencers.
3. **Evidence sufficiency:** it appears in multiple meaningful sources, or in one strong explicit comparison.
4. **Content researchability:** it has observable social, review, creator, UGC, or community material.
5. **Actionability:** studying it can change positioning, content, objections, or search terms.

The surviving pool is divided by the decision it can inform:

| Layer | Classification logic | Why it is studied |
|---|---|---|
| Direct | Similar problem, function or scenario, and buying decision | Positioning, selling points, comparison and rebuttal angles |
| Indirect | Different category or workflow, but solves the same pain | Substitute behavior, category avoidance and counter-positioning |
| Aspirational | Overlapping audience with more mature content or UGC | Hooks, formats, creator models and platform-native expression |

A practical research allocation is approximately **60% direct, 20% indirect, and 20% aspirational**. Direct competitors remain the evidence core; indirect competitors reveal how users bypass the category; aspirational competitors prevent product relevance from being confused with content maturity.

## What the Skill Produces

| Stage | Deliverable | Decision enabled |
|---|---|---|
| Product intake | Product intake card and initial keyword map | Defines the research surface |
| Candidate discovery | Source-traced candidate pool | Shows who may matter before premature filtering |
| Pool layering | Prioritized direct, indirect, and aspirational pool | Allocates research depth and purpose |
| Positioning | Competitor Positioning Cards | Normalizes how each competitor sells itself |
| Differentiation | Differentiation Hypothesis Matrix | Converts differences into testable content angles |
| Owned social | Competitor Owned Social Map | Shows how competitors educate and activate the market |
| Search design | Platform-specific Social Search Map | Defines what to search, where, and why |
| Collection | Traceable content candidate pool | Creates the raw input for later deep analysis |

The skill deliberately stops before single-post deep analysis, winning and losing pattern synthesis, opportunity-gap synthesis, creator briefs, monitoring systems, and final reference-pool curation.

## Eight Workflow Modules

The executable instructions live in [`SKILL.md`](./SKILL.md). Detailed decision rules and output schemas are separated into focused references:

1. [`01-product-intake-keywords.md`](./references/01-product-intake-keywords.md)
2. [`02-competitor-candidate-discovery.md`](./references/02-competitor-candidate-discovery.md)
3. [`03-competitor-pool-layering.md`](./references/03-competitor-pool-layering.md)
4. [`04-competitor-positioning-card.md`](./references/04-competitor-positioning-card.md)
5. [`05-differentiation-hypothesis-matrix.md`](./references/05-differentiation-hypothesis-matrix.md)
6. [`06-owned-social-map.md`](./references/06-owned-social-map.md)
7. [`07-social-search-map-builder.md`](./references/07-social-search-map-builder.md)
8. [`08-content-candidate-collector.md`](./references/08-content-candidate-collector.md)

Codex loads only the references needed for the current request while enforcing the required upstream prerequisites.

## Installation

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/april-momo-creator/competitor-content-discovery.git ~/.codex/skills/competitor-content-discovery
```

Restart Codex after installation so the skill can be discovered in new tasks.

## Example Requests

```text
Use $competitor-content-discovery to build a competitor map for [product URL].
```

```text
Classify these products into direct, indirect, and aspirational competitors, and show the evidence behind each decision.
```

```text
Build a cross-platform Social Search Map before collecting content references for [product].
```

```text
Collect a traceable raw candidate pool from TikTok, Instagram, YouTube, Reddit, LinkedIn, and X using the approved search map.
```

## Evidence Discipline

- Current product, pricing, social, ranking, review, and content facts should be verified from live public sources.
- Official product pages and primary platform pages take priority over third-party summaries.
- Every candidate should preserve its source URL, discovery clue, date observed, and visible metrics when relevant.
- Facts, inferences, and items needing validation should remain visibly separate.
- Unknown classifications are allowed during discovery; premature certainty is not.

## Case Study

The skill was developed from a detailed manual competitor-research workflow and tested against a real AI product research case before being converted into a reusable Codex skill and reimplemented for use inside a social-media AI agent.

The interactive case study exposes the reasoning chain, decision gates, ownership boundaries, and validation process:

**[View the interactive case study](https://xinyue-competitor-skill-case.april41595.chatgpt.site)**

> The case-study site is currently access-restricted. Repository visitors without permission may not be able to open it.

## Repository Structure

```text
competitor-content-discovery/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── 01-product-intake-keywords.md
│   ├── 02-competitor-candidate-discovery.md
│   ├── 03-competitor-pool-layering.md
│   ├── 04-competitor-positioning-card.md
│   ├── 05-differentiation-hypothesis-matrix.md
│   ├── 06-owned-social-map.md
│   ├── 07-social-search-map-builder.md
│   └── 08-content-candidate-collector.md
└── LICENSE
```

## License

Released under the [MIT License](./LICENSE).
