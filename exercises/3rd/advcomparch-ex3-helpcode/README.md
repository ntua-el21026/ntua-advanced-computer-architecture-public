# Exercise 3 lock benchmark and build inputs

The synchronization benchmark compares TAS and TTAS using compare-and-swap or test-and-set, together with a pthread mutex baseline. The student modifications are preserved as [hash-verified assembly records](../../../course-source-reconstruction/README.md) for `locks_scalability.c`, `lock.h`, and `Makefile`. Assemble these files against the exact authorized baseline in a disposable working copy.

## Host counter check

From this directory in the assembled copy:

```bash
make check-real BIN_DIR=/tmp/ntua-lock-check   TEST_THREADS=2 TEST_ITERATIONS=1000 TEST_GRAIN=1
```

Use a fresh output directory. The check compiles and validates the five lock variants for that bounded configuration. Its counter expectation is `nthreads * iterations`. It is separate from the [historical host timing and simulation results](../benchmarks/README.md).

## Simulator configuration

The original `ask3.cfg` selects the simulated topology. The course `advcomparch_mcpat.py` wrapper maps Sniper outputs into the McPAT workflow. Obtain both from the authorized course source and supply them at their original paths in the working copy. The [container build guide](../docker/README.md) describes the existing pinned image workflow. Its simulated results and modeled energy are distinct from host timings.
