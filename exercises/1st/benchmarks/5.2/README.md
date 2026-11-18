# Section 5.2 Results

This directory contains the branch-instruction statistics for Exercise 1.

## Contents

- `summary.csv`: machine-readable branch statistics.
- `summary.txt`: human-readable summary.
- `train/`: raw outputs for train inputs.
- `ref/`: raw outputs for ref inputs.

## Regeneration

The existing summaries are historical results. New instrumented runs require the [authorized Pin, course, and SPEC inputs](../../../../EXTERNAL_INPUTS.md) and a disposable output tree.

From the repository root:

```bash
./exercises/1st/scripts/run_5_2_branch_stats.py --input both
```
