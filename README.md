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

#### Advection Equation
The advection equation, also known as the transport equation, describes the change of a physical quantity as it is transported by a fluid flow. Its general form is:

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

#### Burger Equation

$$
\frac{\partial u}{\partial t}+(u \cdot \nabla) u=v \nabla^2 u
$$


