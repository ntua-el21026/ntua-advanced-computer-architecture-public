# Local course-source assembly

The components below combine the original course base and changes recorded in the coursework. The overlay preserves changed lines and references unchanged lines by location. It does not include the course base. The original authorship and source attributions remain applicable to locally assembled sources.

Obtain the course edition through an authorized course account or source. [ntua-advanced-computer-architecture](https://www.ece.ntua.gr/en/education/undergraduate/courses?courseId=3352)

Place each input in an external directory under the relative path in the manifest. Run `python3 course-source-reconstruction/restore.py /path/to/authorized-bases /path/to/local-working-copy` from the project root. The script verifies both the source and reconstructed bytes and refuses existing outputs. Keep locally assembled sources and licensed inputs outside any redistributed snapshot.

| Local input path | Source | Required SHA-256 |
|---|---|---|
| `exercises/1st/advcomparch-ex1-helpcode/pintool/branch_predictor.h` | CSLab exercise 1 starter as recorded in initial import 8160b46 | `7dc008132b32b0400f2f76abc24a317fd8d518dc3f9315bcc5550d9709676213` |
| `exercises/1st/advcomparch-ex1-helpcode/pintool/cslab_branch.cpp` | CSLab exercise 1 starter as recorded in initial import 8160b46 | `c6802260cb2d3945ffa6979c27514a704c55419235fb756899500a785ce5e857` |
| `exercises/2nd/advcomparch-ex2-helpcode/pintool/cache.h` | CSLab 2025–26 exercise 2 starter package | `da854ccd6e26d81196600cfa54f48715526af0ec26ee42013eb526d61d20972b` |
| `exercises/2nd/advcomparch-ex2-helpcode/pintool/simulator.cpp` | CSLab 2025–26 exercise 2 starter package | `fa6d6ea7664130404b4b1e6178bbfd036e7b5db2793bf123653c62590cbbb622` |
| `exercises/3rd/advcomparch-ex3-helpcode/Makefile` | CSLab 2025–26 exercise 3 starter package | `73a43ef47025e010e3336f049b6cdd92689225b9b967f5ad279f8e157ecf4881` |
| `exercises/3rd/advcomparch-ex3-helpcode/lock.h` | CSLab 2025–26 exercise 3 starter package | `d08e79fb5d6cd16b25d412dd1e17cf3b79e5653688edbdd3e1906c7b110dcf6b` |
| `exercises/3rd/advcomparch-ex3-helpcode/locks_scalability.c` | CSLab 2025–26 exercise 3 starter package | `3a5e34c295a10dc4c671d017741fb4acbc78e4c721c374a2dda543ffeb04a980` |

Restore the associated exact course helper files at their original paths. See [external input instructions](../EXTERNAL_INPUTS.md) for Pin, SPEC, and the Sniper build.
