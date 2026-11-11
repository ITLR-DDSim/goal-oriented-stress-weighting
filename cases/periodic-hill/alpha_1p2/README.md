# periodic-hill: alpha_1.2

Training condition. OpenFOAM v1912 baseline with `RASModel kOmega`, solved with `simpleFoam`.

| Item | Setting |
| --- | --- |
| Reynolds number | Re = 5600 based on hill height (`nu` = 1/5600) |
| Flow driving | `meanVelocityForce` in `system/fvOptions`, Ubar = 0.7268849125376154 |
| Mesh | 2-D, 8000 cells, supplied in `constant/polyMesh` |
| Convection | U: `bounded Gauss linearUpwind grad(U)`; k, omega: `bounded Gauss upwind` |
| Walls | U no-slip; k `kLowReWallFunction`; omega `omegaWallFunction`; nut `nutLowReWallFunction` |
| Streamwise | `cyclic` |
| Initial fields | uniform: U = (Ubar 0 0), k = 0.00375, omega = 1.6, nut = 0.00235, p = 0 |

## Run

```sh
simpleFoam
```

The run takes 20000 SIMPLE iterations and is converged by about iteration 10000 (initial Ux residual about 1e-9).
`system/sampleDict` samples velocity profiles and `system/wallSample` samples the bottom-wall fields, for example
`postProcess -func sampleDict -latestTime`.

No reference data or learned closure is included.
