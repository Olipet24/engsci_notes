
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

### Definition of Compressibility

**Compressibility** (coeff. of compressibility), $\beta$: measure of realitve volume change of fluid element in response to application in change of pressure:
$$
\beta \equiv -\frac{1}{\hat{\nu}} \frac{d\hat{\nu}}{d p}
$$
where $\nu$ is fluid volume, and $p$ is the pressure
 if fluid element assume to have unit mass, then $\hat{\nu} = \nu$. and $\nu = \frac{1}{\rho}$ which is the spefic volume
Thus
$$
\beta = -\frac{1}{\nu} \frac{d\nu}{d\rho}=\frac{1}{\rho} \frac{d\rho}{dp}
$$

where:
$$
\frac{d\nu}{d\rho} = -\frac{1}{\rho^2}
$$

Which can be rewritten to show that fluid experiences a change in pressure $dp$ the corresponding changes in specific vol $d\nu$ and density $d\rho$ will be
$$
d\nu = -\beta \nu dp
$$
and 
$$
d\rho=\beta \rho dp
$$
Compression of fluid is path dependent and change in the specific vol. will depend on the compression process. 
From thermo, if we assume that $\nu = \nu(T, s)$ or $\rho = \rho(T, s)$ and $p = p(T,s)$, then we can write by using the chain rule:

![[Pasted image 20250109165649.png]]
The first term is iso thermal, and the second is isotropic

![[Pasted image 20250109165740.png]]

The former defines compressibility for processes in which the temp remains const. and the other for reverse adiabatic compressions (no heat is added to taken away from fluid element)

For water under STP conditions (1 atm)
$$
\beta_{T} = 5 \times 10^{-10} \frac{\text{m}^2}{\text{N}}
$$
for air:
$$
\beta_{T} = 10 \times 10^{-5} \frac{\text{m}^2}{\text{N}}
$$
Thus gas is *far more* compressible then liquid

### Flow regimes
- defined by mach number:
$$
M = \frac{V}{A}
$$
where $V$ is the flow velocity and $a$ is the speed of sound for the gas or speed of sound speed. The formal definition of the sound speed is as follows:
$$
a^2 \equiv \left( \frac{\partial p}{\partial \rho} \right)_{s}
$$
Since the speed of sound can be related to the isentorpic compressibility as follows:
$$
a^2 = \frac{1}{\rho \beta_{s}}
$$
Freestream mach number:
$$
M_{\infty} = \frac{V_{\infty}}{a_{\infty}}
$$
**Incrompressible Subsonic** $M_{\infty} \leq 0.1$
![[Pasted image 20250109171523.png]]
Relatively smooth streamlines and continous varying low properties

**Compressible Subsonic** $0.1 \leq M_{\infty} \leq 0.8$
![[Pasted image 20250109171736.png]]

**Transonic Regime** $0.8 \leq M_{\infty} \leq 1.2$
![[Pasted image 20250109172003.png]]
**Supersonic Regime** $1.2 \leq M_{\infty} \leq 5$
![[Pasted image 20250109171943.png]]
**Hypersonic Regime** $M_{\infty} \geq 5$
![[Pasted image 20250109171911.png]]