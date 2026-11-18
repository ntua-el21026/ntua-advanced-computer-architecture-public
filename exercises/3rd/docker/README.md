# Exercise 3 Docker Image

The [authorized local inputs](../../../EXTERNAL_INPUTS.md) document which course files must be supplied locally and how to reconstruct the mixed-source targets. Historical measurements are still included.

The Dockerfile records the pinned Sniper 8.0 build for Exercise 3. Building the image requires the authorized course wrapper at its historical path. Running the lock targets additionally requires the [assembled sources](../../../course-source-reconstruction/README.md) and the authorized configuration.

## Image

- Local image tag: `advca-sniper:8.0`.
- Base image: `snipersim/snipersim`, pinned by digest in `Dockerfile`.
- External helper: `advcomparch_mcpat.py`, supplied locally before it can be copied into Sniper's tools directory.

The image keeps Sniper itself unchanged except for permission compatibility
needed to run the container as the host WSL user.

## Workflow

With the [authorized inputs](../../../EXTERNAL_INPUTS.md) in the disposable working copy, use the controller script from that copy's root:

```bash
./exercises/3rd/scripts/run_sniper_docker.sh pull
./exercises/3rd/scripts/run_sniper_docker.sh build-image
./exercises/3rd/scripts/run_sniper_docker.sh check
./exercises/3rd/scripts/run_sniper_docker.sh smoke
```

On WSL, the CentOS 6 based Sniper image may require
`kernelCommandLine=vsyscall=emulate` in `%UserProfile%\.wslconfig`.
