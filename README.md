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
