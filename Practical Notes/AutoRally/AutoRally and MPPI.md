![[AutoRally Fig_1.png]]

### AutoRally Platform

Platform requirements:
- Operate outdoors
- Drive on uneven dirt surfaces
- Carry desktop equivalent computer with discrete GPU
- Carry all required sensors onboard
- Survive repeated crashes
- Built, operated, and maintained by small team

Car:
- Motor
- Brakes

Electronics on chassis:
- **GPS** receiver provides absolute position at 20 Hz, accurate to
approximately 2 cm under ideal condition
- To sense wheel speeds, a **Hall-effect sensor** and magnets arranged in a circular pattern to
trigger the sensor were installed on each wheel hub.

Electronics on Compute Box
- DM-GX4-25 **IMU** provides raw acceleration and angular rate data 
- Two machine vision **cameras**

GPS is inherently low rate and lacks orientation information. IMU measurements are
relatively high rate but do not directly provide heading or linear velocity information. By
combining the time-synchronized signals from these two sensors, a very accurate and high rate
estimate of position, velocity, and orientation can be obtained. This state information is sufficient
for many advanced control systems.
### MPPI

Model Predictive Path Integral Control

https://www.youtube.com/watch?v=1AR2-OHCxsQ

"MPPI uses a dynamics model and cost function to generate control plans by optimising over trajectory roll-outs in real time using GPU computing."

Cost:
- Staying on the track
- Achieving a desired velocity
- Control cost

Stochastic optimal control method, forward sampling. Evaluates many control sequences with weighted average of sequences.

Model trained by human driver. Bayesian linear-regression.