What am I trying to do?
I want to verify my wheel-slip behaviour on the simulator with the same test done on the real car. The graphs don't have to match but the behaviour must match.

Once it is verified, the simulator can be trusted to develop the required control techniques:
- ABS
- Longitudinal Traction Control
- Lateral Traction Control

 Recent paper by ForzaETH 2024
 - Velocity estimation based on EKF (https://link.springer.com/chapter/10.1007/978-3-319-08338-4_25)
 - However the velocity estimation is not accurate 
" The longitudinal velocity state estimates produced by the two systems in question are depicted in Fig. 10. The algorithm was executed for approximately one minute in order to calculate performance metrics, while the trajectories were plotted for a reduced time corresponding to two laps of the test track. The RMSE over the entire testing time was then computed for both localization frameworks, as summarized in Table 5. The localization performance yields a low positional RMSE of ∼ 0.08m, on the other hand, the velocity estimation RMSE yields a rather high ∼ 0.25ms−1 and still leaves room for improvement. A possible reason for the worse performance of the velocity estimation is, that the velocity directly originates from the Odometry Filter as in Section 4.2 which fuses the information from ERPM wheel-odometry and IMU data, where the ERPM data is highly influenced by the friction of the track and can easily result in a low-quality odometry signal due to wheel-slip."

##### CHATGPT on how to make a velocity estimator:

Measuring the velocity of a moving body can be accomplished through various accurate methods, depending on the context, equipment available, and the nature of the motion. Here are some accurate methods commonly used:

1. Radar Gun
- Principle: Uses the Doppler effect to measure the velocity of an object.
- Usage: Commonly used in sports (e.g., measuring the speed of a baseball pitch) and law enforcement (e.g., measuring the speed of a vehicle).

2. Laser Doppler Velocimetry (LDV)
- Principle: Uses laser beams to measure the velocity of particles in a fluid or on the surface of a solid body.
- Usage: Often used in fluid dynamics experiments and industrial applications for precise velocity measurements.

3. Pitot Tube
- Principle: Measures the fluid flow velocity by converting the kinetic energy in a flow stream to potential energy.
- Usage: Widely used in aviation to measure the airspeed of aircraft.

4. High-Speed Camera and Motion Analysis
- Principle: Captures rapid sequences of images which are then analysed to determine the position of the object over time.
- Usage: Used in scientific research, biomechanics, and sports analysis to measure velocities with high precision.

5. Global Positioning System (GPS)
- Principle: Uses satellite signals to determine the position and movement of an object over time.
- Usage: Commonly used in vehicles, smartphones, and outdoor sports to measure speed and track movement.

6. Accelerometer and Gyroscope Sensors
- Principle: Measure the acceleration and angular velocity of an object, which can be integrated over time to determine velocity.
- Usage: Found in smartphones, wearables, and various scientific instruments for motion tracking.

7. Tachometer
- Principle: Measures the rotational speed of a shaft or disk.
- Usage: Used in engines and other mechanical systems to determine the rotational velocity.

8. Timing Gates
- Principle: Measures the time it takes for an object to pass between two points.
- Usage: Used in sports (e.g., sprinting) to measure speed over a known distance.

9. Ultrasonic Sensors
- Principle: Emit ultrasonic waves and measure the time it takes for the waves to reflect back from an object.
- Usage: Used in robotics and automotive applications for distance and speed measurement.

10. Inertial Measurement Units (IMUs)
- Principle: Combine accelerometers, gyroscopes, and sometimes magnetometers to measure the orientation and velocity of an object.
- Usage: Used in drones, spacecraft, and wearable devices for comprehensive motion tracking.