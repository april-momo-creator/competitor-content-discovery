---
name: competitor-content-discovery
description: "Run the front half of competitor-related social content research: product intake and initial keywords, competitor candidate discovery, competitor pool layering, competitor positioning cards, product-vs-competitor differentiation hypotheses, owned social maps, social search maps, and cross-platform content candidate collection. Use when asked to identify competitors, classify direct/indirect/aspirational competitors, prepare competitor positioning or differentiation analysis, inspect competitor official social accounts, generate social search keywords, or collect raw content candidates before deeper content analysis."
---

# Competitor Content Discovery

## Scope

Use this skill for the research chain from product understanding to content candidate collection. It intentionally stops before single-content deep analysis, winning/losing pattern synthesis, opportunity-gap synthesis, creator briefs, risk review, monitoring systems, or final reference-pool curation.

The core logic is:

1. Understand the product before looking for competitors.
2. Discover who should be studied before judging their value.
3. Layer competitors before deep-diving them.
4. Understand how competitors sell themselves before deciding product differentiation.
5. Check owned social before generating social search maps.
6. Generate a search map before collecting cross-platform content candidates.

## Required Chain

When the user asks for a full competitor-related research workflow, complete these in order:

1. Product intake and initial keywords.
2. Competitor candidate discovery.
3. Competitor pool layering.
4. Competitor positioning cards.
5. Differentiation hypothesis matrix.
6. Owned social map.
7. Social search map.
8. Content candidate collection.

For partial requests, only run the needed scenario references, but enforce prerequisites:

- Do not run competitor discovery without enough product understanding. If missing, run `01-product-intake-keywords.md` first.
- Do not run positioning, differentiation, owned social, search map, or content collection without a competitor pool. If missing, run `02-competitor-candidate-discovery.md` and `03-competitor-pool-layering.md` first.
- Do not run differentiation without product intake plus competitor positioning inputs. If missing, run `04-competitor-positioning-card.md` first.
- Do not collect content candidates without a Social Search Map. If missing, run `07-social-search-map-builder.md` first.

If the user provides an upstream artifact, verify it is usable instead of recreating it. A usable artifact includes enough names, links, type labels, and evidence to support the next step.

## Scenario References

Load exactly the needed reference file(s):

| User asks for | Load | Required? | Output |
|---|---|---:|---|
| Understand product, extract target users/use cases/pains/selling points/initial keywords | `references/01-product-intake-keywords.md` | Always first if product context is weak | Product intake card + initial keyword map |
| Find competitor candidates from multiple clues | `references/02-competitor-candidate-discovery.md` | Required if no candidate list exists | Competitor candidate pool |
| Classify direct/indirect/aspirational competitors and priority pool | `references/03-competitor-pool-layering.md` | Required before deep research | Layered competitor pool |
| Scan competitor website and positioning | `references/04-competitor-positioning-card.md` | Required before differentiation | Competitor Positioning Card |
| Compare product vs competitors for contentizable differences | `references/05-differentiation-hypothesis-matrix.md` | Required before search-map generation | Differentiation hypothesis matrix |
| Inspect competitor official social accounts | `references/06-owned-social-map.md` | Required when the user asks about competitor social/content | Competitor Owned Social Map |
| Build second-round social search terms | `references/07-social-search-map-builder.md` | Required before content candidate collection | Social Search Map |
| Collect raw cross-platform content candidates | `references/08-content-candidate-collector.md` | Required only when content mining is requested | Content candidate pool |

## Evidence Rules

For live product, competitor, pricing, social, review, ranking, or content data, verify from current public sources. Prefer official websites and primary platform pages first, then reputable third-party sources. Capture source URL, platform, date observed, and visible metrics when relevant.

Separate facts from hypotheses. Use "verified", "inferred", and "needs validation" when evidence strength differs.

## Output Style

Match the user's language. Use compact tables for pools, maps, cards, and matrices. Keep synthesis short and actionable. Every deliverable should make the next step easier to run.

Do not include final reference-pool curation, winning/losing pattern synthesis, or opportunity-gap synthesis in this skill unless the user explicitly asks to extend the skill scope.
