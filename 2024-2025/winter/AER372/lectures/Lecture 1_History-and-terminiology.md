
## Syllabus and Course Information

Office Hour: Thursday 11-12 SF4003

Course notes: self sufficient; if you closely follow the notes and listening in the class, it is enough to be successful in the class, but the textbook is useful

Thursday: 1 hr lecture, 1 hr tutorial

**Create Lab groups for by Monday 27th**
- Labs has a preparation proportion
- Need to read the general health and safety portion

Final exam comes from the recommended problems, so make sure to do them

## Lecture content

Purpose of a control mechanism: maintain process characteristics at the desired targets despite the effects of external noise and other perturbations by:
- ensuring systems stability at all times;
- reducing the difference between the system's real and desired ultimate behaviors (steady state)
- creating proper system dynamics (transient response) towards desired targets
- mitigating the effect of external factors on system's behaviors

**Control Mechanisms**:
- Natural Controllers:
	- Controlled by nature, happen due to laws of physics
- Artificial (Human Made control systems)
	- uses inputs and math to make a decision

**Artificial Control Systems**:
- manual control: control actions made by humans (Car, Canadarm2)
- Automatic control: Some or all aspects of system's behavior controlled without human's intervention (UAV, Nuclear Power Plant)

**Automatic Control Systems**:
- Regulatory control: controller maintains the system at a desired set point (despite noise)
	- i.e. thermostat
- Tracking (servo) control: ensures that system output(s) follows a desired trajectory (despite noise)
	- i.e. rover path tracking

Can also divide Automatic control systems as:
- Open-loop control: The controller does not rely on the systems behavior to adjust the systems command, there is no feedback
	- i.e. Toaster
- Closed-loop (feedback) Control: controller determines control actions based on measurements of the systems controlled output
	- Capable of handling system variations and uncertainties, external noise and disturbances, and unsatisfactory dynamics

### Closed-loop Controller
Pros:
- robustness to uncertainty unknown or inaccurate plant model, external  disturbances, sensor and actuator noise)
	- Reliable sensing leads to system correction through computation and actuators
- modification: can modify natural performance
Cons:
- more complex
- can potentially make system unstable, 

**Classic Feedback Control**
- system parameters are mostly invariant or insignificantly very during operation
- control actions rely on immediate values, not future ones
- no guarantee for optimal control actions
- relise on linear input-output relationship for operation range, or in the close vicinity of normal operating input

**Robust and adaptive feedback control**:
- Can handle considerable variations in system parameters

**Predictive Feedback Control**:
- can estimate future value of output and use them for deriving control actions
**Optimal Feedback Control**:
- can obtain optimal control actions e.g. w.r.t. energy time, speed, etc.
**Nonlinear Feedback Control**:
- Can handle nonlinear input-output relationships

#### Examples
**Example 1**
![[Pasted image 20250106174301.png]]

This control system use the On-Off technique
- When the outside temperature gets below a certain threshold relative to the setpoint temp due to heat loss, the heating system turns on until temperature rises back to the temp set point
- The disturbance to the system might be opening the window or changing the temperature of the environment


**Example 2**
![[Pasted image 20250106174328.png]]
Controls the amount of gas intake in the car to control the speed of the car
For every degree of throttle change, we increase the speed by 10 mph.

***Open Loop Controller***
A disturbance to the system is the Road Grade (slope): Every 1% road grade changes speed by 5mph (-ve sign on the second control diagram shows that increase in road grade leads to *decrease* in speed).
- Use Dynamics to take in to effect that it takes time for the system to change; not an instantaneous process
The bottom Open loop equation for the third diagram, without any disturbance (w = 0)
- Since the controllers gain is the exact inverse of the plant's (throttle) gain
- r is  the desired speed, and $y_{ol}$ is the control system
$y_{ol} = 10(u - 0.5w) = -10\left( \frac{1}{10} r - 0.5w \right) = r-5w$
- Demonstrates that open loop system cannot handle *Disturbances*, but does provide accurate result without it

Error: (desired - real): $e = r- y_{ol} = 5w$ 
$e\% = \frac{e}{r} = \frac{5w}{r} \%$

![[Pasted image 20250106174349.png]]
***Closed Loop Controller***
$y_{cl} = -10(u - 0.5 w)$
$u = 10(r-y_{cl})$
=> $y_{cl} = 10[10(r-y_{cl}) - 0.5w] = 100r - 100y_{cl}-5w$

Solving for $y_{cl}$:
$101y_{cl} = 100$




**Note:** Robustness: Regulation & sensitivity
- Regulation of its disturbances
- Sensitivity to noise