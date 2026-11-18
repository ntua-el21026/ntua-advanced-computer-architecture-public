# Project Structure Utility

This directory contains a small helper for producing a readable repository
tree.

## Files

- `project_struct.py`: walks the repository, honors `.gitignore`, and writes an
  ASCII tree.
- `project_struct.txt`: archived directory capture of the original coursework workspace. It records earlier contents and is preserved as provenance. Use the navigable [exercise index](../../exercises/README.md) for the current layout.

## Regeneration

From a disposable working copy, run this from the repository root to generate a separate current tree. The utility writes to the path recorded in the script.

```bash
python3 docs/project_structure/project_struct.py
```

The script requires the Python package `pathspec`.
