# PDE-Solver
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
    <td>&ensp;<a href="#burger">Burgers' Equation</a></td>
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
#### [Burgers' Equation](#pde)
Burgers' equation describes the evolution of **wave profiles** in various contexts. Wave profiles describe the shape and characteristics of waves as they propagate through a medium. These profiles can include information about the wave’s amplitude, wavelength, frequency, and phase. In the context of fluid dynamics and other physical phenomena, wave profiles help visualize how waves evolve over time and space.

Burgers’ equation is widely used in **fluid mechanics** to model turbulence and shock waves, in **nonlinear acoustics** to describe the propagation of high-intensity sound waves, in **traffic flow theory** to simulate vehicle density and speed variations, and in **gas dynamics** to study the behavior of gases under various conditions.

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


