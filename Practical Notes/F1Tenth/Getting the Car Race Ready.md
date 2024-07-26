#### Notes

- Jetson doesn't work when battery drops below 11.5V

- Shutdown the car with a one minute timer from the terminal
	- `sudo shutdown`

- Jetson password
	- `jetson`

- Powering the car from the jack doesn't power the VESC

#### VESC HFI Tuning

Try adjusting the inductance value of the motor that might help with the 45 deg silenced mode which can have more available torque from the motor.

##### VESC.yaml

- 3606.0
- 0.0

- -1.2135
- 0.5304
##### Joy-teleop.yaml

Line 32:
- scale:50

#### Friction Test

Measured the frictional force of the car
- Estimated mu: (lateral) 0.903293972335692
#### Start Stop Test

The board that the lidar bounces off is tilted.
- Pitch forward is amplified.
- Pitch back is de-amplified
If the car veers from the straight the distance from the lidar increases and becomes inaccurate.

Current issue *Can't go backwards
#### Hardware To Consider
- Safe LiDAR
- Safe body
- Safe wires
- Monitor, keyboard, mouse combo
- More batteries
- Power Supply (12V, 20W)