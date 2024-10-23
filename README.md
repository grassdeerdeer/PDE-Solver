Survey: Survey Papers, Method Papers, Dataset, Code

## [Content](#content)
<table>
<tr><td colspan="2"><a href="#survey-papers">1. Survey</a></td></tr> 
<tr><td colspan="2"><a href="#dataset">2. Dataset</a></td></tr>
<tr>
    <td>&ensp;<a href="#benchmark">2.1 Benchmark</a></td>
    <td>&ensp;<a href="#pde">2.2 PDE</a></td>
</tr>
</table>

<a id="survey-papers"></a>
## [Survey Papers](#content)

<a id="dataset"></a>
## [Dataset](#content)

<a id="benchmark"></a>
### [Benchmark](#content)
1. PINNacle: A Comprehensive Benchmark of Physics-Informed Neural Networks for Solving PDEs. [paper](https://arxiv.org/abs/2306.08827)

<a id="pde"></a>
### [PDE](#content)


<table>
<tr>
    <td>&ensp;Name</td>
    <td>&ensp;Application</td>
</tr>
<tr>
    <td>&ensp;<a href="#advection">Advection Equation</a></td>
    <td>&ensp;</td>
</tr>
<tr>
    <td>&ensp;<a href="#burger">Burgers Equation</a></td>
    <td>&ensp;</td>
</tr>
<tr>
    <td>&ensp;<a href="#poisson">Poisson Equation</a></td>
    <td>&ensp;</td>
</tr>
<tr>
    <td>&ensp;<a href="#heat">Heat Equation</a></td>
    <td>&ensp;</td>
</tr>
<tr>
    <td>&ensp;<a href="#navier-stokes">Navier-Stokes Equations</a></td>
    <td>&ensp;</td>
</tr>
</table>


<a id="advection"></a>
#### [Advection Equation](#pde)
The advection equation, also known as the transport equation, describes the change of a physical quantity as it is transported by a fluid flow. The advection equation is widely used in fields such as **atmospheric science** to model the transport of temperature, humidity, and pollutants; **oceanography** to describe the movement of salinity and temperature; **environmental science** to simulate the dispersion of pollutants in air and water; and **engineering** to analyze the transport of heat and substances within fluids.

Its general form is:

$$
\frac{\partial \phi}{\partial t}+ \mathbf{v} \cdot \nabla \phi=0
$$

where $\phi$ is the physical quantity being transported (e.g., temperature, concentration), $t$ is time, $\mathbf{v}$ is the velocity vector of the fluid, $\nabla \phi$ is the gradient of $\phi$.

1-D:

$$
\frac{\partial \phi}{\partial t}+u \frac{\partial \phi}{\partial x}=0
$$

2-D:

$$
\frac{\partial \phi}{\partial t}+u \frac{\partial \phi}{\partial x}+v\frac{\partial \phi}{\partial y}=0
$$

3-D:

$$
\frac{\partial \phi}{\partial t}+u \frac{\partial \phi}{\partial x}+v\frac{\partial \phi}{\partial y}+w\frac{\partial \phi}{\partial z}=0
$$

where $u$, $v$, and $w$ are the fluid velocities in the $x$, $y$, and $z$ directions, respectively.


<a id="burger"></a>
#### [Burgers Equation](#pde)
Burgers equation describes the evolution of **wave profiles** in various contexts. Wave profiles describe the shape and characteristics of waves as they propagate through a medium. These profiles can include information about the wave’s amplitude, wavelength, frequency, and phase. In the context of fluid dynamics and other physical phenomena, wave profiles help visualize how waves evolve over time and space.

Burgers equation is widely used in **fluid mechanics** to model turbulence and shock waves, in **nonlinear acoustics** to describe the propagation of high-intensity sound waves, in **traffic flow theory** to simulate vehicle density and speed variations, and in **gas dynamics** to study the behavior of gases under various conditions.

Its general form is:

$$
\frac{\partial \mathbf{u}}{\partial t}+(\mathbf{u} \cdot \nabla) \mathbf{u}=v \nabla^2 \mathbf{u}
$$

where $\mathbf{u}$ is the velocity field vector, $t$ is time, $\nabla$ is the gradient operator, $\nu$ is the viscosity coefficient, $\nabla^2$ is the Laplacian operator.

1-D:

$$
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}=v\frac{\partial^2 u}{\partial x^2} \\
$$

2-D:

