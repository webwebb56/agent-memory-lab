# EXP-0006 — Orthogonal auto-eval (low-token)

## Goal
Improve memory quality using **cheap, automatic signals** rather than question-based eval that costs operator attention and tokens.

## Hypothesis
Tracking redundant questions + retrieval cost + size caps + schema coverage will:
- reduce repeated asks
- keep curated memory compact
- increase practical recall reliability

## Intervention (minimal)
Maintain private files (not committed):
- `memory/schema.yml` — schema slots to cover
- `memory/metrics.jsonl` — append-only event log

## Signals
1. **Redundant-question rate**
   - Definition: agent asks for information that should be available in memory.
   - Capture: append an event when detected.

2. **Retrieval cost proxy**
   - Capture: rough count of file reads/tool calls used to answer.

3. **Size caps**
   - `memory/INDEX.md` target: <= 40 lines
   - `MEMORY.md` target: <= 200 lines

4. **Schema coverage**
   - Periodically verify the schema slots have an obvious home (INDEX/MEMORY/etc.).

## Cadence
Do checks only when already doing maintenance (e.g., consolidation every ~2 days).

## Success criteria
- Redundant-question incidents trend down over 2–4 weeks.
- Curated memory stays within caps.
