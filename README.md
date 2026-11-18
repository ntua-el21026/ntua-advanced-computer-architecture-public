# Advanced Computer Architecture

Three NTUA ECE studies by **Michail Athanasios Peppas** investigate branch prediction, two-level cache design, and synchronization. The portfolio includes experiment drivers, simulator changes, per-workload results, plots, and the May–June 2026 reports. The studies use Intel Pin for branch and cache instrumentation, host timing for the lock experiments, and Sniper and McPAT for simulated timing and modeled energy.

| Study | Engineering contribution | Evidence |
| --- | --- | --- |
| [Branch prediction](exercises/1st/README.md) | Instrument branch categories and compare direction predictors, branch-target buffers, return-address stacks, and perceptrons. The reference-input study compares three selected predictors on 11 workloads. | [Reference-input results](exercises/1st/benchmarks/5.7/summary_by_predictor.csv), [report](exercises/1st/report/03121026_1.pdf) |
| [Cache hierarchy](exercises/2nd/README.md) | Extend a two-level cache simulator and sweep L2 capacity, associativity, and block size. Compare LRU, MRU, Random, LFU, LIP, and SRRIP under selected configurations. | [L2 sweep](exercises/2nd/benchmarks/4.2/summary_by_config.csv), [policy comparisons](exercises/2nd/benchmarks/4.3/summary_by_policy.csv), [report](exercises/2nd/report/03121026_2.pdf) |
| [Synchronization and coherence](exercises/3rd/README.md) | Compare TAS and TTAS variants based on compare-and-swap or test-and-set with a pthread mutex. Evaluate lock scaling on the host and cache-sharing topologies in simulation. | [Host timing](exercises/3rd/benchmarks/4.1/real/summary.csv), [simulated topology results](exercises/3rd/benchmarks/4.2/summary.csv), [report](exercises/3rd/report/03121026_3.pdf) |

On the recorded reference-input workloads, Perceptron-M141-N32 had the lowest arithmetic mean direction MPKI (2.634), while Perceptron-M56-N72 had the lowest instruction-weighted direction MPKI (1.110). MPKI measures misses per thousand instructions. The [reference-input summary](exercises/1st/benchmarks/5.7/summary_by_predictor.csv) reports both aggregations for all three predictors.

## Reproduction and scope

The reports, tables, and diagrams can be inspected locally. Exercises 1 and 2 require a compatible Intel Pin kit, exact authorized CSLab starter files, and licensed SPEC CPU2006 workloads at the documented paths. Exercise 3 requires the authorized synchronization source bases for local assembly. The host path uses Linux, GCC, GNU Make, pthreads, CPU affinity, and `timeout`. The simulation path adds the pinned Sniper 8.0 container and the course McPAT wrapper and configuration.

Begin with the [external input register](EXTERNAL_INPUTS.md), [source assembly instructions](course-source-reconstruction/README.md), and [SPEC workload manifest](SPEC_DEPENDENCY_MANIFEST.md). The snapshot includes workload metadata and selected recorded counters and timings. Obtain any required benchmark files through authorized course or SPEC access.

To set up a working copy from the GitHub repository, run the following commands.

```bash
git clone https://github.com/ntua-el21026/ntua-advanced-computer-architecture-public.git
cd ntua-advanced-computer-architecture-public
```

Build Pin targets after restoring their exact source bases and companion files, then set `PIN_ROOT` to your installation. Run the experiment drivers from the project root. Use a separate output directory where supported or a disposable working copy, particularly for regeneration and summary commands that can write to the existing benchmark trees. The [exercise index](exercises/README.md) and [supporting documentation](docs/README.md) map the evidence and run instructions.

## Validation and limitations

Local verification reconstructed and hash-checked seven source files using the exact course bases, parsed 110 Python files, and syntax-checked the three Sniper shell entry points. In a disposable build, all five lock variants reached the expected protected counter value of 2,000 with two threads and 1,000 iterations per thread. The [lock exercise build instructions](exercises/3rd/advcomparch-ex3-helpcode/README.md) describe the check. Reproducing the recorded Pin, SPEC, Sniper, or host performance results requires the corresponding inputs and environment.

Pin-derived branch miss rates and cache IPC describe the instrumented models and selected workloads. Host lock timings are measurements on the recorded machine. Sniper cycles and McPAT power and energy are estimates for the simulated configuration. The CPU2006 suite is retired, and these are coursework observations with recorded configuration and hardware scope.

## Attribution

Original contributions are covered by the [project MIT license](LICENSE). The two byte-matched upstream Sniper headers retain their [revision-specific notice](LICENSES/Sniper-7500506.txt). CSLab materials, publications, Pin, SPEC, Sniper, and McPAT have separate terms.
