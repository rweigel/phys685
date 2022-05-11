**Study Guide**

* Wednesday, May 11th from 4:30 – 7:10 pm in the regular classroom. 
* Approximately four problems
* The exam will cover concepts covered in the HW problems. 1-2 problems will cover topics covered on the mid--term and 1-2 problems will cover topics covered after the midterm. The problems won't require as much algebra, however. Make sure that you (1) understand the key steps and (2) can work out what the solution should look like. As discussed in class, (2) is important in general and also to help you determine if you've made an algebraic error.
* Don't fall into the trap of reading solutions and concluding that because the solution makes sense, you can solve the problem. Understanding someone else's solution is much easier than producing a solution on your own. After reading a solution, close your notes and attempt the problem on your own.
* If needed, I will give you
    * Legendre Polynomials
    * Green's 2nd identity (unless I ask you to derive)
    * the binomial expansion,
    * the non--cartesian Laplace's equation in 2-- and 3--D.
    * Equations for bound charge densities and bound currents.

    All other equations, including the general solution to Laplace's equation in 2--D in cartesian, cylindrical, and spherical, you'll need to know.

----

**PHYS 685 Final Exam**

---> **Solve 3 of 4 problems** <---

Wednesday, May 11th, 2022

2 hours and 40 minutes

**Equations**

$$
\mathbf{\nabla} f = 
{\partial f \over \partial r}\hat{\mathbf r}
+
{1 \over r}{\partial f \over \partial \theta}\hat{\boldsymbol \theta}
+
{1 \over r\sin\theta}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}
$$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} = 
{1 \over r^2}{\partial \left( r^2 U_r \right) \over \partial r}
+
{1 \over r\sin\theta}{\partial \over \partial \theta} \left(  U_\theta\sin\theta \right)
+
{1 \over r\sin\theta}{\partial U_\phi \over \partial \phi}
$$

$\displaystyle
\boldsymbol{\nabla}\times \mathbf{U} =
{\frac {1}{r\sin \theta }}\left({\frac {\partial }{\partial \theta }}\left(U_{\phi }\sin \theta \right)
-
{\frac {\partial U_{\theta }}{\partial \phi }}\right) {\hat {\mathbf {r} }}
+
{\frac {1}{r}}\left({\frac {1}{\sin \theta }}{\frac {\partial U_{r}}{\partial \phi }}
-
{\frac {\partial }{\partial r}}\left(rU_{\phi }\right)\right) {\hat {\boldsymbol {\theta }}}
+
{\frac {1}{r}}\left({\frac {\partial }{\partial r}}\left(rU_{\theta }\right)
-
{\frac {\partial U_{r}}{\partial \theta }}\right) {\hat {\boldsymbol {\phi }}}$


$\displaystyle
\nabla^2f={ {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial f \over \partial r}\right)+{1 \over r^{2}\sin \theta }{\partial  \over \partial \theta }\left(\sin \theta {\partial f \over \partial \theta }\right)+{1 \over r^{2}\sin ^{2}\theta }{\partial ^{2}f \over \partial \phi ^{2}}}$$

$\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$, $\sigma_b=\mathbf{P}\bfcdot \hat{\mathbf{n}}$,
$\rho_b=-\boldsymbol{\nabla}\bfcdot \mathbf{P}$

For linear material, $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$, $\epsilon\equiv\epsilon_o(1+\chi_e)$

$\mathbf{H}=\mathbf{B}/\mu_o-\mathbf{M}$, $\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}$, $\mathbf{J}_b=\boldsymbol{\nabla}\times \mathbf{M}$, 

For linear material, $\mathbf{M}=\chi_m\mathbf{H}$, $\mu\equiv\mu_o(1+\chi_m)$

Power series expansions for $\delta \lt 1$.

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + \frac{n(n+1)}{2!}\delta^2- \frac{n(n+1)(n+2)}{3!}\delta^3+...$$

$$\ln(1+\delta)=\delta + \frac{\delta^2}{2} + \frac{\delta^3}{3} + ...$$

$$e^\delta = 1 + \frac{\delta}{1!} + \frac{\delta^2}{2!} + ...$$

Green's theorem (second identity)

$$\int_{\mathcal{V}} \left(\phi\nabla^2\psi -\psi\nabla^2\phi\right)d^3x=\oint_{\mathcal{S}}\left(\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}\right) da$$

# Parallel Plate Capacitor

Consider a large parallel plate capacitor with a hemispherical bulge on the grounded plate.  The bulge has radius $b$ and bulges toward the second plate.  The distance between the plates is $d$, $d\gg b$.  The second plate is at potential $V_o$. A cross--section of the geometry is shown. Assume that the capacitor plates are infinite in extent.

<img width="53%" src="figures/capacitor_with_bulge.svg"/>

1. Find the potential everywhere inside the capacitor when $b=0$ (no bulge; ordinary parallel plate capacitor). Indicate the coordinate axes used on a diagram.
2. Find the potential everywhere inside the capacitor when $b \ne 0$.

# Dipole in a Dielectric Sphere

A perfect dipole $\mathbf{p}=p_o\hat{\mathbf{z}}$ at the origin is at the center of a dielectric sphere of radius $b$ that is centered on the origin. The dielectric constant of the sphere is $\epsilon$.

Find the potential everywhere.

# Magnetizable Sphere in Uniform Field

An initially unmagnetized sphere of radius $b$ and permeability $\mu_i$ is placed is a region of free space (so a permeability of $\mu_o$) where there is an external magnetic field $B_{\text{ext}}\zhat$.

Assume that the scalar magnetic potential, $\psi_m$, will have the form, for $r\le b$

$$\psi^i_m(r,\theta)=A_1r\cos\theta\thickspace ,$$

and for $r \ge b$,

$$\psi^o_m(r,\theta)=-\frac{B_{\text{ext}}}{\mu_o}r\cos\theta+\frac{B_2}{r^2}\cos\theta\thinspace$$

1\. Find the unknown constants $A_1$ and $B_2$.

2\. Find $\mathbf{B}$ inside the sphere.

3\. Find the magnetization of the sphere.

# Rotating Sphere

An origin--centered sphere with uniform surface charge density $\sigma$ and radius $b$ rotating around the $z$--axis with angular velocity $\omega$ results in a surface current of $\mathbf{K}=\omega b\sigma\sin\theta\hat{\boldsymbol{\phi}}$.

Use

$$\mathbf{A}(\mathbf{x})=\frac{\mu_o}{4\pi}\int \frac{\mathbf{K}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da'$$

and

$$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$$

and one or more of

$\displaystyle l=0\quad\quad \displaystyle Y_{00}(\theta,\phi)=\sqrt{1\over 4\pi}=\sqrt{1\over 4\pi}P_o(\cos\theta)$


$l=1
\quad 
\begin{cases}
\displaystyle Y_{11}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{i\phi}\\ \\
\displaystyle Y_{10}(\theta,\phi)=\sqrt{3\over 4\pi} \cos\theta=\sqrt{3\over 4\pi} P_1(\cos\theta)\\ \\
\displaystyle Y_{1,-1}(\theta,\phi)=-Y_{11}^{*}(\theta,\phi)
\end{cases}
$

and

$$\int_0^{2\pi}d\phi\int_0^\pi\sin\theta d\theta Y^\*\_{l'm'}(\theta',\phi')Y_{lm}(\theta,\phi)=\delta_{ll'}\delta_{mm'}$$

to show that for $r \lt b$,

$$\mathbf{A}=\frac{\mu_o b \omega \sigma}{3} r\sin\theta \hat{\boldsymbol{\phi}}$$