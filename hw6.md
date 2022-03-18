# Long Tube with Line of Charge

1. Do problem [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge) with the modification that $\sigma'=\lambda'\delta(y-y')$ and show that how it can be used to arrive at the result quoted in problem 2.15(b) of Jackson.
1. Use your answer to part 1. and reciprocity to find the potential inside the tube when $\rho=0$ inside the tube, the side at $x=1$ is held at a potential of $V_o$, and the other three sides are grounded. (This is an analog to [HW #3.1.4](#1-d-cartesian-green-function) where we solved a problem that was easy to solve without reciprocity using reciprocity).

**Solution**

1\. The steps used to derive

$$B_n = \frac{\sinh(n\pi x')}{\sinh(n\pi(x'-1))}A_n$$

and

$$\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\sigma'}{\epsilon_o}$$

For this problem, replace $\sigma'$ with $\sigma'=\lambda'\delta(y-y')$ in the above equation.

$$\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\lambda'\delta(y-y')}{\epsilon_o}$$

Multiplication of both sides by $\sin(l\pi y) dy$ and integration from $y=0$ to $1$ and using

$$\int_0^1\sin(l\pi y)\sin(n\pi y) dy=0\qquad\mbox{ for }l\ne n$$

$$\int_0^1\sin(l\pi y)\sin(n\pi y) dy=\frac{1}{2}\qquad\mbox{ for }l=n$$

$$\int_0^1\sin(l\pi y) \delta(y-y') dy=\sin(l\pi y')$$

gives, after changing the dummy index from $l$ to $n$,

$$A_n = - \frac{2\lambda'}{n\pi\epsilon_o}\frac{\sinh(n\pi(x'-1))}{\sinh(n\pi)}\sin(n\pi y')$$

$$B_n = - \frac{2\lambda'}{n\pi \epsilon_o}\frac{\sinh(n\pi x')}{\sinh(n\pi)}\sin(n\pi y')$$

for $n=1, 2, 3 , ...$. Note that $n$ is not constrained to be odd as it was in [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge). The new result is

$$\psi_l = -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(x'-1)]\sinh(n\pi x)\sin(n\pi y)\sin(n\pi y')$$

$$\psi_r= -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi x')\sinh[n\pi (x-1)]\sin(n\pi y)\sin(n\pi y')$$

or, using $-\sinh(x)=\sinh(-x)$ and defining $x_{\lt}$ to the the smaller of $x$ and $x'$ and $x_{\gt}$ to the the larger of $x$ and $x'$,

$$\psi =  \sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-x_{\gt})]\sinh(n\pi x_{\lt})\sin(n\pi y)\sin(n\pi y')$$

Using $G=(4\pi\epsilon_o/L_z\lambda')\psi$ gives

$$G =  8\sum_{n=1}^{\infty} \frac{1}{n}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-x_{\gt})]\sinh(n\pi x_{\lt})\sin(n\pi y)\sin(n\pi y')$$

This is the same equation as problem 2.15 of Jackson except that the $x$ and $y$ variables are swapped. Given the fact that the problem is unchanged if the coordinates on the diagram for [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge) are swapped, we are free to change replace $x$ with $y$ and vice-versa in our equation above and so we conclude that it follows from this geometrical symmetry that

$$G =  8\sum_{n=1}^{\infty} \frac{1}{n}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-y_{\gt})]\sinh(n\pi y_{\lt})\sin(n\pi x)\sin(n\pi x')$$

Alternatively, the equivalence can be proved using an identity such as equation 3.169 of Jackson.

2\. First, obtain an answer using the standard boundary value method. The potential

$$\Phi = \sum_{n=1}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$$

satisfies the three boundary conditions for which the potential on the boundary is zero.

To determine $A_n$, multiply both sides by $\sin(l\pi y)dy$ and integrate from $y=0$ to $y=1$. This gives

$$A_n=\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\quad n=1,3,...$$

$$A_n=0\quad n=2,4,...$$

and so the answer we expect is

$$\Phi = \sum_{n=1,3,...}^{\infty}\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)$$

----

To solve this problem using $G$, we need to compute

