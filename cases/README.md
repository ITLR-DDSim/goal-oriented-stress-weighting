# Case set-ups

README-only placeholders for OpenFOAM v1912 baseline cases with `RASModel kOmega`.

| Configuration | Training | Tests |
| --- | --- | --- |
| Square duct | Re_b = 2600 | Re_b = 1100, 1800 |
| Periodic hill | alpha = 1.5 | alpha = 1.0, 1.2 |

Each case will contain `0/`, `constant/`, and `system/`. These case files have not yet been added.

Jet-in-crossflow cases are excluded pending coordination with Prof. Jee’s group. No DNS or LES fields or learned-closure implementation are included. These baseline/adjoint materials alone do not reproduce the final trained-model predictions. See [data sources](../data-sources/README.md).
