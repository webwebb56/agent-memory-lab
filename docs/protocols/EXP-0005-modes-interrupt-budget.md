# EXP-0005 — Modes + interrupt budget

## Hypothesis
Explicitly tracking a **primary mode** (Exploration / Decision / Construction / Grounding / Sparring / Synthesis / Escapism-check) and enforcing a small **hard-interrupt budget** will:
- reduce “interesting-but-empty” drift
- increase decision clarity and follow-through
- without increasing perceived friction

## Intervention
1. Maintain a private runtime state file (not committed):
   - current mode (nullable)
   - dials (pushback intensity, intervention frequency)
   - interrupt budget counters
2. The agent selects a **primary mode** per response.
3. A “hard interrupt” can be used at most **N** times per day/session.

### Definition: hard interrupt
A message that explicitly challenges the current trajectory and forces a choice, e.g.
- “This is elegant but fragile. Pick robustness or elegance.”
- “This looks like escapism. Do you want exploration or a decision?”

## Protocol

### Baseline (3 days)
- No explicit mode tracking.
- Log: perceived clarity, whether a next action was selected.

### Intervention (7 days)
- Use mode selection + budget.
- Log the same outcomes.

## Metrics
Primary:
- **Next-action rate**: % of substantive exchanges that end with a concrete next action.
- **Perceived clarity** (Andrew self-report 1–5, optional).

Secondary:
- **Hard interrupt count** used.
- **Annoyance** (Andrew self-report 1–5, optional).

## Success criteria
- Next-action rate increases by >= 20% OR
- Perceived clarity improves by >= 1 point
- without annoyance increasing by >= 1 point.

## Notes
- Mode labels should remain implicit unless they help.
- Safety/policy confirmations can occur regardless of mode.
