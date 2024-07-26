
##### Step 1: Transport the code on a memory stick
Copy the workspace you made from (Starting the simulator) to usb (NTFS format)

##### Step 2: Connect the battery and accessories to the car
First check the battery charge:
charge to 4.2V/Cell
storage to 3.8V/Cell
not lower than 3.5/Cell

**Using the checker**
- Orientate the checker so the display is facing you
- Orientate the black and red wires from the 4-wire JST cable, so that the black wires are on the left and the red are on the right
- Plug the wires into the battery with these orientation, with the JST connected to the far left 4 pins on the checker
- The checker should beep and display the voltage of each cell and the total voltage

Charging the battery (EZ-peak Dual)
- Plug the charger to the wall
	- The charger will Flash the LEDs (Run upwards direction) while standing by
- Connect the battery as shown:
- ![[Traxxas Charger.jpeg]]
- Press and hold the "Charge rate select" button and the "START/STOP" button together until there is a beep
- Use the selector button to make sure the light is on balance charge
- Use the selector button to make sure the battery type is on LiPO
- Use the "Charge rate selector" button to choose 3A
	- All of these elections is confirmed by the corresponding LED on next to the label
- Hold down the "START/STOP" for a second or 2 for the charging to start
- The charger will make a sound when it starts
	- The green light at the top will blink while charging
	- The RED current lights will go up to 3A from 1A while charging
- When charging is done, the green light will be steady and the charger will make a sound
	- May have to remove when the light is at 3A.
- Remove the battery and turn off the charger

Plug the following accessories to communicate with the car:
- Monitor (HDMI)
- Keyboard (USB)
- Mouse (USB)
- Memory stick with workspace (USB)

Connect the battery, 
- JST: (Orientate the wired, Red to brown)
- Yellow connector (One orientation)

##### Step 3: Starting the system
Flip the on switch, so the 2 toggle switches are in the on position

Once the computer is at the home screem:
- Create a folder in the Home directory with the same name as your ros project (e.g. user_test)
- Copy the workspace you made (e.g. ros2_ws) and paste it in the folder you made

Open a terminal and add the source line to the .bashrc
```bash
gedit ~/.bashrc
```
Add the following line:
`source ~/user_test/ros2_ws/install/setup.bash`

Now in the terminal, build your ROS workspace
```bash
cd user_test/ros2_ws
colcon build --symnlink-install
```

##### Step 4: Put the code onto the car
Open 5 terminals (4 on the left, 1 big on the right)

Ctrl + Shift + E
Click the first window
Ctrl + Shift + O
Ctrl + Shift + O
Click the first window
Ctrl + Shift + O


(Labeled Up to Down, Left to Right)
###### Terminal 1:
```bash
urg
```

###### Terminal 2:
- Turn on the PS4 controller by pressing the PS button, and see connected bluetooth devices.
```bash
bringup
```
- You'll notice a line that says 'Connected Bluetooth Device' if it is successful
###### Terminal 3:
```bash
pf
```
###### Terminal 4:
```bash
ros2 run rviz2 rviz2
```
###### Terminal 5:

```bash
ros2 run user_test Moving_Forward
```