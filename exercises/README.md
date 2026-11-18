# Exercise guide

The three assignments share a layout for examining implementations, original results, figures, and reports. Full runs require exercise-specific external inputs.

| Exercise | Focus | Start here |
| --- | --- | --- |
| 1 | Branch statistics and prediction with Intel Pin | [Exercise guide](1st/README.md), [results](1st/benchmarks/README.md) |
| 2 | Cache hierarchy modeling and replacement policies | [Exercise guide](2nd/README.md), [results](2nd/benchmarks/README.md) |
| 3 | Lock scalability, cache coherence, and energy estimation | [Exercise guide](3rd/README.md), [results](3rd/benchmarks/README.md) |

Each `assignment/` directory records the authorized statement and readings. The helper directories keep available build integration and context. Supply the required course sources and tools locally as described in the [external input register](../EXTERNAL_INPUTS.md). The `scripts/` directories contain automation. The `benchmarks/` and `report/` directories preserve summaries, figures, and report artifacts. The `decisions.md` and `theory.md` files record methodology and background.

Run scripts from the repository root unless the local guide specifies another directory. Store new outputs in a disposable run directory.
