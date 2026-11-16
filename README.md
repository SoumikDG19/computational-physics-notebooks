Computational Physics Notebooks
> From quantum wavefunctions to the internal structure of stars.
A collection of Python notebooks exploring quantum mechanics and stellar structure through mathematical modelling, numerical methods, and scientific visualisation.
These projects connect physical equations with executable calculations: matching wavefunctions at potential boundaries, exploring quantised states, estimating energy eigenvalues, and modelling the interior of a polytropic star.
Author: Soumik Dutta Gupta  
Focus: Quantum mechanics · Numerical methods · Astrophysics
Explore the notebooks
Notebook	Physical problem	Methods and outputs
1D Potential Step	Scattering at a potential discontinuity, above and below the step height	Boundary matching, reflection and transmission coefficients, and probability-density plots
Quantum Tunnelling	Transmission through a finite rectangular barrier	Wavefunction construction, comparison with an analytical transmission formula, and energy-dependent reflection and transmission
Quantum Harmonic Oscillator	Stationary states of the linear harmonic oscillator	Hermite polynomials, wavefunctions, probability densities, energy levels, and classical–quantum comparisons
Hydrogen Atom	Angular and radial behaviour of hydrogenic wavefunctions	Three-dimensional angular-function plots and radial-distribution curves using NumPy, Matplotlib, and SymPy
Numerical Solution of the Schrödinger Equation	Bound states in oscillator, infinite-well, and attractive delta-potential models	Numerov-based integration, node counting, energy searches, normalisation, and comparisons with analytical energies
Lane–Emden Equation	Stellar structure under a polytropic equation of state	Numerical integration, first-zero estimates, enclosed-mass profiles, and solar-model comparisons
The table provides a suggested reading order. Start with the potential-step and tunnelling notebooks for scattering, then explore bound states and numerical methods before moving to stellar structure.
Computational approach
The collection brings together several parts of scientific computing:
Physical modelling: Expressing potentials, boundary conditions, and governing equations in code.
Numerical methods: Integrating differential equations, searching for eigenvalues, counting nodes, and normalising wavefunctions.
Analytical comparisons: Comparing selected numerical calculations with known expressions for transmission coefficients and energy levels.
Scientific visualisation: Using two- and three-dimensional plots to examine wavefunctions, orbital angular structure, and stellar profiles.
Tools
Tool	Use in the notebooks
Python	Calculations, functions, and numerical workflows
NumPy	Arrays, complex arithmetic, special-polynomial evaluation, and numerical integration
SciPy	Physical constants
Matplotlib	Two- and three-dimensional scientific plots
SymPy	Hydrogenic radial functions and symbolic-to-numerical evaluation
pandas	Reading and working with solar-model data
JupyterLab / Jupyter Notebook	Equations, explanations, code, and figures in one document
The tunnelling notebook also imports `ipywidgets`.
Getting started
1. Get the notebooks
Clone the repository:
```bash
git clone https://github.com/SoumikDG19/computational-physics-notebooks.git
cd computational-physics-notebooks
```
2. Install the dependencies
In your preferred Python 3 environment, run:
```bash
python -m pip install jupyterlab ipykernel "numpy>=2.0" scipy matplotlib sympy pandas ipywidgets
```
NumPy 2.0 or newer is required because the numerical Schrödinger-equation notebook uses `numpy.trapezoid`.
3. Open a notebook
Launch JupyterLab from the repository directory:
```bash
jupyter lab
```
Open a notebook, choose a Python kernel from the environment containing the dependencies, and execute its cells from top to bottom. Read the equations and parameter definitions alongside the plots.
Data for the stellar-model comparisons
The solar-comparison sections of `LANE-EMDEN EQUATION.ipynb` require a whitespace-separated file named `ssm.dat` in the same directory as the notebook.
The code expects these column names:
```text
M/Msun  R/Rsun  Rho  P  T
```
These represent enclosed mass, radius, density, pressure, and temperature. The comparison plots normalise the density, pressure, and temperature to their first tabulated values.
Supply this dataset to reproduce the solar comparisons. Without it, skip the cell that reads `ssm.dat` and the subsequent cells that use the loaded data. The quantum mechanics notebooks define their example parameters directly in the code.
Model conventions
Several examples use scaled units, such as setting mass and the reduced Planck constant to one. Check each notebook's definitions before interpreting numerical values.
The attractive delta potential is represented numerically by a narrow rectangular well.
The hydrogen notebook examines angular functions and radial distributions in separate sections.
The Lane–Emden notebook uses a polytropic model to explore stellar structure and compare selected profiles with solar-model data.
About
I am interested in understanding physical systems through mathematical reasoning and computation, with a particular interest in quantum mechanics and astrophysics. This repository brings together my computational physics notebooks as an educational portfolio.
Questions, corrections, and discussions about the physics or implementation are welcome through the repository's Issues page.
