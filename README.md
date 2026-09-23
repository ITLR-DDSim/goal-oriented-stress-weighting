# Goal-Oriented Stress Weighting

Supporting repository for **Goal-Oriented Weighting of Reynolds-Stress Data for Learning Turbulence Models in Complex Flows**.

The method uses an offline adjoint calculation to identify Reynolds-stress data that influence a selected flow quantity. These sensitivities are converted into fixed weights for turbulence-model training.

This repository is being prepared to share the associated solvers, weight-construction procedure and selected case set-ups. **Currently, it contains folder descriptions only; code and case files are not yet available.**

## Repository structure

| Directory | Purpose |
| --- | --- |
| [`solvers/`](solvers/README.md) | Incompressible and compressible adjoint solvers, and an incompressible frozen-omega solver |
| [`weights/`](weights/README.md) | Conversion of adjoint sensitivities into global component weights and spatially varying loss weights |
| [`cases/`](cases/README.md) | Square-duct and periodic-hill case set-ups |
| [`environment/`](environment/README.md) | Software requirements and build/run instructions |
| [`data-sources/`](data-sources/README.md) | References and access information for external DNS, LES and experimental data |

Each directory has a README describing its intended contents.

## Cases

| Configuration | Training condition | Test conditions |
| --- | --- | --- |
| Square duct | Re_b = 2600 | Re_b = 1100 and 1800 |
| Periodic hill | alpha = 1.5 | alpha = 1.0 and 1.2 |

The planned baseline case files use the k–omega model in OpenFOAM v1912. Weight-construction scripts require Python 3 and NumPy.

## Scope and data access

The release focuses on adjoint calculations, weight construction and the selected case set-ups; it does not include a learned turbulence-closure implementation.

External datasets are identified in [`data-sources/`](data-sources/README.md) and are not currently distributed here. Jet-in-crossflow case files remain pending coordination with Prof. Jee’s group. The LES fields are not part of the planned release.
