# Assignment 2 — Numerical Kinematics and Jacobian Analysis

Individual coursework completed for **IN3140 – Introduction to Robotics** at the University of Oslo, spring 2024.

This assignment builds on Assignment 1 by implementing kinematic calculations in Python and analysing the simplified 3DOF CrustCrawler manipulator using its Jacobian.

## Objectives

- Implement forward and inverse kinematics.
- Check consistency between the two implementations.
- Calculate alternative joint configurations for a target position.
- Derive the Jacobian and investigate singular configurations.
- Calculate Cartesian end-effector velocity from joint velocities.

## Work Completed

### Forward and Inverse Kinematics

Implemented Python functions that map:
- Joint angles to end-effector position
- End-effector position to possible joint configurations

The inverse-kinematics implementation incorporated a correction to the derivation from Assignment 1.

### Consistency Checks

Used the forward- and inverse-kinematics functions together to check whether calculated joint configurations reproduced the target position.

Also worked with the specified target position to calculate alternative joint-angle solutions.

### Jacobian Derivation

Derived the geometric Jacobian using the joint axes and origins obtained from the homogeneous transformations.

The report includes both the linear-velocity and angular-velocity components.

### Singularity Analysis

Investigated singular configurations using the determinant of the translational Jacobian.

Discussed and illustrated configurations involving:
- Collinear arm links
- An end-effector position on the base rotation axis
- Axis alignment in a spherical wrist

### End-Effector Velocity

Implemented a Python function for calculating Cartesian end-effector velocity from joint angles and joint velocities.

## Files and Media

- [Taskdescription.pdf](Taskdescription.pdf) — Assignment brief
- The submitted PDF report — Derivations, illustrations and explanations
- Python scripts — Kinematics, consistency checks and velocity calculations
- [media/](media/) — Supporting illustrations and results

The report identifies the scripts associated with each task.

## Contribution

The assignment was completed individually.

As noted in my original reflection, I received a corrected inverse-kinematics expression from a fellow student and implemented it in Python.

## Reflection

Translating the analytical expressions into Python made it easier to inspect results and compare forward and inverse calculations.

An important lesson was that testing a few configurations is not enough to establish correctness across the entire workspace.

The implementation would benefit from more extensive testing of boundary positions, unreachable targets and cases with fewer distinct solutions.

## Limitations and Improvements

The submitted work is coursework rather than a fully tested kinematics library.

Further improvements would include:
- Automated tests covering a wider range of configurations
- Explicit handling of unreachable target positions
- Detection and removal of duplicate solutions
- Consistent documentation of angle and distance units
- Review of the singularity explanations in the report

## Running the Code

The Python scripts can be inspected and run separately. Check their imports and input conventions before execution.

A tested dependency list and unified execution procedure have not yet been documented.

ROS and Gazebo are not required for the calculations in this assignment.

[Back to project overview](../README.md)
