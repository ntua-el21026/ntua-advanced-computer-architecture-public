# Exercise 1 Intel Pin instrumentation

The course statistics collector and return-address-stack model are external. The direction-predictor and branch-driver changes are available as source-assembly records. The two exact upstream Sniper headers remain in the predictor tree alongside the applicable MIT notice.

From the [external input register](../../../../EXTERNAL_INPUTS.md), obtain the matching course release, companion sources, and a compatible Intel Pin kit. Run the [verified source assembly](../../../../course-source-reconstruction/README.md) in a disposable working copy. Build from this directory in that copy using:

```bash
make PIN_ROOT=/path/to/pin
```

The retained `makefile` and `makefile.rules` integrate the target with the locally installed Pin kit. Use the [exercise guide](../../README.md) for experiment and output paths.
