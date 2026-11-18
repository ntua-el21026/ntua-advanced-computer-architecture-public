# Exercise 3 - Synchronization and Coherence

This directory contains the third Advanced Computer Architecture exercise. The
work studies TAS, TTAS, and pthread mutex synchronization under cache
coherence using Sniper 8.0, McPAT, and real-machine measurements.

## Contents

- [Assignment references](assignment/README.md) identify the external course statement and any assigned reading.
- [advcomparch-ex3-helpcode](advcomparch-ex3-helpcode/README.md) documents the retained build integration and exact locally supplied inputs.
- `docker/`: reproducible Sniper 8.0 image wrapper and compatibility fixes.
- `scripts/`: real-machine and Sniper experiment runners.
- `benchmarks/`: generated raw results, summaries, and diagrams.
- `report/`: final report source and compiled output.
- `decisions.md`: material implementation and evaluation decisions.

## Build

Assemble the three lock/build files using the [authorized source bases](../../course-source-reconstruction/README.md). From the resulting working copy, build a bounded real-machine check:

```bash
cd exercises/3rd/advcomparch-ex3-helpcode
make check-real BIN_DIR=/tmp/ntua-lock-check TEST_THREADS=2 TEST_ITERATIONS=1000 TEST_GRAIN=1
```

For Sniper runs, also provide the authorized configuration and McPAT wrapper described in the [input register](../../EXTERNAL_INPUTS.md). Inside the pinned Sniper container:

```bash
make sniper SNIPER_BASE_DIR=/root/sniper
```

See [the script guide](scripts/README.md) for the experiment commands and output layout.

On hardware matching the 16-physical/24-logical target, begin with the historical preflight and local checks in a disposable tree:

```bash
./exercises/3rd/scripts/preflight_16core.py
./exercises/3rd/scripts/run_sniper_docker.sh build-image
./exercises/3rd/scripts/run_sniper_docker.sh smoke
```

Run the full matrices only after the smoke test passes:

```bash
./exercises/3rd/scripts/run_sniper_docker.sh run-4.1
./exercises/3rd/scripts/run_sniper_docker.sh run-4.2
./exercises/3rd/scripts/run_4_1_real_scalability.py \
  --iterations 50000000 \
  --repeats 5 \
  --warmups 1
```

Generate report diagrams after all summaries exist:

```bash
python3 exercises/3rd/benchmarks/diagrams/make_diagrams.py
```

## Results and Report

Completed Sniper and real-machine summaries are stored under `benchmarks/4.1/`
and `benchmarks/4.2/`. The plotting workflow writes report-ready PNG/PDF
figures under `benchmarks/diagrams/`. The final report source and compiled PDF
are stored under `report/`.

## Interpreting the outputs

The real-machine runner records host timings; Sniper reports simulator timing/cycles, and McPAT estimates power/energy from the simulated configuration. Preserve those distinctions in comparisons. The 16-physical/24-logical preflight and container defaults describe the original target environment, so inspect affinity, resources, paths, and output roots before new execution. The [root guide](../../README.md) provides a smaller counter check and input/provenance requirements.
