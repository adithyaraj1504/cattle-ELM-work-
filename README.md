# Multi-Patch Cattle Compartmental Modeling with Extreme Learning Machines & Preconditioned GMRES Solvers

This repository contains numerical implementations and Jupyter notebooks exploring matrix-free **Extreme Learning Machines (ELM)** coupled with **GMRES solvers** and various preconditioners for modeling compartmental epidemiological dynamics in cattle populations.

## Data & Simulation Parameters

* **Time Horizon**: $t \in [0, 24]$
* **Temporal Resolution**: 720 evaluation steps ($dt = 24 / 720 = 0.0333$)
* **Target Dynamics**: Synthetic temporal trajectory data generated across the 24-time unit interval to simulate compartmental population transitions across patches.

## Repository Contents

* **`2_cattle_problem.ipynb`**: Baseline implementation of the multi-patch cattle compartmental model using standard Extreme Learning Machines across the 720 temporal evaluation steps.
* **`2_cattle_problem_with_GMRES.ipynb`**: Integration of Generalized Minimal Residual (GMRES) iterative solvers to handle large-scale linear systems within the modeling pipeline.
* **`2_cattle_problem_with_GMRES_with_jacobi_preconditioner.ipynb`**: Enhanced solver architecture incorporating Jacobi preconditioning to improve convergence rates and numerical stability.
* **`2_cattle_problem_with_GMRES_with_polynomial_preconditioner.ipynb`**: Advanced implementation utilizing polynomial preconditioners for accelerated spectral distribution shaping.
* **`2_cattle_problem_with_GMRES_with_small_block_diagonal_preconditioner.ipynb`**: Specialized block-structured preconditioning tailored for multi-patch spatial coupling dynamics.

## Overview

The workflows demonstrate efficient scientific computing methods—combining data-driven ELM architectures with robust Krylov subspace iterative techniques (GMRES) and customized preconditioners—to accurately forecast and simulate epidemiological spread across multi-patch systems.
