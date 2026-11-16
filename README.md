# Super Artillery: From Calculus to Intelligent Aiming

### Mathematical Modeling, Numerical Simulation, and Gradient-Based Optimization

**Final Project — Math Concepts for Developers | SoftUni | November 2026**

## Project Overview

Super Artillery is a Python-based mathematical investigation inspired by a classic DOS artillery game.

The project explores how mathematics can be used to predict the trajectory of a launched object and automatically determine the angle required to reach a target.

What begins as a simple game mechanic connects to real applications in physics simulations, educational software, and robotic ball-launching systems.

The main focus is not to build a complete game, but to understand, implement, and evaluate the mathematical methods behind projectile motion and automatic aiming.

## Motivation

The idea came from an old DOS game called **Super Artillery**, which I found particularly interesting and enjoyable.

In the game, players had to adjust the firing angle while considering distance and wind. I became curious about the mathematics behind these decisions and how similar principles could be applied outside computer games.

This project is an opportunity to connect that personal interest with calculus, numerical methods, and optimization.

## Research Question

**How accurately can numerical methods simulate projectile motion, and how effectively can Gradient Descent determine a suitable launch angle to hit a target?**

The investigation focuses on three questions:

1. How does the time-step size affect the accuracy of Euler's method?
2. Can Gradient Descent determine a launch angle that reaches a specified target?
3. How do the learning rate and initial angle affect optimization convergence?

## Mathematical Methods

The project investigates three complementary approaches.

### 1. Analytical Projectile Motion

Classical equations of motion provide an exact reference solution under idealized physical conditions.

The horizontal and vertical positions are:

$$
x(t) = v_0 \cos(\theta)t
$$

$$
y(t) = v_0 \sin(\theta)t - \frac{1}{2}gt^2
$$

### 2. Euler's Numerical Method

Euler's method approximates projectile motion through discrete time steps.

It is selected because it is simple to implement and makes the relationship between differential equations, numerical approximation, and accumulated error easy to investigate.

The numerical results will be compared with the analytical solution.

### 3. Gradient Descent

Gradient Descent is investigated as an iterative approach to finding a suitable launch angle.

The optimization minimizes the difference between the predicted landing distance and the target distance.

Although the simplified model has an analytical solution, Gradient Descent provides an opportunity to study convergence, learning rate, initialization, and optimization limitations.

## Why These Methods?

The methods were selected for their interpretability, educational value, and suitability for experimental comparison.

The analytical solution provides a reference, Euler's method demonstrates numerical integration, and Gradient Descent introduces derivative-based optimization.

More advanced alternatives, including higher-order numerical integration and other optimization techniques, will be discussed to explain the advantages and limitations of the selected approaches.

The objective is not to claim that these methods are universally optimal, but to evaluate when and why they are useful.

## Physical Model and Assumptions

The initial model assumes:

- Constant gravitational acceleration.
- Two-dimensional projectile motion.
- Flat terrain and equal launch and landing heights.
- No wind or aerodynamic drag.
- Fixed initial launch speed within each experiment.
- A point-mass projectile without rotation.

Real-world trajectories are also influenced by wind, air resistance, projectile properties, and environmental conditions.

These factors motivate possible future extensions. The current investigation begins with an idealized model so that numerical results can be validated against an analytical solution.

## Technologies

- **Python 3.14** — programming language.
- **JupyterLab** — interactive mathematical analysis and documentation.
- **NumPy** — numerical calculations.
- **Matplotlib** — trajectory and experiment visualizations.
- **SymPy** — optional symbolic mathematical verification.
- **pytest** — automated testing.
- **Git and GitHub** — version control and project documentation.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/VesiBaleva/Math-Concepts-for-Developers.git
cd Math-Concepts-for-Developers
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Launch JupyterLab:

```bash
jupyter lab
```

Open `notebooks/artillery_math.ipynb` and run the cells in order.

## Evaluation Plan

The project will evaluate:

- **Trajectory prediction:** How launch angle and initial velocity affect projectile motion.
- **Numerical accuracy:** How Euler's method compares with the analytical solution for different time steps.
- **Automatic aiming:** Whether Gradient Descent can find a launch angle within a specified target tolerance.
- **Convergence behavior:** How learning rate and initial angle affect optimization performance.
- **Method suitability:** Why the selected methods are appropriate and where alternative approaches may perform better.

## Limitations and Future Work

The initial model is idealized and does not include real-world trajectory measurements.

Therefore, the project demonstrates mathematical and numerical behavior rather than experimentally validated physical predictions.

Possible extensions include wind, aerodynamic drag, varying launch heights, more advanced numerical methods, and an interactive simulation interface.

## References

The notebook will include references to the mathematical and computational sources used throughout the investigation.

Relevant documentation includes:

- [Python Documentation](https://docs.python.org/3/)
- [NumPy Documentation](https://numpy.org/doc/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/)
- [SymPy Documentation](https://docs.sympy.org/latest/)
- [Project Jupyter](https://jupyter.org/)

Additional academic references will be added as the mathematical research develops.

---

**Author:** Veselina Baleva  
**Course:** Math Concepts for Developers — SoftUni  
**Year:** 2026