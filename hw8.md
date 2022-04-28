# HW 8

## Long Polarized Cylinder

A long solid cylinder of radius $b$ is aligned with the $z$--axis and centered on the origin. The rod is polarized such that $\mathbf{P}=2P_o\sin^2\phi\thinspace\hat{\mathbf{s}}$.

Find

1. $\psi(s,\phi)$
2. $\mathbf{E}(s,\phi)$

due to the bound surface charges only. Assume the cylinder has $\chi_e=0$. 

**Solution**

1\. See [HW 5.3](#2-d-cylindrical-boundary-value-problem). Steps are similar.

Note that the bound charge is

$$
\rho_b = -\boldsymbol{\nabla}\cdot\mathbf{P} = - {1 \over s}{\partial \left( s P_s  \right) \over \partial s} = -\frac{2P_o}{s}\cos\phi\sin\phi=-{P_o \over s}\sin 2\phi
$$

To find the contribution from the bound charge, one could find the potentials $\psi(s\gt s')$ and $\psi(s\lt s')$ due to a shell with density $\sigma'=-P_o\sin 2\phi/s'$. The potential at $s$ is then the sum of the potentials due to differential shells from $0$ to $s$ and $s$ to $b$.

## Dipole in a Dielectric Sphere

A perfect dipole $\mathbf{p}=p_o\hat{\mathbf{z}}$ at the origin is at the center of a dielectric sphere of radius $b$ that is centered on the origin. The dielectric constant of the sphere is $\epsilon$.

Find

1. $\psi(r,\theta)$
2. $\mathbf{D}(r,\theta)$

and

3. Explicitly compute $\oint \mathbf{D}\bfcdot d\mathbf{a}$ for a surface of an origin--centered sphere of radius $r\lt b$.

**Solution**

1.

$$
\psi(r,\theta)=
\begin{cases}
\displaystyle\frac{p_o\cos\theta}{4\pi\epsilon}\left(\frac{1}{r^2}+2\frac{\epsilon-\epsilon_o}{\epsilon+2\epsilon_o}\frac{r}{b^3}\right)
\qquad & r\le b
\\\\
\displaystyle\frac{p_o\cos\theta}{4\pi\epsilon}\frac{3}{\epsilon+2\epsilon_o}\frac{1}{r^2}
\qquad &r\ge b
\end{cases}
$$

Checks: When $\epsilon=\epsilon_o$, we have simply a dipole in free space and $\psi(r,\theta)=\mathbf{p}\bfcdot\hat{\mathbf{r}}/(4\pi\epsilon_or^2)$. 

If $\chi_e$ is large (so $\epsilon$ is large), the dielectric becomes like a conductor. In this case, the electric field can be made to be zero if positive charges cluster in shell of vanishing radius around the negative charges in the dipole and if negative charges cluster around the positive charge in the dipole. In the limit that $\chi_e$ is large, $\psi(r,\theta)\rightarrow 0$, which is consistent with this.

It would be useful to compute $\rho_b$ to verify that it is consistent with the stated distribution of charges for large $\chi_e$. There are two ways to do this: (1) Compute $-\boldsymbol{\nabla}\bfcdot \mathbf{P}=\epsilon_o\chi_e \nabla^2\psi$. We expect that $\rho_b$ should be proportional to $\delta(\mathbf{r}-d/2\zhat) - \delta(\mathbf{r}+d/2\zhat)$ in the limit that $d\rightarrow 0$. Showing this takes a bit of delta function manupulation. Alternatively, (2), we could re--do the problem using point charges $\pm q$ at $\pm d$. In this case, we will have more terms in $\psi(r,\theta)$, but will be able to more clearly identify $\delta(\mathbf{r}-d/2\zhat)$ and $\delta(\mathbf{r}+d/2\zhat)$ when computing $\nabla^2\psi$.

%That is, for $r\lt b$, start by assuming a solution of $\psi_+ + \psi_- + \chi_e\psi_+ + \chi_e\psi_-$ added to the general solution to Laplace's equation with only $r^l$ terms, where $\psi_+$ and $\psi_-$ are the free-space solutions

%2\. 

%Using $\mathbf{D}=\epsilon\mathbf{E}$ gives

## Point Charge and Dielectric Sphere

An origin--centered dielectric sphere with radius $b$ has a susceptibility of $\chi_e$. A point charge is at $(x,y,z)=(0,0,z_o)$, where $z_o \gt b$.

Find the potential. Note that as $\chi_e\rightarrow \infty$, the solution should match that of a point charge outside of a conducting sphere.

Hints:

The potential will be due to the point charge and the bound charges induced on the sphere. You will need to consider three regions:

* Inner $r\lt b$
* Middle $b \lt r \lt z_o$
* Outer $r\gt z_o$

In the outer region, the potential due to the point charge can be expressed (from 3.38 of Jackson) as

$$\psi_q(r\gt z_o) = \frac{q}{4\pi\epsilon_o}\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{z_o^l}{r^{l+1}}P_l(\cos \theta)$$

In the inner and middle region, the potential due to the point charge can be expressed as

$$\psi_q(r\lt z_o)=\frac{q}{4\pi\epsilon_o}\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l}{z_o^{l+1}}P_l(\cos \theta)$$