$$\Phi(x,y) = -\frac{1}{4\pi}\oint_\mathcal{S} \Phi(x,x',y,'y) \frac{\partial G}{\partial n'}\Bigg|_{\mathcal{S}} da'$$

(You should be able to explain what happened to the other terms in 1.42 of Jackson, which the above is based on and also the justification for the following equation.)

For this problem, the required integration is
%<code>!!!</code>The surface $\mathcal{S}$ is the surface of the volume $\mathcal{V}$, which is the volume inside the tube. $\mathcal{S}$ has a cross-sectional area of 1x1 and a length of $L_z$. On the two open ends of the tube, $n'=\pm z'$ and $\partial G/\partial z'=0$. On three of the sides of the volume, $\Phi=0$. This leaves the side at $x=1$, which has an outward normal of $n=x$. The integration needed is thus

$$\Phi(x,y) = -\frac{1}{4\pi}\int_0^1\int_0^{L_z} \Phi(1,x,y,y') \frac{\partial G}{\partial x'}\Bigg|_{x'=1} dy'dz'$$

Using $\Phi(1,x,y,y')=V_o$ and the fact that integration over $z'$ gives $L_z$, we have

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\int_0^1\frac{\partial G}{\partial x'}\Bigg|_{x'=1} dy'$$

Using the relationship

$$G=\frac{4\pi\epsilon_o}{L_z\lambda'}\psi$$

this is

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\frac{4\pi\epsilon_o}{L_z\lambda'}\int_0^1\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1} dy'$$

Using $\psi = \psi_l\Theta(x'-x)+\psi_r\Theta(x-x')$,

$$\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1}= \Theta(1-x)\frac{\partial \psi_l}{\partial x'}\Bigg|_{x'=1}+\Theta(x-1)\frac{\partial \psi_r}{\partial x'}\Bigg|_{x'=1}$$

(The two other terms in $\partial \psi/\partial x'$ involving the derivative of $\Theta$ cancel; this was considered in a previous HW problem.) The second term in this equation is zero because the volume extends from $x=0$ to $x=1$ for which $\Theta(x-1)=0$. Also, in this range of $x$, $\Theta(1-x) = 1$. This leaves

$$\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1}= \frac{\partial \psi_l}{\partial x'}\Bigg|_{x'=1}$$

Using

$$\psi_l = -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(x'-1)]\sinh(n\pi x)\sin(n\pi y)\sin(n\pi y')$$

gives

$$\frac{\partial \psi}{\partial x'}\Bigg|\_{x'=1}= -\sum_{n=1}^{\infty} \frac{2\lambda'}{\epsilon_o}\frac{1}{\sinh(n\pi)}\cosh(0)\sinh(n\pi 
x)\sin(n\pi y)\sin(n\pi y')$$

and the integral

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\frac{4\pi\epsilon_o}{L_z\lambda'}\int_0^1\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1} dy'$$

can be rewritten as

$$\Phi(x,y) = \sum_{n=1}^{\infty}\frac{2V_o}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)\int_0^1 \sin(n\pi y')  dy'$$

The integral is zero for $n=2, 4, ...$ and $2/n\pi$ for $n=1,3,...$. The final result is then

$$\Phi(x,y) = \sum_{n=1,3,...}^{\infty}\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)$$

which is the same as the result found earlier.

# Azimuthal Symmetry

1\. Find $\Phi(r,\theta)$ for problem [HW 4.1](#green-function-for-infinite-dome) in terms of an infinite sum involving the Legendre polynomials. 

2\. Find the surface charge density on the part of the dome in the $x$--$y$ plane.

**Solution**

1\. Letting $V_o=1$ so that potential is units of $V_o$, the exact solution on the $z$--axis is

$$\Phi(z)=1-\frac{z}{\sqrt{b^2+z^2}}$$

which can be written as

$$\Phi(z)=1-\frac{z}{|z|}\frac{1}{\sqrt{1+\displaystyle\frac{b^2}{z^2}}}$$

or

$$\Phi(z)=1-\frac{z}{|b|}\frac{1}{\sqrt{1+\displaystyle\frac{z^2}{b^2}}}$$

I've kept the absolute values because in some problems, it matters. Here it does not because $b$ is by definition positive, and we are considering the solution for $z\gt 0$. We can thus write the exact solution as either

$$\Phi^o(z)=1-\frac{1}{\sqrt{1+\displaystyle\frac{b^2}{z^2}}}$$

or

$$\Phi^i(z)=1-\frac{z}{b}\frac{1}{\sqrt{1+\displaystyle\frac{z^2}{b^2}}}$$

Where the superscript indicates the equation will be used for either the outer ( $o$; $z\gt b$) or inner ($i$; $z\lt b$) solution.

[The binomial expansion](https://rweigel.github.io/phys305/binomial_expansion.html) has the form

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + \frac{n(n+1)}{2!}\delta^2- \frac{n(n+1)(n+2)}{3!}\delta^3...$$

For $n=1/2$, we have

$$\frac{1}{(1+\delta)^n} = 1 - \frac{1}{2}\delta + \frac{\frac{1}{2}\frac{3}{2}}{2}\delta^2- \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\delta^3...$$

Using $\delta=b/z$ gives

$$\frac{1}{(1+\delta)^n} = 1 - \frac{1}{2}\frac{b^2}{z^2} + \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}- \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}...$$

Using this in the $b/z$ expansion for $\Phi^o$ gives

$$\Phi^o(z)=1-\frac{1}{\sqrt{1+\frac{b^2}{z^2}}}= \frac{1}{2}\frac{b^2}{z^2} - \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}+ \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}+...$$

or

$\displaystyle\Phi^o(z)=\sum_{l=2,4,...}\frac{C_l}{z^l}\qquad$ with $\qquad\displaystyle C_l=(-1)^{(l/2+1)} \frac{(l-1) !!}{(l/2)!}\frac{b^l}{2^{l/2}}$

where the double factorial is similar to the usual factorial with every other term omitted: $n!!\equiv 1\cdot 3\cdot 5\cdot ... n$ for $n$ odd and $n!!\equiv 2 \cdot 4\cdot 6\cdot ... n$ for $n$ even.

For $z\lt b$, we have the same equation as above except with the $b$ and $z$ swapped.


We know that the potential for a charge distribution with azimuthal symmetry can be written in the form

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

This equation must match a power series expansion of the potential along the $+z$-axis, which corresponds to $\theta=0$ and $r=z$.

$$\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)P_l(1)$$

or, equivalently,

$$\psi(z)=A_oP_0(1)+A_1P_1(1)z+...+\frac{B_oP_0(1)}{z}+\frac{B_1P_1(1)}{z^2}+...$$

The values of $P_l(1)$ can be determined from the first recursion relationship of 3.29 of Jackson:

$(l+1)P_{l+1}-(2l+1)xP_l+lP_{l-1}=0$

with $x=\cos 0 = 1$, this is

$(l+1)P_{l+1}(1)=(2l+1)P_l(1)-lP_{l-1}(1)$

The first few values can be computed manually

$l=1\qquad P_2(1)=(3P_1(1)-P_0(1))/2=1$

$l=2\qquad P_3(1)=(5P_2(1)-2P_1(1))/3=1$

$l=3\qquad P_4(1)=(7P_2(1)-3P_1(1))/4=1$

Based on the above, we expect that $P_l(1)=1$ for all $l$. (But this is not a proof.) 

For this to match our $z\gt b$ expansion of

$$\Phi^o(z)= \frac{1}{2}\frac{b^2}{z^2} - \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}+ \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}+...$$

