# Resonance
Route any prompt to the best LLM — cost, speed, quality, automatic.


---

## AI-maintained project notes (secondary — 2026-11-13)

This section supplements the maintainer-authored README above; it does not replace or certify original claims.

- The current source tree, runtime configuration and executed tests are the implementation source of truth. Roadmap items and draft PRs are not shipped functionality.
- Preserve original model configurations, benchmark inputs and user-provided data. Never substitute synthetic or placeholder records silently.
- Record provider/model versions, prompt/configuration, seeds, latency/cost methodology, environment and reproducible test outputs for evaluation claims.
- Mark unverified metrics and unsupported provider capabilities as unknown/unverified.
- See [MODEL_AUDIT_ROUTER.md](MODEL_AUDIT_ROUTER.md) for independent model review instructions.

---

## Engineering Audit & Handover — 2026-11-17

**Reviewed commit:** `c57136e485c7c2f00144a28faa7a88ff886a06dc` (`main`).

### Confirmed findings
- The reviewed branch contains only `README.md`, `LICENSE`, and `MODEL_AUDIT_ROUTER.md`; no executable application source or automated tests were found.
- The described automatic LLM routing by cost, speed, and quality is not demonstrated by runnable code on this branch.

### Next actions
1. Define the provider/model registry, supported routing criteria, and fallback behavior.
2. Implement a minimal end-to-end router with explicit provider timeouts and secret handling.
3. Add a reproducible evaluation dataset for quality, latency, and cost before claiming that one model is “best.”

**Verification status:** source-tree inspection only; no runnable product or test suite verified.

---

## Examples Used
- Routing a low-latency request to a fast model
- Selecting a lower-cost model for a simple classification task
- Comparing provider quality, latency, and cost on the same prompt


---

## Comparison with Existing Open-Source Projects

Resonance is described as a router that selects an LLM based on cost, speed and quality. The current README is minimal and the reviewed branch contains documentation but no executable routing implementation or automated tests. These projects are relevant model-routing and evaluation references.

| Project | Established focus | Relationship to Resonance |
|---|---|---|
| [LiteLLM](https://github.com/BerriAI/litellm) | Unified API interface, provider routing, fallbacks and spend tracking across many LLMs | A mature provider gateway; Resonance's proposed distinction is choosing a model based on measured task-specific quality, latency and cost rather than only exposing a common API. |
| [RouteLLM](https://github.com/lm-sys/RouteLLM) | Research and tooling for routing requests between models based on capability/cost trade-offs | A close conceptual comparator; Resonance should define its own routing policy and benchmark protocol before claiming an advantage. |
| [LangChain](https://github.com/langchain-ai/langchain) | Framework for building LLM applications and model integrations | A broad application framework; Resonance's stated scope is narrower and centres on model selection/routing. |

### Where Resonance could be different
- **Decision-focused routing:** the product idea is to choose a model per request using multiple criteria, not simply expose many providers.
- **Cost/speed/quality trade-off:** the concept treats these as explicit dimensions of routing policy.
- **Potential task-aware selection:** it could use a benchmark suite to learn which model performs best for different task classes.

### Where established projects are stronger
LiteLLM has broad provider support and operational features; RouteLLM is a direct research reference for model routing. The current Resonance branch does not demonstrate a working router, provider registry, fallback behavior or measured routing quality.

### Evidence and limitations
Define a representative task set, quality rubric, latency measurement, token/cost accounting and provider/model versions. Report routing regret against the best model per task and include fallback/error behavior. “Best model” is task- and date-dependent; do not claim universal superiority. This is a concept comparison, not a routing benchmark.
