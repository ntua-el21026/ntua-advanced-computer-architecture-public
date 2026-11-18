# Section 5.3 Results

This directory contains the branch-predictor comparison for Exercise 1.

## Contents

- `summary.csv`: per-benchmark predictor results.
- `summary_by_group.csv`: grouped predictor-family summary.
- `summary_by_predictor.csv`: aggregate view by predictor.
- `summary.txt`: human-readable summary.
- `train/`: raw train-input outputs.

## Regeneration

The existing summaries are historical results. New instrumented runs require the [authorized Pin, course, and SPEC inputs](../../../../EXTERNAL_INPUTS.md) and a disposable output tree.

From the repository root:

```bash
./exercises/1st/scripts/run_5_3_predictors.py
```
