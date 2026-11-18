# Exercise 1 build and workload inputs

The course statistics collector and return-address-stack model are external. The direction-predictor and branch-driver changes are available as source-assembly records. The two exact upstream Sniper headers remain in the predictor tree alongside the applicable MIT notice.

See the [pintool guide](pintool/README.md) and [authorized input register](../../../EXTERNAL_INPUTS.md). The SPEC train/reference executables, inputs, and comparison harness are externally obtained from an authorized matching kit. Historical runner scripts, where present, and the [benchmark evidence](../benchmarks/README.md) preserve the original workload selections, configurations, metrics, and timing context. Follow the [SPEC dependency manifest](../../../SPEC_DEPENDENCY_MANIFEST.md) for exact placement. Run newly authorized workloads in a disposable copy.

The `pintool/` directory contains the available build integration. Supply the exact course `cslab_branch_stats.cpp` and assemble `cslab_branch.cpp` locally using the required baseline and retained changes. `make PIN_ROOT=/path/to/pin` is conditional on both the complete sources and a compatible Intel Pin kit.
