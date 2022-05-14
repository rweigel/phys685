**Study Guide**

* Wednesday, May 11th from 4:30 – 7:10 pm in the regular classroom. 
* Approximately four problems
* The exam will cover concepts covered in the HW problems. 1-2 problems will cover topics covered on the mid--term and 1-2 problems will cover topics covered after the midterm. The problems won't require as much algebra, however. Make sure that you (1) understand the key steps and (2) can work out what the solution should look like. As discussed in class, (2) is important in general and also to help you determine if you've made an algebraic error.
* Don't fall into the trap of reading solutions and concluding that because the solution makes sense, you can solve the problem. Understanding someone else's solution is much easier than producing a solution on your own. After reading a solution, close your notes and attempt the problem on your own.
* If needed, I will give you
    * Legendre Polynomials
    * Green's 2nd identity (unless I ask you to derive)
    * the binomial expansion,
    * the non--cartesian Laplace's equation in 2-- and 3--D.
    * Equations for bound charge densities and bound currents.

    All other equations, including the general solution to Laplace's equation in 2--D in cartesian, cylindrical, and spherical, you'll need to know.

----

**PHYS 685 Final Exam**

!!! **Solve 3 of 4 problems** !!!

Wednesday, May 11th, 2022

2 hours and 40 minutes

**Equations**

$$
\mathbf{\nabla} f = 
{\partial f \over \partial r}\hat{\mathbf r}
+
{1 \over r}{\partial f \over \partial \theta}\hat{\boldsymbol \theta}
+
{1 \over r\sin\theta}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}
$$

$$
\boldsymbol{\nabla}\cdot\mathbf{U} = 
{1 \over r^2}{\partial \left( r^2 U_r \right) \over \partial r}
+
{1 \over r\sin\theta}{\partial \over \partial \theta} \left(  U_\theta\sin\theta \right)
+
{1 \over r\sin\theta}{\partial U_\phi \over \partial \phi}
$$

$\displaystyle
\boldsymbol{\nabla}\times \mathbf{U} =
{\frac {1}{r\sin \theta }}\left({\frac {\partial }{\partial \theta }}\left(U_{\phi }\sin \theta \right)
-
{\frac {\partial U_{\theta }}{\partial \phi }}\right) {\hat {\mathbf {r} }}
+
{\frac {1}{r}}\left({\frac {1}{\sin \theta }}{\frac {\partial U_{r}}{\partial \phi }}
-
{\frac {\partial }{\partial r}}\left(rU_{\phi }\right)\right) {\hat {\boldsymbol {\theta }}}
+
{\frac {1}{r}}\left({\frac {\partial }{\partial r}}\left(rU_{\theta }\right)
-
{\frac {\partial U_{r}}{\partial \theta }}\right) {\hat {\boldsymbol {\phi }}}$


$\displaystyle
\nabla^2f={ {1 \over r^{2}}{\partial  \over \partial r}\left(r^{2}{\partial f \over \partial r}\right)+{1 \over r^{2}\sin \theta }{\partial  \over \partial \theta }\left(\sin \theta {\partial f \over \partial \theta }\right)+{1 \over r^{2}\sin ^{2}\theta }{\partial ^{2}f \over \partial \phi ^{2}}}$$

$\mathbf{D}=\epsilon_o\mathbf{E}+\mathbf{P}$, $\sigma_b=\mathbf{P}\bfcdot \hat{\mathbf{n}}$,
$\rho_b=-\boldsymbol{\nabla}\bfcdot \mathbf{P}$

For linear material, $\mathbf{P}=\epsilon_o\chi_e\mathbf{E}$, $\epsilon\equiv\epsilon_o(1+\chi_e)$

$\mathbf{H}=\mathbf{B}/\mu_o-\mathbf{M}$, $\mathbf{K}_b=\mathbf{M}\times \hat{\mathbf{n}}$, $\mathbf{J}_b=\boldsymbol{\nabla}\times \mathbf{M}$, 

For linear material, $\mathbf{M}=\chi_m\mathbf{H}$, $\mu\equiv\mu_o(1+\chi_m)$

Power series expansions for $\delta \lt 1$.

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + \frac{n(n+1)}{2!}\delta^2- \frac{n(n+1)(n+2)}{3!}\delta^3+...$$

$$\ln(1+\delta)=\delta + \frac{\delta^2}{2} + \frac{\delta^3}{3} + ...$$