$$
\begin{gathered}
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}+v \frac{\partial u}{\partial y}=v\left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}\right) \\
\frac{\partial v}{\partial t}+u \frac{\partial v}{\partial x}+v \frac{\partial v}{\partial y} =v\left(\frac{\partial^2 v}{\partial x^2}+\frac{\partial^2 v}{\partial y^2}\right) \\
\end{gathered}
$$

3-D:

$$
\begin{gathered}
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}+v \frac{\partial u}{\partial y}+w \frac{\partial u}{\partial z}=v\left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}+\frac{\partial^2 u}{\partial z^2}\right) \\
\frac{\partial v}{\partial t}+u \frac{\partial v}{\partial x}+v \frac{\partial v}{\partial y}+w \frac{\partial v}{\partial z}=v\left(\frac{\partial^2 v}{\partial x^2}+\frac{\partial^2 v}{\partial y^2}+\frac{\partial^2 v}{\partial z^2}\right) \\
\frac{\partial w}{\partial t}+u \frac{\partial w}{\partial x}+v \frac{\partial w}{\partial y}+w \frac{\partial w}{\partial z}=v\left(\frac{\partial^2 w}{\partial x^2}+\frac{\partial^2 w}{\partial y^2}+\frac{\partial^2 w}{\partial z^2}\right)
\end{gathered}
$$

<a id="poisson"></a>
#### [Poisson Equation](#pde)
Poisson equation describes the potential field generated by source term. Its general form is:

$$
\Delta \phi = f
$$

where $\Delta$ is the Laplace operator, often denoted as $\nabla^2$. $\phi$ is the unknown function. $f$ is a known function, typically representing a source term or distribution.

1-D:

$$
\frac{\partial^2 \phi}{\partial x^2}=f(x)
$$

2-D:

$$
\frac{\partial^2 \phi}{\partial x^2}+\frac{\partial^2 \phi}{\partial y^2}=f(x, y)
$$

3-D:

$$
\frac{\partial^2 \phi}{\partial x^2}+\frac{\partial^2 \phi}{\partial y^2}+\frac{\partial^2 \phi}{\partial z^2}=f(x, y, z)
$$


* In **electrostatics**, it describes the relationship between the electric potential $\phi$ and the charge density $\rho$. The equation is given by:

$$
\Delta \phi = -\frac{\rho}{\epsilon_0}
$$

where $\epsilon_0$ is the permittivity of free space. 

* In **gravitational fields**, Poisson equation relates the gravitational potential $\phi$ to the mass density $\rho$.  The equation is given by:

$$
\Delta \phi = 4 \pi G \rho 
$$

where $G$ is the gravitational constant. 



* For **heat conduction**, it is used to describe the steady-state temperature distribution in a medium. The equation is given by:

$$
\Delta \phi = -\frac{q}{k}
$$

Where $T$ is the temperature, $q$ is the heat source term, and $k$ is the thermal conductivity. 

* In **fluid dynamics**, solving Poisson’s equation helps determine the pressure field necessary to maintain a given velocity distribution in the fluid. This is crucial for understanding and predicting fluid behavior in various engineering and scientific problems, such as aerodynamics, hydrodynamics, and weather modeling. The general form of Poisson equation in this context is:

$$
\Delta p = -\rho(\nabla \cdot \mathbf{u})
$$

where $p$ is the pressure, $\rho$ is the fluid density, $\mathbf{u}$ is the velocity field, $\Delta$ is the Laplace operator, $\nabla \cdot \mathbf{u}$ represents the divergence of the velocity field. This equation is particularly important for incompressible flows, where the divergence of the velocity field is zero, simplifying the equation to:

$$
\Delta p = 0
$$


<a id="heat"></a>
#### [Heat Equation](#pde)
The heat equation describes how heat (or temperature) diffuses through a given region over time. The heat equation is widely used to model heat conduction in **materials**, analyze thermal performance in **electronics**, predict temperature changes in **natural environments**, and understand temperature distributions in **medical imaging**.

Its general form is:

$$
\frac{\partial u}{\partial t} = \alpha \Delta u
$$

where $u$ is the temperature, $\alpha$ is the thermal diffusivity of the material, defined as $\alpha = \frac{k}{\rho c}$ where $k$ is the thermal conductivity, $\rho$ is the density, and $c$ is the specific heat capacity.

1-D:

$$
\frac{\partial u}{\partial t}=\alpha\left(\frac{\partial^2 u}{\partial x^2}\right)
$$

2-D:

$$
\frac{\partial u}{\partial t}=\alpha\left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}\right)
$$

