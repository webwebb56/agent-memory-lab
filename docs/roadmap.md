# Roadmap

## EXP-0001: Anchor/Index file
- Intervention: introduce a <= 30 line `INDEX.md` pointing to key memory chunks.
- Measure: retrieval speed + context spend.

## EXP-0002: Threshold-based persistence
- Intervention: when context crosses a threshold, persist key facts/decisions *before* compaction.

## EXP-0003: Consolidation cadence
- Intervention: every N days, distill daily logs → curated memory; prune noise.

## EXP-0004: Semantic retrieval
- Intervention: vector store / embeddings for retrieval across long history.
