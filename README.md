# Contractile Fiber Simulation

## Description
This repository contains a Jupyter Notebook for simulating the mechanical properties of contractile fibers based on the mathematical model from Larry Taber's "Continuum Modeling in Mechanobiology". The script analyzes stress fiber deformation under the influence of cytoskeletal and nuclear stiffness.

## Installation
To run the script, you'll need Python and the following libraries installed:

```
pip install numpy matplotlib jupyter
```
## Usage
1. Clone the repository:git clone https://github.com/karinaurazova/stress_fiber

2. Launch Jupyter Notebook:jupyter notebook stress_fiber.ipynb

3. Follow the instructions in the notebook to run simulations and generate plots.

## Theory
The model implements equations from Sections 5.3-5.4 of Taber's textbook to analyze mechanical properties of contractile fibers within cells:
```math
\begin{equation}
\begin{cases}
& u(X) = C_1 \sinh(\alpha X), \\
& C_1 = \frac{K - 1}{\alpha \cosh(\alpha L) + \beta \sinh(\alpha L)}, \\
& \alpha^2 = \frac{k K^2}{2 c_a}, \\
& \beta = \frac{k_n K^2}{2 c_a}, \\
& \lambda = 1 + u', \\
& \sigma = 2 c_a \left(\frac{\lambda}{K} - 1\right),
\end{cases}
\end{equation}
```
Where:
- u(X): Fiber displacement
- λ: Stretch ratio  
- σ: Cauchy stress
- k: Cytoskeletal stiffness
- kₙ: Nuclear stiffness
- K: Uniform contraction magnitude
- cₐ: Active strain-energy coefficient
- L: Undeformed length
- A₀: Cross-sectional area

## Parameters
Default values used in simulations:
- L = 1.0 (undeformed length)
- A₀ = 0.01 (cross-section)  
- cₐ = 1.0 (active energy coefficient)
- K = 0.5 (contraction magnitude)
- k = [0, 10, 100, 1000] (cytoskeletal stiffness)
- kₙ = [0, 1] (nuclear stiffness)

## Output
1. Stretch ratio (λ) vs position (X)
2. Normalized Cauchy stress (σ/cₐ) vs position (X)

## Contributing
Contributions are welcome! Please open an issue or submit a pull request with any improvements. You can always write to me karina_urazova@icloud.com

## Reference
Taber, L.A. (2020) *Continuum Modeling in Mechanobiology*. Springer. https://link.springer.com/book/10.1007/978-3-030-43209-6