3-D:

$$
\frac{\partial u}{\partial t}=\alpha\left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}+\frac{\partial^2 u}{\partial z^2}\right)
$$

<a id="navier-stokes"></a>
#### [Navier-Stokes Equations](#pde)
The Navier-Stokes equations describe the motion of fluid substances such as liquids and gases. Solving these equations primarily aims to determine the velocity field and pressure field of the fluid at different positions and times. The Navier-Stokes equations represent the **conservation of momentum**. These equations are always solved together with the **continuity equation**, which represents the conservation of mass.

The general form of the **incompressible Navier-Stokes** equations is: 

$$
\begin{gathered}
\frac{\partial \mathbf{u}}{\partial t}+(\mathbf{u} \cdot \nabla) \mathbf{u} = -\frac{1}{\rho} \nabla p+\nu \nabla^2 \mathbf{u}+\mathbf{f}\\
\nabla \cdot \mathbf{u} = 0 \quad (\text{continuity equation})
\end{gathered}
$$

where $\mathbf{u}$ is the velocity field, $t$ is time, $\rho$ is the fluid density, $p$ is the pressure, $\nu$ is the kinematic viscosity, $\mathbf{f}$ represents external forces (e.g., gravity).

1-D:

$$
\begin{gathered}
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}=-\frac{1}{\rho} \frac{\partial p}{\partial x}+\nu \left(\frac{\partial^2 u}{\partial x^2}\right)+f_x \\
\frac{\partial u}{\partial x}=0\\
\end{gathered}
$$


2-D:

$$
\begin{gathered}
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}+v \frac{\partial u}{\partial y}=-\frac{1}{\rho} \frac{\partial p}{\partial x}+\nu \left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}\right)+f_x \\
\frac{\partial v}{\partial t}+u \frac{\partial v}{\partial x}+v \frac{\partial v}{\partial y}=-\frac{1}{\rho} \frac{\partial p}{\partial y}+\nu \left(\frac{\partial^2 v}{\partial x^2}+\frac{\partial^2 v}{\partial y^2}\right) +f_y\\
\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}=0\\
\end{gathered}
$$



3-D:

$$
\begin{gathered}
\frac{\partial u}{\partial t}+u \frac{\partial u}{\partial x}+v \frac{\partial u}{\partial y}+w \frac{\partial u}{\partial z}=-\frac{1}{\rho} \frac{\partial p}{\partial x}+\nu \left(\frac{\partial^2 u}{\partial x^2}+\frac{\partial^2 u}{\partial y^2}+\frac{\partial^2 u}{\partial z^2}\right) +f_x\\
\frac{\partial v}{\partial t}+u \frac{\partial v}{\partial x}+v \frac{\partial v}{\partial y}+w \frac{\partial v}{\partial z}=-\frac{1}{\rho} \frac{\partial p}{\partial y}+\nu \left(\frac{\partial^2 v}{\partial x^2}+\frac{\partial^2 v}{\partial y^2}+\frac{\partial^2 v}{\partial z^2}\right)+f_y \\
\frac{\partial w}{\partial t}+u \frac{\partial w}{\partial x}+v \frac{\partial w}{\partial y}+w \frac{\partial w}{\partial z}=-\frac{1}{\rho} \frac{\partial p}{\partial z}+\nu \left(\frac{\partial^2 w}{\partial x^2}+\frac{\partial^2 w}{\partial y^2}+\frac{\partial^2 w}{\partial z^2}\right)+f_z\\
\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}+\frac{\partial w}{\partial z}=0\\
\end{gathered}
$$

where $u$, $v$, and $w$ are the velocities in the $x$, $y$, and $z$ directions, respectively. $f_x$, $f_y$, and $f_z$ are the external forces in the $x$, $y$, and $z$ directions.

---



For compressible fluids, the density $\rho$ can vary with time and space. The Compressible Navier-Stokes include an additional energy equation to account for changes in internal energy and temperature. The general form of the **compressible Navier-Stokes** equations is:

$$
\begin{gathered}
\frac{\partial(\rho \mathbf{u})}{\partial t}+\nabla \cdot(\rho \mathbf{u} \otimes \mathbf{u})=-\nabla p+\nabla \cdot \tau+\rho f \\
\frac{\partial \rho}{\partial t}+\nabla \cdot(\rho \mathbf{u})=0  \quad (\text{Continuity Equation, mass conservation})\\
\frac{\partial(\rho E)}{\partial t}+\nabla \cdot(\rho E \mathbf{u})=-\nabla \cdot(p \mathbf{u})+\nabla \cdot(\tau \cdot \mathbf{u})+\nabla \cdot(\kappa \nabla T)+\rho f \cdot \mathbf{u} \quad (\text{Energy Equation, energy conservation})
\end{gathered}
$$

