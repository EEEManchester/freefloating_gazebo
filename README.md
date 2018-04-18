freefloating_gazebo
===================

A Gazebo plugin to simulate underwater vehicles and visualize with UWsim.

## Gazebo plugins
The package builds two Gazebo plugins:

- freefloating_gazebo_fluid (world plugin)
simulates buoyancy and viscous force from water

- freefloating_gazebo_control (model plugin)
opens topics for wrench and joint states, in order to control the considered robots

## Other executables

Also builds an external PID controler: pid_control.

These PID's allow position or velocity control of the vehicle body and joints. Depth control is also possible for the body, where z-depth is controlled in position while other axis are controlled in velocity.
Subscribes to setpoint and states topics, and publishes on the wrench and torque topics that are subscribed to by the freefloating_gazebo_control plugin.
Private parameters `body_control` and `joint_control` allow setting the default mode (body: position / velocity / depth, joint: position / velocity).

## Examples

The examples can be downloaded from the freefloating_gazebo_demo package.

## References

Please use the following reference when citing this work:

[O. Kermorgant, "A dynamic simulator for underwater vehicle-manipulators", International Conference on Simulatation, Modeling and Programming for Autonomous Robots SIMPAR 2014, Oct 2014](https://hal.archives-ouvertes.fr/hal-01065812)