In all three regions, the contribution from the induced bound charges must have the form

$$\psi_b(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

In the inner region, the potential due to the bound charges will not have $B_l$ terms. In the middle and outer region, the potential due to the bound charges will not have $A_l$ terms.

**Solution**

One could start with

$$\psi_i(r,\theta)=\sum_{l=0}^{\infty}A^i_lr^lP_l(\cos\theta)$$

$$\psi_m(r,\theta)=\sum_{l=0}^{\infty}\left(A^m_lr^l + B^m_lr^{-l-1}\right)P_l(\cos\theta)$$

$$\psi_o(r,\theta)=\sum_{l=0}^{\infty}B^o_lr^{-l-1}P_l(\cos\theta)$$

for the inner ($i$), middle ($m$), and outer ($o$) regions and the conditions

$
\psi_i(b,\theta)=\psi_m(b,\theta)
\qquad
\psi_m(z_o,\theta)=\psi_o(z_o,\theta)
$

$
\mathbf{D}_i(b,\theta)-\mathbf{D}_m(b,\theta)=0
\qquad
\mathbf{D}_m(z_o,\theta)-\mathbf{D}_o(z_o,\theta)=\sigma'
$

where $\sigma'=q\delta(\theta)/(2\pi z_o^2\sin\theta)$. In this case, we need to find $A^i_l$, $A^m_l$, $B_l^m$, and $B_l^o$.

Using the hint, we one start with

$$\psi_i(r,\theta) =
\psi_q(r\lt z_o)
+
\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)$$

$$\psi_m(r,\theta)=
\psi_q(r\lt z_o)+
\sum_{l=0}^{\infty}B^m_lr^{-l-1}P_l(\cos\theta)
$$

$$
\psi_o(r,\theta) =
\psi_q(r\gt z_o)
+
\sum_{l=0}^{\infty}B^o_lr^{-l-1}P_l(\cos\theta)
$$

Where now we need to find $A_l$, $B_l^m$, and $B_l^o$. In the middle region and outer region, the contribution from the dielectric must be the same and so we can conclude $B_l^m=B_l^o$.

Therefore, we only need to find $A_l$ and $B_l$ in

$$\psi_i(r,\theta) =
\frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l}{z_o^{l+1}}P_l(\cos \theta)
+
\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)
$$

$$\psi_m(r,\theta)=
\frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l}{z_o^{l+1}}P_l(\cos \theta)
+
\sum_{l=0}^{\infty}B_lr^{-l-1}P_l(\cos\theta)
$$

$$
\psi_o(r,\theta) =
\frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{z_o^l}{r^{l+1}}P_l(\cos \theta)
+
\sum_{l=0}^{\infty}B_lr^{-l-1}P_l(\cos\theta)
$$

$A_l$ and $B_l$ can be found using $\psi_i(b,\theta)=\psi_m(b,\theta)$ and $\mathbf{D}_i(b,\theta)-\mathbf{D}_m(b,\theta)=0$. The arguments provided obviate the need to use the boundary conditions at $r=z_o$ because they were implicitly used in simplifying the set of equations to be solved.
