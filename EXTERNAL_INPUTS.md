# Authorized local inputs

This snapshot keeps original experimental analysis, exact timing and counter results, and locally reproducible course setup instructions. Existing MIT terms apply to original project contributions. The two exact Sniper headers retain the bundled revision-specific [upstream notice](LICENSES/Sniper-7500506.txt).

## What the original inputs provided

| Original material | Role and retained evidence | Reproduction |
| --- | --- | --- |
| Course statements and lecture decks | Defined tasks, metrics and conceptual background. The reports, student notes and results are available. Obtain the exact course edition through the NTUA entry points below. | Full inspection of the retained work. Original teaching material requires authorized access. |
| Research papers | Supported the choice of averaging and predictor models. Publisher links and the student analysis remain. | Full inspection, with external reading. |
| SPEC workloads and runner harness | 29 workload executables, seven LFS pointer paths to benchmark inputs, 34 preprocessed GCC/assembly items, 111 supplied input or reference artifacts, and 58 harness/comparison files were omitted. The manifests, scripts, selected logs and original section summaries are available. | Conditional on authorized, matching CPU2006 inputs and the exact invocation. |
| Xalan data-bearing captures | Nine captures that included transformed workload data were reduced to factual records pointing to the existing measurements. | Partial from the retained tables; conditional for exact replay. |
| Pin and the CSLab build baselines | Pin runs the instrumented client. The course bases provide simulator, predictor, lock and build components needed to assemble or build the student changes. The seven mixed-source assemblies, student drivers, and two verified Sniper headers are available. The prior starter archives are external. | Conditional on matching authorized course files and a compatible Pin installation where applicable. |
| Course Sniper configuration and McPAT inputs | The configuration and wrapper drive timing simulation and power estimation. Original parameter, counter, timing and aggregate results, including the 90 `power.values.csv` extracts, remain. | Full inspection of recorded values, conditional replay with authorized tooling and configuration. |

## Course and publisher material

| Original relative path | Publisher or course reference |
|---|---|
| `docs/lectures/Lec01-overview.pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec02-Superscalar-SW-VLIW (loop unroling).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec03-dynamic (SCOREBOARD - TOMASULO).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec04-branch_pred (predictors).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec05-speculation (TOMASULO ROB).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec06-SIMD (vectors).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec07-Simulation.pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec08-TLP (multithread).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec09-GPU (loop-level parallelism).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec10-Coherence (MSI - MESI).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec11-MemoryConsistency (TSO-TAS-TTAS).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `docs/lectures/Lec12-interconnects (networks).pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `exercises/1st/assignment/advanced-ca-2025-2026-askisi1.pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `exercises/2nd/assignment/advanced-ca-2025-2026-askisi2.pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `exercises/3rd/assignment/advanced-ca-2025-2026-askisi3.pdf` | [Authorized source or course index](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352) |
| `exercises/1st/assignment/CAL-2024-geomean.pdf` | [Authorized source or course index](https://users.elis.ugent.be/~leeckhou/papers/CAL-2024-geomean.pdf) |
| `exercises/1st/assignment/Dynamic Branch Prediction with Perceptrons.pdf` | [Authorized source or course index](https://www.cs.utexas.edu/~lin/papers/hpca01.pdf) |
| `exercises/1st/assignment/Optimal 2-BitBranchPredictors.pdf` | [Authorized source or course index](https://research.ibm.com/publications/optimal-2-bit-branch-predictors) |

## Instructor dependencies

Use the exact 2025–26 starter release from the authorized course source. Follow the [source assembly procedure](course-source-reconstruction/README.md), and supply these additional files at their historical paths in a local working copy. The nine adapted Pentium-M headers are edition-specific. An MIT Sniper equivalent can be investigated separately but is not evidence of historical equivalence.

- `exercises/1st/advcomparch-ex1-helpcode/pintool/cslab_branch_stats.cpp`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/ras.h`
- `exercises/2nd/advcomparch-ex2-helpcode/pintool/globals.h`
- `exercises/2nd/advcomparch-ex2-helpcode/run_benchmarks.sh`
- `exercises/3rd/advcomparch-ex3-helpcode/ask3.cfg`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/branch_predictor_return_value.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/global_predictor.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/lpb.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/pentium_m_bimodal_table.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/pentium_m_branch_predictor.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/pentium_m_branch_target_buffer.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/pentium_m_indirect_branch_target_buffer.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/saturating_predictor.h`
- `exercises/1st/advcomparch-ex1-helpcode/pintool/pentium_m_predictor/simple_bimodal_table.h`
- `exercises/3rd/advcomparch-ex3-helpcode/advcomparch_mcpat.py`

## Pin, SPEC, and Sniper

Install a compatible [Intel Pin kit](https://www.intel.com/content/www/us/en/developer/articles/tool/pin-a-binary-instrumentation-tool-downloads.html) and pass its root using `make PIN_ROOT=/path/to/kit`. A separately licensed [SPEC CPU2006](https://www.spec.org/cpu2006/) kit is required for exact workloads. Supply the binaries, data, and comparison rules locally at `exercises/1st/advcomparch-ex1-helpcode/spec_execs_{train,ref}_inputs/` and `exercises/2nd/advcomparch-ex2-helpcode/spec_benchmarks/`, as described in the [dependency manifest](SPEC_DEPENDENCY_MANIFEST.md). Do not treat preserved empty files as usable benchmark inputs. The original run captures and summaries describe coursework on selected workloads rather than official CPU2006 scores.

For Exercise 3, place the authorized course McPAT wrapper at its original path before using the existing Docker build context. The pinned Sniper image is unchanged. The `power.values.csv` files store original component names, parameter values and statistics without redistributing the historical XML template. The authorized Sniper/McPAT tooling generates XML during a full reproduction.
