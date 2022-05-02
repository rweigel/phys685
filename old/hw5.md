# HW 5

## Limit Check

The potential inside of the long (in $z$ direction) duct with cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

can be written as

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

In Example 3.3 of Griffiths, he finds the potential for a long duct with one open face. The diagram for that example is similar to the above except there is no conductor on the right side and $b=\infty$. The solution he finds is

$II.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\frac{e^{-n\pi x/a}}{n}\sin(n\pi y/a)$

1\. Show that the infinite $b$ solution ($II.$) matches the finite $b$ solution ($I.$) in the limit that $a/b \ll 1$. (You do not need to derive $I.$ or $II.$, but should be able to.)

2\. In the limit that $b/a \ll 1$, it would seem that near the center of the duct ($y=a/2$), the system appears as two infinite parallel conducting plates held at different potentials, which is a 1-D problem solved before. Show that in the limit $b/a \ll 1$, equation $I.$ reduces to the solution for an infinite conducting plate in the $x=0$ plane held at $V_o$ and a grounded infinite conducting plate in the $x=b$ plane. (You'll need to use $e^u\simeq 1 + u$ for $u\ll1$ multiple times and also the [Gregory and Leibniz formula for $\pi$](https://mathworld.wolfram.com/PiFormulas.html)).

**Solution**

**1\.** We need to show that 

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}$ reduces to $\displaystyle e^{-n\pi x/a}$ when $a/b\ll 1$, or, equivalently, $b/a \gg 1$

Re-writing the numerator and denominator in terms of exponentials

$\sinh[n\pi (b-x)/a]=\frac{1}{2}\left(e^{n\pi (b-x)/a}-e^{-n\pi (b-x)/a}\right)=\frac{1}{2}e^{n\pi b/a}\left(e^{-n\pi x/a}-e^{-2n\pi b/a}e^{n\pi x/a}\right)$

$\sinh(n\pi b/a)=\frac{1}{2}\left(e^{n\pi b/a}-e^{-n\pi b/a}\right)=\frac{1}{2}e^{n\pi b/a}\left(1-e^{-2n\pi b/a}\right)$

gives

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}=\frac{e^{-n\pi x/a}-e^{-2n\pi b/a}e^{n\pi x/a}}{1-e^{-2n\pi b/a}}$

In the numerator, the term $e^{-2n\pi b/a}e^{n\pi x/a} \rightarrow 0$ as $b/a \rightarrow \infty$ for $x=[0,b]$.

In the denominator, the term $e^{-2n\pi b/a}\rightarrow 0$ as $b/a \rightarrow \infty$.

As a reuslt, the ratio approaches $\displaystyle e^{-n\pi x/a}$ as expected.

**2\.** We need to show that near $y=a/2$, the sum in $II.$ approaches $\frac{\pi}{4}(1-x/b)$ so that $V(x,a/2)\rightarrow V_o(1-x/b)$.

In the middle of the duct, $y=a/2$ so we replace $\sin(n\pi y/a)$ with 
$\sin(n\pi/2)=(-1)^{n}$ for $n=1,3,...$. Using $\sinh x=(e^x-e^{-x})/2$ and $e^x\simeq 1-x$ for $x\ll 1$ gives

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}\simeq \frac{1+n\pi(b-x)/a - (1-n\pi(b-x)/a)}{1+n\pi b/a-(1-n\pi b/a)}=1-\frac{x}{b}$

We are left with

$\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)\simeq \frac{4V_o}{\pi}\left(1-\frac{x}{b}\right)\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}$

From [mathworld.wolfram.com](https://mathworld.wolfram.com/PiFormulas.html),

$\frac{\pi}{4}=\sum_{k=1}^\infty \frac{(-1)^{k+1}}{2k-1}$

Using $n=2k-1$, we can re-write this as 

$\frac{\pi}{4}=\sum_{n=1,3,...}^\infty \frac{(-1)^{(n+3)/2}}{n}$

Finally, for $n=1,3,...$, $(-1)^{(n+3)/2}=1,-1,1,...=(-1)^{n}$ and so

$\frac{\pi}{4}=\sum_{n=1,3,...}^\infty \frac{(-1)^{(n+3)/2}}{n}=\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}$

