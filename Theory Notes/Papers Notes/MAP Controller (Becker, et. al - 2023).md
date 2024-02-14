
The challenge with autonomous racing
- Completing the lap at high speed.
- The car's behaviour is highly non-linear

Three categories of control strategies
- Reactive Methods
	- Compute control actions based on sensor input
	- No proper state estimation
	- Performance is limited since information about the track and car is disregarded
- Geometric Method
	- Uses geometric properties, usually from a kinematic single-track model
	- Pure pursuit, Stanley control
	- Do not take into account the dynamic model
- Model-Based Controller
	- MPC (Model-Predictive Control) Methods
	- Apply optimal control over a receding horizon
	- Takes vehicle dynamic model into account
	- Precise state-estimation and knowledge of the car and delays are required
	- Most computationally demanding
	- Difficult to implement

This paper proposes to incorporate model knowledge into simple control architecture of geometric controllers.

**MAP** 
- High accuracy
- Low complexity
- Track an arbitrary race-line trajectory at high-speed

Uses the Pacejka tire model

Current SotA
- MPC 
	- Complex
	- Not implemented Commonly on F1Tenth
- Pure Pursuit
	- Simple
	- Commonly Implemented
	- Pursues a look-ahead point on the raceline
	- Based on where it wants to go, it generates a steering angle
	- A large look ahead distance causes corner cutting
	- A small lookahead causes oscillations