we need $A_l=0$ for all $l$ and

$B_0=0$ because there is no $1/z$ term in the $z\gt b$ expansion.

$B_1=+\frac{b^2}{2}$ because the $1/z^2$ constants must match.

$B_2=0$ because there is no $1/z^3$ term in the $z\gt b$ expansion.

$\displaystyle B_3=-\frac{\frac{1}{2}\frac{3}{2}}{2}b^4$ 

because the $1/z^4$ constants must match.

$B_4=0$

$$B_5P_5(1)=+\frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}b^6$$

etc.



We now have values for the $B_l$s:

$B_{l-1}=C_l\qquad l=2, 4, ...$

or, explicitly,

$$B_{l-1}=(-1)^{(l/2+1)} \frac{(l-1) !!}{(l/2)!}\frac{b^l}{2^{l/2}}\qquad l=2,4,...$$

The above steps are what is needed to find the constants for the potential $\Phi^o$ for $z \gt b$. The steps for finding the potential $\Phi^i$ for $z \lt b$ are similar. In this case, the $B_l$ terms are all zero and only every other $A_l$ term is non--zero.

2\. From 1., you will have a potential for $z/b\lt 1$ of the form

$$\psi(r,\theta)=\frac{B_1P_1(\cos\theta)}{r^2}+\frac{B_3P_3(\cos\theta)}{r^4}+...$$

From Gauss's law, the surface charge density just outside of a conductor is $\sigma=\epsilon_o\mathbf{E}\bfcdot\hat{\mathbf{n}}$, where $\hat{\mathbf{n}}$ is the outward normal to the surface. Equivalently,

$\displaystyle\sigma=-\epsilon_o\frac{\partial \psi}{\partial n}$ 

where the partial derivative is evaluated at the the surface.

In this problem, $n=z$ and we need to evaluate the partial derivative at $z=0$. That is, we need to compute

$$\frac{\partial \psi}{\partial z}=\left[\frac{\partial }{\partial z}\frac{B_1P_1(\cos\theta)}{r^2}+\frac{\partial}{\partial z}\frac{B_3P_3(\cos\theta)}{r^4}+...\right]_{z=0}$$

Given that $\cos\theta = z/r$, we can write

$$\frac{\partial \psi}{\partial z}=\left[\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}+\frac{\partial}{\partial z}\frac{B_3P_3(z/r)}{r^4}+...\right]_{z=0}$$

