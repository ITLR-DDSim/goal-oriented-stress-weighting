# Square duct

Training case: `Re_b_2600/`. Test cases: `Re_b_1100/` and `Re_b_1800/`.

OpenFOAM v1912 with `RASModel kOmega`. Each case contains initial/boundary fields (`0/`), physical and turbulence settings (`constant/`), and mesh-generation and numerical controls (`system/`). Run `blockMesh` and then `simpleFoam` in the case directory; see each case README for its settings.

Reference DNS: Pinelli et al. (2010); data are not included.
