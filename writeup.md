# Flying Car NanoDegree Project 3

## Building a Controller

This is a write up which includes all the rubric points and how I addressed each one

### Implement Body Rate Control in C++

For implementing the body rate control, the desired body rate and current body rate is given, I first calculated the error in the desired and current body rate and then multiplied it with the gain parameter kpPQR to get the ubar. Then multiplied ubar with the moment of inertia Ixx, Iyy, Izz

### Implement roll pitch control in C++

In the roll pitch control function, the desired lateral acceleration, current attidue and desired collective thrust is used to calculate the desired pitch and roll rates by using rotation matrix R and using gain KpBank.


### Implement altitude controller in C++

In the altitude controller, need to calculate the desired quad thrust given the altitude setpoint, actual altitude, vertical velocity setpoint, actual vertical velocity and vertical acceleration feed-forward command.

First, calculating the error in desired and actual value of posZ and velZ and then using the gain parameters kpPosZ and kpVelZ to find the ubar and then calculating the acceleration in the z direction and from acceleration finding the thrust.

### Implement Lateral position Control in C++

In the implementation of lateral position control, horizontal acceleration is calculated by using desired lateral position, velocity, acceleration and current pose. I am calculating the difference of the desired and current postion, velocity, and acceleration and multiplying the error with the gain parameters to get the horizontal acceleration.

### Implement yaw control in C++



### Implement calculating the motor commands given commanded thrust and moments in C++

To calculate the motor commands from commanded thrust and moments, first will calculate the force for each direction x, y, z by dividing the moment with the length.

as force = torque / length

then using these forces to get the motor command for each motor