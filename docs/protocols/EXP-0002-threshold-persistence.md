# EXP-0002 — Threshold-based persistence (“write before compression”)

## Hypothesis
Proactively persisting high-value facts/decisions when a conversation is getting “large” reduces post-compaction/session-restart information loss.

## Intervention
Introduce a **checkpoint** routine that writes a small, structured update to disk **before** context is likely to be truncated.

### Trigger (practical)
Any of:
- long/complex thread (operator subjective)
- large tool output(s)
- end-of-day
- explicit operator command: “checkpoint”

(We can later replace this with a quantitative trigger if we can reliably estimate context usage.)

### Checkpoint format
Write to `memory/YYYY-MM-DD.md` and, if stable, promote to `MEMORY.md`.

Checklist:
- New decisions made
- New preferences learned
- Commitments + dates
- Open loops

## Protocol

### Baseline (3 days)
- No checkpoints.
- Log any “forgotten detail” incidents.

### Intervention (7 days)
- Run a checkpoint at least once per day and whenever a trigger occurs.
- Log forgotten-detail incidents and time-to-retrieve.

## Metrics
- Forgotten-detail incidents per day
- Time-to-retrieve for recurring facts
- Number of promotions to `MEMORY.md`

## Success criteria
- >= 50% reduction in forgotten-detail incidents during intervention.

## Risks
- Over-writing noise into long-term memory (mitigate with promotion rubric).
