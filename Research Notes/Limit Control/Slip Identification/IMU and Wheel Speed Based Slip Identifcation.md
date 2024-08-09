#### IMU Based Localisation and Slip Estimation

*Jinyang, Yi et. al*

4 WHEEL SKID STEER ROBOTS
IMU measurements (accelerometer and gyroscope) and wheel speed measurements (encoders) are used for slip and localisation estimation.

This is done with a non-linear KF (Kalman Filter). The wheel-slip measurements are fed-back into the KF to improve the accuracy over dead-reckoning localisation.

#### Joint Wheel-Slip and Vehicle Motion Estimation

*Berntop, Karl*

FRONT WHEEL DRIVE CAR
IMU, GPS and wheel-encoders are used. Joint vehicle-motion and wheel-slip.

Estimations for 16 states:
- Pos
- Vel
- Accel
- Gyro bias
- Roll
- Yaw
- Yaw rate
- Yaw accel
- Slip

Linear states are estimated using a constrained Kalman filter. The longitudinal velocity and yaw angle are too non-linear to be linearised by the Kalman filter. A particle filter is used for these states. 

Assumptions/Further work
- Calibration improvements can be taken into account based on where the IMU is located. 