Thus,

$\displaystyle V(x)\simeq \frac{4V_o}{\pi}\left(1-\frac{x}{b}\right)\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}=\frac{4V_o}{\pi}\frac{\pi}{4}\left(1-\frac{x}{b}\right)=V_o\left(1-\frac{x}{b}\right)$

## Long Rectangular Duct with Sheet of Charge 

An infinitely long, hollow, and conducting duct is parallel to the $z$-axis and has sides bounded by $0\le x \le 1$ and $0\le y\le 1$. All sides are grounded. An infinitely long non-conducting sheet of charge with surface charge density $\sigma'$ is in the $x=x'$ plane between $y=0$ and $y=1$. See the left part of the figure below.

<img src="figures/square_duct.svg"/>

1\. Find equations $\psi_l(x,y)$, the potential for $x\lt x'$, and $\psi_r(x,y)$, the potential for $x\gt x'$. Based on the discussion in class, we can easily write down equations for $\psi_l$ and $\psi_r$ that are zero on the conducting walls:

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

where $n$ is an integer, matches the boundary conditions on the walls of the conductor. You need to find $A_n$ and $B_n$ such that the two conditions

$\psi_l(x',y)=\psi_r(x',y)$

and

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

are satisfied.

2\. Write a single equation for the potential $\psi(x,y)$ using $\psi_l$, $\psi_r$, and the Heavyside step function $\Theta$.

The Green function is $G=(4\pi\epsilon_o/A\sigma')\psi$, where $A=\int_0^1dy\int_{0}^L dz$ and $L$ is the length of the duct. (You may want to verify this.)

3\. Use $\psi(x,y)$ and Green's second identity (Equation 1.35 of Jackson), or equivalently, the Green function stated above and equation 1.42 of Jackson to find the potential when the duct is filled with a nonconducting material with a uniform charge density $\rho_o$ as shown in the right part of the figure above.

----

Note: In problem 2.15 of Jackson, he gives the Green function for the case where a line of charge parallel to the $z$-axis passes through $(x,y)=(x',y')$. That problem is a bit more complicated than the problem considered here. In problem 2.16, of Jackson, he states the result of using the Green function from problem 2.15 to find the potential for the configuration in part 3. above.

----

**Solution**

**1\.** Both

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

and

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

satisfy $\partial^2 \psi/\partial^2 x+\partial^2 \psi/\partial^2 y=0$ and the boundary conditions

$\psi_l(0,y)=0 \quad \psi_l(x,0)=0 \quad \psi_l(x,1)=0$

$\psi_r(1,y)=0 \quad \psi_r(x,0)=0 \quad \psi_r(x,1)=0$

The equations for $\psi_l$ and $\psi_r$ could have been derived using the above six boundary equations and starting with 

$\psi_l=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[A_n\sinh(n\pi x)+a_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[B_n\sinh(n\pi x)+b_n\cosh(n\pi x)\Big]$

or most generally

$\psi_l=\sum_{n=0}^{\infty}\Big[A^l_n\sin(n\pi y)+B^l_n\cos(n\pi y)\Big]\Big[C^l_n\sinh(n\pi x)+D^l_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\Big[A^r_n\sin(n\pi y)+B^r_n\cos(n\pi y)\Big]\Big[C^r_n\sinh(n\pi x)+D^r_n\cosh(n\pi x)\Big]$

However, the result will be the same. In problems such as these, it is often easier to reason out what the form of the solution will be rather than starting from the most general equation. In this case, we need the $\sin$ solution in the $y$ direction because it can have zeros at two locations. The $\sinh(n\pi(x-1))$ term is justified because we know that $A\sinh x$ and $B\cosh x$ can be combined into a $C\sinh (x + \delta)$ with a "phase" shift $\delta$.

The continuity condition

$\psi_l(x',y)=\psi_r(x',y)$

gives

$\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x') = \sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x'-1))$

It follows that

$\displaystyle B_n = \frac{\sinh(n\pi x')}{\sinh(n\pi(x'-1))}A_n$

