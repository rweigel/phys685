
# Limit Check

The potential inside of the long duct whos cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

can be written as

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

In Example 3.3 of Griffiths, he finds the potential for a long duct with one open face. The diagram is similar to the above except there is no conductor on the right side and $b=\infty$. The solution he finds is

$II.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\frac{e^{-n\pi x/a}}{n}\sin(n\pi y/a)$

1. Show that the finite $b$ solution ($I.$) matches the infinite $b$ solution ($II.$) in the limit that $a/b \ll 1$.

2. In the limit that $b/a \ll 1$, it would seem that near the center of the duct ($y=a/2$), the system appears as two infinite parallel conducting plates held at different potentials, which is a 1-D problem solved before. Show that in this limit equation $I.$ reduces to the solution for an infinite conducting plate in the $y=0$ plane held at $V_o$ and an infinite conducting plate in the $y=b$ plane held at $V=0$. (You'll need to use $e^u\simeq 1 + u$ for $u\ll1$ multiple times and also the [Gregory and Leibniz formula for $\pi$](https://mathworld.wolfram.com/PiFormulas.html)).

# Long Rectangular Tube with Sheet of Charge 

An infinitely long, hollow, and conducting rectangular tube is parallel to the $z$-axis and has sides bounded by $0\le x \le 1$ and $0\le y\le 1$. All sides are grounded.

A infinitely long non-conducting sheet of charge with surface charge density $\sigma'$ is in the $x=x'$ plane between $y=0$ and $y=1$. See the left part of the figure below.

1\. 

Find equations $\psi_l(x,y)$, the potential for $x\lt x'$, and $\psi_r(x,y)$, the potential for $x\gt x'$. 

In class, I showed that 

$$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$$

$$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$$

where $n$ is an integer, matches the boundary conditions on the walls of the conductor. You need to find $A_n$ and $B_n$ such that the two conditions


$$\psi_l(x',y)=\psi_r(x',y)$$

and

$$\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$$

are satisfied.

2\.

Write a single equation for the potential $\psi(x,y)$ using $\psi_l$, $\psi_r$, and the Heavyside step function $\Theta$.

The Green function is $G=(4\pi\epsilon_o/A\sigma')\psi$, where $A=\int_0^1dy\int_{0}^L dz$ and $L$ is the length of the tube. (You may want to verify this.)

3.

Use $\psi(x,y)$ and Green's second identity (Equation 1.35 of Jackson), or equivalently, the Green function stated above and equation 1.42 of Jackson to find the potential when the tube is filled with a nonconducting material with a uniform charge density $\rho_o$ as shown in the right part of the figure above.

----

Note: In problem 2.15 of Jackson, he gives the Green function for the case where a line of charge parallel to the $z$-axis passes through $(x,y)=(x',y')$. That problem is a bit more complicated than the problem considered here. In problem 2.16, of Jackson, he states the result of using the Green function from problem 2.15 to find the potential for the configuration in part 3. above.