For the first term, we have, using the product rule for derivatives

$$
\begin{align*}
\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2} & =\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)+B_1P_1(z/r)\frac{\partial(1/r^2)}{\partial z}\right]\_{z=0}\\\\
&=\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)\right]\_{z=0}+B_1P_1(0)\frac{\partial(1/r^2)}{\partial z}\Bigg|\_{z=0}
\end{align*}
$$

Given that $P_1(0)=0$, we are left with

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)\right]_{z=0}$$

At $z=0$, $r=s$ (the radial cylindrical coordinate), so

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^2}\left[\frac{\partial }{\partial z}P_1(z/r)\right]_{z=0}$$

Using the chain rule for derivatives

$\displaystyle \frac{df(g(u))}{du} = \frac{df}{dg}\frac{dg}{du}$ 

with $f=P_1$ and $g=z/r$, the term in square braces can be re-written, giving

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^2}\left[\frac{\partial P_1(g)}{\partial g}\frac{\partial (z/r)}{\partial z}\right]_{z=0}$$

Using

$$\frac{\partial (z/r)}{\partial z}\Big|\_{z=0}=\left[\frac{1}{r}-\frac{z}{r^2}\right]_{z=0}=\frac{1}{s}$$

leaves

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^3}\frac{\partial P_1(g)}{\partial g}\Big|\_{g=0}$$

Given that $\frac{\partial P_1(g)}{\partial g}=1$, we are left with

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^3}$$

The remainder of the problem involves steps similar to the above. To obtain a general solution, we need to know $dP_l/dx|_{x=0}$. This can be found using the second equation of 3.29 of Jackson:

$$\frac{dP_{l+1}}{dx}-x\frac{dP_{l+1}}{dx} - (l+1)P_l=0$$

When evaluated at $x=0$, this is

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} =(l+1)P_l(0)$$

Using again the recursion relationship

$(l+1)P_{l+1}-(2l+1)xP_l+lP_{l-1}=0$

with $x=0$, gives

$P_{l+1}(0)=-\frac{l}{l+1}P_{l-1}(0)$

so

$l=1$, $P_2(0)=-\frac{1}{2}P_0(0)=-\frac{1}{2}$

$l=2$, $P_3(0)=-\frac{2}{3}P_1(0)=0$

$l=3$, $P_4(0)=-\frac{3}{4}P_2(0)=\frac{3}{4}\frac{1}{2}$

$l=4$, $P_5(0)=-\frac{4}{5}P_3(0)=0$

$l=5$, $P_6(0)=-\frac{5}{6}P_4(0)=-\frac{5}{6}\frac{3}{4}\frac{1}{2}$

or, in general

$P_l(0)=\frac{(l-1)!!}{l!!}(-1)^{l/2}\qquad l=2,4,...$

From which it follows

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} = 0 \qquad l=1,3,...$$

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} = (l+1)\frac{(l-1)!!}{l!!}(-1)^{l/2}=\frac{(l+1)!!}{l!!}(-1)^{l/2}\qquad l=2,4,...$$

Shifting the index by $-1$ gives

$$\frac{dP_{l}}{dx}\Big|_{x=0} = 0 \qquad l=0,2,...$$

$$\frac{dP_{l}}{dx}\Big|_{x=0} =\frac{l!!}{(l-1)!!}(-1)^{(l-1)/2}\qquad l=1,3,...$$

So the first few non--zero terms are

$$l=1\qquad \frac{dP_{1}}{dx}\Big|_{x=0}=\frac{1!!}{0!!}(-1)^0=1$$

$$l=3\qquad \frac{dP_{3}}{dx}\Big|_{x=0}=\frac{3!!}{2!!}(-1)^1=-\frac{3}{2}$$

$$l=5\qquad \frac{dP_{5}}{dx}\Big|_{x=0}=\frac{5!!}{4!!}(-1)^2=\frac{5\cdot 3\cdot 1}{4\cdot 2}=\frac{15}{8}$$

Check: Table 3.15 gives the first five Legendre polynomials. Manual evaluation of the derivatives gives:

$dP_0(x)/dx=0$

$dP_1(x)/dx\Big|_{x=0}=1$

$dP_2(x)/dx\Big|_{x=0}=0$

$dP_3(x)/dx\Big|_{x=0}=-\frac{3}{2}$

$dP_4(x)/dx\Big|_{x=0}=0$

From [A table](https://en.wikipedia.org/wiki/Legendre_polynomials#Rodrigues'_formula_and_other_explicit_formulas), $P_5={\textstyle {\tfrac {1}{8}}\left(63x^{5}-70x^{3}+15x\right)}$ so

$dP_5(x)/dx\Big|_{x=0}=\frac{15}{8}$
