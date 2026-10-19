# CrustCrawler Robotic Manipulator Control

Robotics coursework covering coordinate transformations, kinematics, dynamic modelling and feedback control of a simplified three-degree-of-freedom (3DOF) CrustCrawler manipulator.

This repository contains four individual assignments completed in **IN3140 – Introduction to Robotics** at the **University of Oslo in spring 2024**.

The work combines mathematical derivations, Python implementations and ROS/Gazebo simulation. An optional practical exercise also provided experience with a physical CrustCrawler robot.

## Demonstration

As an optional extension to the coursework, I participated in a guided practical exercise exploring circular drawing with the physical CrustCrawler.

- [Physical robot — circular drawing attempt](oblig4/media/circle_drawing.mp4): The robot performs the circular movement but does not reach the paper because the base-frame height was not accounted for.
- [Physical robot — excessive downward movement](oblig4/media/circle_motion.mp4): The arm moves too far down and makes forceful contact with the table, illustrating a problem with the vertical positioning.
- [Gazebo simulation](oblig4/media/circle_gazebo.mp4): Circular-motion footage from the simulation environment.

The physical exercise involved substantial guidance and assistance and was separate from the mandatory submissions. These recordings document exploratory attempts and positioning issues, rather than a successfully validated drawing implementation.

## Technologies and Methods

- Python and SymPy
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

The inverse-kinematics work was revised in Assignment 2. See the assignment README for reflections and known limitations.

[Assignment files and reflection](oblig1/README.md) · [Task description](oblig1/Taskdescription.pdf) · [Media](oblig1/media/)

### Assignment 2 — Python Implementation and Jacobian Analysis

Implemented the kinematic calculations in Python and investigated the relationship between joint motion and end-effector motion.

The work included:
- Forward- and inverse-kinematics functions
- Consistency checks between the two functions
- Calculation of alternative joint configurations for a target position
- Derivation of the geometric Jacobian
- Analysis and illustration of singular configurations
- A function mapping joint velocities to Cartesian end-effector velocity

[Assignment files and reflection](oblig2/README.md) · [Task description](oblig2/Taskdescription.pdf) · [Media](oblig2/media/)

### Assignment 3 — Dynamic Modelling

Worked with energy-based modelling and equations of motion, progressing from a simplified two-link model to a computational three-link model.

The work included:
- An Euler–Lagrange derivation for a vertically moving particle
- Potential and kinetic energy calculations
- A Lagrangian and equations of motion for a two-link manipulator
- Symbolic Python calculations for the three-link model
- Implementation work on inertia, Coriolis/centrifugal and gravitational terms
- Assembly of the joint-torque expression

[Assignment files and reflection](oblig3/README.md) · [Task description](oblig3/Taskdescription.pdf) · [Media](oblig3/media/)

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

For the final trajectory task, my submitted approach explored base-axis circular motion rather than completing the requested Cartesian drawing trajectory. A separate, assisted optional exercise explored circular drawing with the physical robot and highlighted vertical-positioning issues.

[Assignment files and reflection](oblig4/README.md) · [Task description](oblig4/Taskdescription.pdf) · [Media and videos](oblig4/media/)

## My Contribution

The four mandatory assignments were individual submissions. My work included mathematical derivations, Python programming, written reports, controller implementation and simulation experiments.

The work also involved the following resources and assistance:
- Provided starter code and course simulation packages for Assignment 4
- A corrected inverse-kinematics expression received from a fellow student and implemented in Python, as documented in the Assignment 2 reflection
- Substantial guidance and assistance during the separate optional physical-robot drawing exercise

## Repository Guide

```text
robotic-manipulator-control/
├── oblig1/    # Coordinate transformations and analytical kinematics
├── oblig2/    # Python kinematics, Jacobian and singularity analysis
├── oblig3/    # Dynamic modelling and symbolic calculations
├── oblig4/    # Feedback control, simulation and demonstration videos
└── README.md
```

Each assignment folder contains:
- `Taskdescription.pdf` — The assignment brief
- `README.md` — An overview and reflection on the work
- `media/` — Supporting images or demonstrations
- The submitted report and any associated source files

## Running the Code

This repository is a coursework archive rather than a single runnable application.

### Mathematical and Python Assignments

Assignments 1–3 contain reports and, where applicable, Python scripts. Inspect each script for its imports, inputs and execution requirements before running it.

### ROS/Gazebo Simulation

Assignment 4 was developed for the University of Oslo IFI ROS environment using the course container and CrustCrawler packages.

The original setup instructions are included in [Assignment 4's task description](oblig4/Taskdescription.pdf). They depend on course-specific resources and have not been verified as an installation procedure for another machine.

The exact ROS distribution and Gazebo version have not yet been confirmed.

## Limitations and Further Work

This repository preserves the original coursework submissions rather than a fully validated robotics application. Assignment-specific READMEs document known issues, assistance received and reflections.

Key areas for further work:
- Correcting remaining analytical errors and expanding kinematics tests
- Handling unreachable targets and duplicate inverse-kinematics solutions
- Verifying the three-link dynamics implementation
- Reconciling calculated controller gains with simulation settings
- Recovering the missing circular-motion and drawing-demonstration code
- Documenting a reproducible execution and simulation environment

The dynamics and controller implementations should not be treated as validated software for physical robot control.

## What I Learned

The assignments connected analytical robot modelling with programming and simulation.

Key learning outcomes included:
- Defining coordinate frames and applying the DH convention
- Translating kinematic expressions into Python
- Understanding Jacobians and singular configurations
- Building energy-based dynamic models
- Implementing and comparing feedback controllers
- Interpreting simulation responses and recognising model limitations
- Connecting simulation work with physical robot behaviour
- Identifying the need for better testing, verification and reproducibility
