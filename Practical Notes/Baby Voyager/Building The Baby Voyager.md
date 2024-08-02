### Version 1 (Test 1)

ESP32 used as the microcontroller and the Arduino IDE. Bluetooth connects to a bluetooth serial terminal on the phone. Outputs a  formatted message with IMU and Wheel speed values.

I2C
- SDA = P21
- SCL = P22

IMU
- x = Forward
- y = Lateral
- z = Twist

Motor
- PWM_1 = P26
- PWM_2 = P14

Motor driver layout:

![[Motor Driver.png]]

Encoder
- Motor_1 = P18
- Motor_2 = P19

Power (Motor is overdriven directly from the battery)
- 5V
- GND

Calculate the maximum PWM based on LiPo battery
5V (Max for Motor)
Divide
8.4V (Max for 2 cell)

0.625 ratio
Applied to 255 max PWM
= **159 PWM** (Rounded down to 155)

ESP32 Pinout with coloured wired:

![[BV_v0_esp32.jpeg]]