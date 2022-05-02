# Cylinder Boundary Value Problem 

A long cylinder of radius $s_o$ has a magnetization

$$
\mathbf{M}=(ps\sin 2\phi + qs\cos\phi)\hat{\mathbf s}
+
(ps\cos 2\phi-2qs\sin\phi)\hat{\boldsymbol{\phi}}
$$ 

where $s$ is the cylindrical radial coordinate and $p$ and $q$ are constants. Find $\mathbf{B}$ due to the cylinder.

**Partial Solution**

$$\mathbf{M}=(p\rho\sin 2\phi + q\rho\cos\phi)\hat{\boldsymbol{\rho}}+(p\rho\cos 2\phi-2q\rho\sin\phi)\hat{\boldsymbol{\phi}}$$ 

$$\boldsymbol{\nabla}\cdot\mathbf{M}=\frac{1}{s}\frac{\partial (sM_s)}{\partial s} + \frac{1}{s}\frac{\partial M_{\phi}}{\partial s}=0$$

1. $\psi_m$ finite for $r=0$
1. $\psi_m\rightarrow 0$ as $r\rightarrow\infty$
1. $\psi_m$ is continuous
1. $(\mathbf{B}_2-\mathbf{B_1})\boldsymbol{\cdot}\hat{\mathbf{n}}=0$

Start with 

$$\psi_i=As\cos\phi + Bs^2\sin2\phi\qquad\qquad \psi_o=as\cos\phi + bs^2\sin2\phi$$

**BC 3**

$$\psi_i(s_o,\phi)=\psi_o(s_o,\phi)$$

$$A=\frac{a}{s_o^2}\qquad\qquad B=\frac{b}{s_o^2}$$

**BC 4**

$$\mathbf{B} = \mu_o(\mathbf{H}+\mathbf{M})$$

$$\mathbf{B}_i = \mu_o(\mathbf{H}_i+\mathbf{M}_i) = \mu_o\left(-\frac{\partial \psi_i}{\partial s}+\mathbf{M}\right)$$

$$\mathbf{B}_o = \mu_o(\mathbf{H}_o+\mathbf{M}_o) = -\mu_o\frac{\partial \psi_o}{\partial s}$$

$$\mathbf{B}\_i\cdot\hat{\mathbf{n}}=\mu_o\left(-\frac{\partial \psi_i}{\partial s}\Bigg|_{s=s_o}+M_s(s_o,\phi)\right)$$

$$\mathbf{B}\_o\cdot\hat{\mathbf{n}}=-\mu_o\frac{\partial \psi_o}{\partial s}\Bigg|_{s=s_o}$$

$$(\mathbf{B}_o-\mathbf{B}_i)\boldsymbol{\cdot}\hat{\mathbf{n}}=0$$

$$\hat{\mathbf{n}}=\hat{\mathbf{s}}$$

$$-\frac{\partial \psi_o}{\partial s}\Bigg|\_{s=s_o}+\frac{\partial \psi_i}{\partial s}\Bigg|_{s=s_o}-M(s_o,\phi)=0$$

$$\frac{a}{s_o^2} + A = qs_o\qquad\qquad \frac{2b}{s_o^3} + 2Bs_o = ps_o$$

$$a = \frac{qs_o^3}{2}\qquad\qquad A = \frac{qs_o}{2}\qquad\qquad b = \frac{ps_o^4}{4}\qquad\qquad B = \frac{p}{4}$$

$$\psi_i=\frac{q}{2}ss_o\cos\phi+\frac{p}{4}s^2\sin 2\phi$$

$$\psi_o=\frac{q}{2}\frac{s_o^3}{s}\cos\phi+\frac{p}{4}\frac{s_o^4}{s^2}\sin 2\phi$$

An alternative method of solution uses direct integration of $\mathbf{K}_b$ and $\mathbf{J}_b$.

# Cylinder with uniform $\mathbf{M}$ 

A cylinder centered on the origin with radius $b$ and end caps in the $z=\pm L$ plane has a permanent magnetization $\mathbf{M}=M_o\hat{\mathbf{z}}$.

1. Find the approximate magnetic potential, $\psi_m(z)$, by assuming $z\pm L\gg b$ and approximating an integrand of an appropriate integral in Section 5.9C of Jackson as a power series in the cylindrical radial coordinate $s'$ prior to integrating;
1. Determine the exact $\psi_m(z)$; and
1. Determine the $\mathbf{H}$ and $\mathbf{B}$ at all points on $z$-axis of the using the exact <strike>cylinder</strike> $\psi_m(z)$.

**Solution**

----
_Note_

