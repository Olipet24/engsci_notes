
### Microscopic Vs Macro descriptions

System of gas molecules in the room:
- Microscopic description: gas is made of many particles each with instantaneous positions, velocities, and internal energies, which is not computationally efficient and impossible to calculate
- Macroscopic description: assume gas is a continuum, which has a collective response, and greatly reduces information we need to describe behavior of the gas. We can describe the system by using a small number of intensive + extensive macro quantities
	- under thermodynamic equilibirum, macro description reduces to intensive macro properties of pressure and temperature

#### Gas kinetic theory
- Statistical based approach for describing state of collection of gaseous particles
- many possible microscopic states of gas represent through PDF, $f(t, \vec{x},\vec{v}, \phi_{k})$,
	- $\vec{x}$ is position coordinates, $\vec{v}$ is random variables associate with translational velocities, and internal dof $\phi_{k}$
- requires the solution of a high-dimensional, integral-differential equation for $f$ (i.e. boltzmann equation).

#### Continuum treatment and gasdynamics
- provided sufficien no. of intermolecular collisions, collection of gaseous particle near LTE (local thermodynamic equilibrium) can be treated as continuum
	- in this case avg. macro properties is sufficient
![[Pasted image 20250109164424.png]]
- measure of high inter-molecular collisional rates leading to near LTE provided by **Knudsen No.**
 $$
\text{Kn} = \frac{\text{mean free path}}{\text{characteristic length}} = \frac{\lambda}{l}
$$
- non dimensional parameter which measures gas potential to maintain conditions of thermo equil.
	- Lower no. allows for good continuum assumption (i.e $\text{Kn} \ll 1$ or $\text{Kn} < 0.1$)
	- under normal conditions, the mean free path is 100-500 times the molecular diameter, and ratio of intermolecular seperate distance d, to the molecular diameter is of order 10. Thus mean free path is approx 10-50 times greater then mean molecular seperation distance
Under STP conditions at sea level, the mean free path of air is:
$$
\lambda_{\text{air}} = 6.6 \times 10^{-8} \text{m}
$$

Thus, continuum treatment valid for:
$$
l > 6.6 \times 10^{-6} \text{m}
$$
For air under STP conditions at altidue of 130 km, number density lower then sea level => $\lambda = 10.2 \text{ m}$
Thus continuum only valid for $l > 10^3 \text{ m}$

#### Definition of Compressibility

**Compressibility** (coeff. of compressibility), $\beta$

