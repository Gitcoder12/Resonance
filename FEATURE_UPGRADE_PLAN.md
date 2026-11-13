# Resonance — Feature Upgrade Plan

## Objective

A model-routing service concept that chooses which language model to call based on the task's cost, speed and quality requirements.

## Stage 0 — define routing objective

- [ ] Define task taxonomy, quality criteria, budget and latency constraints.
- [ ] Define provider data/privacy expectations and key handling.

## P0 — mock routing MVP

- [ ] Define task categories and a transparent routing policy with explicit fallback behavior.
- [ ] Build a deterministic mock provider interface and test routing decisions without real API calls.

## P1 — real adapter contracts

- [ ] Add provider adapters with timeouts, token/cost metadata and structured errors.
- [ ] Expose routing rationale and let users set budget/latency/quality preferences.

## P2 — empirical routing

- [ ] Evaluate quality, latency and cost on a fixed prompt set with repeated measurements.
- [ ] Add policy learning only after baseline performance and provider data handling are documented.

## First milestone acceptance

- [ ] Fixed fixture prompts are routed to mock providers deterministically.
- [ ] Every route decision has a human-readable reason.
- [ ] Provider errors and missing configuration are tested.
- [ ] No prompt is sent to a real provider without explicit user configuration.
