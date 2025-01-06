
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
- robustness to uncertainty
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