$$e^\delta = 1 + \frac{\delta}{1!} + \frac{\delta^2}{2!} + ...$$

Green's theorem (second identity)

$$\int_{\mathcal{V}} \left(\phi\nabla^2\psi -\psi\nabla^2\phi\right)d^3x=\oint_{\mathcal{S}}\left(\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}\right) da$$

# Parallel Plate Capacitor

A large parallel plate capacitor has a small hemispherical bulge on its grounded plate. The bulge has radius $b$ and bulges toward the second plate. The distance between the plates is $d$, $d\gg b$. The second plate is at potential $V_o$. A cross--section of the geometry is shown. Assume that the capacitor plates are infinite in extent.

<img width="53%" src="figures/capacitor_with_bulge.svg"/>

1. Find the potential everywhere inside the capacitor when $b=0$ (no bulge; ordinary parallel plate capacitor). Indicate the coordinate axes used on a diagram.
2. Find the potential everywhere inside the capacitor when $b \ne 0$.

**Answer**

1\. Origin is at center of bulge with $z$ vertically upwards.

$$\psi_o = V_o\frac{z}{d}=V_o\frac{r}{d}\cos\theta$$

2\.

Let the boundary be a volume between the plates with the sides far from the bulge and far from the plate ends. One the four sides, the potential must match the solution to 1\. At $z=d$, the potential must be $V_o$. 

Thus, a candidate solution is the answer from 1\. and additional terms that approach zero far from the bulge.

$$\psi = V_o\frac{r}{d}\cos\theta + \frac{B_0}{r}P_0 + \frac{B_1}{r^2}P_1+...$$

On the bulge, we require $\psi=0$, so

$$\psi(b,\theta)= 0 = V_o\frac{b}{d}\cos\theta + \frac{B_0}{b}P_0 + \frac{B_1}{b^2}P_1+...$$

For this to be satisfied, all $B_l$ must be zero except for $B_1=-V_ob^3/d$.

$$\psi(r,\theta) = V_o\cos\theta\left(\frac{r}{d}-\frac{b^3}{d}\frac{1}{r^2}\right) = \psi_o\left(1-\frac{b^2}{d^2}\frac{1}{r/b}\right)$$

(The latter form is to emphasize the parameter that determines the influence of the bulge is the dimensionless constant $b^2/d^2$ and the distance scale $r/b$, which is greater than 1.)

Normally we would need to explicilty address the non--bulge part of the plate ($\theta=\pi/2$ and $r\gt b$), but the found solution already satisifes $\psi=0$ on that boundary. The potential on the four sides is the solution to 1\., so the side boundary condition is also satisfied because there $r\gg b$.

This problem is electrically equivalent to a grounded sphere in a constant electric field. Probably it was created by noting that placing grounded conductors at the region of space where $\psi=0$ for the grounded sphere problem and a distant parallel plate at $V_o$ gives a problem that looks different but must have the same solution (from uniqueness). Another version of this problem is three parallel plates with the middle having a conducting bubble).

# Dipole in a Dielectric Sphere

A perfect dipole $\mathbf{p}=p_o\hat{\mathbf{z}}$ at the origin is at the center of a dielectric sphere of radius $b$ that is centered on the origin. The dielectric constant of the sphere is $\epsilon$.

Find the potential everywhere.

**Solution**

!!!!DRAFT!!!!

The problem has azimuthal symmetry and $\nabla^2\psi(r,\theta)=0$ for the inner ($i$) region ($r\lt b$) and outer ($o$) region ($r\gt b$). As a result, in each region the potential has the form

$$\psi=\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)+ \sum_{l=0}^{\infty}\frac{B_l}{r^{l+1}}P_l(\cos\theta)$$

To clarify notation, $\epsilon_i$ is used in place of $\epsilon$.

_Approach 1_

As $r/b\rightarrow 0$ the system appears as an infinite dielectric with two oppositely charged point charges near the origin.
A single point charge in a dielectric has a field and potential with $\epsilon_o$ replaced with $\epsilon$ and a dipole potential is the sum of the potential of two point charges, so a dipole in an infinite dielectric $\epsilon_i$ will have a potential of $ (p_o\cos\theta/4\pi\epsilon_i)(1/r^2)$.

Based on this, we expect that as $r/b\rightarrow 0$, $\psi^i \rightarrow (p_o\cos\theta/4\pi\epsilon_i)(1/r^2)$. From this it follows that $B_l=0$ for $l\ne 0$ and $B_1=p_o/4\pi\epsilon_i$ and so the inner potential should have the form

