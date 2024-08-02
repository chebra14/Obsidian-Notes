
CHATGPT: (26/07/2024)

You can create a function that relates skid steer (differential steering) to Ackermann steering in terms of turning radius. Both types of steering have different mechanisms for turning, but they can be mathematically related by focusing on the turning radius.

### Key Concepts

1. **Ackermann Steering**:
    - This involves turning the front wheels at different angles to achieve a specific turning radius. The steering angle $\theta$ is related to the turning radius $R$ by the wheelbase $L$ (distance between the front and rear axles) and the speed of the vehicle.

1. **Skid Steer (Differential Steering)**:
    - In this type of steering, the left and right wheels are driven at different speeds. The difference in speed between the left and right wheels creates a turning radius $R$. The turning radius is influenced by the width of the vehicle $W$ (distance between the left and right wheels) and the speed difference.

### Mathematical Relationship

For a vehicle using Ackermann steering, the turning radius $R$ can be expressed as:

$R = \frac{L}{\tan(\theta)}$

Where:

- $L$ is the wheelbase.
- $\theta$ is the steering angle of the front wheels.

For a skid steer vehicle, the turning radius $R$ can be expressed as:

$R=\frac{W}{2}×\frac{v_{\text{left}}+v_{\text{right}}}{v_{\text{left}}−v_{\text{right}}}$

Where:

- $W$ is the width of the vehicle.
- $v_{\text{left}}$ and $v_{\text{right}}$ are the speeds of the left and right wheels, respectively.

### Function to Relate Ackermann Steering Angle to Skid Steer Speed Difference

To relate the steering angle $\theta$ in an Ackermann steering system to the wheel speeds in a skid steer system for the same turning radius $R$, you can set the two expressions for $R$ equal to each other and solve for the desired variables.

Given:
$R=\frac{L}{\tan⁡(\theta)}=\frac{W}{2}×\frac{v_{\text{left}}+v_{\text{right}}}{v_{\text{left}}−v_{\text{right}}}$

### Solving for $v_{\text{left}}$ and $v_{\text{right}}$

Rearrange the equation to isolate $v_{\text{left}}$ and $v_{\text{right}}$​. For simplicity, let's introduce a variable $k$ where:

$k = \frac{L}{W} \tan(\theta)$

Thus the equation becomes:

$2k = \frac{v_{\text{left}} + v_{\text{right}}}{v_{\text{left}} - v_{\text{right}}}$

Multiply both sides by ($v_{\text{left}} - v_{\text{right}}$) to get:

$2k(v_{\text{left}} - v_{\text{right}}) = v_{\text{left}} + v_{\text{right}}$

Distribute and rearrange to find $v_{\text{left}}$ and $v_{\text{right}}$:

$2k(v_{\text{left}} - v_{\text{right}}) = v_{\text{left}} + v_{\text{right}}$

$(2k - 1)v_{\text{left}} = (2k + 1)v_{\text{right}}$

Now, solve for $v_{\text{left}}$ and $v_{\text{right}}$​:

$v_{\text{left}} = \frac{(2k + 1)}{(2k - 1)}v_{\text{right}}$​

Thus, if $v_{\text{right}}$ is known or chosen, $v_{\text{left}}$​ can be calculated, and vice versa. The ratio between $v_{\text{left}}$ and $v_{\text{right}}$​ determines the turning radius equivalent to the steering angle $\theta$ in an Ackermann system.

Therefore...

$\theta = \arctan(\frac{2L(n-1)}{W(n+1)})$

where $n$ is the ratio $\frac{v_{\text{left}}}{v_{\text{right}}}$

$n = \frac{2L\tan(\theta) + W}{2L\tan(\theta) - W}$
