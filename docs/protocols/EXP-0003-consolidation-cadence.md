# EXP-0003 — Consolidation cadence (“sleep”) + pruning

## Hypothesis
A periodic consolidation routine (every 1–2 days) improves retrieval quality and reduces long-term noise compared with append-only memory.

## Intervention
Add a consolidation step that:
1. reviews recent daily logs (`memory/YYYY-MM-DD.md`)
2. extracts stable items into `MEMORY.md`
3. updates `memory/INDEX.md` pointers
4. prunes/archives low-value items (optional)

## Protocol

### Baseline (7 days)
- Append-only daily logs; minimal consolidation.

### Intervention (14 days)
- Run consolidation every 2 days.

## Promotion rubric (to `MEMORY.md`)
Promote only if one of:
- identity / preferences
- durable decision / policy
- recurring project fact that will be reused
- long-running commitment + dates

## Metrics
- Retrieval success on repeated queries
- Time-to-retrieve
- Size of `MEMORY.md` (lines)
- “Noise ratio”: items never referenced again (rough)

## Success criteria
- Improved time-to-retrieve OR improved recall success with `MEMORY.md` staying <= ~200 lines.

## Notes
Pruning is optional early; consolidation alone may be enough.
