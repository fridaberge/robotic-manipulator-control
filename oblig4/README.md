# Assignment 4 — Feedback Control and ROS/Gazebo Simulation

Individual coursework completed for **IN3140 – Introduction to Robotics** at the **University of Oslo, spring 2024**.

This assignment investigates feedback control of the CrustCrawler manipulator, focusing on Joint 2 and using the provided ROS/Gazebo simulation environment.

This folder also documents a separate optional practical exercise involving circular drawing with the physical robot.

## Objectives

- Develop a simplified single-joint model
- Analyse the control system in the Laplace domain
- Construct closed-loop block diagrams
- Implement and tune feedback controllers
- Inspect step responses and steady-state error
- Investigate trajectory generation for circular motion

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

### PID and PI Control

Implemented a PID option to account for accumulated error.

Also implemented a PI controller and investigated experimental tuning using the method described in the assignment.

### Circular-Motion Attempt

The final task asked for a trajectory generator that would make the robot draw a circle with a marker.

My submitted approach instead modified the simulation configuration to allow rotation around the robot's base axis. With an adjusted arm position, this produced circular motion around the robot.

This differed from the intended Cartesian drawing trajectory and did not constitute a completed implementation of the requested trajectory generator.

### Optional Extension — Drawing with the Physical Robot

I also participated in an optional practical exercise where the physical CrustCrawler drew a circle with a marker.

This exercise involved substantial guidance and assistance and provided hands-on experience with executing a drawing trajectory on the robot. It was separate from the mandatory submission and is not presented as an independently developed trajectory-planning implementation.

- [Drawing demonstration](media/circle_drawing.mp4)
- [Additional robot footage](media/circle_motion.mp4)

Additional simulation footage is available in the [media folder](media/).

## Files and Media

- [Taskdescription.pdf](Taskdescription.pdf) — Assignment brief and original setup instructions
- [IN3140_oblig4_fridatbe.pdf](IN3140_oblig4_fridatbe.pdf) — Submitted report
- Controller source files — Implementations based on the provided starter code
- [media/](media/) — Controller plots, simulation screenshots, block diagrams and video demonstrations

## Contribution and Assistance

The mandatory assignment was completed as an individual submission using provided starter code and course simulation packages.

My work included:
- Mathematical modelling and control analysis
- Controller implementation
- Simulation and tuning experiments
- Interpretation of response plots
- Written documentation

The optional physical-robot drawing exercise involved substantial guidance and assistance. It is documented separately from the individual mandatory work.

## Reflection

This assignment connected theoretical control calculations with observable robot behaviour in simulation.

The main challenges were selecting an appropriate model, choosing controller gains and interpreting the resulting responses.

The circular-motion task highlighted the importance of clarifying the intended trajectory before implementing a solution. The optional drawing exercise provided additional experience with the physical robot and the practical execution of a drawing movement.

## Limitations and Improvements

The simulation gains differed from those calculated in the analytical section, and the PI tuning calculations require further review. The reported response measurements should therefore be treated as exploratory coursework results.

Source code for the base-axis circular-motion attempt and the optional physical drawing demonstration has not yet been located. The videos document observed movement but do not make these demonstrations reproducible from the repository.

Further improvements would include:
- Checking model parameters and units
- Reconciling analytical gains with simulation settings
- Verifying PI tuning calculations
- Measuring settling time and steady-state error consistently
- Comparing PD, PI and PID under the same test conditions
- Recovering missing code and documenting the trajectory implementation
- Documenting a reproducible simulation setup

The submitted controllers are retained as coursework and should not be treated as validated software for physical robot control.

## Running the Simulation

The original setup depends on the course's ROS 1 environment, CrustCrawler packages and Gazebo.

See [Taskdescription.pdf](Taskdescription.pdf) for the original workspace and launch instructions.

Those instructions refer to course-specific resources and an older environment. They have not been verified as a working installation procedure outside the IFI setup.

[Back to project overview](../README.md)
