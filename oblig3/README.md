# Assignment 3 — Dynamic Modelling

Individual coursework completed for **IN3140 – Introduction to Robotics** at the University of Oslo, spring 2024.

This assignment investigates energy-based dynamic modelling of the CrustCrawler manipulator, progressing from analytical calculations for a simplified two-link model to symbolic Python calculations for a three-link model.

## Objectives

- Apply the Euler–Lagrange method.
- Calculate potential and kinetic energy.
- Derive a simplified manipulator's equations of motion.
- Implement components of a three-link dynamic model.
- Assemble an expression for joint torques.

## Work Completed

### Euler–Lagrange Example

Applied the Euler–Lagrange method to a particle constrained to vertical movement.

Used its kinetic and potential energy to recover the equation of motion given in the assignment.

### Two-Link Model

Derived the potential energy, kinetic energy and Lagrangian for a simplified two-link CrustCrawler.

Used the Euler–Lagrange equations to obtain joint-torque expressions and organised them into:
- An inertia matrix
- Coriolis and centrifugal terms
- A gravity vector

### Three-Link Symbolic Calculations

Used Python and SymPy to work with the more detailed three-link model.

The implementation included:
- Potential-energy calculations using link masses and centre-of-mass positions
- Kinetic-energy calculations using Jacobians and inertia tensors
- Construction of an inertia-matrix expression
- Differentiation of matrix elements for velocity-dependent terms
- Assembly of a joint-torque expression

The report includes code excerpts and selected symbolic outputs.

## Files and Media

- [Taskdescription.pdf](Taskdescription.pdf) — Assignment brief
- [IN3140_oblig3_fridatbe.pdf](IN3140_oblig3_fridatbe.pdf) — Submitted report
- Python source files — Symbolic dynamic-model calculations
- [media/](media/) — Supporting images and outputs

## Reflection

The analytical part helped me connect energy expressions to joint torques and equations of motion.

The computational part was more challenging because matrix dimensions, reference frames and symbolic expressions needed to remain consistent.

Long symbolic outputs were difficult to inspect and verify. The implementation also contains repetitive calculations that could be organised more clearly using reusable functions.

## Limitations and Improvements

The three-link implementation contains calculation and implementation issues and has not been independently validated.

It should not be used as a verified dynamics model for simulation or physical robot control.

Further improvements would include:
- Checking centre-of-mass Jacobians and inertia transformations
- Reviewing matrix products and summations
- Verifying the gravity term derived from potential energy
- Checking the resulting inertia matrix for symmetry
- Testing simple configurations with independently calculated results
- Refactoring repeated calculations into reusable functions

## Running the Code

The computational work uses Python and SymPy.

Inspect each source file for its inputs and imports before running it. Symbolic expressions may be lengthy, and execution time can depend on the calculations performed.

A tested dependency list and execution procedure have not yet been documented.

ROS and Gazebo are not required for this assignment.

[Back to project overview](../README.md)
