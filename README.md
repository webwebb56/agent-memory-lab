# Agent Memory Lab

A research repo for **experimenting with practical, reproducible memory systems for tool-using agents**.

This project treats agent memory as an engineering + science problem:
- Clear hypotheses
- Measurable outcomes
- Version-controlled interventions
- Iteration based on results

## Principles

- **Privacy first:** real personal memory/state stays out of git. Use synthetic data + redacted examples.
- **Layered memory:** working context vs medium-term logs vs curated long-term memory.
- **Forgetting is a feature:** pruning + consolidation beats unlimited accumulation.

## Repo layout

- `docs/` — research plan, conceptual model, protocols, metrics
- `experiments/` — each experiment has its own folder + protocol + results
- `src/` — scripts/automation to support experiments
- `results/` — summaries, plots, tables (small)
- `data/` — example datasets only (`data/private` is ignored)

## Getting started

1. Read the research plan: `docs/research-plan.md`
2. Pick the next experiment in `docs/roadmap.md`
3. Run the protocol and log results in `results/`

## License

TBD (defaulting to MIT once confirmed).
