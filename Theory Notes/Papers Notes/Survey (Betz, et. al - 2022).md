
### Definition of Autonomous Racing
- Race Cars
	- 4 Wheels
	- Combustion or Electrical Engine
	- Real race car (F1) or small-scale (F1Tenth)
- Software and hardware surveyed has a clear connection to automobile racing
	- Simulate race car within a racing environment
	- Specific solutions to racing problems

![[Pasted image 20240129083914.png]]

### Perception

General term for the algorithms that perceive the environment and derive knowledge from it.
- Detecting objects
- Detecting free space
- Mapping the environment
- Localising the vehicle
![[Pasted image 20240129084541.png]]

Fundamental perception problems:
- High speed object detection
- High speed localisation and state estimation
- Localisation on wide areas without specific landmarks
- Precise localisation information necessary to achieve high dynamic trajectory planning and control

### Planning

Plan trajectories for the car to drive around the racetrack.

- Global Planning 
	- Optimise the line for the lowest lap time
- Local Planning
	- Operate in a certain time horizon
	- Aims to avoid obstacles while still providing a fast and reliable path
- Behavioural Planing
	- Provides information about the high level mission planning

Fundamental planning problems:
- Minimum-time optimisation for global optimal race-line
- Long local planning horizon for recursive feasibility
- Obstacle avoidance and vehicle reaction at high speeds
- High re-planning frequency for real-time capability
- Decision making under high uncertainty
- Interaction planning with non-cooperative agents
![[Pasted image 20240129115350.png]]