$$\psi^i=\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)+\frac{p_o}{4\pi\epsilon_i}\frac{\cos\theta}{r^2}$$

As $r/b\rightarrow \infty$, the potential must approach zero (assuming we choose, as usual, that the reference location is "$r=\infty$" and the reference potential is zero). As a result, the $A_l$ terms must all be zero, so the potential for $r\gt b$ must have the form

$$\psi^o=\sum_{l=0}^{\infty}\frac{B_l}{r^{l+1}}P_l(\cos\theta)+\frac{p_o}{4\pi\epsilon_o}\frac{\cos\theta}{r^2}$$

In the above, we have added a term that corresponds to the expected outer field when $b=0$. 

Continuity $\psi_i(b,\theta)=\psi_o(b,\theta)$ and use of $D_r^o(b,\theta)-D_r^i(b,\theta)=0$ with $\mathbf{E}=-\boldsymbol{\nabla}\psi$ and $\mathbf{D}=\epsilon\mathbf{E}$ and algebra will give a result that matches the result quoted in [HW 8.3](hw.html#dipole-in-a-dielectric-sphere), which was the result found by starting with no second term in $\psi^i$ and $\psi^o$:

$$
\psi(r,\theta)=
\begin{cases}
\displaystyle\frac{p_o\cos\theta}{4\pi\epsilon}\left(\frac{1}{r^2}+2\frac{\epsilon-\epsilon_o}{\epsilon+2\epsilon_o}\frac{r}{b^3}\right)
\qquad & r\le b
\\\\
\displaystyle\frac{p_o\cos\theta}{4\pi\epsilon}\frac{3\epsilon}{\epsilon+2\epsilon_o}\frac{1}{r^2}
\qquad &r\ge b
\end{cases}
$$

_Approach 2_

Following the approach taken in [HW 8.3](hw.html#dipole-in-a-dielectric-sphere), we assert that inside and outside the dielectric, there will be a contribution from the dipole of $({p_o}/{4\pi\epsilon_o})({\cos\theta}/{r^2})$, which is the field of the dipole in free space. 

Outside the dielectric, we have

$$\psi^o=\psi_P^o+\frac{p_o}{4\pi\epsilon_o}\frac{\cos\theta}{r^2}$$

For large $r$, $\psi_P^o$ must approach zero, so it will not have $A_l$ terms. So we can write

$$\psi^o=\sum_{l=0}^{\infty}\frac{B_l}{r^{l+1}}P_l(\cos\theta)+\frac{p_o}{4\pi\epsilon_o}\frac{\cos\theta}{r^2}$$

Inside, we have

$$\psi^i=\psi_P^i+\frac{p_o}{4\pi\epsilon_o}\frac{\cos\theta}{r^2}$$

It is very tempting to state that inside the dielectric, $\psi^i_P$ must be finite. In this case, it would not have $B_l$ terms. If one does this you will get a different answer from Approach 1. The reason is the embedded dipole, which has a potential that diverges at the origin, induces a bound charge distribution that diverges at the origin. To get the same answer as in Approach 1, we need to allow $\psi^i_P$ to have a $B_1/r^2$ term. This error would have been noticed upon using the $\epsilon\rightarrow \infty$ check suggeted in [HW 8.2](hw.html#dipole-in-a-dielectric-sphere).

Thus, we need to use

$$\psi^i=\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)+\frac{B_1}{r^2}\cos\theta+\frac{p_o}{4\pi\epsilon_o}\frac{\cos\theta}{r^2}$$

Starting $\psi^o$ given above and this $\psi^i$ will yield the same final result as in Approach 1.

_Approach 3_

The justification for the need of the $B_1/r^2$ terms in Approach 2 will be perhaps clearer if we modify the problem so that the dipole is in a free--space cavity of radius $\Delta$. This creates an additional region to address and more algebra, but one will see that the inner surface of the cavity produces a field of $\frac{p_o}{4\pi\epsilon_i}\frac{\cos\theta}{r^2}$ in the limit that $\Delta \rightarrow 0$.

_Approach 4_

Find the field for an off--center point charge $q$ at $z=\Delta$ in a dielectric. Do this by seeking a potential in three regions. Add this potential to the potential for $-q$ at $z=-\Delta$ and then take the limit as $\Delta \rightarrow 0$.

# Magnetizable Sphere in Uniform Field

An initially unmagnetized sphere of radius $b$ and permeability $\mu_i$ is placed is a region of free space (so a permeability of $\mu_o$) where there is an external magnetic field $B_{\text{ext}}\zhat$.

Assume that the scalar magnetic potential, $\psi_m$, will have the form, for $r\le b$

$$\psi^i_m(r,\theta)=A_1r\cos\theta\thickspace ,$$

and for $r \ge b$,

$$\psi^o_m(r,\theta)=-\frac{B_{\text{ext}}}{\mu_o}r\cos\theta+\frac{B_2}{r^2}\cos\theta\thinspace$$

1\. Find the unknown constants $A_1$ and $B_2$.

2\. Find $\mathbf{B}$ inside the sphere.

3\. Find the magnetization of the sphere.

**Answer**

!!!!DRAFT!!!!

1\.

Continuity of $\psi$ (which follows from the continuity of tangential component of $\mathbf{H}$) is:

$\psi_m^i(b,\theta)=\psi_m^o(b,\theta)$

(The units of the first term $\psi^o_m$ indicate that it a scalar potential for $\mathbf{H}$ and not $\mathbf{B}$. If one assumes the scalar potential was for $\mathbf{B}$, there will be a units problem and continuity in the form above; more importantly, continuity does not apply to a scalar potential for $\mathbf{B}$ because continuity is derived from the condition that the curl of $\mathbf{H}$, not $\mathbf{B}$, is zero. I never went over this in class, but units should have have ruled out the option that $\mathbf{B}=-\boldsymbol{\nabla}\psi_m$.)

This gives

$$A_1b\cos\theta=-\frac{B_\text{ext}}{\mu_o}b\cos\theta + \frac{B_2}{b^2}\cos\theta$$

from which it follows that

$$\boxed{A_1b=-\frac{B_\text{ext}}{\mu_o}b + \frac{B_2}{b^2}}$$

From $\mathbf{\nabla}\bfcdot\mathbf{B}=0$, it follows that at $r=b$

$(\mathbf{B}_o-\mathbf{B}_i)\bfcdot\hat{\mathbf{r}}=0$

or

$(\mu_o\mathbf{H}_o-\mu_i\mathbf{H}_i)\bfcdot\hat{\mathbf{r}}=0$

or

$$\left[\mu_o\frac{\partial \psi_o}{\partial r}-\frac{\partial \psi_o}{\partial r}\right]_{r=b} = 0$$

from which it follows that

$$\boxed{-B_\text{ext}-\mu_o\frac{2B_2}{b^3}=\mu_iA_1}$$

Using the two boxed equations above gives

$$A_1=-\frac{B_\text{ext}}{\mu_o}\frac{3}{\mu_i/\mu_o+2}$$

$$B_2=b^3\frac{B_\text{ext}}{\mu_o}\frac{\mu_i/\mu_o-1}{\mu_i/\mu_o+2}$$

We could find a scalar magnetic potential because $\boldsymbol{\nabla}\times \mathbf{H}=0$, so $\mathbf{H}=-\boldsymbol{\nabla}\psi_m$. Using $\mathbf{H}=\mathbf{B}/\mu$ gives

$\mathbf{B}=-\mu\boldsymbol{\nabla}\psi_m$

The gradient in spherical coordinates is

$$
\mathbf{\nabla} \psi_m = 
{\partial \psi_m \over \partial r}\hat{\mathbf r}
+
{1 \over r}{\partial \psi_m \over \partial \theta}\hat{\boldsymbol \theta}
+
{1 \over r\sin\theta}{\partial \psi_m \over \partial \phi}\hat{\boldsymbol \phi}
$$

Using $\psi_m^i$ gives

$\mathbf{B}^i=-\mu_i\boldsymbol{\nabla}\psi_m=-\mu_iA_1(\cos\theta\hat{\mathbf r}-\sin\theta\hat{\boldsymbol \theta})=\mu_iA_1\zhat$

$$\mathbf{B}^i=B_\text{ext}\frac{3\mu_i/\mu_o}{\mu_i/\mu_o+2}\zhat$$

For $\mu_i=\mu_o$, we get $\mathbf{B}^i=\mathbf{B}_\text{ext}$, as expected.

3\.

$$\mathbf{M}^i=\chi_m^i\mathbf{H}^i=\chi_m^i\frac{\mathbf{B}^i}{\mu_i}=\left(\frac{\mu_i}{\mu_o}-1\right)\frac{\mathbf{B}^i}{\mu_i}$$

For $\mu_i=\mu_o$, we get $\mathbf{M}^i=0$, as expected.

# Rotating Sphere

An origin--centered sphere with uniform surface charge density $\sigma$ and radius $b$ rotating around the $z$--axis with angular velocity $\omega$ results in a surface current of $\mathbf{K}=\omega b\sigma\sin\theta\hat{\boldsymbol{\phi}}$.

Use

$$\mathbf{A}(\mathbf{x})=\frac{\mu_o}{4\pi}\int \frac{\mathbf{K}(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}da'$$

and

$$\displaystyle\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*\_{lm}(\theta',\phi')Y\_{lm}(\theta,\phi)$$

and one or more of

$\displaystyle l=0\quad\quad \displaystyle Y_{00}(\theta,\phi)=\sqrt{1\over 4\pi}=\sqrt{1\over 4\pi}P_o(\cos\theta)$


$l=1
\quad 
\begin{cases}
\displaystyle Y_{11}(\theta,\phi)=-\sqrt{3\over 8\pi} \sin\theta e^{i\phi}\\ \\
\displaystyle Y_{10}(\theta,\phi)=\sqrt{3\over 4\pi} \cos\theta=\sqrt{3\over 4\pi} P_1(\cos\theta)\\ \\
\displaystyle Y_{1,-1}(\theta,\phi)=-Y_{11}^{*}(\theta,\phi)
\end{cases}
$

and

$$\int_0^{2\pi}d\phi\int_0^\pi\sin\theta d\theta Y^\*\_{l'm'}(\theta',\phi')Y_{lm}(\theta,\phi)=\delta_{ll'}\delta_{mm'}$$

to show that for $r \lt b$,

$$\mathbf{A}=\frac{\mu_o b \omega \sigma}{3} r\sin\theta \hat{\boldsymbol{\phi}}$$

**Partial Solution**

!!!!DRAFT!!!

_Key steps_

Let $K_o=\omega b\sigma$

Inside the sphere, $r_{\gt}=b$ and $r_{\lt}=r$.

$\mathbf{K}(\mathbf{x}')=K_o\sin\theta'\hat{\boldsymbol{\phi}}'=K_o\sin\theta'(-\sin\phi'\xhat+\cos\phi'\yhat)$

**Important**: $\hat{\boldsymbol{\phi}}$ depends on $\phi$! So when we switch to using primes for $\mathbf{K}$, we need to change everything in it that depends on $\phi$ to be primed. To emphasize this, I sometimes write non--cartesian unit vectors with primes as done above. See also 1.4.1 of Griffiths 4th Edition (search on "poisonous snake"; I know, snakes are venomous.) I know I mentioned this repeatedly in class. In the future, I may make a song about it to see if that prevents people from making this too--common mistake.

Integration will be easier if we use Euler's identity and the given table above to re--write $\mathbf{K}$ in terms of spherical harmonics. (We did a similar thing in problems where the potential on a sphere or the charge density on a sphere was not written in terms of the Legendre polynomials. It is easier if they are re--writen in terms of the Legendre polynomials.)

$$\sin\theta'\sin\phi'=\frac{Y_{1,-1}(\theta',\phi')+Y_{1,1}(\theta',\phi')}{-2i\sqrt{3/8\pi}}$$

$$\sin\theta'\cos\phi'=\frac{Y_{1,-1}(\theta',\phi')-Y_{1,1}(\theta',\phi')}{2\sqrt{3/8\pi}}$$

so that the orthogonality equation can be used.

$$da'=b^2\sin\theta'd\theta' d\phi'$$

The above with orthogonality will give

$$A_x=\frac{\mu_o}{4\pi}\frac{Y_{1,-1}(\theta,\phi)+Y_{1,1}(\theta,\phi)}{-2i\sqrt{3/8\pi}}\frac{4\pi}{3}r$$

which simplifies to

$$A_x=-\frac{\mu_oK_o}{3}r\sin\theta\sin\phi$$

Similar steps lead to 

$$A_y=\frac{\mu_oK_o}{3}r\sin\theta\cos\phi$$

Using again $\hat{\boldsymbol{\phi}}=-\sin\phi\xhat+\cos\phi\yhat$

gives

$$\mathbf{A}=\frac{\mu_oK_o}{3} r\sin\theta \hat{\boldsymbol{\phi}}$$

