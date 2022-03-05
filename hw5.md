# Long Rectangular Tube with Sheet of Charge 

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


**Solution**

----

1\. Both

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

and

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

satisfy $\partial^2 \psi/\partial^2 x+\partial^2 \psi/\partial^2 y=0$. And the boundary conditions

$\psi_l(0,y)=0 \quad \psi_l(x,0)=0 \quad \psi_l(x,1)=0$

$\psi_r(1,y)=0 \quad \psi_r(x,0)=0 \quad \psi_r(x,1)=0$

The equations for $\psi_l$ and $\psi_r$ could have been derived using the above six boundary equations and starting with 

$\psi_l=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[A_n\sinh(n\pi x)+a_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[B_n\sinh(n\pi x)+b_n\cosh(n\pi x)\Big]$

or most generally

$\psi_l=\sum_{n=0}^{\infty}\Big[A^l_n\sin(n\pi y)+B^l_n\cos(n\pi y)\Big]\Big[C^l_n\sinh(n\pi x)+D^l_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\Big[A^r_n\sin(n\pi y)+B^r_n\cos(n\pi y)\Big]\Big[C^r_n\sinh(n\pi x)+D^r_n\cosh(n\pi x)\Big]$

However, the result will be the same. In problems such as these, it is often easier to reason out what the form of the solution will be rather than starting from the most general equation. In this case, we need the $\sin$ solution in the $y$ direction because it can have zeros at two locations. The $\sinh(n\pi(x-1))$ term is justified because we know that $a\sinh x$ and $b\cosh x$ can be combined into a $C\sinh (x + \delta)$ with a "phase" shift $\delta$.

The continuity condition

$\psi_l(x',y)=\psi_r(x',y)$

gives

$\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x') = \sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x'-1))$

It follows that

$\displaystyle B_n = \frac{\sinh(n\pi x')}{\sinh(n\pi(x'-1))}A_n$

The jump condition

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

gives

$\sum_{n=0}^{\infty}(n\pi)\sin(n\pi y)\Big[- B_n\cosh(n\pi(x'-1))+A_n\cosh(n\pi x')\Big]=\frac{\sigma'}{\epsilon_o}$

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

$\displaystyle B_n = - \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{\sinh(n\pi x')}{\sinh(n\pi)}$$

for $n=1, 3, 5, ...$ and $A_n=B_l=0$ for $n = 2, 4, ...$.

$\psi_l = -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(x'-1))\sinh(n\pi x)\sin(n\pi y)$

$\psi_r= -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi x')\sinh(n\pi (x-1))\sin(n\pi y)$

or, using $-\sinh(x)=\sinh(x)$ and defining $x_{\lt}$ to the the smaller of $x$ and $x'$ and $x_{\gt}$ to the the larger of $x$ and $x'$,

$\displaystyle\psi =  \sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(1-x_{\gt}))\sinh(n\pi x_{\lt})\sin(n\pi y)$

or, in terms of $\Theta$,

$\displaystyle\psi = \psi_l\Theta(x'-x)+\psi_r\Theta(x-x')$

----

2.Using $G=(4\pi\epsilon_o/A\sigma')\psi$ gives

$\displaystyle G = \frac{4\pi\epsilon_o}{A\sigma'}\Big[\psi_l\Theta(x'-x)+\psi_r\Theta(x-x')\Big]$

----

3\. The surface integral in equation 1.44 of Jackson (why?) leaving 

$\displaystyle\Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\int_{\mathcal V} G(\mathbf{x},\mathbf{x}') \rho(\mathbf{x}')d^3x$

$G$ does not depend on $y'$ or $z'$ and $\rho=\rho_o=const$, so

$\displaystyle\Phi(x) = \frac{A}{4\pi\epsilon_o}\int_0^1 G(x,x') \rho\thinspace dx'$

where $A$ is as defined in the problem statement.

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_0^1  \Big[\psi_l\Theta(x'-x)+\psi_r\Theta(x-x')\Big]\thinspace dx'$

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_x^1  \psi_l\thinspace dx'+\frac{\rho_o}{\sigma'}\int_0^x  \psi_r\thinspace dx'$

The first integral requires the integration

$\displaystyle\int_x^1\sinh(n\pi(x'-1))\thinspace dx'=\frac{\cosh(0)-\cosh(n\pi(x-1))}{n\pi}$

The second integral requires the integration

$\displaystyle\int_0^x\sinh(n\pi x')\thinspace dx'=\frac{\cosh(n\pi x)-\cosh(0)}{n\pi}$

Evaluation of the integrals thus gives

$\displaystyle\Phi(x) =-\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty}  \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\thickspace\Large{\times}
$

$\Big[\sinh(n\pi x)(1-\cosh[n\pi (x-1)])+\sinh[n\pi(x-1)](\cosh(n\pi x)-1))\Big]
$

Using again

$\sinh(\alpha-\beta)=\sinh(\alpha)\cosh(\beta)-\sinh(\beta)\cosh(\alpha)$

with $\alpha=n\pi(x-1)$ and $\beta=n\pi$

$\Phi(x) = -\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty} \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\Big[-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]\Big]$

To combine $\sinh(n\pi x)+\sinh[n\pi(x-1)$ into one term, note that when expanded in terms of exponentials the following sum has four terms

$\sinh(u)+\sinh(u-1) = \frac{1}{2}\left(e^u-e^{-u}+e^{u-1}+e^{-(u-1)}\right)$

The following product has four terms

$\cosh\alpha\sinh\beta = \frac{1}{4}\left(e^{\alpha+\beta}-e^{-(\alpha+\beta)}+e^{\alpha-\beta}-e^{-(\alpha-\beta)}\right)$

Setting $\alpha + \beta = u$ and $\alpha-\beta=u-1$

gives $\alpha = u-1/2$ and $\beta=1/2$. Thus

$\displaystyle\sinh(n\pi x)+\sinh[n\pi(x-1)] = 2\cosh[n\pi(x-1/2)]\sinh(n\pi/2)$

and

$\frac{-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]}{\sinh(n\pi)}=\Big[-1+\frac{\sinh(n\pi/2)}{\sinh(n\pi)}2\cosh[n\pi(x-1/2)]\Big]$

Finally, using

$\displaystyle\sin(2x)=2\cosh(x)\sinh(x) \Rightarrow \sinh(x)=2\cosh(x/2)\sinh(x/2)$

gives 

$\displaystyle\frac{\sinh(x/2)}{\sinh(x)}=\frac{1}{2\cosh(x/2)}$

and the final result of

$\displaystyle\Phi = \frac{4}{\pi^3\epsilon_o}\sum_{n=1,3,...}^{\infty}\frac{\sin(n\pi y)}{n^3}\left[1-\frac{\cosh[n\pi(x-1/2)]}{\cosh(n\pi/2)}\right]$

Defining $m = (n-1)/2$ gives the result of problem 2.16 of Jackson.
