https://www.youtube.com/watch?v=-qV1_xyrgzs
- Track the motor position down to zero speed by injecting signals
- The inductance of the motor on the DNQ axis is dependant on the position

Perplexity: Why do sensorless motors cog at 0 speed?
- Sensorless motors cog at 0 speed due to the interaction between the permanent magnet and the slotted stator. The permanent magnet, as it rotates, interacts with the steel lamination's in the stator, creating a torque that causes the motor to stutter or jump at low speeds. This phenomenon is more pronounced at lower speeds because the motor is not yet moving quickly enough to smooth out the interaction between the magnet and the stator

The inductance of the motor depends on the motor position. The teeth of the motor don't always line with the stator depending on the rotor position, so the inductance changes. That's why 2-pole in-runners don't work well, because they are very smooth, and the inductance doesn't change very much.

- 4-pole synchronous motors and generators have solid rotors with salient poles while 4-pole induction motors and generators have squirrel cage rotors. In 2-pole motors and generators the rotors are cylindrical

Terminal plot for current and inductance:
```bash
foc_plot_hfi_en 2
```
- Press 'full brake' (the anchor next to 'STOP')
- Get a sinusoidal graph

Space vector modulation diagram. In the alpha and beta frame, in the FOC control. Output a voltage vector at some angle. And then in the opposite direction at some amplitude. Then measure the currents and take the difference. Then rotate the motor and do it again 8, 16 or 32 times in a revolution.

Using the resitance, voltage and time, the inductance can be derived.

The inductance is then plotted at all the positions. You cannot tell however if the rotor position is at a north or south pole tooth of the stator. Iron core magnets have a property that when you put a voltage step, the current will initially rise linearly with a low gradient, after the voltage saturates, the current will rise faster. The north and south bias will rise at different points.

Find difference in and Ld-Lq axis inductance. 

https://www.youtube.com/watch?v=H-6qzmeCNtw&t=34s

Silence by running half the zero vector frequency (32 kHz), and only 2 injections are made instead of 16.

45 deg does not work (constant high pitched noise, doesn't move). Possibly because the inductance value was not accurate enough. Try and adjust the inductance and see if it helps

Better than encoders and hall sensors. However the inductance value must be accurate.

Coupled HFI works better. This does injection in the D axis, as opposed to the difference between the d and q axis. Less sensitive to absolute axis. Doesn't work very well when in the saturation region.
