Single Track Environment
#### Params

From f110_env,
line 128

'mu': 1.0489, 
'C_Sf': 4.718, 
'C_Sr': 5.4562, 
'lf': 0.15875, 
'lr': 0.17145, 
'h': 0.074, 
'm': 3.74, 
'I': 0.04712, 
's_min': -0.4189, 
's_max': 0.4189, 
'sv_min': -3.2, 
'sv_max': 3.2, 
'v_switch': 7.319, 
'a_max': 9.51, 
'v_min':-5.0, 
'v_max': 20.0, 
'width': 0.31, 
'length': 0.58

mu: surface friction coefficient
C_Sf: Cornering stiffness coefficient, front
C_Sr: Cornering stiffness coefficient, rear
lf: Distance from center of gravity to front axle
lr: Distance from center of gravity to rear axle
h: Height of center of gravity
m: Total mass of the vehicle
I: Moment of inertial of the entire vehicle about the z axis
s_min: Minimum steering angle constraint
s_max: Maximum steering angle constraint
sv_min: Minimum steering velocity constraint
sv_max: Maximum steering velocity constraint
v_switch: Switching velocity (velocity at which the acceleration is no longer able to create wheel spin)
a_max: Maximum longitudinal acceleration
v_min: Minimum longitudinal velocity
v_max: Maximum longitudinal velocity
width: width of the vehicle in meters
length: length of the vehicle in meters

#### Observation

- ego_idx
- scans
- poses_x
- poses_y
- poses_theta
- linear_vels_x
- linear_vels_y
- ang_vels_z
- collisions
- lap_times
- lap_counts