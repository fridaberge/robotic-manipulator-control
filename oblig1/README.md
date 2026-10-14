# Assignment 1 — Coordinate Transformations and Kinematics

Individual coursework completed for **IN3140 – Introduction to Robotics** at the University of Oslo, spring 2024.

This assignment introduces coordinate transformations and analytical kinematics for a simplified three-degree-of-freedom (3DOF) CrustCrawler manipulator.

## Objectives

- Describe the robot using coordinate frames and the Denavit–Hartenberg convention.
- Derive forward kinematics.
- Express end-effector positions in different reference frames.
- Derive inverse kinematics and discuss possible joint configurations.

## Work Completed

### Coordinate Transformations

Calculated a homogeneous transformation describing the task coordinate frame relative to the robot's base coordinate frame.

The derivation considered both the relative orientation and translation of the frames.

### Robot Model and Forward Kinematics

Illustrated the workspace and assigned coordinate frames to the simplified robot.

Established a Denavit–Hartenberg parameter table and multiplied the joint transformation matrices to obtain the forward-kinematics expression.

### End-Effector Position

Used the specified link lengths and robot configuration to calculate the end-effector position relative to the base and task coordinate frames.

This required translating the angles shown in the assignment into the joint angles defined by my chosen DH convention.

### Inverse Kinematics

Used an analytical approach to derive joint-angle expressions from a desired end-effector position.

Discussed alternative configurations and special cases where the end-effector lies on the base rotation axis.

## Files and Media

- [Taskdescription.pdf](Taskdescription.pdf) — Assignment brief
- [IN3140_oblig1_fridatbe.pdf](IN3140_oblig1_fridatbe.pdf) — Submitted report
- [media/](media/) — Supporting illustrations and images

## Reflection

The main challenge was keeping coordinate frames, angle conventions and signs consistent throughout the derivations.

The assignment helped me understand how the choice of coordinate frames affects the expressions used in both forward and inverse kinematics.

The original inverse-kinematics derivation contains errors, and the discussion of the number of solutions is incomplete. The inverse-kinematics work was revised in Assignment 2.

## Limitations and Improvements

The report is retained as originally submitted and should not be treated as a verified reference solution.

Further improvements would include:
- Checking intermediate transformation matrices independently
- Verifying numerical results against a Python implementation
- Correcting the inverse-kinematics derivation
- Revisiting the workspace assumptions and solution-count discussion

## Viewing the Work

The main deliverable is the PDF report. No ROS or Gazebo environment is required to review this assignment.

[Back to project overview](../README.md)
