# Solvers

Planned custom solvers for OpenFOAM v1912. Documentation only; source code has not yet been added.

- `incompressibleAdjointFoam/`: incompressible RANS adjoint for square duct and periodic hill (formerly `pehillAdjointFoam`).
- `compressibleAdjointFoam/`: compressible counterpart for jet in crossflow (formerly `jicAdjointFoam`).
- `incompressibleFrozenOmegaFoam/`: omega converged against frozen high-fidelity U and k (formerly the incompressible `frozenOmegaFoam`).

Each solver will contain `{solver}.C`, `createFields.H`, and `Make/files` and `Make/options`. No closure implementation is included.
