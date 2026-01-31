# EXP-0004 — Semantic retrieval (embeddings/RAG)

## Hypothesis
Semantic search over curated memory artifacts outperforms keyword-only retrieval as the corpus grows.

## Intervention
Introduce a small semantic index over *curated* memory units (not raw chat logs), e.g.:
- decisions
- preferences
- SOPs
- project notes

## Protocol (staged)
1. Pilot with synthetic dataset (public) to validate tooling.
2. Local private index (not committed) for real usage.

## Metrics
- Top-k retrieval accuracy (manual grading)
- Time-to-retrieve
- Operator satisfaction

## Success criteria
- Higher accuracy than keyword search at similar or lower time-to-retrieve.

## Privacy
- Do not commit embeddings of private data.
