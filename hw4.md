# HW 4

## Green function for infinite dome

In class, I showed how to find the potential $\psi$ due to a point charge inside of a grounded, conducting, and closed dome when the radius of the dome is infinite. The potential was found using the method of images. (A dome is a hemisphere plus a cap.) 

Use this $\psi$ and equation 1.35 of Jackson (or equation 1.42; $\psi$ is proportional to a Green function) to find the potential $\Phi$ for the following problem:

An conducting dome has its base in the $x-y$ plane and the radius of the dome is infinite. There are no charges inside of the dome. The boundary of the dome is grounded except for the region between $x^2 + y^2 < b$, which is held at a potential of $V_o$.

1. Find the potential $\Phi(z)$ inside of the dome (the integral required to find $\Phi(x,y,z)$ requires an approximation of the integrand or numerical integration and will be considered in the future).
2. Find the potential $\Phi(z)$ inside of the dome when $b/z \ll 1$. Do this by Taylor series expanding $\Phi(z)$ for small $b/z$. Does the answer make sense?
3. Sketch the electric field lines inside of the dome.

Note that a related problem (but with a different Green function) considered in 2.6 of Jackson.

**Solution**

1\. The potential that satisfies the boundary conditions in the limit that that that the radius of the dome is much larger than $r'$ is