The jump condition

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

gives

$\displaystyle\sum_{n=0}^{\infty}(n\pi)\sin(n\pi y)\Big[- B_n\cosh(n\pi(x'-1))+A_n\cosh(n\pi x')\Big]=\frac{\sigma'}{\epsilon_o}$

The term in square brackets

$-B_n\cosh(n\pi(x'-1)) + A_n\cosh(n\pi x')$

rewritten using the continuity relationship $B_n = A_n\sinh(n\pi x')/\sinh(n\pi(x'-1))$ is

$\displaystyle A_n\left[\cosh(n\pi x')-\frac{\sinh(n\pi x')\cosh(n\pi(x'-1))}{\sinh(n\pi(x'-1))}\right]$

or

$\displaystyle A_n\frac{\sinh(n\pi(x'-1))\cosh(n\pi x')-\sinh(n\pi x')\cosh(n\pi(x'-1))]}{\sinh(n\pi(x'-1))}$

The numerator simplifies to $\sinh(-n\pi)=-\sinh(n\pi)$. This can be seen by expanding the hyperbolic functions as exponentials or using the identity

$\sinh(\alpha-\beta)=\sinh(\alpha)\cosh(\beta)-\sinh(\beta)\cosh(\alpha)$

with $\alpha = n\pi (x' - 1)$ and $\beta = n\pi x'$.

The continuity condition equation thus simplifies to

$\displaystyle\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\sigma'}{\epsilon_o}$

Multiplication of this by $\sin(l\pi y) dy$ and integration from $y=0$ to $1$ and using

$\displaystyle\int_0^1\sin(l\pi y)\sin(n\pi y) dy=0\qquad\mbox{ for }l\ne n$

$\displaystyle\int_0^1\sin(l\pi y)\sin(n\pi y) dy=\frac{1}{2}\qquad\mbox{ for }l=n$

$\displaystyle\int_0^1\sin(l\pi y) dy=\frac{2}{l\pi}\quad\mbox{ for }l=1, 3, 5, ...$

gives (after changing the dummy index from $l$ to $n$),

$\displaystyle A_n = - \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{\sinh(n\pi(x'-1))}{\sinh(n\pi)}$

$\displaystyle B_n = - \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{\sinh(n\pi x')}{\sinh(n\pi)}$

for $n=1, 3, 5, ...$ and $A_n=B_l=0$ for $n = 2, 4, ...$.

$\boxed{\displaystyle \psi_l(x,x') = -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(x'-1))\sinh(n\pi x)\sin(n\pi y)}$

$\boxed{\displaystyle \psi_r(x,x')= -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi x')\sinh(n\pi (x-1))\sin(n\pi y)}$

or, using $-\sinh(x)=\sinh(x)$ and defining $x_{\lt}$ to the the smaller of $x$ and $x'$ and $x_{\gt}$ to the the larger of $x$ and $x'$,

$\displaystyle\psi(x,x') =  \sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(1-x_{\gt}))\sinh(n\pi x_{\lt})\sin(n\pi y)$

or, in terms of $\Theta$,

$\displaystyle\psi(x,x') = \psi_l\Theta(x'-x)+\psi_r\Theta(x-x')$

----

**2\.** Using $G(x)=(4\pi\epsilon_o/A\sigma')\psi(x)$ gives

$\displaystyle G(x,x') = \frac{4\pi\epsilon_o}{A\sigma'}\Big[\psi_l(x,x')\Theta(x'-x)+\psi_r(x,x')\Theta(x-x')\Big]$

----

**3\.** The surface integral in equation 1.44 of Jackson is zero (why?) leaving 

$\displaystyle\Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\int_{\mathcal V} G(\mathbf{x},\mathbf{x}') \rho(\mathbf{x}')d^3x'$

$G$ does not depend on $y'$ or $z'$ and $\rho=\rho_o=const$, so integration over $y$ and $z$ gives

$\displaystyle\Phi(x) = \frac{\rho_oA}{4\pi\epsilon_o}\int_0^1 G(x,x') \thinspace dx'$

where $A$ is as defined in the problem statement. Using $G$ from part 2. gives

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_0^1  \Big[\psi_l(x,x')\Theta(x'-x)+\psi_r(x,x')\Theta(x-x')\Big]\thinspace dx'$

The step function modifies the limits of integration, so

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_x^1  \psi_l(x,x')\thinspace dx'+\frac{\rho_o}{\sigma'}\int_0^x  \psi_r(x,x')\thinspace dx'$

The interpretation of this equation is that to find the potential at $x$,  sum over the potential due to differential sheets at different $x'$. The first integral is the potential just to the left of all differential sheets to the right of $x$. The second integral is the potential just to the right of all differential sheets to the left. This is the equation you would probably write down in order to compute the potential due to a slab if you did not know about Green functions -- the total potential is simply the sum of potentials due to all differential sheets.

The first integral requires the integration

$\displaystyle\int_x^1\sinh(n\pi(x'-1))\thinspace dx'=\frac{\cosh(0)-\cosh(n\pi(x-1))}{n\pi}$

The second integral requires the integration

$\displaystyle\int_0^x\sinh(n\pi x')\thinspace dx'=\frac{\cosh(n\pi x)-\cosh(0)}{n\pi}$

Using these, evaluation of the integrals gives

$\displaystyle\Phi(x) =-\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty}  \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\thickspace\Large{\times}
$

$\Big[\sinh(n\pi x)(1-\cosh[n\pi (x-1)])+\sinh[n\pi(x-1)](\cosh(n\pi x)-1))\Big]
$

Using again $\sinh(\alpha-\beta)=\sinh(\alpha)\cosh(\beta)-\sinh(\beta)\cosh(\alpha)$

with $\alpha=n\pi(x-1)$ and $\beta=n\pi$

$\displaystyle\Phi(x) = -\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty} \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\Big[-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]\Big]$

To combine $\sinh(n\pi x)+\sinh[n\pi(x-1)$ into one term, note that when expanded in terms of exponentials the following sum has four terms

$\sinh(u)+\sinh(u-1) = \frac{1}{2}\left(e^u-e^{-u}+e^{u-1}+e^{-(u-1)}\right)$

The following product has four terms

$\cosh\alpha\sinh\beta = \frac{1}{4}\left(e^{\alpha+\beta}-e^{-(\alpha+\beta)}+e^{\alpha-\beta}-e^{-(\alpha-\beta)}\right)$

Setting $\alpha + \beta = u$ and $\alpha-\beta=u-1$

gives $\alpha = u-1/2$ and $\beta=1/2$. Thus

$\displaystyle\sinh(n\pi x)+\sinh[n\pi(x-1)] = 2\cosh[n\pi(x-1/2)]\sinh(n\pi/2)$

and

$\displaystyle\frac{-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]}{\sinh(n\pi)}=\Big[-1+\frac{\sinh(n\pi/2)}{\sinh(n\pi)}2\cosh[n\pi(x-1/2)]\Big]$

Finally, using

$\displaystyle\sin(2x)=2\cosh(x)\sinh(x) \Rightarrow \sinh(x)=2\cosh(x/2)\sinh(x/2)$

gives 

$\displaystyle\frac{\sinh(x/2)}{\sinh(x)}=\frac{1}{2\cosh(x/2)}$

and the final result of

$\displaystyle\Phi = \frac{4}{\pi^3\epsilon_o}\sum_{n=1,3,...}^{\infty}\frac{\sin(n\pi y)}{n^3}\left[1-\frac{\cosh[n\pi(x-1/2)]}{\cosh(n\pi/2)}\right]$

Defining $m = (n-1)/2$ gives the result of problem 2.16 of Jackson.

## 2-D Cylindrical Boundary Value Problem

A non-conducting and infinitely long cylindrical shell of radius $b$ has a surface charge density of $\sigma=\sigma_2\sin\thinspace2\phi$. 

1. Find $\psi(s,\phi)$ using the boundary value method. Note that the general solution to Laplace's equation in cylindrical coordinates for a problem with no $z$ dependence is

   $\psi=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi) s^n+a_o\ln s+\sum_{n=1}^\infty (a_n\cos n\phi+b_n \sin n\phi)s^{-n}$

2. Repeat 1. assuming $\sigma=\sigma_o + \sigma_2\sin\thinspace2\phi$. In this case, the $\ln s$ term cannot be dropped for the $s>b$ solution; $a_o$ is determined from the requirement that for large $s$, the potential should be that for a line of charge with linear density $\lambda$ that is the average of $\sigma$ over $\phi$.

%In class, I did the a problem for $\sigma=\sigma_o\cos\thinspace\phi$. In justifying dropping the $\rho^n$ and $\ln\rho$ terms, I mentioned that this was justified because the potential should go to zero as $\rho\rightarrow \infty$. What I neglected to mention is that this is because for large $\rho$, the system appears as a line of charge with linear charge density, $\lambda$, and $\lambda=0$ for the given $\sigma$. This can be seen by computing the linear charge density $\lambda = \int_0^{2\pi} \sigma b d\phi$.

**Solution**

I'll solve part 2., which reduces to part 1. if $\sigma_o=0$. I will also solve this the long way. After solving this problem the long way, you should be able to identify short--cuts, one of which is find the potnential due to a long and uniformly charged cylinder and adding the result to the answer of part 1.

We can conclude that the $ s ^n$ terms are zero for the potential outside of the cylinder because at large $ s $ the cylinder will be approximately that for a line of charge, for which potential will be proportional to $\overline{\lambda}\ln s $ for large $ s $, where $\overline{\lambda}$ is the azimuthally averaged surface charge density: $\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$. That is, for large $ s $, the potential should be the same as that when all of the charge on the cylinder is collapsed onto a line, for which the potential is $\psi=const-(\overline{\lambda}/2\pi\epsilon_o)\ln s $, giving $a_o=-\overline{\lambda}/2\pi\epsilon_o$ and $A_o=const$. The constant $A_o$ is determined by defining a reference potential $V_r$ at a reference point $s_r$. For example, if $\psi( s _r)=V_r$, then $V_r=A_o-\overline{\lambda}\ln s _r/2\pi\epsilon_o$ and the terms $A_o+a_o\ln s $ combine to form

$A_o+a_o\ln s =V_r-(\overline{\lambda}/2\pi\epsilon_o)\ln( s / s _r)$

----
**Note** For a line of charge, we can't choose a reference potential to be zero at infinity. This is related to the problem that arises if one attempts to use $V=\frac{1}{4\pi\epsilon_o}\int {dq}/{|\mathbf{r}-\mathbf{r'}|}$ to compute the potential for an infinite line of charge. The derivation of this integral assumes that the potential is zero at large $\mathbf{r}$. Using Gauss' law, one can show that this is not the case -- $E_{ s }=\frac{\lambda}{2\pi\epsilon_o}\frac{1}{ s }$ and so $\psi =  \psi_o  - \frac{\lambda}{2\pi\epsilon_o}\ln s $, where $ \psi^o $ is a constant. We can't choose $\psi( s =\infty)=0$ because it gives $ \psi_o =-\infty$. So to compute the potential for an infinite line of charge, one must either use the integral equation for the electric field or Gauss' law. See also 2.3.4 of Griffiths where he notes that the integral diverges for a charge distribution that extends to infinity.

----


Outside the cylinder, the general form is then

$ \psi^o =A_o'+a_o\ln s +\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi) s ^{-n}$

I've kept the $\ln s $ term. In the following, I'll show how the values of $A_o'$ and $a_o$ given above follow from an alternative argument than the one given above. 

Inside the cylinder, the potential should be finite and so the $\ln s $ and $ s ^{-n}$ terms are dropped. (If the cylinder had a constant charge density, we would expect the potential to be constant inside of the cylinder and would keep only the $A_o$ term.)

Inside the cylinder, the general form is then

$\displaystyle\psi^i=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi) s ^n$

The two boundary conditions are

$\psi^o (b,\phi)= \psi^i(b,\phi)$ and $\displaystyle \left[\partial  \psi^o /\partial  s -\partial  \psi^i/\partial  s \right]_{ s =b}=-\sigma/\epsilon_o$

(Make sure that you know how to derive the second boundary condition.)

The boundary condition $\psi^o (b,\phi)= \psi^i(b,\phi)$ gives

$\displaystyle A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)b^n$

This equation gives

$A_o'+ a_o\ln b = A_o$

and

$\displaystyle A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$

from "matching terms", which means integrating both sides by either $\cos n'\phi\thinspace d\phi$ or $\sin n'\phi\thinspace d\phi$, with $n'$ being an integer greater than zero, and integrating from $\phi=0$ to $2\pi$ and using 

$\displaystyle\int_0^{2\pi}\cos n\thinspace d\phi = 0;\qquad\displaystyle\int_0^{2\pi}\sin n\thinspace d\phi = 0;\qquad\displaystyle\int_0^{2\pi}\cos n'\phi\sin n\phi\thinspace d\phi = 0$

$\displaystyle\int_0^{2\pi}\cos n'\phi\cos n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$

$\displaystyle\int_0^{2\pi}\sin n'\phi\sin n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$


Notice that in cylindrical problems we integrate over $\phi$, so the limits of integration are from $0$ to $2\pi$. In contrast, in spherical problems with a $\theta$ dependence, we integrate from $0$ to $\pi$.

To determine the relationship between the coefficients quoted above, it is often easier to write out the first few terms in the sums

$A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\cos n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\cos n\phi)b^n$

in alignment as

$$
\begin{align*}
&& A_o'+a_o\ln b &&+ && (a_1\cos \phi+b_1\sin \phi)b^{-1} &&+ && (a_2\cos 2\phi+b_2\sin 2\phi)b^{-2}  && +&& ... && \\
= && A_o && + && (A_1\cos \phi+B_1\sin \phi)b^{1} &&+ && (A_2\cos 2\phi+B_2\sin 2\phi)b^{2} && +&& ... &&
\end{align*}
$$

and then read off the matching terms

$A_o'+a_o\ln b = A_o$

$a_1/b = A_1b\quad b_1/b = B_1b$

$a_2/b^2 = a_2b^2\quad b_2/b^2 = B_2b^2$

$a_3/b^3 = a_3b^2\quad b_3/b^3 = B_3b^2$

$...$

in order to conclude the general result stated earlier of

$A_o'+ a_o\ln b = A_o$

$A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$

The boundary condition

$\displaystyle\left[\partial  \psi^o /\partial  s -\partial  \psi^i/\partial  s \right]_{ s =b}=-\sigma/\epsilon_o$

gives

$$
\begin{align*}
&& a_o/b &&  - &&(a_1\cos \phi+b_1\sin \phi)b^{-2} &&-&&2(a_2\cos 2\phi+b_2\sin 2\phi)b^{-3} &&+ &&... \\
&&           && - && (A_1\cos \phi+B_1\sin \phi) &&-&& 2(A_2\cos 2\phi+B_2\sin 2\phi)b^{1} &&+&& ... &&\\
=&& -(\sigma_o/\epsilon_o)&& && && && -(\sigma_2/\epsilon_o)\sin\thinspace2\phi
\end{align*}
$$

This gives

$a_o/b=-\sigma_1/\epsilon_o$

$-a_1/b^2-A_1=0\quad -b_1/b^2-B_1=0$

$-2a_2/b^3-2A_2b = 0\quad -2b_2/b^3-2B_2b = -\sigma_2/\epsilon_o$

$-3a_3/b^4-3A_3b^2 = 0\quad -3b_3/b^4-3B_3b^2 = 0$

$...$

The equation $a_o=-b\sigma_o/\epsilon_o$ from the second boundary condition combines with $A_o'+a_o\ln b = A_o$ from the first boundary condition to give

$A_o=A_o'-(b\sigma_o/\epsilon_o)\ln b$

The equation $a_1/b = A_1b$ from the first boundary condition combines with $-a_1/b^2-A_1=0$ from the second boundary condition to give

$2A_1=0$

which is only possible if $A_1=0$.  Similarily, all terms except $b_2$ and $B_2$ are zero.

The equation $b_2/b^2 = B_2b^2$ from the first boundary condition and $-2b_2/b^3-2B_2b = -\sigma_o/\epsilon_o$ combine to give

$B_2=+\sigma_2/4b\qquad\qquad b_2=b^3\sigma_2/4$

The final result is

$\displaystyle\psi^i=A_o'-(b\sigma_o/\epsilon_o)\ln b+\frac{\sigma_2}{4\epsilon_0}\frac{ s ^2}{b}\sin 2\phi$

$\displaystyle\psi^o =A_o'-(b\sigma_o/\epsilon_o)\ln  s +\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi$

If the reference potential is chosen to be zero at $ s =0$, then $A_o'=(b\sigma_1/\epsilon_o)\ln b$ and

$\boxed{\displaystyle\psi^i=\frac{\sigma_2}{4\epsilon_0}\frac{ s ^2}{b}\sin 2\phi}$

$\boxed{\displaystyle\psi^o =(b\sigma_o/\epsilon_o)\ln (b/ s )+\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi}$

(In this problem, the reference potential was not given intentionally. Ideally you recognized that a reference potential was needed to fully specify the solution. Also note that we cannot specify a constant reference potential at any other $s$ because the potential depends on $\phi$.)

*Note*: Inspection of this answer suggests a faster way of solving the general problem of

$\sigma_o + \sigma_1\sin \phi + \sigma_2\sin 2\phi + ...$

or more generally,

$\sigma_o + \sigma_{1s}\sin \phi + \sigma_{1c}\cos\phi + \sigma_{2s}\sin 2\phi + \sigma_{2c}\cos 2\phi + ...$

First find the potential due to $\sigma_o$. Then, write $\psi^i$ and $\psi^o$ not as an infinite sum, but rather as a sum that involves only terms of $\sin n\phi$ and $\cos n\phi$ that appear in $\sigma$.

*Check*: Earlier it was argued that for large $ s $, $\psi^o $ should approach

$\psi^o ( s \rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln s $

where 

$\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$

Using $\sigma=\sigma_o + \sigma_2\sin\thinspace2\phi$ gives $\overline{\lambda}=2\pi b\sigma_o$ and so the computed value of $ \psi^o $ of

$\displaystyle\psi^o =(b\sigma_o/\epsilon_o)\ln (b/ s )+\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi=(b\sigma_o/\epsilon_o)\ln b-(b\sigma_o/\epsilon_o)\ln  s +\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi$

matches the limit

$\psi^o ( s \rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln s =const-(b\sigma_o/\epsilon_o)\ln s$
