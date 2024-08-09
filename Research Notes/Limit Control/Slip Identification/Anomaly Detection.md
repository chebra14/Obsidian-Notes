*What I want it to do v. What it's actually doing*

##### General

- Steering is not equal to request
- Wheel speed is not equal to request

This could be due to:
- Control errors (PID not tuned correctly)
- Bad sensor feedback

##### Straight

- Wheel-spin (Velocity Solution)
- Wheel-lock (Velocity Solution)
- Non zero yaw (Gyro solution)

##### Turning

- Oversteer (Gyro solution)
- Neutral Steer (Velocity Solution)
- Understeer (Gyro solution)

###### Skid Steer

- Spinning