An alternative way of obtaining a solution is to note that 
    
$$\mathbf{K}_b=\mathbf{M}\times\hat{\mathbf{n}}=M_o\hat{\mathbf{z}}\times\hat{\mathbf{s}}=M_o\hat{\boldsymbol{\phi}}$$
    
$$\mathbf{J}_b=\boldsymbol{\nabla}\times\mathbf{M}=0$$

Therefore, the problem is equivalent to a solenoid with a finite length with a surface current of $K_{\phi}=2M_o/\mu_o$. The method of solution suggested here is intentionally more complex as it applies to a more general set of problems.

----

1\. The macroscopic Maxwell equations associated with the magnetic field are 

$$\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{B}=0\quad\text{and}\quad \boldsymbol{\nabla}\times\mathbf{H}=\mathbf{J}_f$$

where $\mathbf{J}_f$ is the free current (i.e., not bound current). Using the definition of the magnetization implied by $\mathbf{B}=\mu_o(\mathbf{H}+\mathbf{M})$ and $\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{B}=0$, the macroscopic equations can be written as

$$\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{H}=-\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{M}\quad\text{and}\quad \boldsymbol{\nabla}\times\mathbf{H}=\mathbf{J}_f$$

When $\mathbf{J}_f=0$, $\boldsymbol{\nabla}\times\mathbf{H}=0$ so one can write $\mathbf{H}$ as the gradient of a scalar function that will be called $\psi_m$: $\mathbf{H}=-\boldsymbol{\nabla}\psi_m$ and so

$$\nabla^2\psi_m=\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{M}$$

From this, it follows that

