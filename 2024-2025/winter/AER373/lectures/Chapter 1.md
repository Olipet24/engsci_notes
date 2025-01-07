**Structure**: object designed to transmit forces

Aircraft structures are designed to transmit lift forces from the wings and the fuselage to the wing box, the stiffest/strongest part of the aircraft

Materials composed of atoms in crystalline pattern. Forces change the distance between atoms, but reach a new equilibrium state by minimizing the pot. energy of the system.

We assume that the materials are **continua**. The averaged force acting in a continuum is called **Stress**. 
- Stress is fundamental model effect of forces on materials

#### Purpose of Stress analysis

1. can the material survive the applied loads?
	- Will the material yield? <- when material behaves plastically
	- Will the material fracture? <-cracks
	- Will the material creep/fatigue?
		- Fatigue: When the material repeatedly cycled and used <-most common in aerospace (microscopic cracks occur (unavoidable))
		- Creep: Very slowly deforms eg. concrete
2. Can the structure serve the purpose it is intended:
	- will the deformations make the part unusable or dangerous? <- anneal
	- will the structure buckle due to compressive loads? <- non-elastic property

The goal of stress analysis of solids and structures is to determine the stresses and strains in a structure of arbitrary shape with known body forces + imposed fores and displacements at boundaries.

Once strains are known => displacements can be calculated using integration

In general stressed bodies are not statically determinate, solving problem requires:
1. Equilibrium: The governing DE
2. Boundary Conditions: External forces and constraints acting on the system
3. Constitutive model: Relationship b/w stress and strains
4. Compatibility: Continuous single value displacements

**Stress**: the force per unit area
$$\sigma = \frac{P}{A} \text{  [Pa]}$$
Stress induces a strain:
$$
\epsilon = \frac{\sigma}{E}
$$
=>Poisson's Ratio?

###