# yk/do52pro

Minimal QMK target for the DO52 Pro split keyboard with:

- RP2040 Pro Micro-compatible controllers
- wired serial split
- right half as USB/master
- PS/2 trackpoint on the right half
- two 5-way switch clusters

Build:

```sh
qmk compile -kb yk/do52pro -km default
```

Notes:

- The main matrix and right-half column mirroring follow the public DO42/DO52 layout style.
- The two 5-way clusters are assumed to live on the last row of each half:
  left `row 5, col 0..4`, right `row 11, col 4..0`.
- If a D-pad direction reads in the wrong spot on real hardware, only the
  matrix indices for those ten keys should need adjustment.
- `EE_HANDS` is enabled so each half can be marked left/right independently.
