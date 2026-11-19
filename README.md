# BridgeMap

Cross-lingual public reasoning engine: maps a political dispute into an argument graph from Chinese- and English-language sources, separating factual from value disagreements and highlighting claims that appear in only one ecosystem.

> Status: skeleton only. No implementation yet.

## Pipeline
1. Ingestion → `src/ingest/`
2. Claim extraction → `src/extract/`
3. Cross-lingual clustering → `src/cluster/`
4. Argument graph + evidence → `src/graph/`
5. Steelmen → `src/steelman/`
6. Evaluation → `evaluation/`

## Layout
```
data/        raw/{zh,en}, processed, gold (hand-labelled test sets)
schemas/     JSON schemas shared by every stage
configs/     thresholds and model settings
src/         pipeline stages + prompts
review/      human review tool
frontend/    static public site
evaluation/  reader benchmarks (ITT, omission, loaded language, parity)
tests/       automated checks
docs/        architecture, principles, evaluation, Devin handoff
```

See `docs/` for design notes.
