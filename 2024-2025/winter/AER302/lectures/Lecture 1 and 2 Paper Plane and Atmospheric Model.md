This lecture covers quercus lectures 1 and 2

## <u>Syllabus</u>

Every week, there is a 5 minute presentation, first group gets min(3) and coached by professor worth 5%

## <u>Paper plane Example </u>

For paper airplane: $L = Wcos(\gamma), D = Wsin(\gamma)$, where $\gamma$ is the angle relative to the horizontal and the velocity vector of the plane, and $W$ is the normal force

From these equations, we derive performance terms to be $tan(\gamma)_{min} =\frac{D}{L} = \frac{1}{\frac{L}{D}} = \frac{1}{\frac{C_L}{C_D}_{max}}$
###### N2L equations for flight of airplane

$m\dot{v} = -Wsin(\gamma) - D = -Wsin(\gamma) - \frac{1}{2}\rho v^2 S C_D$ 
$mv\dot{\gamma} = -Wcos(\gamma) + L = -Wcos(\gamma) + \frac{1}{2}\rho v^2 S C_L$

From these equations, we want to solve for the $v(t)$ and $\gamma(t)$ to solve for the trajectory of the plane

## <u>Atmospheric Flight </u>

####  (Standard) Atmospheric Model
These variable are important in modelling the atmosphere
- Temperature
- Density
- Pressure

### Fundamental Concepts
1. Perfect gas: $P = \rho R T$
2. Hydrostatic Equation: $\delta P = -\rho g \delta h$, $h$ is the altitude

<u>Altitude</u>:
1. Geometric: $h_G$ above ground (surface)
2. Absolute: $h$ w.r.t Earth center: $h = h_G + R$, where $R$ is the Earth's radius
3. Geopotential: $h$ (assuming that gravity is constant)

For (3.), the gravitational constant can change with respect to different coordinates/locations on earth

In this class we assume that $h$ is Geopotential, since difference between earth's surface and 65 km, the difference is very, very small.

### Relationships between Temperature, Pressure, Density, and Altitude

##### Graph based on observation:
![[Pasted image 20250106104517.png]]
Notice that the vertical regions are *Isothermal*, the temperature does not change
#### Gradient Region (Troposphere (0-11 km))
$T = T_1 + a_1 (h - h_1)$
$a_1 = -0.0065 K/M$
Thus, differentiating yields
$dT = a_1 \delta h$

From hydrostatic equation:
$dT = -\rho g \delta h$
$\frac{\delta P}{P} = \frac{- g \delta h}{R T} = -\frac{g}{a_1 R} \frac{\delta T}{T}$

=>$ln(\frac{p}{p_1}) = -\frac{g}{a_1 R} \frac{T}{T_1}$
$\frac{P}{P_1} = \frac{T}{T_1}^{-\frac{g}{a_1 R}}$

Using the Ideal gas law (2.) we can derive an expression for density

$\frac{\rho}{\rho_1} = \frac{T}{T_1}^{-\frac{g}{a_1 R} - 1}$

#### Isothermal Region
- $T = T_1$

$\frac{\delta P}{P} = -\frac{g}{R T} \delta h$
Integrating:
$P = P_1e^{\frac{-g}{RT}(h-h_1)}$
Using the ideal gas law:
 $\rho = \rho_1 e^{\frac{g}{RT} (h-h_1)}$

Where the subscript 1 values are taken from the base of the isothermal layer
#### Example Problem
At Sea level: 
- $T_s = 288.16 K$
- $P_s = 1.01 * 10^5 N/m^2$
- $\rho_s = 1.225 kg/m^3$
At 11K km, use the Gradient region equations
At 14 km, use the Isothermal region equates

#### Pressure Altitude
@ SAM: Represented by **Altitude**
=> The altitude corresponding to an actual pressure reading is called the pressure altitude
=> represents the pressure in the unit altitude