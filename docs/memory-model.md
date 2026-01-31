# Memory model

## Human analogy
Humans use:
- books (knowledge stores)
- tables of contents (summaries)
- indexes (fast lookup)
- value-based filtering (attention)
- consolidation (sleep)

## Agent mapping
- **System prompt / SOUL**: invariants and behavioral constraints ("system 1")
- **Curated long-term memory**: durable facts/preferences/decisions ("system 2")
- **Daily logs**: verbose traces and raw events
- **Index / anchor**: a one-screen map pointing to the right place

## Failure modes
- Retrieval failure (missing cues)
- Overgrowth (memory becomes a junk drawer)
- Overcompression (summaries lose key details)

## Design principles
- Separate *storage* from *retrieval cues*
- Prefer pointers + rubrics over dumping raw text
- Schedule consolidation