where $\mathbf{u}$ is the velocity field, $p$ is the pressure, $\nu$ is the kinematic viscosity, $\mathbf{f}$ represents external forces, $\mathbf{\tau}$ is the viscous stress tensor. $E$ is the total energy per unit mass, $\kappa$ is the thermal conductivity, $T$ is the temperature.



* The viscous stress tensor $\mathbf{\tau}$ for a compressible Newtonian fluid is given by:

$$
\tau=\mu\left(\nabla \mathbf{u}+(\nabla \mathbf{u})^T\right)+\lambda(\nabla \cdot \mathbf{u}) \mathbf{I}
$$

where $mu$ is the dynamic viscosity, $\lambda$ is the second viscosity coefficient, and $\mathbf{I}$ is the identity matrix.

* The viscous stress tensor $\mathbf{\tau}$ for ideal compressible fluid is zero because ideal fluids are assumed to have no viscosity.

$$
\tau = 0
$$

1-D:


2-D:



3-D:

$$
\mathbf{\tau}=\left(\begin{array}{ccc}
\tau_{x x} & \tau_{x y} & \tau_{x z} \\
\tau_{y x} & \tau_{y y} & \tau_{y z} \\
\tau_{z x} & \tau_{z y} & \tau_{z z}
\end{array}\right)
$$

$$
\begin{gathered}
 \frac{\partial(\rho u)}{\partial t}+\frac{\partial\left(\rho u^2\right)}{\partial x}+\frac{\partial(\rho u v)}{\partial y}+\frac{\partial(\rho u w)}{\partial z}=-\frac{\partial p}{\partial x}+\frac{\partial \tau_{x x}}{\partial x}+\frac{\partial \tau_{x y}}{\partial y}+\frac{\partial \tau_{x z}}{\partial z}+\rho f_x \\
 \frac{\partial(\rho v)}{\partial t}+\frac{\partial(\rho u v)}{\partial x}+\frac{\partial\left(\rho v^2\right)}{\partial y}+\frac{\partial(\rho v w)}{\partial z}=-\frac{\partial p}{\partial y}+\frac{\partial \tau_{y x}}{\partial x}+\frac{\partial \tau_{y y}}{\partial y}+\frac{\partial \tau_{y z}}{\partial z}+\rho f_y \\
 \frac{\partial(\rho w)}{\partial t}+\frac{\partial(\rho u w)}{\partial x}+\frac{\partial(\rho v w)}{\partial y}+\frac{\partial\left(\rho w^2\right)}{\partial z}=-\frac{\partial p}{\partial z}+\frac{\partial \tau_{z x}}{\partial x}+\frac{\partial \tau_{z y}}{\partial y}+\frac{\partial \tau_{z z}}{\partial z}+\rho f_z \\
\frac{\partial \rho}{\partial t}+\frac{\partial(\rho u)}{E x}+\frac{\partial(\rho v)}{\partial y}+\frac{\partial(\rho w)}{\partial z}=0 \text(Continuity Equation)\\
 \frac{\partial(\rho E)}{\partial t}+\frac{\partial(\rho u E)}{\partial x}+\frac{\partial(\rho v E)}{\partial y}+\frac{\partial(\rho w E)}{\partial z}=-\frac{\partial(p u)}{\partial x}-\frac{\partial(p v)}{\partial y}-\frac{\partial(p w)}{\partial z}+\frac{\partial\left(u \tau_{x x}+v \tau_{y x}+w \tau_{z x}\right)}{\partial x}+\frac{\partial\left(u \tau_{x y}+v \tau_{y y}+w \tau_{z y}\right)}{\partial y}+\frac{\partial\left(u \tau_{x z}+v \tau_{y z}+w \tau_{z z}\right)}{\partial z}+\frac{\partial}{\partial x}\left(\kappa \frac{\partial T}{\partial x}\right)+\frac{\partial}{\partial y}\left(\kappa \frac{\partial T}{\partial y}\right)+\frac{\partial}{\partial z}\left(\kappa \frac{\partial T}{\partial z}\right)+ \rho(uf_x+vf_y+wf_z) \text(Energy Equation)
\end{gathered}
$$



