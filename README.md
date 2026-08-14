# Hydrodynamics — MSc Homework Notebooks (2025)

Homework notebooks written for the *Hydrodynamics* course of the MSc in Physics,
University of Amsterdam, academic year 2024/2025 (Alessio Martini).

Two self-contained Jupyter notebooks, both solved numerically from scratch with
`numpy` and plotted with `matplotlib` — no solver library, no external data.

## The notebooks

### `hydrodynamics - homework 1.ipynb` — corner flow past a falling plate

A flat plate falls through water, moving parallel to itself. The problem is
treated as two-dimensional, and the fluid occupies a **wedge of opening angle
$\alpha$** between the plate and the free surface — the classic Stokes corner
(scraping-flow) geometry.

The notebook evaluates the closed-form similarity solution for the velocity
field in polar coordinates,

$$u_r,\, u_\theta \;\propto\; \frac{U}{\alpha - \sin\alpha\cos\alpha}\,(\dots)$$

with the wedge normalisation $\alpha - \sin\alpha\cos\alpha$ that also fixes the
sign of the stress, converts it to Cartesian components, and plots it as a
quiver field on a polar grid. Three opening angles — $\alpha = \pi/4$, $\pi/2$
and $3\pi/4$ — are shown one above the other, so the way the flow pattern
reorganises as the wedge opens can be read straight off the three panels.

### `hydrodynamics - homework 3.ipynb` — the Burgers equation and shock formation

Numerical study of the **Burgers equation**, the standard one-dimensional model
for how a nonlinear advection term steepens a smooth profile until a shock forms
— catastrophe theory in a fluid setting. The equation is integrated with an
explicit **Euler** scheme over a grid of cases:

- **three values of the viscosity**, spanning the near-inviscid regime, where
  the profile steepens into a sharp front, to the strongly viscous one, where
  diffusion smooths the gradient before a shock can form;
- **four different initial conditions**;

with each time evolution plotted at five or six successive times, so the
steepening and the eventual balance between nonlinear advection and viscous
diffusion are visible as a sequence rather than as a single snapshot.

> Homework 2 is not in this repository — only assignments 1 and 3 were handed in
> as notebooks.

## Running the notebooks

```bash
pip install numpy matplotlib
jupyter lab
```

Nothing else is required — no input files, no seeds, no course-specific
packages.

## Related repositories

- [`liquid-fragmentation-report`](https://github.com/alessiomartini/liquid-fragmentation-report)
  — the written group report on liquid fragmentation, for the same course.
- [`msc-non-equilibrium-statistical-mechanics`](https://github.com/alessiomartini/msc-non-equilibrium-statistical-mechanics)
  — numerical coursework from Non-Equilibrium Statistical Mechanics, same MSc year.
