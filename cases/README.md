# Case set-ups

OpenFOAM v1912 baseline cases with `RASModel kOmega` (steady `simpleFoam`).

| Configuration | Training | Tests |
| --- | --- | --- |
| Square duct | Re_b = 2600 | Re_b = 1100, 1800, 3500 |
| Periodic hill | alpha = 1.2 | alpha = 1.0, 1.5 |

Each case contains `0/`, `constant/` and `system/`. All cases use second-order `linearUpwind` convection for U and first-order upwind for k and omega. Running each case from its uniform initial fields gives the converged k–omega baseline from which the trained models were deployed.

Jet-in-crossflow cases are excluded pending coordination with Prof. Jee’s group. No DNS or LES fields or learned-closure implementation are included. These baseline/adjoint materials alone do not reproduce the final trained-model predictions. See [data sources](../data-sources/README.md).
