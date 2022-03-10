http://web.uconn.edu/~ch351vc/Leg3/node1.html

http://bolvan.ph.utexas.edu/~vadim/classes/17f/mme.pdf

# Legendre Polynomials


$
\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} =
\begin{cases}
\displaystyle\sum_{l=0}^\infty \frac{r^{'l}}{r^{l+1}}P_l(\cos \gamma)  & \mbox{if } r \gt r' \\ \\
\displaystyle\sum_{l=0}^\infty \frac{r^{l}}{r^{'l+1}}P_l(\cos \gamma) & \mbox{if } r \lt r'
\end{cases}
$

or

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$

where $r_{\lt}$ ( $r_{\gt}$) is the smaller (larger) of $r\equiv|\mathbf{x}|$ and $r'\equiv|\mathbf{x}'|$ and $\gamma$ is the angle between $\mathbf{x}$ and $\mathbf{x}'$. 

It is important to remember that $\gamma$ depends on both unprimed and primed coordinates:

$\displaystyle\cos\big(\gamma(\theta,\phi,\theta',\phi')\big) = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$

$\displaystyle\cos\big(\gamma(x,y,z,x',y',z')\big) = \frac{xx'+yy'+zz'}{rr'}$

$\displaystyle\cos(\gamma(\mathbf{x},\mathbf{x}')) =\frac{\mathbf{x}\cdot\mathbf{x}'}{|\mathbf{x}| |\mathbf{x'}|}$

$\displaystyle\cos\big(\gamma(x,y,z,x',y',z')\big) = \frac{xx'+yy'+zz'}{rr'}\quad\mbox{using }r = |\mathbf{x}|\mbox{ and }r' = |\mathbf{x'}|$

$\displaystyle\cos\big(\gamma(\theta,\phi,\theta',\phi')\big) = \sin\theta\sin\theta'\cos\phi\cos\phi' + \sin\theta\sin\theta'\sin\phi\sin\phi'+\cos\theta\cos\theta'$

$\displaystyle\cos\big(\gamma(\theta,\phi,\theta',\phi')\big) = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$

Using this form of $1/|\mathbf{x}-\mathbf{x}'|$, the potential for a point charge is

$\displaystyle I.\quad\Phi(\mathbf{x}) = \frac{q}{4\pi\epsilon_o}\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l_{\tiny{<}}}{r^{l+1}_{\tiny{>}}}P_l(\cos \gamma)$

And the potential for a charge distribution and $r\gt \max(r')$.

$\displaystyle II.\quad\Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\int\frac{dq'}{|\mathbf{x}-\mathbf{x}'|} = \frac{1}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{1}{r^{l+1}}\int (r')^lP_l(\cos\gamma)\rho(\mathbf{x}')d^3x'
$

## Derivation

This form of  $1/|\mathbf{x}-\mathbf{x}'|$ with $\gamma = \theta$ follows from Taylor series expansion of $1/|z-z'|$, the general solution of $\nabla^2\Psi(r,\theta)=0$

$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$

and the uniqueness of solutions to Laplace's equation. (See Section 3.3 of Jackson). Note that in this derivation, the constraint is $\frac{r'}{r} \gt 1$ or $\frac{r}{r'} \gt 1$.

Another way of deriving this expression is from a Taylor series expansion of

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{1}{\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}} = \frac{1}{\sqrt{r^2+r'^2-2r'r\cos\gamma}}$

However, this derivation requires the constraints of

$r'^2 \gt r^2 - 2rr'\cos\gamma$

or

$r'^2 \gt r^2 - 2rr'\cos\gamma$

Using $\gamma=\pi$, the constraint is that for arbitrary $\gamma$

$\frac{r'}{r} \gt 1+\sqrt{2}$

or

$\frac{r}{r'} \gt 1+\sqrt{2}$

To show that the result derived using a Taylor series expansion is convergent for 

$\frac{r'}{r} \gt 1+\sqrt{2}$

or

$\frac{r}{r'} \gt 1+\sqrt{2}$

requires showing that $|P_n(\cos\gamma)| \lt 1$. See Chapter 12.1 and 12.2 of Arfken for details.

## Example

Example: Point charge at $y=y_o$ with $y_o \gt 0$. 

$r'=y_o$ and $(x',y',z')=(0,y_o,0)$, so

$\displaystyle\cos \gamma = \frac{xx'+yy'+zz'}{rr'} = \frac{0+yy_o+0}{ry_o} =\frac{y}{r} = \sin\theta\sin\phi$

Using $I.$,

$\displaystyle I.\quad\Phi(\mathbf{x}) = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$

$\displaystyle
\Phi(\mathbf{x})=
\begin{cases}
		\displaystyle\frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{y_o^{l}}{r^{l+1}}P_l(\sin\theta\sin\phi)  & \mbox{if } r \gt y_o \\ \\
		\displaystyle\frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^{l}}{y_o^{l+1}}P_l(\sin\theta\sin\phi) & \mbox{if } r \lt y_o
\end{cases}
$

Using $II.$, and for $r\gt y_o$

$
\displaystyle II.\quad\Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{1}{r^{l+1}}\int (r')^lP_l(\cos\gamma)\rho(\mathbf{x}')d^3x'
$

and defining the integral as $I(\mathbf{x})$

$I(\mathbf{x})=\int (r')^lP_l(\cos\gamma)\rho(\mathbf{x}')d^3x'$

**Cartesian**

The charge density in cartesian coordinates is

$\displaystyle\rho({\mathbf{x}}')=q\delta(x')\delta(y'-y_o)\delta(z')$

$\displaystyle I(\mathbf{x}) = \int \left(\sqrt{x'^2+y'^2+z'^2}\right)^lP_l(\cos\gamma)q\delta(x')\delta(y'-y_o)\delta(z')dx'dy'dz'$

$\displaystyle\cos\gamma=\frac{xx'+yy'+zz'}{rr'}=\frac{xx'+yy'+zz'}{r\sqrt{x'^2+y'^2+z'^2}}$

$
\displaystyle I(\mathbf{x}) = \int \left(\sqrt{x'^2+y'^2+z'^2}\right)^lP_l\left(\frac{xx'+yy'+zz'}{r\sqrt{x'^2+y'^2+z'^2}}\right) \times q\delta(x')\delta(y'-y_o)\delta(z')dx'dy'dz'
$

$\displaystyle I(\mathbf{x}) = qy_o^lP_l\left(\frac{yy_o}{ry_o}\right)=qy_o^lP_l\left(\frac{y}{r}\right)=qy_o^lP_l(\sin\theta\sin\phi)$

$\displaystyle \Phi(\mathbf{x})=\frac{1}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{1}{r^{l+1}}I(\mathbf{x})=\frac{q}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{y_o^l}{r^{l+1}}P_l(\sin\theta\sin\phi)$

as before.

**Spherical**

In spherical coordinates, the charge is at $(r',\theta',\phi')=(y_o,\pi/2,\pi/2)$, so the charge density 

$\displaystyle \rho({\mathbf{x}}')=\frac{q}{r'^2}\delta(r'-y_o)\delta(\theta'-\pi/2)\delta(\phi'-\pi/2)$

Note: If the charge was at $y=-y_o$, the $\delta(r'-y_o)$ term is un-changed because $r'$ is positive and $\delta(r'+y_o)$ would correspond to a charge at $r'=-y_o$. The $\delta(\phi'-\pi/2)$ would need to be changed to $\delta(\phi'-3\pi/2)$.

In this case

$\displaystyle I(\mathbf{x}) = \int (r')^lP_l(\cos\gamma) \rho(\mathbf{x}') d^3x' = \int (r')^lP_l(\cos\gamma) \rho(\mathbf{x}') r'^2\sin\theta' dr'd\theta'd\phi'$

$\displaystyle I(\mathbf{x}) = \int_0^{\infty}(r')^l\frac{q}{r'^2}\delta(r'-y_o)r'^2dr'\times\int_0^{2\pi}\int_0^\pi\delta(\theta'-\pi/2)\delta(\phi'-\pi/2)P_l\big(\cos(\gamma(\theta,\phi,\theta',\phi')\big)\sin\theta'd\theta'd\phi'
$

$\displaystyle = qy_o^l\times\int_0^{2\pi}\int_0^\pi\delta(\theta'-\pi/2)\delta(\phi'-\pi/2)P_l\big(\cos(\gamma(\theta,\phi,\theta',\phi')\big)\sin\theta'd\theta'd\phi'$

$\displaystyle = qy_o^lP_l\big(\cos(\gamma(\theta,\phi,\pi/2,\pi/2)\big)\sin(\pi/2)$

$\displaystyle = qy_o^lP_l(\sin\theta\sin\phi)$

as before, where the following was used

$$
\begin{align*}
\cos(\gamma(\theta,\phi,\theta',\phi')) & = \sin\theta\sin\theta'\cos(\phi-\phi') + \cos\theta\cos\theta'\\
\cos(\gamma(\theta,\phi,\pi/2,\pi/2)) & = \sin\theta\sin(\pi/2)\cos(\phi-\pi/2) + \cos\theta\cos(\pi/2)\\
& =\sin\theta\cos(\phi-\pi/2)\\
& =\sin\theta\sin\phi 
\end{align*}
$$

# Spherical Harmonics/Associated Legendre Functions

$
\frac{1}{|\mathbf{x}-\mathbf{x}'|} =
\begin{cases}
\displaystyle\sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r'^{l}}{r^{l+1}}Y^*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)  & \mbox{if } r \gt r' \\ \\
\displaystyle\sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r^{l}}{r'^{l+1}}Y^*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi) & \mbox{if } r \lt r'
\end{cases}
$

or

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$

The general solution to Laplace's equation $\nabla^2\Phi(r,\theta,\phi)=0$ is

$\displaystyle\Phi(r,\theta,\phi)=\sum_{l=0}^\infty \sum_{m=-l}^l \left(A_{lm}r^l+\frac{B_{lm}}{r^{l+1}}\right)Y_{lm}(\theta,\phi)$

where $Y_{lm}$ are the spherical harmonic functions that depend on the associated Legendre functions $P_{lm}$:

$\displaystyle Y_{lm}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi}\frac{(l-m)!}{(l+m)!}} P_l^m(\cos\theta)e^{im\phi}$

The $m=0$ term is related to the regular Legendre polynomial $P_l$ (that is, $P_l^0=P_l$:

$\displaystyle Y_{l0}(\theta,\phi)=\sqrt{\frac{2l+1}{4\pi}}P_l(\cos\theta)$

$P_l^m(\cos\theta)e^{im\phi}$ are angular part of product form solutions to Laplace's equation (Eqn. 3.2 of Jackson), $Y_{l,-m}=(-1)^mY_{lm}^\*$, and $Y_{lm}$ are normalized

$\displaystyle\int_0^{2\pi}d\phi\int_0^{\pi}Y^\*_{l'm'}(\theta,\phi)Y_{lm}(\theta,\phi)\sin\theta d\theta=\delta_{ll'}\delta_{mm'}$

The above is a 2-D example of properties that have been used before for 1-D orthogonal functions, e.g.,

$\displaystyle\int_0^{\pi}P_{l'}(\cos\theta)P_l(\cos\theta)\sin\theta d\theta=\int_{-1}^{1}P_{l'}(x)P_l(x) dx=\frac{2}{2l+1}\delta_{ll'}$

and

$\displaystyle\int_0^{1}\sin(n'\pi x)\sin(n\pi x) dx=\frac{2}{\pi}\delta_{nn'}$

(By convention, we use orthonormal functions for 3-D boundary value problems for $\Phi(r,\theta,\phi)$, but only orthogonal for $\Phi(r,\theta)$, $\Phi(x,y)$ problems.)


$\displaystyle l=0\quad\quad \displaystyle Y_{00}(\theta,\phi)=\sqrt{1\over 4\pi}=\sqrt{1\over 4\pi}P_o(\cos\theta)$


$l=1
\quad 
\begin{cases}
\displaystyle Y_{11}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{i\phi}\\ \\
\displaystyle Y_{10}(\theta,\phi)=\sqrt{3\over 4\pi} \cos\theta=\sqrt{3\over 4\pi} P_1(\cos\theta)\\ \\
\displaystyle Y_{1,-1}(\theta,\phi)=Y_{11}^{*}(\theta,\phi)
\end{cases}
$


$
l=2
\quad
\begin{cases}
\displaystyle Y_{22}(\theta,\phi)={1\over 4}\sqrt{15\over 2\pi} \sin^{2}\theta  e^{2i\phi}\\ \\
\displaystyle Y_{21}(\theta,\phi)=-\sqrt{15\over 8\pi} \sin\theta\cos\theta e^{i\phi}\\ \\
\displaystyle Y_{20}(\theta,\phi)=\sqrt{5\over 4\pi} \frac{1}{2}(3\cos^{2}\theta-1)=\sqrt{5\over 4\pi} P_2(\cos\theta)\\ \\
\displaystyle Y_{2,-1}(\theta,\phi)=Y_{21}^\*(\theta,\phi)\\ \\
\displaystyle Y_{2,-2}(\theta,\phi)=Y_{22}^\*(\theta,\phi)
\end{cases}
$

----

Delta function representations (2.8 of Jackson)

$\displaystyle\sum_{l=0}^{\infty}\sum_{m=-l}^{l}Y^\*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi) = \delta(\cos\theta-\cos\theta')\delta(\phi-\phi')=\frac{\delta(\theta-\theta')}{\sin\theta}\delta(\phi-\phi')$

Compare with 1-D case used before

$\displaystyle2\sum_{n=1}^{\infty}\sin(n\pi x)\sin(n\pi x') = \delta(x-x')$

An arbitrary function can be expanded as 

$\displaystyle f(\theta,\phi)=\sum_{l=0}^\infty \sum_{m=-l}^l A_{lm}Y_{lm}(\theta,\phi)\qquad\quad A_{lm} = \int Y^\*_{lm}(\theta,\phi)f(\theta,\phi)d\Omega$

which is analogous to what has been used before for orthogonal functions (2.8 of Jackson)

$\displaystyle f(\theta)=\sum_{l=0}^\infty A_{l}P_{l}(\cos\theta)\qquad\quad A_{l} = \int_{0}^{\pi} P_l(\cos\theta)f(\theta)\sin\theta d\theta=\int_{-1}^{1} P_l(x)f(x) dx$

and

$\displaystyle f(x)=\sum_{n=1}^\infty A_{n}\sin(n\pi x)\qquad\quad A_n = \int_0^{1} \sin(n\pi x)f(x) dx\quad\quad\mbox{(when }f(0)=f(1)=0\mbox{)}$

## Derivation

See Jackson Chapter 3.

## Heirarchy of $1/r$ terms

Simplest charge distributions that give a potential with the lowest-order 1/r term. 

Certain non-simple charge distributions with similar symmetry will lead to potentials with these lowest order $1/r$ terms.

Monopole $\Phi \sim 1/r$

Dipole $\Phi \sim 1/r^2$

Quadrupole $\Phi \sim 1/r^3$

Octapole $\Phi \sim 1/r^4$

## In-Class Problem

Example: Point charge at $y= y_o$ with $y_o \gt 0$. 

1\. Starting with

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^\*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$

and using


$
l=0\quad\quad \displaystyle Y_{00}(\theta,\phi)=\sqrt{1\over 4\pi}=\sqrt{1\over 4\pi}P_o(\cos\theta)
$

$
l=1 
\quad\begin{cases} 
\displaystyle Y_{11}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{i\phi}\\ \\
\displaystyle Y_{10}(\theta,\phi)=\sqrt{3\over 4\pi} \cos\theta=\sqrt{3\over 4\pi} P_1(\cos\theta)\\ \\
\displaystyle Y_{1,-1}(\theta,\phi)=Y_{11}^{*}(\theta,\phi)
\end{cases}
$


find $l=0$ and $l=1$ terms of potential for $r\gt y_o$. Compare with the result found using Legendre polynomials of

$\displaystyle\Phi(\mathbf{x})=\frac{q}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{y_o^l}{r^{l+1}}P_l(\sin\theta\sin\phi)$

2\. Repeat using equations 4.2-4.5 of Jackson.

# Comparison of Legendre and Spherical Harmonic Forms

Legendre has a single summation, spherical harmonic requires additional summation.

Legendre (for $r > r'$)

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r'^l}{r^{l+1}}P_l(\cos \gamma)$

$
\displaystyle \Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\mathbf{x'})}{|\mathbf{x}-\mathbf{x}'|}d^3x' =\frac{1}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{1}{r^{l+1}}\int (r')^lP_l(\cos\gamma)\rho(\mathbf{x}')d^3x'
$

Spherical Harmonic (for $r > r'$)

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r'^{l}}{r^{l+1}}Y^\*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$

$
\displaystyle\Phi(\mathbf{x})  = \frac{1}{4\pi\epsilon_0}\int \frac{\rho(\mathbf{x'})}{|\mathbf{x}-\mathbf{x}'|}d^3x'
 =  \frac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty \sum_{m=-l}^l\frac{4\pi}{2l+1}\frac{Y_{lm}(\theta,\phi)}{r^{l+1}}\left[\int (r')^lY^*_{lm}(\theta',\phi')\rho(\mathbf{x}')d^3x'\right]
$

Define the term in square brackets as $q_{lm}$, which is a constant

$\displaystyle\Phi(\mathbf{x})=\frac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty \sum_{m=-l}^l\frac{4\pi}{2l+1}\frac{Y_{lm}(\theta,\phi)}{r^{l+1}}q_{lm}$

----

Comparison of dipole $l=1$ term:

Legendre:

$
\displaystyle
\Phi_{l=1}(r,\theta,\phi) = \frac{1}{4\pi\epsilon_0}\frac{1}{r^2}\int r'\big(\sin\theta\sin\theta'\cos(\phi-\phi') + \cos\theta\cos\theta'\big)
\times \rho(r',\theta',\phi')r'^2\sin\theta dr' d\theta' d\phi'
$

Spherical Harmonic:

$\displaystyle\Phi_{l=1} = \frac{1}{3\epsilon_o}\frac{Y_{lm}(\theta,\phi)}{r^{l+1}}\left[q^\*\_{11} + q_{10} + q_{11}\right]$

$\displaystyle q_{lm} = \int (r')^lY^*_{lm}(\theta',\phi')\rho(r',\theta',\phi')r'^2\sin\theta dr' d\theta' d\phi'$

To plot $\Phi$ for a grid of $(r,\theta,\phi)$ values, one integration is needed for each grid point for Legendre form. In the spherical harmonic form, three integrations are needed. Then for each grid point, only evaluation of $Y_{lm}(\theta,\phi)/r^{l+1}$ is needed.  

If only one value of $(r,\theta,\phi)$ is needed, 3x as many integrations needed for spherical harmonic form over Legendre form
