# Exercise 2 Intel Pin instrumentation

The cache hierarchy, replacement-policy and reporting changes are available as source-assembly records for `cache.h` and `simulator.cpp`. The exact `globals.h` and the historical `run_benchmarks.sh` belong to the course baseline.

From the [external input register](../../../../EXTERNAL_INPUTS.md), obtain the matching course release, companion sources, and a compatible Intel Pin kit. Run the [verified source assembly](../../../../course-source-reconstruction/README.md) in a disposable working copy. Build from this directory in that copy using:

```bash
make PIN_ROOT=/path/to/pin
```

The retained `makefile` and `makefile.rules` integrate the target with the locally installed Pin kit. Use the [exercise guide](../../README.md) for experiment and output paths.
