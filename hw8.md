# HW 8

## Long Polarized Cylinder

A long solid cylinder of radius $b$ is aligned with the $z$--axis and centered on the origin. The rod is polarized such that $\mathbf{P}=2P_o\sin^2\phi\thinspace\hat{\mathbf{s}}$.

Find

1. $\psi(s,\phi)$
2. $\mathbf{E}(s,\phi)$

due to the bound surface charges only. Assume the cylinder has $\chi_e=0$. 

## Dipole in a Dielectric Sphere

A perfect dipole $\mathbf{p}=p_o\hat{\mathbf{z}}$ at the origin is at the center of a dielectric sphere of radius $b$ that is centered on the origin. The dielectric constant of the sphere is $\epsilon$.

Find

1. $\psi(r,\theta)$
2. $\mathbf{D}(r,\theta)$

and

3. Explicitly compute $\oint \mathbf{D}\bfcdot d\mathbf{a}$ for a surface of an origin--centered sphere of radius $r\lt b$.

## Point Charge and Dielectric Sphere

An origin--centered dielectric sphere with radius $b$ has a susceptibility of $\chi_e$. A point charge is at $(x,y,z)=(0,0,z_o)$, where $z_o \gt b$.

Find the potential. Note that as $\chi_e\rightarrow \infty$, the solution should match that of a point charge outside of a conducting sphere.

Hints:

The potential will be due to the point charge and the bound charges induced on the sphere. You will need to consider three regions:

1. $r\lt b$
2. $b \lt r \lt z_o$
3. $r\gt z_o$

In region 3., the potential due to the point charge can be expressed as (from 3.38 of Jackson)

$$\psi_q = \frac{q}{4\pi\epsilon_o}\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{z_o^l}{r^{l+1}}P_l(\cos \theta)$$

In regions 1. and 2., the potential due to the point charge can be expressed as

$$\psi_q=\frac{q}{4\pi\epsilon_o}\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \frac{q}{4\pi\epsilon_o}\sum_{l=0}^\infty \frac{r^l}{z_o^{l+1}}P_l(\cos \theta)$$

In all three regions, the contribution from the induced bound charges must have the form

$$\psi_b(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

In region 1., the potential due to the bound charges will not have $B_l$ terms. In region 2. and 3., the potential due to the bound charges will not have $A_l$ terms.


