# CrustCrawler Robotic Manipulator Control

Robotics coursework covering coordinate transformations, kinematics, dynamic modelling and feedback control of a simplified three-degree-of-freedom (3DOF) CrustCrawler manipulator.

This repository contains four individual assignments completed in **IN3140 – Introduction to Robotics** at the **University of Oslo in spring 2024**.

The work combines mathematical derivations, Python implementations and ROS/Gazebo simulation. The coursework also included experience with a physical CrustCrawler robot.

## Technologies and Methods

- Python
- SymPy
- ROS 1 and Gazebo
- LaTeX
- Denavit–Hartenberg modelling
- Forward and inverse kinematics
- Jacobian and singularity analysis
- Euler–Lagrange dynamics
- PD, PI and PID control

## Assignment Overview

### Assignment 1 — Coordinate Transformations and Kinematics

Established coordinate frames and derived kinematic relationships for a simplified 3DOF model of the CrustCrawler.

The work included:
- Transformations between world, base and task coordinate frames
- Workspace illustrations
- Denavit–Hartenberg parameters and homogeneous transformations
- Forward kinematics and end-effector position calculations
- Analytical inverse kinematics
- Discussion of alternative joint configurations

The original submission contains errors in the inverse-kinematics derivation and discussion of solution counts. These are acknowledged in the assignment README, and the inverse-kinematics work was revised in Assignment 2.

[Assignment files and reflection](oblig1/) · [Task description](oblig1/Taskdescription.pdf) · [Media](oblig1/media/)

### Assignment 2 — Python Implementation and Jacobian Analysis

Implemented the kinematic calculations in Python and investigated the relationship between joint motion and end-effector motion.

The work included:
- Forward- and inverse-kinematics functions
- Consistency checks between the two functions
- Calculation of alternative joint configurations for a target position
- Derivation of the geometric Jacobian
- Analysis and illustration of singular configurations
- A function mapping joint velocities to Cartesian end-effector velocity

The reflection identifies opportunities for more extensive edge-case testing and better handling of positions with fewer distinct inverse-kinematics solutions.

[Assignment files and reflection](oblig2/) · [Task description](oblig2/Taskdescription.pdf) · [Media](oblig2/media/)

### Assignment 3 — Dynamic Modelling

Worked with energy-based modelling and equations of motion, progressing from a simplified two-link model to a computational three-link model.

The work included:
- An Euler–Lagrange derivation for a vertically moving particle
- Potential and kinetic energy calculations
- A Lagrangian and equations of motion for a two-link manipulator
- Symbolic Python calculations for the three-link model
- Implementation work on inertia, Coriolis/centrifugal and gravitational terms
- Assembly of the joint-torque expression

The submitted three-link implementation is retained as coursework and should not be treated as a validated dynamics model.

[Assignment files and reflection](oblig3/) · [Task description](oblig3/Taskdescription.pdf) · [Media](oblig3/media/)

### Assignment 4 — Feedback Control and ROS/Gazebo Simulation

Investigated feedback control of Joint 2 using a simplified single-joint model and the provided simulation environment.

The work included:
- Single-joint dynamic modelling
- Laplace-domain analysis and closed-loop block diagrams
- PD gain calculations based on desired response characteristics
- PD implementation and experimental tuning
- Step-response plots and discussion of steady-state error
- PID implementation as a possible improvement
- PI implementation and experimental tuning

The final task asked for a ROS trajectory generator that would make the robot draw a circle. My submitted approach instead modified the simulation configuration to allow rotation around the robot's base axis. This produced circular motion but did not implement the intended Cartesian drawing trajectory.

The source code for the final circular-motion attempt has not yet been located. The report documents the approach taken.

[Assignment files and reflection](oblig4/) · [Task description](oblig4/Taskdescription.pdf) · [Media](oblig4/media/)

## My Contribution

All four assignments were completed individually.

My work included mathematical derivations, Python programming, written reports, controller implementation and simulation experiments.

The control assignment used provided starter code and course simulation packages. As documented in the Assignment 2 reflection, I received a corrected inverse-kinematics expression from a fellow student and implemented it in Python.

## Repository Guide

- `oblig1/` — Coordinate transformations and analytical kinematics
- `oblig2/` — Python kinematics, Jacobian and singularity analysis
- `oblig3/` — Dynamic modelling and symbolic calculations
- `oblig4/` — Feedback control and simulation

Each assignment folder contains:
- `Taskdescription.pdf` — The assignment brief
- `README.md` — Reflections on the work
- `media/` — Supporting images and demonstrations
- The submitted report and any associated source files

## Running the Code

This repository is a coursework archive rather than a single runnable application.

### Mathematical and Python Assignments

Assignments 1–3 contain reports and, where applicable, Python scripts. Inspect each script for its imports, inputs and execution requirements before running it.

A complete dependency list and tested execution procedure have not yet been documented.

### ROS/Gazebo Simulation

Assignment 4 was developed for the University of Oslo IFI ROS environment using the course container and CrustCrawler packages.

The original setup instructions are included in [Assignment 4's task description](oblig4/Taskdescription.pdf). They depend on course-specific resources and are not a verified installation guide for another machine.

The exact ROS distribution and Gazebo version have not yet been confirmed.

## Limitations

The original submissions contain calculation errors, implementation issues and incomplete work. Assignment-specific reflections provide further context.

Areas for improvement include:
- More comprehensive kinematics tests
- Handling of unreachable targets and duplicate solutions
- Verification of the three-link dynamics implementation
- More systematic controller tuning and response measurements
- Recovery or reimplementation of the final trajectory generator
- Documentation of a reproducible simulation environment

## What I Learned

The assignments connected analytical robot modelling with programming and simulation.

Key learning outcomes included:
- Defining coordinate frames and applying the DH convention
- Translating kinematic expressions into Python
- Understanding Jacobians and singular configurations
- Building energy-based dynamic models
- Implementing and comparing feedback controllers
- Interpreting simulation responses and recognising model limitations
- Identifying the need for better testing and verification
