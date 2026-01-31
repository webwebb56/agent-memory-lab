# Metrics

## Primary
- **Recall success rate**: does the agent retrieve the correct item when needed?
- **Time-to-retrieve**: elapsed time + number of file/tool reads
- **Context spend**: how much history/files had to be loaded

## Secondary
- **Stability**: does memory remain coherent over time?
- **Noise ratio**: proportion of stored items that are never used again

## Logging
Each experiment should produce a short `results/<date>_<exp>.md` with:
- setup
- run notes
- measured outcomes
- decision: keep / modify / revert
