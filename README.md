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

The numerical results are compared with the analytical solution.

### 3. Gradient Descent

Gradient Descent is investigated as an iterative approach to finding a suitable launch angle.

The optimization minimizes the difference between the predicted landing distance and the target distance.

Although the simplified model has an analytical solution, Gradient Descent provides an opportunity to study convergence, learning rate, initialization, and optimization limitations.

## Why These Methods?

The methods were selected for their interpretability, educational value, and suitability for experimental comparison.

The analytical solution provides a reference, Euler's method demonstrates numerical integration, and Gradient Descent introduces derivative-based optimization.

More advanced alternatives, including higher-order numerical integration and other optimization techniques, are discussed as possible future extensions.

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

These factors motivate possible future extensions. The investigation uses an idealized model so that numerical results can be validated against an analytical solution.

## Technologies

- **Python 3** — programming language (developed using Python 3.14).
- **JupyterLab** — interactive mathematical analysis and documentation.
- **NumPy** — numerical calculations.
- **Matplotlib** — trajectory and experiment visualizations.
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

Install dependencies using the repository requirements file (if present):

```bash
python -m pip install -r requirements.txt
```

Alternatively, install the packages needed to run the notebook directly:

```bash
python -m pip install jupyterlab numpy matplotlib ipython
```

Launch JupyterLab:

```bash
jupyter lab
```

Open `notebooks/artillery_math.ipynb`, then use **Restart Kernel and Run All Cells** to reproduce the calculations, tables, and plots. No external dataset is required.

## Evaluation and Results

The completed notebook evaluates the mathematical methods through controlled experiments:

- **Trajectory prediction:** The analytical equations establish a reference trajectory under idealized conditions.
- **Euler method accuracy:** Time steps of 0.5, 0.2, 0.1, 0.05, and 0.01 seconds are compared against the analytical flight time and range. The range error decreases from approximately 6.868 m to 0.141 m as the step size is reduced.
- **Automatic aiming:** Gradient Descent searches for a launch angle that reaches a target 30 m away at a fixed launch speed of 20 m/s.
- **Learning-rate sensitivity:** Among the tested values, a learning rate of 0.0001 reaches the target tolerance in 7 recorded iterations, while 0.0005 fails to converge within the 1000-iteration limit.
- **Initial-angle sensitivity:** Suitable starting angles converge toward either approximately 23.7° or 66.3°. Starting at exactly 45° fails because the loss gradient is zero at that point.

The notebook includes numerical tables, convergence plots, discussion of the observed behavior, and limitations of both methods.

## Limitations and Future Work

The implemented model is idealized and does not include real-world trajectory measurements.

Therefore, the project demonstrates mathematical and numerical behavior rather than experimentally validated physical predictions.

Possible extensions include wind, aerodynamic drag, varying launch heights, more advanced numerical methods, and an interactive simulation interface.

## References

The full academic bibliography and in-text citations are provided in **Section 6 — References** of the notebook. Principal sources include:

- [OpenStax — University Physics Volume 1: Projectile Motion](https://openstax.org/books/university-physics-volume-1/pages/4-3-projectile-motion)
- [OpenStax — University Physics Volume 1: Newton's Second Law](https://openstax.org/books/university-physics-volume-1/pages/5-3-newtons-second-law)
- [Chasnov — Numerical Methods: Initial Value Problem](https://math.libretexts.org/Bookshelves/Applied_Mathematics/Numerical_Methods_%28Chasnov%29/07%3A_Ordinary_Differential_Equations/7.02%3A_Numerical_Methods_-_Initial_Value_Problem)
- [Cornell University — CS 4220: Gradient Descent](https://www.cs.cornell.edu/courses/cs4220/2026sp/lec/2026-04-08.html)

---

**Author:** Veselina Baleva  
**Course:** Math Concepts for Developers — SoftUni  
**Year:** 2026