# HW 7

## Monopole Expansion

### 

A point charge $q$ is at $(x,y,z)=(0,y',0)$

1. Starting with

    $\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$ 

    find the potential $\psi(r,\theta,\phi)$ for $r\gt |y'|$ to order $1/r^3$

2. Starting with

    $\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$

    find the potential $\psi(r,\theta,\phi)$ for $r\gt |y'|$ to order $1/r^2$

3. Show that your answers for 1. and 2. are equal

**Solution**

1\. There are many ways of writing $\cos\gamma$. In the following, I emphasis the dependence of $\gamma$ on $\mathbf{x}$ and $\mathbf{x}'$ by writing $\gamma(\mathbf{x},\mathbf{x}')$.

$$\cos(\gamma(\mathbf{x},\mathbf{x}')) =\frac{\mathbf{x}\cdot\mathbf{x}'}{|\mathbf{x}| |\mathbf{x'}|} = \frac{xx'+yy'+zz'}{rr'}$$

In this problem, $x'=z'=0$ and so $r'=y'$, leaving

$$\cos(\gamma) = \frac{y}{r}=\sin\theta\sin\phi$$

Here we have $r \gt |y'|$, so $r_{\gt}=r$ and $r_{\lt}=r'=y'$ and so

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{y'^l}{r^{l+1}}P_l(\cos \gamma)$

To order $1/r^3$, this is

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{1}{r} + \frac{y'}{r^2}\sin\theta\sin\phi +\frac{1}{2}\frac{y'^2}{r^3}\left(3\sin^2\theta\sin^2\phi-1\right)$$

2\. We need to evaluate the $l=0$ and $l=1$ terms of

$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{y'^{l}}{r^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$


$l=0$

$$\frac{4\pi}{2\cdot 0 + 1}\frac{1}{r}Y^*\_{00}(\theta',\phi')Y_{00}(\theta,\phi)=\frac{1}{r}$$

Where $Y_{00}(\theta,\phi)=\sqrt{1\over 4\pi}$ was used

$l=1$

$$\frac{4\pi}{2\cdot 1 + 1}\frac{y'}{r^2}
\left[
Y^*\_{1,-1}(\theta',\phi')Y_{1,-1}(\theta,\phi) + Y^*\_{1,0}(\theta',\phi')Y_{1,0}(\theta,\phi) +
Y^*\_{1,1}(\theta',\phi')Y_{1,1}(\theta,\phi)
\right]$$

From a table,

$$Y_{11}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{i\phi},$$

$$Y_{10}(\theta,\phi)=\sqrt{3\over 4\pi} \cos\theta,\text{ and}$$

$$Y_{1,-1}(\theta,\phi)=Y_{11}^{*}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{-i\phi}$$

Note that the potential must not be imaginary, so the algebra must be such that $i$ is not in the solution. Here we have $\theta'=\pi/2$, so $Y^*_{10}(\theta',\phi')=\sqrt{3\over 4\pi} \cos\theta'=0$, leaving

$$\frac{4\pi}{3}\frac{y'}{r^2}
\left[
Y^*\_{1,-1}(\theta',\phi')Y_{1,-1}(\theta,\phi) + 
Y^*\_{1,1}(\theta',\phi')Y_{1,1}(\theta,\phi)
\right]$$

Substitution of equation from the table gives

$$\frac{4\pi}{3}\frac{y'}{r^2}
\left[
\frac{3}{8\pi}\sin\theta'\sin\theta e^{i(\phi-\phi')} + 
\frac{3}{8\pi}\sin\theta'\sin\theta e^{-i(\phi-\phi')}
\right]$$

Using $\theta'=\pi/2$ and $\phi'=\pi/2$ gives

$$\frac{y'}{2}\frac{\sin\theta}{r^2}
\left[
ie^{i\phi} - ie^{-i\phi}
\right]$$

Using the Euler identity for complex exponentials gives

$$\frac{y'}{r^2}\sin\theta\sin\phi$$

The sum of the $l=0$ and $l=1$ terms are thus

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{1}{r} + \frac{y'}{r^2}\sin\theta\sin\phi$$

This could also be written in cartesian coordinates (with $r=$ as

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{1}{r} + \frac{y'y}{r^3}=\frac{1}{\sqrt{x^2+y^2+z^2}}\left(1 + \frac{yy'}{x^2+y^2+z^2}\right)$$


3\. Not applicable b/c the answer to 2. was simplified so it matches by inspection.

_Checks_:

1. If $y'=0$, we get $1/r$, as expected.
2. Symmetry with respect to $x\rightarrow -x$ and $z\rightarrow -z$.



###

A straight line of charge with uniform charge density $\lambda$ extends from $y=-L$ to $y=L$.

1. Starting with

    $\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$

    find the potential $\psi(r,\theta,\phi)$ for $r\gt |y'|$ to order $1/r^3$

2. Starting with

    $\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$

    find the potential $\psi(r,\theta,\phi)$ for $r\gt |y'|$ to order $1/r^2$

3. Use either 1. or 2. to find $\psi(x,y,z)$ for $r\gt |y'|$ to order $1/r^2$.

**Solution**

1\.

$$\psi=\frac{1}{4\pi\epsilon_o}\int_{-L}^{L} \frac{\lambda dy'}{|\mathbf{x}-\mathbf{x}'|}=
\frac{\lambda}{4\pi\epsilon_o}\int_{-L}^{L}dy'\sum_{l=0}^\infty \frac{y'^l}{r^{l+1}}P_l(\cos \gamma)$$

$$\phantom{\psi}=
\frac{\lambda}{4\pi\epsilon_o}\int_{-L}^{L}dy'\left[\frac{1}{r} + \frac{y'}{r^2}P_1(\cos\gamma)+\frac{y'^2}{r^3}P_2(\cos\gamma)+...\right]$$

$\cos\gamma=\sin\theta\sin\phi$ as in the point charge case (all differential charges are on the $y$--axis) and so it can be factored out of the integral (in general, this term cannot be factored out, however; recall that in general $\gamma=\gamma(\mathbf{x},\mathbf{x}')$). Also, $r$ does not depend on $y'$, so it can be factored out of the integral. Thus,

$$\psi=
\frac{\lambda}{4\pi\epsilon_o}\left[\frac{1}{r}\int_{-L}^{L}dy' +
\frac{P_1(\cos\gamma)}{r^2}\int_{-L}^{L}dy'y'
+
\frac{P_2(\cos\gamma)}{r^3}\int_{-L}^{L}dy'y'^2
+...\right]$$

Note that the 2nd, 4th, ... integrals are zero because their integrands are an odd function on the integration interval. This leaves

$$\psi=
\frac{\lambda}{4\pi\epsilon_o}\left[\frac{1}{r}\int_{-L}^{L}dy' +
\frac{P_2(\cos\gamma)}{r^3}\int_{-L}^{L}dy'y'^2
+...\right]$$

2\. 

$$\psi=\frac{1}{4\pi\epsilon_o}\int_{-L}^{L} \frac{\lambda dy'}{|\mathbf{x}-\mathbf{x}'|}=
\frac{\lambda}{4\pi\epsilon_o}\int_{-L}^{L}dy'\sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{y'^{l}}{r^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$$

Factoring out all terms that do not depend on primed variables gives

$$\psi=
\frac{\lambda}{\epsilon_o}\sum_{l=0}^\infty \frac{1}{2l+1}\sum_{m=-l}^l Y\_{lm}(\theta,\phi)\frac{1}{r^{l+1}}\int_{-L}^{L}dy'y'^lY^*\_{lm}(\theta',\phi')$$

$\theta'$ and $\phi'$ do not depend on $y'$ because $\theta'=\phi'=\pi/2$ for all differential charges on the line, so $Y^*\_{lm}(\theta',\phi')$ can also be factored out

$$\psi=
\frac{\lambda}{\epsilon_o}\sum_{l=0}^\infty \frac{1}{2l+1}\sum_{m=-l}^l Y\_{lm}(\theta,\phi)Y^*\_{lm}(\pi/2,\pi/2)\frac{1}{r^{l+1}}\int_{-L}^{L}dy'y'^l$$

Using the algebra from the point charge expressed using spherical harmonics will given the same result as in 1\.

3\. 

$$\psi=
\frac{\lambda}{4\pi\epsilon_o}\left[\frac{1}{r}\int_{-L}^{L}dy' +
\frac{P_1(\cos\gamma)}{r^2}\int_{-L}^{L}dy'y'
+
...\right]$$

Using $P_1(\cos\gamma)=\cos\gamma$ and $\cos\gamma=\sin\theta\sin\phi=y/r$ gives

$$\psi=
\frac{\lambda}{4\pi\epsilon_o}\frac{2L}{\sqrt{x^2+y^2+z^2}}$$

The net charge on the line is $2L\lambda$ and so this leading order term is as expected. There is no "dipole" term ($1/r^2$) because the charge distribution is symmetric about the origin (see 3.4.2 of Griffiths, which give an alternative equation for the dipole term in terms of the dipole moment expressed as an integral).

## Polarized Obect

A cylinder of radius $b$ and height $2h$ is centered on the origin, has a centerline aligned with the $z$--axis, and has a "frozen--in" polarization of $\mathbf{P}=P_o\zhat$.

1. Compute $\sigma_b$ and $\rho_b$
2. Find the potential $\psi(z)$ on on the $z$--axis for $z\gt \sqrt{b^2+h^2}$
3. Find the potential $\psi(r,\theta)$ to order $1/r^4$ for $z\gt \sqrt{b^2+h^2}$.

**Solution**

1\. The bound charge associated with with polarization is $\sigma_b=\pm P_o$ on the top/bottom caps of the cylinder and $\rho_b=0$. As a result, the electric field produced by this $\mathbf{P}$ is the same as the electric field produced by two disks with $\sigma=\pm P_o$ for which several methods are available for computing $\psi$.

2\. The potential for a disk in the $x$--$y$ plane and centered on the origin is

$$V = \frac{\sigma}{2\epsilon_o}\left(\sqrt{b^2+z^2}-|z|\right)$$

(the derivation is treated in intro physics textbooks). As a check, for $|z|\gg b$, the leading term is $(\pi b^2\sigma/4\pi\epsilon_o)(|z|/z^2)$ and for $|z|\ll b$, the first--order term in the electric field is $(\sigma/2\epsilon_o)|z|/z$ (the potential in this limit is $(\sigma b/2\epsilon_o)(1-|z|/b)$).

The potential for the given case is found by replacing $z$ with $z-h$ for the top cap and $z+h$ for the bottom cap and using $\sigma=P_o$ for the top cap and $\sigma=-P_o$ for the bottom cap, so that

$$\psi(z) = \psi_+ + \psi_-$$

$$\phantom{\psi(z)} = \frac{P_o}{2\epsilon_o}\left(\sqrt{b^2+(z-h)^2}-|z-h|+\sqrt{b^2+(z+h)^2}+|z+h|)\right)$$

3\. This problem has azimuthal symmetry and so $\psi(r,\theta)$ can be found for small $b/z$ by first expresing $\psi(z)$ as a power series expansion in $1/z$. Factoring out $z$ gives

$$\psi(z) = \frac{P_o|z|}{2\epsilon_o}\left(\frac{2h}{z}+\sqrt{1+\delta_+}-\sqrt{1+\delta_-})\right)$$

where

$\displaystyle\delta_+\equiv \frac{c^2}{z^2}-\frac{2h}{z}\qquad \displaystyle \delta_-\equiv \frac{c^2}{z^2}+\frac{2h}{z}\quad$ and $\quad c^2\equiv b^2+h^2$.

There is a significant amound of algebra involed in obtaining a power series expansion. WolframAlpha [gives](https://www.wolframalpha.com/input?i2d=true&i=expand+2Divide%5Bh%2Cx%5D+%2Bsqrt%5C%2840%291%2BDivide%5BPower%5Bb%2C2%5D%2BPower%5Bh%2C2%5D%2CPower%5Bx%2C2%5D%5D-2Divide%5Bh%2Cx%5D%5C%2841%29+-+sqrt%5C%2840%291%2BDivide%5BPower%5Bb%2C2%5D%2BPower%5Bh%2C2%5D%2CPower%5Bx%2C2%5D%5D%2B2Divide%5Bh%2Cx%5D%5C%2841%29)

$$\psi(z)= \frac{P_o|z|}{2\epsilon_o}\left(\frac{b^2h}{z^3}+\frac{b^2h^3-3b^4h/4}{z^5}+...\right)$$

For $z\gt 0$, this is

$$\psi(z)= \frac{P_o}{2\epsilon_o}\left(\frac{b^2h}{z^2}+\frac{b^2h^3-3b^4h/4}{z^4}+...\right)$$

and so to order $1/r^4$, 

$$\psi(r,\theta) = \frac{P_o}{2\epsilon_o}\left(\frac{b^2h}{r^2}P_1(\cos\theta)+\frac{b^2h^3-3b^4h/4}{r^4}P_3(\cos\theta)\right)$$

----

One issue not addressed is for what $z$ (or $r$) this applies to. The expansion of $\sqrt{1+\delta_+}$ requires $\delta_+ \lt 1$, corresponding to $z \gt h + b$ and $z \lt h-b$. However, I asked for a solution valid for $z\gt \sqrt{h^2+b^2}$, which is less than $h+b$. The solution above actually valid for  $z\gt \sqrt{h^2+b^2}$ even though this does not follow from the arguments made for deriving it. A similar issue arises in 3.4.1 of Griffiths where he derives the monopole expansion. In that derivation the parameter $\epsilon$ must be less than one and the resulting equation is actually valid for $r'>r$ even though the $\epsilon = (r'/r)(r'/r-2\cos\alpha)$, where $\alpha$ can vary between $0$ and $2\pi$.

One argument that can be made for the validity of the solution given above for $z\gt \sqrt{h^2+b^2}$ instead of only $z \gt h + b$ is as follows. We know for a charge at $r'$, the solution can be expressed by an expansion of $1/|\mathbf{x}-\mathbf{x}'|$ as a sum of $C_lr'^l/r^{l+1}P_l$ terms, where $C_l$ is a constant, which is valid for $r>r'$. In the given problem, all of the charges are at $r\le \sqrt{h^2+b^2}$ and so we expect that such a solution exists. However, we found a solution in this form, and by uniqueness, it must be the only solution.

An alternative way of showing this is to use the equation for the potential of a ring centered on the origin and offset from the $x$--$y$ plane, which is given on page 104 of Jackson: 

$$\Phi(r,\theta)=\frac{q}{4\pi\epsilon_o}\sum \frac{c^l}{r^{l+1}}P_l(\cos\alpha)P_l(\cos\theta)$$

where, using the variables in this problem, $c=\sqrt{h^2+b^2}$ and $\cos\alpha=h/c$. This equation is valid for $r\gt c$ (that is, for $r \gt \sqrt{h^2+b^2}$), which was asked for in the problem statement. To find the potential for the positively charged disk, we need to integrate rings. This is done by replacing $q$ with $P_o s ds d\phi$ and $b$ in $c$ and $\cos\alpha$ with $s$. With this, we need to evaluate

$$\psi_+(r,\theta)=\frac{P_o}{2\epsilon_o}\sum_{l=0}^\infty\frac{P_l(\cos\theta)}{r^{l+1}}\int_0^b(\sqrt{h^2+s^2})^lP_l\left(\frac{h}{\sqrt{h^2+s^2}}\right)sds$$

When this is added to the potential for the negatively charged disk, the $l=0, 2, ...$ terms cancel leaving

$$\psi(r,\theta)=\frac{P_o}{\epsilon_o}\sum_{l=1,3,...}^\infty\frac{P_l(\cos\theta)}{r^{l+1}}\int_0^b(\sqrt{h^2+s^2})^lP_l\left(\frac{h}{\sqrt{h^2+s^2}}\right)sds$$

For both the $l=1$ and $l=3$ terms, the integral is straightforward and the result is the same found earlier.

## Dielectric

###

A point charge $q$ is at the origin. A thick dielectric shell with susceptibility $\chi_e$ with inner radius $b$ and outer radius $c$ is centered on the origin.

<img src="figures/dielectric.svg"/>

Find $\psi(r)$ using at least two different methods.

###

A conducting shell of radius $b$ has a potential of $\psi(b)$, where $\psi(b)$ is the potential found in part 1. A conducting shell of radius $2c$ is at potential $\psi(2c)$, where $\psi(2c)$ is the potential found in part 1. A thick dielectric shell with susceptibility $\chi_e$ with inner radius $b$ and outer radius $c$ is between the two conductors.

<img src="figures/dielectric2.svg"/>

1. Starting with $\psi_i = A_i + B_i/r$ and $\psi_o = A_o + B_o/r$, use the boundary conditions, continuity, and the jump condition to find the potential in the region between the two conductors.
2. Use your answer to 1. to find the electric field between the two conductors.