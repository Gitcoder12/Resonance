# Project Status — Resonance

**Snapshot date:** 2026-11-16  
**Status type:** Initial documentation and repository-tree assessment  
**Default branch:** main  
**Review completeness:** Partial — not a code audit or release certification

## Project purpose
Concept for routing prompts to a suitable LLM based on cost, speed and quality.

## Current maturity (README-declared or upstream description; not independently verified)
Observed root contains only README.md, LICENSE and MODEL_AUDIT_ROUTER.md; no routing implementation, provider adapters, manifest or tests were visible.

## Observed repository structure
README.md, LICENSE and MODEL_AUDIT_ROUTER.md.

## Known issues and risks to investigate
README states automatic best-model routing, but there is no implementation evidence in the root. 'Best' requires a defined workload, model set, evaluation data and cost/latency/quality trade-off. Provider pricing and capabilities change over time. No tests or benchmarks exist in the observed root.

## Recommended next actions
Treat as concept until runnable code is added; define task categories and measurable router objective; build a static benchmark of candidate models and tasks; record dated prices/model versions; compare router against fixed-model and round-robin baselines; avoid claiming automatic optimal routing without evidence.

## Verification record
| Check | Result |
|---|---|
| Repository metadata / fork relationship | Not applicable / not checked |
| Default-branch top-level tree | Inspected |
| README | Inspected |
| Deep source review | Not performed |
| Tests / build / runtime | Not run |
| Security / dependency audit | Not run |
| Independent review | Not performed |

## Change log
- 2026-11-16: Added this initial status snapshot on a review branch. No application code or existing data changed.

> Update this file only after the corresponding inspection or verification has actually been performed. Distinguish observed facts, README claims, hypotheses and unrun checks.