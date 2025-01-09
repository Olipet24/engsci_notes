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

in this case, static electrical systems do not have energy storag 