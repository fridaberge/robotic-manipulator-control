# CrustCrawler Robotic Manipulator Control

This repository contains my individual mandatory assignments from **IN3140 – Introduction to Robotics** at the University of Oslo.

The project focuses on modelling and controlling a 3DOF CrustCrawler robotic manipulator, starting from coordinate frames and kinematics, and progressing toward dynamics, control theory, simulation and trajectory planning.

## Technologies

- Python
- ROS 1
- Gazebo
- LaTeX
- PID control
- Robotic kinematics and dynamics

## Project Overview

The work is divided into four mandatory assignments:

### Assignment 1: Kinematics

In the first assignment, I established coordinate frames for a 3DOF CrustCrawler robotic arm and derived the forward and inverse kinematics.

This included describing the robot geometry, defining transformations between coordinate frames and calculating joint configurations for desired end-effector positions.

### Assignment 2: Numerical Kinematics and Jacobian

In the second assignment, I implemented the kinematic calculations from Assignment 1 in Python.

I also derived and implemented the Jacobian matrix for the manipulator, allowing the relationship between joint velocities and end-effector velocity to be analysed numerically for given joint angles.

### Assignment 3: Dynamics

In the third assignment, I derived the Lagrangian formulation and dynamic model for the manipulator.

This part focused on understanding how the robot's motion is affected by its physical parameters, joint variables and dynamic equations.

### Assignment 4: Control and Simulation

In the fourth assignment, I worked with control theory for the robotic manipulator, including PD and PID control.

The robot was simulated using ROS 1 and Gazebo. I created closed-loop block diagrams, analysed the robot motion through plots and tuned the PID controller to improve the motion.

The final part of the assignment involved trajectory planning, where the manipulator was intended to draw a circular trajectory with a marker. The implemented result produced a circular motion, although the motion was somewhat uneven and the trajectory interpretation differed from the intended task.

## My Contribution

All assignments were completed individually.

I implemented the mathematical derivations, Python calculations, control logic and simulation work myself, with the exception of some provided starter code for the final assignment.

## Results

The project resulted in:

- Forward and inverse kinematics for a 3DOF CrustCrawler manipulator
- Python implementation of kinematic calculations
- Jacobian derivation and numerical evaluation
- Lagrangian-based dynamic model
- PD and PID controller implementation
- ROS 1/Gazebo simulation of manipulator motion
- PID tuning and motion analysis using plots
- Initial trajectory planning for circular motion

The final simulated robot movement produced a circular trajectory, but the motion was somewhat uneven. This highlighted the importance of controller tuning, trajectory interpretation and simulation-based validation in robotics.

## Repository Structure

```text
robotic-manipulator-control/
├── oblig1/              # Coordinate frames, forward and inverse kinematics
├── oblig2/              # Python implementation of kinematics and Jacobian
├── oblig3/              # Lagrangian formulation and dynamic model
├── oblig4/              # PD/PID control, ROS/Gazebo simulation and trajectory planning
└── README.md
