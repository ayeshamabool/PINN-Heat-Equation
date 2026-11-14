# Comparative Numerical Analysis of the One-Dimensional Heat Equation Using Finite Difference Methods and Physics-Informed Neural Networks

## Overview
This project solves 1D Heat Equation: u_t = alpha * u_xx
Domain L = 1.0, Time T = 1.0, alpha = 0.1
Initial Condition: u(0,x) = sin(pi*x)
Boundary Conditions: u(t,0) = 0, u(t,1) = 0

## Methods
1. Finite Difference Method (FDM) - Explicit Scheme
   Nx = 100, Nt = 2500, r = 0.3922 (Stable, r <= 0.5)
2. Physics-Informed Neural Networks (PINN)
   Fully Connected Network, Adam Optimizer, Physics Loss

## Analytical Solution
u(x,t) = exp(-0.1 * pi^2 * t) * sin(pi*x)
Used to validate both FDM and PINN.

## Results
- PINN Final Loss: 0.00009
- PINN Error: ~0.47% (Relative L2 Error)
- FDM: Stable and accurate, error decreases with grid refinement.
- Both methods show excellent agreement with analytical solution.

## Files
- FDM-Heat-Equation-Solver.ipynb - Initial Version
- FDM_Heat_Equation_Solver_Updated_Step1.ipynb - Refined Final Version

## Author
Ayesha Maqbool - BS Mathematics - BZU, Multan

## Tech Stack
Python, PyTorch, NumPy, Matplotlib, Google Colab