$\displaystyle\psi = \frac{kq}{\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}}-\frac{kq}{\sqrt{(x-x')^2+(y-y')^2+(z+z')^2}}$

This equation was derived using the method of images in class and is the same equation that solves the problem for a point charge at $\mathbf{x}'$ above an infinite grounded plane that lies in the $x$-$y$ plane. $\phi$ satisfies the boundary conditions that when $z=0$, $\psi(x,y,0)=0$ and when $r'\gg r$, $\psi=0$ (showing the latter requires re--writing the denominators in terms of $r'$ and $r$).

Given that we are only interested in the potential along the $z$--axis, we can set $x'=y'=0$. (In 2.6 of Jackson, he does this after the integral required to find $\Phi(x,y,z)$ is found.) We then have

$\displaystyle\psi = \frac{kq}{\sqrt{x^2+y^2+(z-z')^2}}-\frac{kq}{\sqrt{x^2+y^2+(z+z')^2}}$

Green's second identity (Equation 1.35) with $\Phi$ in place of $\phi$ is

$\displaystyle\int_\mathcal{V} \left(\Phi\nabla^2\psi -\psi\nabla^2\Phi\right)d^3x=\oint_\mathcal{S}\left(\Phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \Phi}{\partial n}\right) da$

In this problem $\mathcal{V}$ is the volume of the dome and $\mathcal{S}$ has two surfaces -- a large disk in the $x$--$y$ plane and the curved part of the dome.

The Laplacian of $\psi$ can be written down by inspection. The charge density is that for point charges at $(x,y,z)=(0,y,\pm z')$, so

$\nabla^2\psi=-kq\delta(x)\delta(y)\delta(z-z')+kq\delta(x)\delta(y)\delta(z+z')$

$\displaystyle\int_\mathcal{V} \Phi\nabla^2\psi d^3x=\int_\mathcal{V} \Phi\left[-kq\delta(x)\delta(y)\delta(z-z')+kq\delta(x)\delta(y)\delta(z+z')\right]d^3x$

$\delta(z+z')$ is zero in $\mathcal{V}$, for which $z$ is always positive and $z'$ was given to be above the $x$-$y$ plane, so it is positive. The integral simplifies to  

$\displaystyle\int_\mathcal{V} \Phi\nabla^2\psi d^3x=-\frac{kq}{\epsilon_o}\int_\mathcal{V} \Phi \delta(x)\delta(y)\delta(z-z')d^3x=-\frac{kq}{\epsilon_o}\Phi(0,0,z)=\frac{kq}{\epsilon_o}\Phi(z)$.

Inside $\mathcal{V}$, we were given that there are no charges, so $\nabla^2\Phi=0$. Therefore, the left-hand side of Equation 1.35 reduces to $-(kq/\epsilon_o)\Phi(z)$.

On $\mathcal{S}$, $\psi=0$, so the second surface integral is zero. We are left with

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=\oint_\mathcal{S}\Phi\frac{\partial \psi}{\partial n} da$

The surface is composed of the two parts -- the curved part and its base. On the curved part, $\Phi=0$ was given. On the base, $\Phi=0$ for $x^2+y^2\lt b^2$ and $\Phi=V_o$ otherwise. As a result, the surface integral reduces to

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=\int_\mathcal{x^2+y^2\lt b^2}V_o\frac{\partial \psi}{\partial n} da$. In cylindrical coordinates, we have

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=V_o\int_{0}^{2\pi}\int_0^b\frac{\partial \psi}{\partial n} sdsd\phi$

The outward normal to $\mathcal{V}$ is -$z$, so

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=-V_o\int_{0}^{2\pi}\int_0^b\frac{\partial \psi}{\partial z} sdsd\phi$

What remains is to evaluate the partial derivative (and recall that ${\partial \psi}/{\partial z}$ in the integral means ${\partial \psi}/{\partial z}|_{\text{on }\mathcal{S}}$). In this problem, $\text{on }\mathcal{S}$ corresponds to $z=0$.)

$\displaystyle\frac{\partial \psi}{\partial z}\Bigg|_{z=0}=2kq\frac{z'}{\sqrt{s^2+z'^2}^3}$

Evaluation of the integral gives

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=-4\pi kqV_o\left[\frac{z'}{|z'|}-\frac{z'}{\sqrt{b^2+z'^2}}\right]$

Cancellation and using $z'/|z'|=1$ for $z'\gt 0$ gives

$\displaystyle \Phi(z')=V_o\left[1-\frac{z'}{\sqrt{b^2+z'^2}}\right]$

Using the same arguments used in [HW 3.1](#1-d-cartesian-green-function), we can replace $z'$ with $z$, leaving

$\displaystyle \Phi(z)=V_o\left[1-\frac{z}{\sqrt{b^2+z^2}}\right]$

2\. The solution can be written as

$\displaystyle \Phi(z)=V_o\left[1-\frac{1}{\sqrt{1+\frac{b^2}{z^2}}}\right]$

Using [the binomial expansion](https://rweigel.github.io/phys305/binomial_expansion.html), 

$\displaystyle \Phi(z)=V_o\left[1-\left(1-\frac{1}{2}\left(\frac{b}{z}\right)^2 + ... \right)\right]$

To lowest order in $b/z$, 

$\displaystyle \Phi(z) \simeq \frac{V_o}{2}\left(\frac{b}{z}\right)^2 \qquad z\gg b$

For large $z$, the (positive) charge on the disk appears as a point charge at the origin. As a result, we may expect that the potential will fall off as $1/z$. Here the potential falls off more slowly. The reason is that there is also a contribution from the negative charges in the plane. As a result, for large $z$, the system appears to have zero charge at the origin and so there is no $1/z$ term. (The interpretation of the power series expansion of potential will be covered in more detail later.)

3\. This was discussed in class. In general, it is easiest to draw equipotential lines starting with one near the boundary. Then, draw electric field lines that are perpendicular to the equipotential lines.

## 2--D Cartesian Boundary Value Problem

Review Griffiths 3.3.1 (3rd and 4th edition). You should be able to quickly derive the potential for Figure 3.20 (3rd and 4th edition) when any one of the sides is at $V_o$ and the other three are grounded. See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.html).

Suppose the sides of Figure 3.20 of Griffiths 3rd or 4th edition are held at $V_l$, $V_r$, $V_t$, and $V_b$, where $l=$left, $r=$right, $t=$top, and $b=$bottom. Find the potential inside the rectangular pipe.

Hints:

1. The total potential will be the the sum of the potentials from four different problems (1)
 $V_l$ non--zero and all other sides zero, (2) $V_r$ non--zero and all other sides zero, etc. I will ask you to explain why in class.
2. You can build the solution to three of the four problems described in the first hint using a transformation of coordinate system and the solution to one of the problems.

**Solution**

The potential inside of the long (in $z$ direction) duct with cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

is

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

The geometry for the $V_l$ case is

<img src="figures/square_duct2.svg"/>

The choice of coordinate system for $I.$ was arbitrary and we can translate the duct used for $I.$ to the left and down so that the position of the duct is the same as that in Figure 3.20 of Griffiths.

This is effected by replacing $x$ with $x+b/2$ and $y$ with $y+a/2$ in the equation for $V(x,y)$:

$\qquad\displaystyle \psi_l(x,y)=\frac{4V_l}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b/2-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi (y/a-1/2))$

Check: When $y=\pm a/2$, $\psi_l=0$ and when $x=b/2$, $\psi_l=0$.

To find $\psi_r$, replace $x$ with $-x$ and $V_l$ with $V_r$ in the equation for $\psi_l$:

$\qquad\displaystyle \psi_r(x,y)=\frac{4V_r}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b/2+x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi (y/a-1/2))$

Check: When $y=\pm a/2$, $\psi_r=0$ and when $x=-b/2$, $\psi_l=0$.

To find $\psi_t$, swap $a$ and $b$, $x$ and $y$, and $V_r$ with $V_t$  in the equation for $\psi_r$:

$\qquad\displaystyle \psi_r(x,y)=\frac{4V_t}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (a/2+y)/b]}{n\sinh(n\pi a/b)}\right)\sin(n\pi (x/b-1/2))$

Check: When $x=\pm b/2$, $\psi_t=0$ and when $y=-a/2$, $\psi_t=0$.

To find $\psi_t$, replace $y$ with $-y$, and $V_t$ with $V_b$ in the equation for $\psi_t$:

$\qquad\displaystyle \psi_b(x,y)=\frac{4V_b}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (a/2-y)/b]}{n\sinh(n\pi a/b)}\right)\sin(n\pi (x/b-1/2))$

Check: When $x=\pm b/2$, $\psi_t=0$ and when $y=a/2$, $\psi_t=0$.

The total potential can be written as

$\psi = \psi_l+\psi_r+\psi_t+\psi_b$

This potential satisifes Laplaces's equation and the boundary conditions for the case where all four sides are at a different potential.

## 2--D Spherical Boundary Value Problem

In 2.7 of Jackson 3rd edition, he solves for the potential outside of a sphere with hemispheres held at $\pm V$ using a Green function. In example 3.7 of Griffiths 4th edition (example 3.6 in 3rd edition), he describes how to solve for the potential outside of a sphere with a potential of $V(\theta)$ on its surface. As a result, Jackson's example is related to Griffiths' example.

Study these two examples and be prepared to answer questions (such as how they are related) about them in class.
