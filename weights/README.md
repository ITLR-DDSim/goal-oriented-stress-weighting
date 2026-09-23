# Weight construction

Planned Python 3 + NumPy scripts; currently documentation only.

- `dJdb.py`: adjoint solution to component sensitivities G_ij (Eqs. B7–B9), including the factor of two for paired shear degrees of freedom.
- `weights.py`: G_ij to loss weights. `global_weights` produces the six-component vector in Table 2. `cellwise_weights` produces W_ij(x), including its mask, cell-relevance and component-priority factors (Eq. 7, Eqs. 10–12 and B10). A self-check is planned under `__main__`.

Input formats and run commands will accompany the scripts. Equation numbers refer to the current manuscript. No code or data are included yet.
