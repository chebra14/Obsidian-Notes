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
- PWM_2 = P16

Motor driver layout:

![[Motor Driver.png]]

Encoder
- Motor_1 = P18
- Motor_2 = P19

LED
- P17

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

### Version 2

SS-12D11-G5MM (Switch)
7805-TO220 (5V Reg)
78L33-TO-92 (3V3 Reg)

HLP-20P-254 (Connector)
HFST-05-TH254 (Logic Power)

CHATGPT:

The standard colour for a power LED is typically green. This colour is widely recognised and associated with an "on" state or indicating that a device is powered up and functioning properly.

For an LED indicating a different status, the colour can vary depending on the specific function or status being indicated. Here are some common conventions:

- **Red**: Usually indicates an error, warning, or that the device is in standby mode.
- **Yellow/Amber**: Often used to indicate a cautionary status or that the device is in a state that requires attention but is not critical.
- **Blue**: Commonly used for Bluetooth connectivity, to indicate that a device is ready to pair or is paired.
- **White**: Sometimes used for general status indicators, often seen in modern electronics for indicating active status or readiness.
- **Multicolour (RGB)**: Some devices use LEDs that can change col ours to convey different statuses, providing more flexibility and detailed feedback.

These conventions can vary by manufacturer and device type, but the above colours are commonly recognised for their respective indications.

| **Assignment** | **Pin** |
| -------------- | ------- |
| Power          | 5V      |
| Ground         | GND     |
| LED_Slip_1     | P17     |
| LED_Slip_2     | P4      |
| Motor_Get_1    | P18     |
| Motor_Get_2    | P19     |
| Motor_Set_1    | P26     |
| Motor_Set_2    | P16     |
| SDA            | P21     |
| SCL            | P22     |

![[BV_v1_esp32.jpeg]]

#### Calculate Yaw_Model

$\dot{\psi}_{\text{model}} = \frac{v_{\text{W1}} - v_{\text{W2}}}{D_{\text{Wheels}}}$

Where:
- $\dot{\psi}$ is the angular velocity
- $v$ is the velocity of a wheel
- $D$ is the distance between the driven wheels

$v_{\text{W}} = \text{Pulse} \times k$

$k = \frac{2\pi r}{t \times N}$

Where:
- Pulse is a counter of number of pulses per some time value $t$.
- $r$ is the radius of the wheel
- $N$ is the number of slots in the encoder wheel

*Blinking light stays on for some reason if the bluetooth terminal isn't connected