# Logistics

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

# Chapter 5

## Long Cylinder

An infinitely long cylinder with an inner radius $a$ and outer radius $b$ has a permeability of $\mu=2\mu_o$. The centerline of the cylinder is along the $z$--axis.

An infinitely long wire along the $z$--axis carries a current $I$ in the $+z$ direction. 

1. Compute and plot $B_\phi(s)$.
2. Compute all bound surface currents, $\mathbf{K}_b$.
3. Compute the bound volume current density, $\mathbf{J}_b$.

Write all of your answers and label your plot at appropriate points in terms of $\mu_o, I, a,$ and $b$.

**Answer**

$$\mathbf{H}=\frac{I}{2\pi s}\hat{\boldsymbol{\phi}}$$

Inside and outside, the field is as it would be if the cylinder was not there. Inside, the field is larger by a factor of $2$. $\chi_m=\mu/\mu_o-1=2$ for this problem and $\chi_m \gt 0$ correspsonds to a paramagnetic material, and so the increase in $B$ inside is expected. 

$$
\mathbf{B}=
\begin{cases}
\displaystyle\frac{\mu_oI}{2\pi s}\hat{\boldsymbol{\phi}} & s<a
\\\\
\displaystyle 2\frac{\mu_oI}{2\pi s}\hat{\boldsymbol{\phi}} & a<s< b
\\\\
\displaystyle\frac{\mu_oI}{2\pi s}\hat{\boldsymbol{\phi}} & s > b
\end{cases}
$$

$$\mathbf{M}=\chi_m\mathbf{H}=(\mu/\mu_o-1)\mathbf{H}=(\mu/\mu_o-1)\frac{I}{2\pi s}\hat{\boldsymbol{\phi}}$$

$\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}$

On the inner surface of the cylinder, $\hat{\mathbf{n}}=-\hat{\mathbf{s}}$ and $\mathbf{M}=(\mu/\mu_o-1)\frac{I}{2\pi a}\hat{\boldsymbol{\phi}}$ so $\mathbf{K}_b = (2\mu_0/\mu_o-1)\frac{I}{2\pi a}\hat{\mathbf{z}}$.

On the outer surface of the cylinder, $\hat{\mathbf{n}}=\hat{\mathbf{s}}$ and $\mathbf{M}=(\mu/\mu_o-1)\frac{I}{2\pi 2a}\hat{\boldsymbol{\phi}}$ so $\mathbf{K}_b = -(2\mu_0/\mu_o-1)\frac{I}{2\pi b}\hat{\mathbf{z}}$.

Note that $\hat{\boldsymbol{\phi}}\times\hat{\mathbf{s}}=-\hat{\mathbf{z}}$.

Also note that the net-bound current in the vertical direction is zero.

$\mathbf{J}_b=\nabla\times \mathbf{M}=0$

because

$\mathbf{M}=(const)\hat{\boldsymbol{\phi}}/s$

and the two terms in involving $M_\phi$ in

$$\boldsymbol{\nabla} \times \mathbf{M} = \left({\frac {1}{s}}{\frac {\partial M_{z}}{\partial \phi }}-{\frac {\partial M_{\phi }}{\partial z}}\right){\hat {\boldsymbol {s}}}+\left({\frac {\partial M_{s}}{\partial z}}-{\frac {\partial M_{z}}{\partial s}}\right){\hat {\boldsymbol {\phi }}}+{\frac {1}{s}}\left({\frac {\partial \left(s M_{\phi }\right)}{\partial s}}-{\frac {\partial M_{s}}{\partial \phi }}\right){\hat {\mathbf {z} }}$$

evaluate to zero.

To check your answer, use Ampere's Law, $\oint \mathbf{B}\cdot d\mathbf{l}=\mu_o I_{\text{encl}}$, accounting for these bound currents as a part of $I_{\text{encl}}$ and verify that you get the same magnetic field computed earlier.

## Cylinder Boundary Value Problem 

A long cylinder of radius $s_o$ has a magnetization

$$
\mathbf{M}=(ps\sin 2\phi + qs\cos\phi)\hat{\mathbf s}
+
(ps\cos 2\phi-2qs\sin\phi)\hat{\boldsymbol{\phi}}
$$ 

where $s$ is the cylindrical radial coordinate and $p$ and $q$ are constants. Find $\mathbf{B}$ due to the cylinder.

## Cylinder with uniform $\mathbf{M}$ 

A cylinder centered on the origin with radius $b$ and end caps in the $z=\pm L$ plane has a permanent magnetization $\mathbf{M}=M_o\hat{\mathbf{z}}$.

1. Find the approximate magnetic potential, $\psi_m(z)$, by assuming $z\pm L\gg b$ and approximating an integrand of an appropriate integral in Section 5.9C of Jackson as a power series in the cylindrical radial coordinate $s'$ prior to integrating;
1. Determine the exact $\psi_m(z)$; and
1. Determine the $\mathbf{H}$ and $\mathbf{B}$ at all points on $z$-axis of the using the exact $\psi_m(z)$.

## Cylinder with $\mathbf{K}=K_o(\phi)\zhat$

$\mathbf{A}(s,\phi,s',\phi')$ for long straight wire that carries a current $I$ and passes through $\phi', s'$. Then find $\mathbf{A}(s,\phi)$ for a long cylinder aligned with the $z$ axis and centered on the origin that carries a surface current $\mathbf{K}(\phi)$.

## Magnetic Moment

Equation 5.50 of of Jackson 3rd Edition is

$$
\mathbf{m}=\frac{1}{2}\int \mathbf{\mathbf{x}'}\times \mathbf{J(\mathbf{x}')} d^3x'
$$

Equation 5.90 of of Griffiths 4th Edition is
 
$$
\mathbf{m}=\frac{1}{2}\int \mathbf{\mathbf{r}}\times \mathbf{J} d\tau
$$

Equation 5.86 of Griffiths 3rd Edition is

$$
\mathbf{m}=I\int d\mathbf{a}
$$

1. Are all of these equations equivalent? Discuss.
2. In Griffiths, primed coordinates are used, but in Jackson they are. Discuss.
3. Compute $\mathbf{m}$ using any of the above equations for a origin--centered uniformly charged sphere of radius $R$ rotating around the $z$ axis with angular velocity $\omega$.