$$\psi_m=-\frac{1}{4\pi}\int\frac{\boldsymbol{\nabla}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

If $\mathbf{M}$ has a discontinuity on a surface $\mathcal{S}$ of the volume $\mathcal{V}$ such that it is zero outside of $\mathcal{V}$, this can be written as

$$\psi_m=-\frac{1}{4\pi}\int_V\frac{\boldsymbol{\nabla}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'+\frac{1}{4\pi}\oint_S\frac{\hat{\mathbf{n}}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da'$$

In this problem, the first form 

$$\psi_m=-\frac{1}{4\pi}\int\frac{\boldsymbol{\nabla}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

can be used if $\mathbf{M}$ is represented using the Heaviside step function $\Theta$:

$$\mathbf{M}=M_o\Theta(a-s)\Big[\Theta(z+L)-\Theta(z-L)\Big]\hat{\mathbf{z}}$$

so that

$$
\begin{align}
\boldsymbol{\nabla}\boldsymbol{\cdot}\mathbf{M}=&\frac{\partial}{\partial z}\left(M_o\Theta(a-s)\big[\Theta(z+L)-\Theta(z-L)\big]\right)\\
\\
=& M_o\Theta(a-s)\big[\delta(z+L)-\delta(z-L)\big]
\end{align}
$$

(Verify graphically that this makes sense by plotting $M$ as a function of $z$; for example when $z=L$, from the graph we expect the slope of $\frac{\partial M_z}{\partial z}$ to be $-\infty$.)

(This solution requires a few more steps than using the alternative form for $\psi_m$ but here I'll use this approach as a review of the $\Theta$ and $\delta$ functions.)

For points on the $z-$axis,

$\mathbf{x}=z\thinspace\hat{\mathbf{z}}$ and $\mathbf{x}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$

$$
\begin{align}
\psi_m & =-\frac{M_o}{4\pi}\int_0^{\infty}\int_0^{2\pi}\int_{-\infty}^{\infty}\frac{\Theta(a-s')\left(\delta(z+L)-\delta(z-L)\right)}{\sqrt{s'^2+(z-z')^2}}s'ds' d\phi' dz'\\
& =-\frac{M_o}{4\pi}\int_0^{a}\int_0^{2\pi}\int_{-\infty}^{\infty}\frac{\delta(z+L)-\delta(z-L)}{\sqrt{s'^2+(z-z')^2}}s'ds' d\phi' dz'\\
&=-\frac{M_o}{4\pi}\int_0^{a}\int_0^{2\pi}\left(\frac{1}{\sqrt{s'^2+(z+L)^2}}-\frac{1}{\sqrt{s'^2+(z-L)^2}}\right)s'ds' d\phi'\\
& =-\frac{M_o}{2}\int_0^{a}\left(\frac{1}{\sqrt{s'^2+(z+L)^2}}-\frac{1}{\sqrt{s'^2+(z-L)^2}}\right)s'ds'\\
& =-\frac{M_o}{2}\int_0^{a}\left(\frac{1}{|z+L|\sqrt{1+s'^2/(z+L)^2}}-\frac{1}{|z-L|\sqrt{1+s'^2/(z-L)^2}}\right)s'ds'
\end{align}
$$

Several students attempted to use the expansion of $1/|\mathbf{x}-\mathbf{x}'|$ with $r=z$ in terms of Legendre polynomials. This is a good idea, but there are several complications.

Complication A: One could use the last two equations on page 103 of Jackson to conclude that

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\sum_{l=0}^{\infty}\frac{c^l}{z^{l+1}}P_l(\cos\alpha)\qquad z\gt c$$

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\sum_{l=0}^{\infty}\frac{z^{l+1}}{c^l}P_l(\cos\alpha)\qquad z\lt c$$

where $\cos\alpha=L/\sqrt{s'^2+L^2}$ and $c=\sqrt{s'^2+L^2}$. To find the potential for a disk of charge, one needs to integrate from $s'=0$ to $s'=b$. This integration is complicated by the fact that the argument to the Legendre polynomials depends on $s'$. For this problem, there is a similar complication as one also needs to integrate from $s'=0$ to $s'=b$.

Complication B:  The expansions given above are for $z\gt c$ and $z\lt c$. So if you integrated these expansions, the result would be valid for $z\gt c_{max}$ and $z\lt c_{max}$, where $c^2_{max}=b^2+L^2$. However, the problem statement asks for the potential when $z\pm L\gg b$, which is not the same as either of these conditions. (To see this, draw out the regions where the solutions apply for $z\gt c_{max}$, $z\lt c_{max}$, and $z\pm L\gg b$). The region $z\pm L\gg b$ corresponds to a $z$ that is a large distance away from both caps. If $L$ is large compared to $b$, such a point could be the origin.

----

_Note_

The equation in the steps shown above that occurs after evaluation of the Heavyside step and Dirac delta functions is what would have been found if we had started with

$$\psi_m=-\frac{1}{4\pi}\int_{\mathcal{V}}\frac{\boldsymbol{\nabla}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'+\frac{1}{4\pi}\oint_{\mathcal{S}}\frac{\hat{\mathbf{n}}'\boldsymbol{\cdot}\mathbf{M}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da'$$
 
Inside $\mathcal{V}$, $\boldsymbol{\nabla}'\boldsymbol{\cdot}\mathbf{M}=0$, which leaves only the surface integral. The surface integral on the curved surface of the cylinder is zero because $\hat{\mathbf{s}}\boldsymbol{\cdot}\mathbf{M}$; the top and bottom caps of the cylinder only contribute and ($\mathbf{n}=\pm \hat{\mathbf{z}}$ on the top/bottom of the cylinder.

At least one student attempted to use the expansion of $1/|\mathbf{x}-\mathbf{x}'|$ for $r=z$ in terms of Legendre polynomials. This is a good idea, but there is a complication that one needs to address. The angle $\alpha$ is not $\theta$ and so $P_l(\cos\alpha$ will depend on $\phi$. This complication was discussed at length in my notes on this expansion. See the example for the offset charged ring given in section 3.3 of Jackson for how to handle this.

----

For $a^2/(z\pm L)^2\ll 1$ and using $(1+\Delta)^n\simeq 1+n\Delta$

$$
\begin{align}
\psi_m & \simeq -\frac{M_o}{2}\int_0^{a}\frac{s'ds'}{|z+L|}\left(1-\frac{s'^2}{2(z+L)^2}\right) + \frac{M_o}{2}\int_0^{a}\frac{s'ds'}{|z-L|}\left(1-\frac{s'^2}{2(z-L)^2}\right)\\\\
& = \frac{M_o}{2}\left[\frac{a^2}{2}\left(\frac{1}{|z-L|}-\frac{1}{|z+L|}\right)+\frac{a^4}{4}\left(\frac{1}{|z-L|^3}-\frac{1}{|z+L|^3}\right)\right]
\end{align}
$$

The absolute value signs are important here. If the condition was $a^2/(z\pm L)^2\lt 1$, it would mean that we are finding a solution that applies to all points on the $z$-axis except in a region of $\pm a$ above and below the ends of the cylinder. If $L\gg a$, the region where the solution is valid would include the origin and $z\gg L$ and these regions have a different functional for for the potential.

2.

The exact integral of

$$\psi_m=-\frac{M_o}{2}\int_0^{a}\left(\frac{1}{\sqrt{s'^2+(z+L)^2}}-\frac{1}{\sqrt{s'^2+(z-L)^2}}\right)s'ds'$$

is

$$\psi_m=\frac{M_o}{2}\left(\sqrt{a^2+(z-L)^2}-\sqrt{a^2+(z+L)^2}-|z-L|+|z+L|\right)$$

When the absolute values are accounted for, the potential function depends on if the point is inside or outside of the cylinder:

$$
\psi_m=\begin{cases}
\begin{array}{ll}
\frac{M_o}{2}\left(\sqrt{a^2+(z-L)^2}-\sqrt{a^2+(z+L)^2}+2z\right) & \mbox{if } |z| \le L \\
\frac{M_o}{2}\left(\sqrt{a^2+(z-L)^2}-\sqrt{a^2+(z+L)^2}+2L\right) & \mbox{if } |z| \ge L
\end{array}
\end{cases}
$$

To verify consistency with the approximate answer, factor out $z\pm L$ from the square root terms and use $(1+\Delta)^n\simeq 1+n\Delta$ with $\Delta = a/(z\pm L)$. (And be careful to use $\sqrt{u^2}=|u|$ when $u$ can be positive or negative!

$$
\begin{align}
\psi_m & = \frac{M_o}{2}\left(\sqrt{a^2+(z-L)^2}-\sqrt{a^2+(z+L)^2}-|z-L|+|z+L|\right)\\\\
& = \frac{M_o}{2}\left(|z-L|\sqrt{1+a^2/(z-L)^2}-|z+L|\sqrt{1+a^2/(z+L)^2}-|z-L|+|z+L|\right)\\\\
& \simeq \frac{M_o}{2}\frac{a^2}{2}\left(\frac{|z-L|}{(z-L)^2}-\frac{|z+L|}{(z+L)^2}\right)\\\\
& = \frac{M_oa^2}{4}\left(\frac{1}{|z-L|}-\frac{1}{|z+L|}\right)
\end{align}
$$

3.

Using

$$
\begin{align}
\mathbf{B}(z) & =\mu_o\mathbf{H}(z)+\mu_o\mathbf{M}(z)\\
& =-\mu_o\boldsymbol{\nabla}\psi_{m}+\mu_oM_o\big[\Theta(z+L)-\Theta(z-L)\big]\hat{\mathbf{z}}
\end{align}
$$

and

$$\boldsymbol{\nabla}\psi_{m}=\hat{\mathbf{z}}\frac{\partial \psi_m}{\partial z}$$

and recalling that $\partial |x|/\partial x=x/|x|$ gives

$$\frac{\partial \psi_m}{\partial z}=\frac{M_o}{2}\left(\frac{z-L}{\sqrt{a^2+(z-L)^2}}-\frac{z+L}{\sqrt{a^2+(z+L)^2}}-\frac{z-L}{|z-L|}+\frac{z+L}{|z+L|}\right)$$

(An alternative is to use the form of the solution given that applies inside and outside of the cylinder and then compute their derivatives separately to avoid needing to use $\partial |x|/\partial x=x/|x|$.)

The solution depends whether $z$ corresponds to inside or outside of the cylinder:

$|z|\ge L$
$$H_z=-\frac{\partial \psi_m}{\partial z}=-\frac{M_o}{2}\left(\frac{z-L}{\sqrt{a^2+(z-L)^2}}-\frac{z+L}{\sqrt{a^2+(z+L)^2}}\right)$$

$|z|\le L$
$$H_z=-\frac{\partial \psi_m}{\partial z}=-\frac{M_o}{2}\left(\frac{z-L}{\sqrt{a^2+(z-L)^2}}-\frac{z+L}{\sqrt{a^2+(z+L)^2}}+2\right)$$

This, along with the evaluation of the step function in the equation above for $\mathbf{B}(z)$ gives a single equation for the magnetic field

$$\mathbf{B}=\frac{\mu_oM_o}{2}\left[\frac{z+L}{\sqrt{a^2+(z+L)^2}}-\frac{z-L}{\sqrt{a^2+(z-L)^2}}\right]$$
    
So the system is equivalent to a solenoid of height $L$ and radius $a$, which is a standard example problem with a solution along the $z-$axis of

$$B_z=\frac{\mu_o K}{2}\left[\frac{z+L}{\sqrt{a^2+(z+L)^2}}-\frac{z-L}{\sqrt{a^2+(z-L)^2}}\right]$$

This observation also points to another way to check your answer. In the limit that $z\gg a \gg L$, the field should approach that from a magnetic dipole along its axis. In this limit, the cylinder looks like a ring, which has an axial field of

$$B_z=\frac{\mu_o Ia^2}{2}\frac{1}{(a^2+z^2)^{3/2}}$$
