# Section 5.4 Results

This directory contains the branch target buffer study for Exercise 1.

## Contents

- `summary.csv`: per-benchmark BTB results.
- `summary_by_btb.csv`: aggregate view by BTB configuration.
- `summary.txt`: human-readable summary.
- `train/`: raw train-input outputs.

## Regeneration

The existing summaries are historical results. New instrumented runs require the [authorized Pin, course, and SPEC inputs](../../../../EXTERNAL_INPUTS.md) and a disposable output tree.

From the repository root:

```bash
./exercises/1st/scripts/run_5_4_btb.py
```
