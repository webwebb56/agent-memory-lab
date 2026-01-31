# Research plan: Agent Memory Lab

## Goal
Design, test, and iterate **agent memory architectures** that improve:
- recall success
- time-to-retrieve
- robustness to context truncation/session restarts
- low “context spend” (tokens/time)

## Core model
We borrow from cognitive neuroscience and human knowledge systems:

- **Working memory** = current chat + loaded files
- **Medium-term** = daily logs / inbox / state files
- **Long-term** = curated memories + invariants + pointers

## Key claims to test
1. A tiny always-readable **INDEX/anchor** improves retrieval speed and reduces context spend.
2. **Threshold-based persistence** (“write before compression”) reduces information loss.
3. Periodic **consolidation** (“sleep”) improves long-term retrieval quality versus append-only logs.

## Method
- Each intervention is an experiment with:
  - hypothesis
  - protocol
  - metrics
  - pre-registered success criteria
- Prefer small changes + fast cycles.

## Ethics & privacy
- Never commit real personal messages, phone numbers, secrets, or live API keys.
- Use synthetic or redacted datasets for reproducibility.
