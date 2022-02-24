
# Limit Check

The potential inside of the long (in $z$ direction) duct with cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

can be written as

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

In Example 3.3 of Griffiths, he finds the potential for a long duct with one open face. The diagram for that example is similar to the above except there is no conductor on the right side and $b=\infty$. The solution he finds is

$II.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\frac{e^{-n\pi x/a}}{n}\sin(n\pi y/a)$

1\. Show that the infinite $b$ solution ($II.$) matches the finite $b$ solution ($I.$) in the limit that $a/b \ll 1$. (You do not need to derive $I.$ or $II.$, but should be able to.)

2\. In the limit that $b/a \ll 1$, it would seem that near the center of the duct ($y=a/2$), the system appears as two infinite parallel conducting plates held at different potentials, which is a 1-D problem solved before. Show that in the limit $b/a \ll 1$, equation $I.$ reduces to the solution for an infinite conducting plate in the $x=0$ plane held at $V_o$ and a grounded infinite conducting plate in the $x=b$ plane. (You'll need to use $e^u\simeq 1 + u$ for $u\ll1$ multiple times and also the [Gregory and Leibniz formula for $\pi$](https://mathworld.wolfram.com/PiFormulas.html)).

# Long Rectangular Tube with Sheet of Charge 

An infinitely long, hollow, and conducting duct is parallel to the $z$-axis and has sides bounded by $0\le x \le 1$ and $0\le y\le 1$. All sides are grounded. An infinitely long non-conducting sheet of charge with surface charge density $\sigma'$ is in the $x=x'$ plane between $y=0$ and $y=1$. See the left part of the figure below.

<img src="figures/square_duct.svg"/>

1\. Find equations $\psi_l(x,y)$, the potential for $x\lt x'$, and $\psi_r(x,y)$, the potential for $x\gt x'$. Based on the discussion in class, we can easily write down equations for $\psi_l$ and $\psi_r$ that are zero on the conducting walls:

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

where $n$ is an integer, matches the boundary conditions on the walls of the conductor. You need to find $A_n$ and $B_n$ such that the two conditions

$$\psi_l(x',y)=\psi_r(x',y)$$

and

$$\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$$

are satisfied.

2\. Write a single equation for the potential $\psi(x,y)$ using $\psi_l$, $\psi_r$, and the Heavyside step function $\Theta$.

The Green function is $G=(4\pi\epsilon_o/A\sigma')\psi$, where $A=\int_0^1dy\int_{0}^L dz$ and $L$ is the length of the duct. (You may want to verify this.)

3\. Use $\psi(x,y)$ and Green's second identity (Equation 1.35 of Jackson), or equivalently, the Green function stated above and equation 1.42 of Jackson to find the potential when the duct is filled with a nonconducting material with a uniform charge density $\rho_o$ as shown in the right part of the figure above.

----

Note: In problem 2.15 of Jackson, he gives the Green function for the case where a line of charge parallel to the $z$-axis passes through $(x,y)=(x',y')$. That problem is a bit more complicated than the problem considered here. In problem 2.16, of Jackson, he states the result of using the Green function from problem 2.15 to find the potential for the configuration in part 3. above.

# 2-D Cylindrical Boundary Value Problem

A non-conducting and infinitely long cylindrical shell of radius $b$ has a surface charge density of $\sigma=\sigma_2\sin\thinspace2\phi$. 

1\. Find $\psi(s,\phi)$ using the boundary value method. Note that the general solution to Laplace's equation in cylindrical coordinates for a problem with no $z$ dependence is

$$\psi=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi) s^n+a_o\ln\rho+\sum_{n=1}^\infty (a_n\cos n\phi+b_n \sin n\phi)s^{-n}$$

%In class, I did the a problem for $\sigma=\sigma_o\cos\thinspace\phi$. In justifying dropping the $\rho^n$ and $\ln\rho$ terms, I mentioned that this was justified because the potential should go to zero as $\rho\rightarrow \infty$. What I neglected to mention is that this is because for large $\rho$, the system appears as a line of charge with linear charge density, $\lambda$, and $\lambda=0$ for the given $\sigma$. This can be seen by computing the linear charge density $\lambda = \int_0^{2\pi} \sigma b d\phi$.

2\. Repeat 1. assuming $\sigma=\sigma_o + \sigma_2\sin\thinspace2\phi$. In this case, the $\ln s$ term cannot be dropped; $a_o$ is determined from the requirement that for large $s$, the potential should be that for a line of charge with linear density $\lambda$ that is the average of $\sigma$ over $\phi$.

