# goal-oriented-stress-weighting

Solvers and supporting data for goal-oriented turbulence-model training, including adjoint calculations, the weighting procedure, and case setups for reproducing the study.

## Current status

Documentation-only folder structure. Solver code, weighting scripts and case files will be added separately; this is not yet a runnable reproduction package.

## Contents

- [Solvers](solvers/README.md): three planned OpenFOAM v1912 custom solvers.
- [Weight construction](weights/README.md): sensitivity conversion and global/cellwise weights.
- [Case set-ups](cases/README.md): square-duct and periodic-hill training and test conditions.
- [Environment](environment/README.md): dependencies and planned build instructions.
- [Data sources](data-sources/README.md): external references and access limitations. No datasets are included.

No learned-closure implementation is included. Jet-in-crossflow case files are excluded pending coordination with Prof. Jee’s group, and no release of LES fields is promised. Licensing and citation metadata remain to be added by the maintainers.
