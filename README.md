# CGE Model with Cobb-Douglas Utility Function

This repository contains a Computable General Equilibrium (CGE) model with a Cobb-Douglas utility function. The model includes sectoral outputs, utility maximization, and budget constraints. The objective of the model is to maximize aggregate utility, subject to production and budget constraints, with prices as endogenous variables.

## Features
- **Cobb-Douglas Utility Function**: The utility function is modeled as a log-linear function of sectoral outputs.
- **Production Function**: A simple production function relating sectoral output to an aggregate utility level.
- **Budget Constraint**: Each sector's budget is constrained by the price and quantity of the goods produced.
- **Numerical Optimization**: The model uses a nonlinear programming (NLP) formulation for solving the optimization problem.

## Model Equations
1. **Production Function**: $$x_i = a_i \cdot u$$
   where:
   - $x_i$ is the output of sector $i$,
   - $a_i$ is the production coefficient for sector $i$,
   - $u$ is the aggregate utility level.

2. **Utility Function**:
   $$
   u = \sum_{i} \alpha_i \cdot \log(x_i + \epsilon)
   $$
   where:
   - $u$ is the aggregate utility,
   - $\alpha_i$ is the utility weight for sector $i$,
   - $x_i$ is the output of sector $i$,
   - $\epsilon$ is a small positive constant added to avoid taking the logarithm of zero.

4. **Budget Constraint**:$$\sum_{i} p_i \cdot x_i \leq Y$$
   where:
   - $p_i$ is the price of goods produced by sector $i$,
   - $x_i$ is the output of sector $i$,
   - $Y$ is the total income available for consumption.

## Requirements

To run this model, you'll need to install the following Python packages:

- `gamspy` (for optimization and model building)
- `numpy` (for numerical operations)
- `scipy` (for solvers)

You can install the required dependencies using `pip`:

```bash
pip install gamspy numpy scipy
