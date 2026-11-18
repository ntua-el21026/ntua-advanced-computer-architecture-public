# Exercise 2 build and workload inputs

The cache hierarchy, replacement-policy and reporting changes are available as source-assembly records for `cache.h` and `simulator.cpp`. The exact `globals.h` and the historical `run_benchmarks.sh` belong to the course baseline.

See the [pintool guide](pintool/README.md) and [authorized input register](../../../EXTERNAL_INPUTS.md). The SPEC train/reference executables, inputs, and comparison harness are externally obtained from an authorized matching kit. Historical runner scripts, where present, and the [benchmark evidence](../benchmarks/README.md) preserve the original workload selections, configurations, metrics, and timing context. Follow the [SPEC dependency manifest](../../../SPEC_DEPENDENCY_MANIFEST.md) for exact placement. Run newly authorized workloads in a disposable copy.

The `pintool/` directory contains the available build integration. The completed `simulator.cpp` source is supplied or constructed locally as documented. `make PIN_ROOT=/path/to/pin` is conditional on both the complete sources and a compatible Intel Pin kit.
