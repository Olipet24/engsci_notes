## Terminology
![[Pasted image 20250109103229.png]]
**System** A collection of components of interest, demarcated by a boundary interacting through certain physical principles (Device/Process/Plant. Consists of two important quantities
- **System Parameters (C)** Properties that define the components of the system
	- i.e. Mass, Resistance
- **State Variables (X)** A minimal set of vars. that completely identify the "state" of the system at each moment. For a system (with given parameters), by knowing input plus state vars. can calculate output
	- Ex: 
		- mech system: positions and velocities of a system of rigid bodies\
		- Elec system: Voltages of the nodes and current through elements of a circuit

**Static System** The output vector $Y(t)$ depends only on the input vector $U(t)$ at any time $t$. State variables *do not* change with input (system with no memory)
- Thus all state vars are actually state params.
Can represent $Y(t)$ as vector with components:
![[Pasted image 20250109103701.png]]

Example:
![[Pasted image 20250109103602.png]]

**Note:** static systems do not have energy storage elements (capacitor, inductor, mass, spring, etc). (System with no memory)

**Dynamic System** current output depends on past history as well as present input. Input changes state variables in time.
![[Pasted image 20250109104605.png]]
$X(t)$ is the state variables (as they differ with time). Note that $Y(t)$ also takes time, $t$, as a direct input.

Some dynamic systems can be acausal (depend on future values of the input vector) i.e. stock market value depends on future revenue
- Physical systems are causal, input dictates output
- 
