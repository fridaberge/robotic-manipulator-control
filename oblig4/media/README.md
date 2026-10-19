# Assignment 4 — Media

Videos, screenshots and diagrams supporting the feedback-control experiments, ROS/Gazebo simulation work and optional physical-robot exercise.

## Video Demonstrations

### Physical Robot — Circular Drawing Attempt

[circle_drawing.mp4](circle_drawing.mp4)

The robot performs a circular movement with a marker but does not reach the paper. The base-frame height was not accounted for when positioning the drawing trajectory, leaving the marker above the drawing surface.

### Physical Robot — Excessive Downward Movement

[circle_motion.mp4](circle_motion.mp4)

In this attempt, the arm moves too far down and makes forceful contact with the table. The recording documents a vertical-positioning issue, not a successful drawing demonstration.

### Gazebo Simulation

[circle_gazebo.mp4](circle_gazebo.mp4)

Circular-motion footage from the Gazebo simulation environment.

### Context and Limitations

The physical-robot videos document an optional practical exercise completed with substantial guidance and assistance. This exercise was separate from the mandatory assignment and is not presented as an independently developed trajectory-planning implementation.

The recordings highlight the importance of accounting for the base-frame height and checking the trajectory's vertical position and clearance before physical execution. They do not demonstrate a validated or safe drawing implementation.

The source code associated with the physical drawing attempts is not currently included in this repository.
## Controller Responses

- [PI.png](PI.png) — Response plot from the PI-control experiment.
- [best_set.png](best_set.png) — Response plot for the tuned settings discussed in the report.
- [graf.png](graf.png) — Response plot from the PD-control experiment.

These plots accompany the report's discussion of tuning, settling time and steady-state error. See the assignment README for limitations concerning the calculations and response measurements.

## Simulation Setup

- [bilde1.png](bilde1.png) — Screenshot documenting the launch of the rqt graph interface.
- [bilde2.png](bilde2.png) — Screenshot documenting the Gazebo simulation setup.

## Base-Axis Rotation Attempt

- [rot1.png](rot1.png)
- [rot2.png](rot2.png)

These screenshots show the robot rotating around its base axis during the approach described in the submitted report.

This movement differed from the requested Cartesian drawing trajectory. It should be distinguished from the separate optional physical-robot drawing exercise shown in the videos.

## Control-System Diagrams

- [tegning.jpg](tegning.jpg)
- [tegning2.jpg](tegning2.jpg)
- [tegning3.jpg](tegning3.jpg)

These drawings show the control-system block diagrams developed during the assignment. Consult the submitted report for the explanation of each diagram.

[Back to Assignment 4](../README.md) · [Project overview](../../README.md)
