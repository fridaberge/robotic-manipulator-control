# Assignment 4 — Feedback Control and ROS/Gazebo Simulation

Individual coursework completed for **IN3140 – Introduction to Robotics** at the University of Oslo, spring 2024.

This assignment investigates feedback control of the CrustCrawler manipulator, focusing on Joint 2 and using the provided ROS/Gazebo simulation environment.

## Objectives

- Develop a simplified single-joint model.
- Analyse the control system in the Laplace domain.
- Construct closed-loop block diagrams.
- Implement and tune feedback controllers.
- Inspect step responses and steady-state error.
- Explore circular robot motion.

## Work Completed

### Single-Joint Model and Control Analysis

Worked with a simplified model of Joint 2 using energy-based calculations.

The report includes:
- A single-joint equation of motion
- Laplace-domain analysis
- Closed-loop block diagrams
- PD gain calculations based on desired response characteristics

### Simulation Setup

Configured the provided course packages and launched the CrustCrawler simulation in Gazebo.

The setup used the University of Oslo IFI ROS environment.

### PD Control

Implemented a PD controller in the provided starter code and investigated its response through simulation plots.

Experimented with proportional and derivative gains and discussed settling time and steady-state error.

The gains used in the simulation differed from those calculated in the analytical section. These results therefore require further review before making quantitative performance claims.

### PID and PI Control

Implemented a PID option to account for accumulated error.

Also implemented a PI controller and investigated experimental tuning using the method described in the assignment.

The report documents the tuning attempts, but the calculations and controller-parameter choices need further verification.

### Circular-Motion Attempt

The final task asked for a trajectory generator that would make the robot draw a circle with a marker.

I interpreted this differently and modified the simulation configuration to allow the robot to rotate around its base axis. With an adjusted arm position, this produced circular motion around the robot.

This was not the intended Cartesian drawing trajectory and did not constitute a completed implementation of the requested trajectory generator.

The source code for this final attempt has not yet been located. The approach is described in the report.

### Optional Extension — Drawing with the Physical Robot

After the mandatory work, I participated in an optional practical exercise using the physical CrustCrawler to draw a circle with a marker.

The exercise involved substantial guidance and assistance. It provided hands-on experience with executing a drawing trajectory on the robot, but should not be interpreted as an independently implemented solution to the mandatory trajectory-planning task.

Videos are available in the [media folder](media/). The source code associated with this demonstration has not yet been located and is not included in the repository.

## Files and Media

- [Taskdescription.pdf](Taskdescription.pdf) — Assignment brief and original setup instructions
- [IN3140_oblig4_fridatbe.pdf](IN3140_oblig4_fridatbe.pdf) — Submitted report
- Controller source files — Implementations based on the provided starter code
- [media/](media/) — Plots, simulation images and demonstrations

## Contribution

The assignment was completed individually using provided starter code and course simulation packages.

My work included modelling, control analysis, controller implementation, tuning experiments and written documentation.

## Reflection

This assignment connected the theoretical control calculations with observable robot behaviour in simulation.

The main challenges were selecting an appropriate model, choosing controller gains and interpreting the resulting responses.

The circular-motion task also demonstrated the importance of clarifying the intended trajectory before implementing a solution.

## Limitations and Improvements

The submitted controllers and measurements are retained as coursework, not as validated control software.

Further improvements would include:
- Reviewing the model parameters and their units
- Reconciling calculated gains with those used in simulation
- Measuring response characteristics more systematically
- Verifying the PI tuning calculations
- Comparing PD, PI and PID under consistent test conditions
- Recovering or reimplementing the intended trajectory generator
- Documenting a reproducible simulation setup

## Running the Simulation

The original setup depends on the course's ROS 1 environment, CrustCrawler packages and Gazebo.

See [Taskdescription.pdf](Taskdescription.pdf) for the original workspace and launch instructions.

Those instructions refer to course-specific resources and an older environment. They have not been verified as a working installation procedure outside the IFI setup.

The exact ROS distribution and Gazebo version have not yet been confirmed.

[Back to project overview](../README.md)
