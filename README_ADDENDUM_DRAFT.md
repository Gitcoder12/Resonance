# Resonance — README Explanation Draft

## In plain language

A model-routing service concept that chooses which language model to call based on the task's cost, speed and quality requirements.

## Current status

Concept-stage; no runnable application is committed.

## Proposed first version

A user selects a task and cost/latency preferences. Resonance evaluates a few mock model options, explains its choice and returns a simulated response. Real provider integration is a later milestone.

## Technical direction

Define a provider interface, task profile, routing policy, cost/latency/quality metadata, timeout/fallback behavior and evaluation harness. Keep policy decisions inspectable.

## Privacy and cost control

Never silently forward prompts to third parties. Require user configuration, disclose provider destinations and define key handling and spend limits.

## Contributing

See FEATURE_UPGRADE_PLAN.md and CONTRIBUTING.md.
