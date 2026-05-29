# Differential Equations for Scientists & Engineers

> **A research-grade, 8-week masterclass in Ordinary and Partial Differential Equations — from first principles to modern ML applications.**  
> No symbolic solvers. No black-box libraries. Pure mathematics, NumPy, and SciPy only.

---

## Overview

This course builds a complete understanding of differential equations from the ground up, connecting classical theory with modern scientific computing and machine learning. Each week is a self-contained Jupyter Notebook packed with rigorous derivations, hand-crafted numerical implementations, and rich visualizations.

By the end you will have derived, implemented, and stress-tested:

- Every major **ODE solver** (Euler, RK4, Adams-Bashforth, BDF, Radau) from scratch
- **Stability analysis** via eigenvalue spectra and phase portraits
- **Boundary Value Problems** with shooting methods and finite differences
- **Fourier Series & Transforms** with hand-rolled DFT and FFT kernels
- The canonical **PDEs** of physics: heat, wave, Laplace, and Burgers equations
- **Stiff systems** and their numerical pathologies (stiffness ratio, A-stability)
- **Neural ODEs** and **Physics-Informed Neural Networks (PINNs)** from scratch in NumPy

---

## Repository Structure

```
differential_equations/
│
├── week1/   01_first_order_odes.ipynb          # Separable, linear, Bernoulli, exact ODEs
├── week2/   02_second_order_and_systems.ipynb  # Characteristic equations, phase planes, systems
├── week3/   03_numerical_methods_odes.ipynb    # Euler, RK4, AB/AM multistep, error analysis
├── week4/   04_stiff_systems_and_bvp.ipynb     # Stiffness, BDF/Radau, shooting & FD for BVPs
├── week5/   05_fourier_and_laplace.ipynb       # Fourier series, DFT/FFT from scratch, Laplace transforms
├── week6/   06_pdes_heat_and_wave.ipynb        # Heat equation (FTCS/CN), wave equation (leapfrog)
├── week7/   07_pdes_elliptic_and_burgers.ipynb # Laplace (SOR, multigrid), Burgers (shock capturing)
└── week8/   08_neural_odes_and_pinns.ipynb     # NODE adjoint method, PINNs for PDEs from scratch
```

---

## Week-by-Week Syllabus

| Week | Topic | Key Implementations |
|------|-------|---------------------|
| 1 | **First-Order ODEs** | Integrating factor, exact ODE solver, Bernoulli substitution, direction fields |
| 2 | **Second-Order ODEs & Systems** | Characteristic roots, variation of parameters, eigenvalue phase portraits, nullclines |
| 3 | **Numerical Methods for ODEs** | Euler/Midpoint/RK4 from scratch, local truncation error, global error convergence plots, Adams-Bashforth/Moulton |
| 4 | **Stiff Systems & BVPs** | Stiffness ratio analysis, BDF-2, implicit Euler, shooting method, finite difference BVPs, Thomas algorithm |
| 5 | **Fourier & Laplace Transforms** | Hand-rolled DFT O(N²), Cooley-Tukey FFT O(N log N), Gibbs phenomenon, Laplace via Bromwich contour |
| 6 | **PDEs: Heat & Wave** | 1D/2D heat (FTCS, Crank-Nicolson), CFL condition, 1D wave (leapfrog), d'Alembert solution verification |
| 7 | **PDEs: Elliptic & Nonlinear** | 2D Laplace (Jacobi, Gauss-Seidel, SOR, 2-level multigrid), Burgers equation (upwind, Lax-Wendroff, WENO) |
| 8 | **Neural ODEs & PINNs** | Adjoint sensitivity from scratch, latent ODE on spiral data, PINN for Poisson/heat/Burgers from scratch |

---

## Prerequisites

- Linear algebra (eigenvalues, matrix decompositions)
- Single and multivariable calculus
- Basic Python / NumPy fluency
- Familiarity with Jupyter Notebooks

The course is self-contained beyond these fundamentals — all numerical methods are derived before they are coded.

---

## Environment Setup

```bash
git clone https://github.com/HAYDARKILIC/differential_equations
cd differential_equations
pip install numpy scipy matplotlib jupyter
```

For Week 8 (Neural ODEs / PINNs), add:
```bash
pip install torch          # CPU-only is fine for all exercises
```

---

## Design Philosophy

Every notebook follows the same structure:

1. **Theory** — rigorous derivation with LaTeX, no hand-waving
2. **From-Scratch Implementation** — coded in pure NumPy before any library call
3. **Verification** — analytical solution checked against numerical, convergence order confirmed
4. **Visualization** — phase portraits, error plots, solution surfaces, animations
5. **Exercises** — open-ended problems that extend the lecture material

---

## Related Repositories

| Repository | Description |
|---|---|
| [`numerical_methods`](https://github.com/HAYDARKILIC/numerical_methods) | Root-finding, quadrature, interpolation, ODE/BVP solvers |
| [`numerical_methods_for_ml`](https://github.com/HAYDARKILIC/numerical_methods_for_ml) | Autodiff, stable linear algebra, optimization for ML |
| [`differential_equations_for_ai`](https://github.com/HAYDARKILIC/differential_equations_for_ai) | Neural ODEs, PINNs, diffusion models, optimal control |
| [`adv_pde_based_image_processing`](https://github.com/HAYDARKILIC/adv_pde_based_image_processing) | Anisotropic diffusion, Finsler flows, CUDA acceleration |

---

## License

MIT — free to use, adapt, and redistribute with attribution.
