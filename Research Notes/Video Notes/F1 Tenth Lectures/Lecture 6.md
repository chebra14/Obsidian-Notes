## Vehicle States, Vehicle Dynamics and Map Representations

### Vehicle States

- Car is a dynamic system with linear and non-linear behaviour.
- Represented wit Ordinary Differential Equations (ODEs)
- $\dot x = Ax + Bu$ 
- $y = Cx$
- The system has states and state matrix ($Ax$) and an input and input matrix ($Bu$)
- Output ($y$) and Output matrix ($Cx$)

CHATGPT:

In control systems, specifically in the context of state-space representation, the term "x dot matrix" typically refers to the matrix representing the derivatives of the state variables with respect to time. Let's break down the terminology:

1. **State Variables (x):** In control theory, a system's behavior is often described by a set of state variables, which are variables that define the current state of the system. These variables could represent physical quantities such as position, velocity, temperature, etc.
    
2. **Derivative (dot notation):** The "dot" notation, such as ẋ, represents the first derivative of a variable with respect to time (dx/dt). It indicates how fast the variable is changing.
    
3. **State-Space Representation:** In control systems, the state-space representation is a mathematical model that describes the behaviour of a dynamic system. It consists of two main matrices - the state matrix (A) and the input matrix (B). The state vector x contains the state variables.
    

Now, the ẋ matrix, often denoted as A*x, represents the derivatives of the state variables. In a continuous-time system, it's a way of expressing how each state variable changes over time. Mathematically, it is given by:

$\dot x = Ax$ 

Here, A is the state matrix, x is the state vector, and x˙x˙ is the vector containing the derivatives of the state variables.

In discrete-time systems, you may see a similar representation using the difference equation:

$x_{k+1}=A\cdot x_k​$ 

In both cases, the $\dot x$ matrix or expression represents the dynamics of the system in terms of how the state variables evolve over time.

- Vehicle sensors derive the states (behaviour and position)
- Position ($x$ and $y$). Heading ($\theta$). Frenet Frame. Velocity. Acceleration. Steering angle.
- Additional. Sideslip angle. Slip angle. Wheelslip.

- Frenet: continuous, differentiable curve in 3D Euclidean space.
- Coordinate system spanned by a tangential vector $t$ and normal vector $n$. 
- s-coordinate is the run length. s = 0 at the beginning of the reference path.
- d-coordinate is lateral positions relative to reference path. d = 0 on the reference path. positive left.
- Distance to the centre line d. Progress along the track s.

### Vehicle Dynamics Modelling
- The more accuracy of a model, requires more model parameters.

- Single Track Model
- Kinematic Single Track Model (Slow)
- Linear Single Track Model (Limits)
- Nonlinear Single Track Model

- Why need it?
- Vehicle Dynamics Simulation
- State Estimation
- Behaviour Prediction
- Model-Based Algorithms