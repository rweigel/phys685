# Gauss' Law 

## Lecture Follow-Up Questions 

An uncharged conducting sphere of radius $2b$ is centered on the origin and has a spherical cavity of radius $b$ that is also centered on the origin.

1. If a charge of $+q$ is at the origin, explain why the surfaces at $r=2b$ and $r=b$ each have a net charge of $+q$ and $-q$, respectively, and not, say, $+q/2$ and $-q/2$.
1. Repeat this question for the case where the inner surface of the cavity is not spherical (but the charge at the origin is still in a cavity)

**Solution**

Several students used the justification of "E is zero inside a conductor". This is not a full justification. If someone said "$+q/2$ and $-q/2$ give E of zero inside the conductor", your proof that this statement is wrong would require using Gauss' law.

1.

Gauss' law using a sphere of radius $b\lt r\lt 2b$:

$$\oint \mathbf{E}\cdot d\mathbf{a} = \frac{Q_{encl}}{\epsilon_o} = \frac{q + q_{r=b}}{\epsilon_o}$$

LHS is zero because field is zero inside conductor. So $q_{r=b}=-q$.

2. 

Same approach but the surface is not a sphere but rather a surface that is always inside conductor; $q_{r=b}=-q$.

## Infinite Line of Charge 

In general, in cylindrical coordinates, the electric field has the form

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

where $s$ is the radial coordinate in cylindrical coordinates.

Consider an infinite line of charge with a uniform charge per unit length of $\lambda_o$ on the $z$-axis. The typical approach to finding that the equation for the electric field is

$$\mathbf{E}(s)=\frac{\lambda_o}{2\pi\epsilon_o}\frac{\hat{\mathbf{s}}}{s}$$

is to use a cylindrical Gaussian surface and Gauss' law. When using Gauss' law, one must make arguments for why

1. $E_s$ does not depend on $\phi$ and $z$

2. $E_z=0$

With these two justifications and Gauss' law, one arrives at only an equation for the radial component of the electric field, $E_s$. To complete the solution, one also needs to provide an argument for why 

3. $E_{\phi}=0$.

Derive the equation given above for the electric field using Gauss' law and explicitly state arguments for 1.-3.

**Solution**

I gave this problem because I have come to realize that students can use Gauss' law to find the electric field, but can't often answer conceptual questions about justifications for the steps needed to get the solution. The problem is that most textbooks don't emphasize the arguments or provide follow-up questions to test their understanding of the arguments and so students don't think too deeply about them.

Understanding the reasoning for this problem is critical for understanding the boundary condition equations

$$(\mathbf{E}\_2-\mathbf{E}\_1)\cdot \hat{\mathbf{n}} = \mathbf{E}\_{2\perp}-\mathbf{E}\_{1\perp} = \left[-\frac{\partial \Psi_2}{\partial n}+\frac{\partial \Psi_1}{\partial n}\right]_{n=0}=\frac{\sigma}{\epsilon_o}$$

$$\mathbf{E}\_{2\parallel}-\mathbf{E}\_{2\parallel}=(\mathbf{E}\_2-\mathbf{E}\_1)\cdot \hat{\mathbf{t}}=0$$

where $n$ is the coordinate that is perpendicular to the boundary surface and outward to the volume enclosed by the boundary surface; $t$ is any coordinate parallel to the surface.

Several students used the solution for $\mathbf{E}$ given for arguments 1.-3., but this is circular reasoning. The point of the problem is to justify all of the steps needed to get to the solution.

I did not expect a solution with the level of detail in what follows. I generally looked for arguments or words that seemed close to something said below. I did not write extended comments on your solutions for statements that were wrong - you should be able to determine what was wrong by reading the following solution.

1. $E_s$ does not depend on $z$ because the charge distribution does not change if we shift the origin of $z$. Said another way, two people who solve this problem using a different location for $z=0$ should get the same result. $E_s$ does not depend on $\phi$ because if we rotate the charge distribution around the $z$-axis by $\phi$, the charge distribution does not change. Said another way, two people who solve the problem using a different $\phi=0$ line perpendicular to the line of charge should get the same answer. The same argument can be used to argue that $E_z$ and $E_{\phi}$ do not depend on $\phi$ and $z$, but this is not needed because in 2. and 3. they are found to be zero.

2. $E_z=0$ - Assume the line extends from $z=\pm L$. Adding the electric field due to a differential charge at $z$ to that from a differential charge at $-z$ gives an electric field that points in the $\hat{\mathbf{s}}$ direction in the $x-y$ plane. An infinite line of charge can be created by letting $L\rightarrow\infty$. Or, for very small $s$, in the $x-y$ plane the line of charge appears infinite.

3. $E_{\phi}=0$ by the same argument as 2.

_Detailed solution using 1.-3. and Gauss' law_

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

A Gaussian cylinder of radius $s$ and a height $h$ and centerline along the $z$-axis has three surfaces, with normals of $\hat{\mathbf{z}}$ on the top cap, $-\hat{\mathbf{z}}$ on the bottom cap, and $\hat{\mathbf{s}}$ on the curved side.

$$\oint \mathbf{E}\cdot \hat{\mathbf{n}}da = \int_\text{top cap} \mathbf{E}\cdot \hat{\mathbf{z}} da +  \int_\text{bottom cap} \mathbf{E}\cdot (-\hat{\mathbf{z}}) da + \int_\text{side}\mathbf{E}\cdot \hat{\mathbf{s}} da$$

$\mathbf{E}\cdot \hat{\mathbf{z}} = E_z(s,\phi,z)$ and we have argued that $E_z=0$, so the first two integrals are zero.

$\mathbf{E}\cdot \hat{\mathbf{s}} = E_s(s,\phi,z)$, so the last integral is, using $da=sdzd\phi$,

$$\int_\text{side}\mathbf{E}\cdot \hat{\mathbf{s}} da = \int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\thinspace d\phi$$

Because $E_s$ is independent of $z$, we can write

$$\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi,z) sdz\thinspace d\phi=\int_{z=-h/2}^{h/2}\int_{\phi=0}^{2\pi} E_s(s,\phi) sdz\thinspace d\phi=h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi$$

Because $E_s$ is independent of $\phi$, we can write

$$h\int_{\phi=0}^{2\pi} E_s(s,\phi) sd\phi=h\int_{\phi=0}^{2\pi} E_s(s) sd\phi$$

Because $s$ and $\phi$ are orthogonal,

$$h\int_{\phi=0}^{2\pi} E_s(s) sd\phi=hE_s(s) s\int_{\phi=0}^{2\pi} d\phi=hE_s(s) s2\pi$$

Note that Gauss' law only gave us $E_s$ - we had to argue why $E_{\phi}$ and $E_z$ were zero. In addition, in order to do the integration in Gauss' law, we needed to provide additional justification for why $E_s$ could only depend on $s$. So this Gauss' law problem had two separate components: 1. arguments that reduce and simplify the general solution

$$\mathbf{E}(s,\phi,z)=E_s(s,\phi,z)\hat{\mathbf{s}}+E_{\phi}(s,\phi,z)\hat{\boldsymbol{\phi}}+E_z(s,\phi,z)\hat{\mathbf{z}}$$

and then 2. evaluation of the integral in Gauss' law. I find that students that don't understand 1. are not able to articulate why a given Gaussian surface can't be used to find the electric field. For example, their answer to why a Gaussian sphere could not be used to find the electric field in this problem typically only involves an ambiguous statement about symmetry; "symmetry" is ambiguous because both a Gaussian sphere and a Gaussian cylinder have symmetry).

# $\delta$ and $\Theta$

## Delta Function (5 pts) 

A charge $Q$ is uniformly distributed on the surface of a sphere of radius $b$. 

Write the equation for the charge density using the Dirac delta function.

**Solution**

$$\rho = \frac{Q}{4\pi b^2}\delta(r-b)$$

Or, equivalently,

$$\rho = \frac{Q}{4\pi r^2}\delta(r-b)$$

Both satisfy

$$Q=\int\rho(\mathbf{x\thinspace d^3x = \int_{0}^{2\pi}\int_0^{\pi}\int_0^{\infty} \rho(\mathbf{x})\thinspacer^2 dr\sin\the\thinspace d\the\thinspace d\phi$$

and are zero everywhere except at $r=b$.

This charge density is easy to guess and verify. Earlier in the semester, I went over the derivation for problems like this. The charge density should be zero everywhere except at $r=b$ and the integral of charge density should be $Q$. Given the problem statement, one can write

$$\rho=C\delta(r-b)$$

and determine the constant $C$ from

$$Q = \int \r\thinspace d^3x$$

where the integral is over all space. In spherical coordinates, for $\rho=\rho(r)$,

$$Q = 4\pi\int_0^{\infty}\rho\thinspacer^2dr=4\pi\int_0^{\infty}C\delta(r-b)r^2dr=C4\pi b^2$$

This gives $C=Q/4\pi b^2$ so that

$$\rho = \frac{Q}{4\pi b^2}\delta(r-b)$$

In the problem statement, I did not ask for the volume charge density. However, this is implied as the delta function is always used to write volume charge densities - part of the motivation for introducing it is so that we don't need to write three equations for the electric field - one for a line of charge, one for a surface charge, and one for a volume charge. With the delta function, only the volume charge equation is needed and the volume integral will reduce to either a surface or line integral.

## Representing $\rho$ Using $\delta$ and $\Theta$ 

1. Find the volume charge density $\rho$ in cylindrical coordinates in terms of $\delta$ and/or $\Theta$ for an infinitely long cylinder of radius $b$ with a charge density per unit length of $\lambda_o$ uniformly distributed on its surface. Assume that the cylinder's centerline is along the $z$-axis.
1. Repeat 1. assuming the cylinder is finite and extends from $z=-h/2$ to $z=h/2$.

''Optional''

3. Find the volume charge density $\rho$ in cylindrical coordinates in terms of $\delta$ and/or $\Theta$ for a uniformly charged disk of radius $b$ with charge density $\sigma_o$ that lies in the $x-y$ plane and is centered on the origin. Use $s$ for the radial coordinate in cylindrical coordinates.

4. Use identity 5. on page 26 of Jackson to convert this to spherical coordinates. Use $r$ for the radial coordinate in spherical coordinates.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|

1. $\rho = \frac{\lambda_o}{2\pi b}\delta(b-s)$

2. $\rho=\frac{\lambda_o}{2\pi b}\delta(b-s)\Big[\Theta(z+{h}/{2})-\Theta(z-{h}/{2})\Big]$

Some students assumed the charge was on the surface of the cylinder. In this case, the solution is

1. $\rho=\frac{\lambda_o}{\pi b^2}\Theta(b-s)$

2. $\rho=\frac{\lambda_o}{\pi b^2}\Theta(b-s)\Big[\Theta(z+{h}/{2})-\Theta(z-{h}/{2})\Big]$

----

3. $\rho=\frac{Q}{\pi b^2}\delta(z)\Theta(b-s)$

4. $\rho = \frac{Q}{\pi b^2}\frac{\delta(\theta-\pi/2)}{r}\Theta(b-r)$
|}
# Continuous Charge Distributions 

A square non-conducting sheet of charge with side length $w$ has a uniform charge density of $\sigma_o$, lies in the $x-y$ plane, and is centered on the origin.

1. Find an integral or integrals that must be evaluated to find $\mathbf{E}(z)$, the electric field on the $z$-axis.
1. Evaluate the integral or integrals and show that for $z/w\ll 1$, $\mathbf{E}(z)$ reduces to the equation for an infinite non-conducting sheet of charge.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
There are several ways to solve this problem. On can first find the field for a line of charge with a charge density of $\lambda$ and length $w$ that lies on the $x$-axis and is centered on the origin - the result is (see Griffiths 4th Edition example 2.2):

$$\mathbf{E}(z)=\frac{k\lambda w}{z\sqrt{z^2+w^2/4}}\hat{\mathbf{z}}$$

Then integrate the field due to differential lines of charges. One needs to account for the fact that the $z$ in this equation will not be the same as the $z$ in this problem. If the differential lines of charge are in the $x$-$y$ plane and lie on the line $x=x'$, then replace the $z$ with $z^2+x'^2$ and use $\lambda = \sigma_odx'$, You can check your answer for this approach by using the result of the following approach after integration with respect to $x'$. 

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\hat{\bf\char"0509}}{\char"0509^2}$$

A second approach requires two integrations. Start with

$$\mathbf{E}_{dq'}(x,y,z) = \frac{dq'}{4\pi\epsilon_0}\frac{\hat{\bf\char"0509}}{\char"0509^2}$$

which expands to

$$\mathbf{E}_{dq'}(x,y,z) =\frac{dq'}{4\pi\epsilon_0}\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}$$

(A third approach is to find the potential $\Psi_{dq'}(x,y,z) = dq'/(4\pi\epsilon_0\char"0509)$ and then use $\mathbf{E}=-\nabla \Psi$.)

and the general definitions

$$\mathbf{r}=x\hat{\mathbf{x}}+y\hat{\mathbf{y}}+z\hat{\mathbf{z}}$$

$$\mathbf{r}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$$

In this problem, $z'=0$ because all charges are in the $x-y$ plane. Using $dq' = \sigma_odx'dy'$, gives

$$\mathbf{E}(x,y,z) = \int_{-w/2}^{w/2}\int_{-w/2}^{w/2}\frac{ \sigma_odx'dy'}{4\pi\epsilon_0}\frac{(x-x')\hat{\mathbf{x}}+(y-y')\hat{\mathbf{y}}+z\hat{\mathbf{z}}}{\big((x-x')^2+(y-y')^2+z^2\big)^{3/2}}$$

$\mathbf{E}(z)$ is obtained by setting $x=y=0$:

$$\mathbf{E}(z) = \int_{-w/2}^{w/2}\int_{-w/2}^{w/2}\frac{ \sigma_odx'dy'}{4\pi\epsilon_0}\frac{-x'\hat{\mathbf{x}}+-y'\hat{\mathbf{y}}+z\hat{\mathbf{z}}}{\big(x'^2+y'^2+z^2\big)^{3/2}}$$

The $\hat{\mathbf{x}}$ and $\hat{\mathbf{y}}$ integrals are zero because their integrands are odd functions. Many students argued they are zero "by symmetry". The word "symmetry" is too general because there are many types of symmetry. It is better to state what kind of symmetry: consider differential charges at $(x,y)$ and $(-x,-y)$ - their horizontal electric fields exactly cancel (ideally provide a diagram). The sheet of charge can be constructed by placing charges with canceling horizontal components and so the horizontal electric field is zero.

To simplify the integration for the $\hat{\mathbf{y}}$ term, define

$$I = \int_{-w/2}^{w/2}dy'\int_{-w/2}^{w/2}\frac{dx'}{(x'^2+a^2)^{3/2}}$$

where $a^2\equiv y'^2+z^2$ and then $E_z(z)=k\sigma_ozI$. This integral can be looked up or found using Mathematica or Wolfram Alpha. Some students reported "computation time exceeded" with Wolfram Alpha. This was probably caused by entering the double integral instead of doing a single integral at a time.

Integration with respect to $x'$ gives

$$I= \int_{-w/2}^{w/2}dy'\frac{x'}{a^2(x'^2+a^2)^{1/2}}\Bigg|_{-w/2}^{w/2}=\int_{-w/2}^{w/2}dy'\frac{w}{a^2(a^2+w^2/4)^{1/2}}$$

Using the earlier definition $a^2\equiv y'^2+z^2$ and a new definition $b^2\equiv z^2+w^2/4$ gives

$$I=\int_{-w/2}^{w/2}\frac{wdy'}{(y'^2+z^2)\sqrt{y'^2+b^2}}$$

This integral can be looked up and the result is (using $\tan^{-1}(u)=-\tan^{-1}(u)$)

$$I=\frac{4}{z}\tan^{-1}\left[\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\right]$$

The final result, using $E_z(z)=k\sigma_ozI$ defined earlier, is 

$$E_z(z)=\frac{\sigma_o}{\pi \epsilon_o}\tan^{-1}\left[\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\right]$$

For $z\ll w$, the argument to the inverse tangent is

$$\frac{w^2}{4z}\frac{1}{\sqrt{z^2+w^2/2}}\simeq \frac{w}{z}\frac{\sqrt{2}}{4}$$

so for $z \gt 0$ and $z\ll w$

$$E_z(z)\rightarrow\frac{\sigma_o}{\pi\epsilon_o}\tan^{-1}(+\infty) = \frac{\sigma_o}{2\epsilon_o}$$

For $z \lt 0$ and $z\ll w$

$$E_z(z)\rightarrow\frac{\sigma_o}{\pi\epsilon_o}\tan^{-1}(-\infty) = -\frac{\sigma_o}{2\epsilon_o}$$

and so the solution matches that for an infinite sheet of charge. Another problem one could ask is to show that for $z\gg w$, $E_z\rightarrow k\sigma_ow^2/z^2$ (far away, the sheet of charge appears as a charge $\sigma_ow^2$ at the origin). To show this, one would need to Taylor series expand the argument of the inverse tangent for small $w/z$.
|}

# Method of Images Review 

Consider the problem of finding the potential $\Phi(\mathbf{x})$ above a grounded and infinite conducting plane when a point charge $q$ is placed above it. (Recall that $\Phi(\mathbf{x})$ is short-hand for $\Phi(x,y,z)$.) 

Assume the conducting plane is in the $x$-$y$ plane and the charge $q$ is placed at at $(x,y,z)=(0,0,z_o)$ 

Due to the point charges, a surface charge density will appear on the conducting plane. To calculate $\Phi(\mathbf{x})$, one needs to know this surface charge density. However, we can't use the direct integration formula used for continuous charge distributions

$$\Phi(\mathbf{x})= \Phi_q(\mathbf{x}) + \int_{plane}\frac{k\thinspace\sigma(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}\thinspace da'$$

because we don't know $\sigma$. ($\Phi_q(\mathbf{x})$ is the potential due to the point charge $q$).

To find $\Phi(\mathbf{x})$, one finds the potential due to a alternantive charge configuration: a point charge $q$ at $(x,y,z) = (0,0,z_o)$ and a point charge $-q$ at $(x,y,z) = (0,0,-z_o)$.

1. Find $\Phi(x,y,z)$ for the alternative charge configuration.
1. Explain why this $\Phi(\mathbf{x})$ is the solution to the original problem.
1. Compute $\partial \Phi(x,y,z)/\partial z$ when $z=0$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
2. From 1.9 of Jackson, if a potential satisfies Poisson's equation in a volume and Dirichlet boundary conditions on the enclosing surface, then it is a unique solution. 

Here the surface is the $z=0$ plane and a hemispherical surface of a large radius above this plane.

Both the original and alternative charge configuration satisfy the same Poisson's equation. In the first case,

$$\nabla^2\Phi=-q\delta(\mathbf{r}-z_o\hat{\mathbf{z}})$$

in the alternative case,

$$\nabla^2\Phi=-q\delta(\mathbf{r}-z_o\hat{\mathbf{z}})+q\delta(\mathbf{r}+z_o\hat{\mathbf{z}})$$

However, because the volume is for $z\gt 0$, the second delta term is zero and so the potential for the alternative case satisfies the same Poisson equation as the original problem.

The potential for the alternative charge configuration satisfies the boundary conditions $\Phi(x,y,0)=0$ and $\Phi=0$ on a half-sphere of large radius. Because solutions to Poisson's equation in a volume bounded by a surface with given boundary conditions are unique, the potential to the alternative problem is the solution for the original problem.
|}

## Point Charge above Infinite Plane 

A point charge $q$ is at a distance $d$ above an infinite and grounded conducting plane. Use the method of images to find:

1. the potential $\Psi(\mathbf{r})$ in the region above the plane;
1. $\nabla^2\Psi$ in the region above the plane;
1. the surface charge density induced on the plane (also verify that this surface charge density gives the expected potential if $\Psi(\mathbf{x})=(1/4\pi\epsilon_0)\int dq/|\mathbf{x}-\mathbf{x'}|$ is used to compute the potential);
1. the force between the plane and the charge using Coulomb's law for the force between $q$ and its image $q'$;
1. the total force acting on the plane by integrating $\sigma^2/2\epsilon_0$ over the whole plane;
1. the work necessary to remove the charge $q$ from its position to infinity;
1. the potential energy between the charge $q$ and its image (compare the answer the work computed in the previous part and discuss).

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
A point charge $q$ is at a distance $d$ above an infinite and grounded conducting plane. Use the method of images to find:

1. the potential $\Psi(\mathbf{r})$ in the region above the plane;
1. $\nabla^2\Psi$ in the region above the plane;
1. the surface charge density induced on the plane (also verify that this surface charge density gives the expected potential if $\Psi(\mathbf{x})=(1/4\pi\epsilon_0)\int dq/|\mathbf{x}-\mathbf{x'}|$ is used to compute the potential);
1. the force between the plane and the charge using Coulomb's law for the force between $q$ and its image $q'$;
1. the total force acting on the plane by integrating $\sigma^2/2\epsilon_0$ over the whole plane;
1. the work necessary to remove the charge $q$ from its position to infinity;
1. the potential energy between the charge $q$ and its image (compare the answer the work computed in the previous part and discuss).

1.

$$\Psi = \frac{kq}{\sqrt{x^2+y^2+(z-d)^2}}-\frac{kq}{\sqrt{x^2+y^2+(z+d)^2}}$$

Justification given in previous problem.

2. 

Using the fact that

$$\nabla^2\left[\frac{1}{|\mathbf{x}-\mathbf{x}'|}\right] = -4\pi\delta(\mathbf{x}-\mathbf{x}')$$

gives

$$\nabla^2\Psi=-q\delta(x)\delta(y)\delta(z-d)+q\delta(x)\delta(y)\delta(z+d)$$

For $z\gt 0$, $\delta(z+d)=0$, so

$$\nabla^2\Psi=-q\delta(x)\delta(y)\delta(z-d)$$

Many students computed $\nabla^2\Psi$ and found it to be zero. This is not necessary as we know that the potential $\Psi(\mathbf{x})$ for a point charge at $\mathbf{x}'$, $\nabla^2\Psi = 0$ except at $\mathbf{x}=\mathbf{x}'$. At $\mathbf{x}=\mathbf{x}'$, $\nabla^2\Psi=0/0$ and the resolution of this indeterminacy using the delta function was explored in an earlier homework by modeling a point charge as a sphere of uniform charge density and a vanishing radius.

3. 

At the surface of a conductor, from Gauss' law,

$$\sigma=\epsilon_o\mathbf{E}\cdot\hat{\mathbf{n}}$$

where $\hat{\mathbf{n}}$ is the normal to the surface and $\mathbf{E}$ is the field on the surface. For the plane, $\hat{\mathbf{n}}= \hat{\mathbf{z}}$, so

$$\mathbf{E}\cdot\hat{\mathbf{n}}=-(\boldsymbol{\nabla}\Psi)\cdot\hat{\mathbf{z}}=-\frac{\partial \Psi}{\partial z}$$

$$\frac{\partial \Psi}{\partial z}=\frac{-(z-d)kq}{(x^2+y^2+(z-d)^2)^{3/2}}-\frac{-(z+d)kq}{(x^2+y^2+(z-d)^2)^{3/2}}=\frac{2dkq}{(x^2+y^2+(z-d)^2)^{3/2}}$$

At the surface, $z=0$, so

$$\frac{\partial \Psi}{\partial z}\Bigg|_{z=0}=\frac{2kqd}{(x^2+y^2+d^2)^{3/2}}$$

giving

$$\sigma=-\frac{q}{2\pi}\frac{d}{(x^2+y^2+d^2)^{3/2}}$$

Using

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_0}\int \frac{dq}{|\mathbf{x}-\mathbf{x'}|}$$ 

with $dq=\sigma dx'dy'$ and $|\mathbf{x}-\mathbf{x'}|=\sqrt{(x-x')^2+(y-y')^2+z^2}$ gives the required integral to find the potential due to the surface charges:

$$\Psi(x,y,z)=-\frac{qd}{8\pi\epsilon_0}\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}dx'dy'\frac{1}{((x-x')^2+(y-y')^2+z^2)^{1/2}}\frac{1}{(x'^2+y'^2+d^2)^{3/2}}$$

As mentioned on Piazza, we have not covered the technique for finding $\Psi(\mathbf{x}$, so find the potential for $z=0$ only, set $x=y=0$, giving

$$\Psi(0,0,z)=-\frac{qd}{8\pi\epsilon_0}\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}dx'dy'\frac{1}{(x'^2+y'^2+z^2)^{1/2}}\frac{1}{(x'^2+y'^2+d^2)^{3/2}}$$

Using polar coordinates with $s'^2=x'^2+y'^2$,

$$\Psi(z)=-\frac{qd}{8\pi\epsilon_0}\int_{0}^{\infty}\int_{0}^{2\pi}s'ds'd\phi'\frac{1}{(s'^2+z^2)^{1/2}}\frac{1}{(s'^2+d^2)^{3/2}}$$

Integration over $\phi'$ gives

$$\Psi(z)=-\frac{qd}{4\pi\epsilon_0}\int_{0}^{\infty}s'ds'\frac{1}{(s'^2+z^2)^{1/2}}\frac{1}{(s'^2+d^2)^{3/2}}$$

Using $u^2=s'^2+z^2$ gives

$$\Psi(z)=-\frac{qd}{4\pi\epsilon_0}\int_{z}^{\infty}u\thinspace du'\frac{1}{(u^2)^{1/2}}\frac{1}{(u^2-z^2+d^2)^{3/2}}$$

$$\Psi(z)=-\frac{qd}{4\pi\epsilon_0}\int_{z}^{\infty}\text{sign}(u)\thinspace du'\frac{1}{(u^2-z^2+d^2)^{3/2}}$$

where $\text{sign}(u)=u/|u|$. Using an integral table, $\int du(u^2+c^2)^{-3/2}= u/(c^2 \sqrt{c^2 + u^2})$ with $c^2\equiv d^2-z^2$ gives, for both signs of $z$,

$$\Psi(z)=-\frac{qd}{4\pi\epsilon_0}\left[\frac{1}{d^2-z^2}-\frac{|z|}{|d|(d^2-z^2)}\right]$$

Most students did not have absolute value signs in their solution because they did not use $\sqrt{z^2}=|z|$. Getting the absolute value in the answer below requires consideration of $z\gt 0$ and $z\lt 0$ cases in the above (in general, this would matter, but it does not matter for this problem because we are considering only $z\gt 0$). Using this fact and the fact that $d\gt 0$ by definition, so $|d|=d$, gives

$$\Psi(z)=-\frac{qd}{4\pi\epsilon_0}\frac{1}{|z|+d}$$

This is the potential for the charges on the surface above and below the surface; it is symmetric around $z=0$ as expected. For $z\gt 0$, $|z|+d=|z+d|$, so we have recovered the second term in the potential for part 1. When $z \lt 0$, this potential is equal and opposite to the potential for the point charge above the plane, giving a zero potential for $z\lt 0$.

4.

The force is

$$F=\frac{kq}{(2d)^2}$$

5.

Integration should give the same force as 4.

6.

The downward force as a function of the position of the charge above the plane is

$$F=\frac{kq^2}{(2z)^2}$$

Integrating this force

$$W_{ext}= \int\mathbf{F}_{ext}\cdot d\mathbf{l} = \int_{z=d}^{\infty}\frac{kq^2dz}{(2z)^2}=\frac{kq}{4d}$$

Note that one should get a positive answer for the work required to remove the charge - the external force on the charge $q$ is in the same direction of its movement.

7. The potential energy of $q$ and its image is

$$U=-\frac{kq^2}{2d}$$

which corresponds to minus the work required to move charge $q$ out with $q'$ fixed: $\Delta U = U_f-U_i = 0 - U_i = W_{ext}$.

The discrepancy is due to the fact that in part 7., we assumed that the image charge (or equivalently, the induced charges on the plane) was fixed. As $q$ is moved upwards, the induced charge on the sheet decreases and so the force on $q$ due to the induced charges will be less than that assumed in 7.  To see that the force implied by use of 7. is 2x that in 6., compute the force using $dU/dz$ with $U$ from 7.: $U=-kq^2/(2z)$.

Another way at arriving at the same result as 6. is to consider $\int E^2 d^3x$ with a volume of integration of $z\gt 0$. If one uses a volume of integration of all space, then one arrives at the result in 7.

Many students essentially copied an online solution (without citation!) that states "The potential energy is twice the work required to move the particle to infinity. The reason they don't match is because the image particle is not a real particle. We must remember that there are actually no fields within the conductor. The potential energy calculation above is counting the energy of the fields in the conductor, which don't actually exist."

The problem with the statement of "We must remember that there are actually no fields within the conductor" is that no statement is made about why the calculation in 7. counts the energy of the fields in the conductor (the $z\lt 0$ region).  The other problem is copying an answer without citation.
|}
# Green

## Reciprocity -- Discrete

#green-s-reciprocity-theorem

#green-s-reciprocity-use&l=589&c=1

## Reciprocity -- Continuous

#green-s-identity-derivation&l=663&c=1

#alternative-derivation-of-reciprocity-for-continuous-rho&l=697&c=1

## Green Function Solution General Equation I

#jackson-equation-1-42&l=1017&c=1

## Green Function Solution General Equation II

<span style="background-color:yellow">I did not grade this problem. Most of the answers are in the book - the motivation for this problem is that upon first read, you probably did not notice many of the issues raised by the questions. When reading Jackson, one needs to fill in many of the missing steps as I have done here (or read another reference!)</span>

The following is an expanded version of the discussion of Green functions in Jackson 1.10 and 2.6. It is an alternative to a problem in which only questions 14. and 15. are asked. 

Jackson considers a sphere geometry in 2.6 and in this problem, an infinite plane geometry is used. The steps required are similar and slightly less complicated.

Work through it and answer the questions posed. Label your answers and put a box around them.

I don't know of many other introductory references for this, but the following may also be of use
* http://physics.usask.ca/~hirose/p812/notes/Ch2.pdf
* http://wtamu.edu/~cbaird/SuppGreenFunctionMethod.pdf
* http://physics.gmu.edu/~joe/PHYS685/Topic2.pdf
* Most mathematical physics textbooks will have a discussion of Green's functions.
* [https://www.amazon.com/Elements-Greens-Functions-Propagation-Publications/dp/0198519982 Elements of Greens Functions by Barton] is a very comprehensive treatment of Green functions in physics.

### Preliminaries 

Using the divergence theorem for a vector field $\mathbf{A}$ that can be written in the form $\mathbf{A}=\phi \nabla\psi$, show that

$$\int_\mathcal{V} \left(\phi\nabla^2\psi + \nabla\phi\boldsymbol{\cdot}\nabla\psi\right)d^3x=\oint_\mathcal{S}\phi\frac{\partial \psi}{\partial n} da$$

where $\phi(\mathbf{x})$ and $\psi(\mathbf{x})$ are scalar functions and $\mathcal{S}$ is the surface of the volume $\mathcal{V}$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$$\mathbf{\nabla}\cdot (f\mathbf{F}) = f(\mathbf{\nabla}\cdot \mathbf{F}) + \mathbf{F}\cdot(\mathbf{\nabla}f)$$

integrating both sides over a volume $\mathcal{V}$

$$\int_{\mathcal{V}}\mathbf{\nabla}\cdot (f\thinspace\mathbf{F})\thinspace d^3x = \int_{\mathcal{V}}\Big(f\thinspace(\mathbf{\nabla}\cdot \mathbf{F}) + \mathbf{F}\cdot(\mathbf{\nabla}f)\Big)\thinspace d^3x$$

and re-writing the LHS using the divergence theorem

$$\oint_{\mathcal{S}}\mathbf{U}\cdot \hat{\mathbf{n}}\thinspace da=\int_{\mathcal{V}}\boldsymbol{\nabla}\cdot \mathbf{U}\thinspace d^3x$$

with $\mathbf{U}=f\thinspace\mathbf{F}$ gives

$$\oint_{\mathcal{S}} f\thinspace\mathbf{F}\cdot\hat{\mathbf{n}}\thinspace da=\int_{\mathcal{V}} \Big(f\thinspace(\mathbf{\nabla}\cdot \mathbf{F}) +\mathbf{F}\cdot(\mathbf{\nabla}f)\Big)\thinspace d^3x$$

Using $f = \phi$, $\mathbf{F}=\nabla\psi$, and $\nabla\psi\cdot\hat{\mathbf{n}}=\partial \psi/\partial n$ in the above gives

$$\oint_\mathcal{S}\phi\frac{\partial \psi}{\partial n} da=\int_\mathcal{V}\Big(\phi\nabla^2\psi + \nabla\psi\boldsymbol{\cdot}\nabla\phi\Big)d^3x$$

Using the fact that the dot product commutes and swapping the LHS and RHS gives

$$\int_\mathcal{V} \left(\phi\nabla^2\psi + \nabla\phi\boldsymbol{\cdot}\nabla\psi\right)d^3x=\oint_\mathcal{S}\phi\frac{\partial \psi}{\partial n} da$$
|}

* Verify this equation by choosing your own (simple) scalar functions and volume. 
* Does the surface need to be closed? 
* Can the volume have a cavity?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
* This should work for any functions for which the divergence theorem applies.
* Surface needs to be closed. This is implied by the notation, but the notation is required because the divergence theorem was used.
* Volume can have a cavity. The divergence theorem still applies. Given a cavity, there will be two surfaces, and outer and inner. The normal direction points outward for the surfaces, so a sphere with a cavity centered on the origin will have an outside surface normal in the $\hat{\mathbf{r}}$ direction and an inside surface normal in the $-\hat{\mathbf{r}}$ direction.
|}

Next, show that

$$\int_\mathcal{V} \left(\phi\nabla^2\psi -\psi\nabla^2\phi\right)d^3x=\oint_\mathcal{S}\left(\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}\right) da$$

Assume that $\phi(\mathbf{x})$ is a scalar function that is created by a continuous scalar volume charge density $\rho(\mathbf{x})$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Repeat the derivation given earlier except with $\mathbf{A}=\psi \nabla\phi$ to get

$$\int_\mathcal{V} \left(\psi\nabla^2\phi + \nabla\psi\boldsymbol{\cdot}\nabla\phi\right)d^3x=\oint_\mathcal{S}\psi\frac{\partial \phi}{\partial n} da$$

and combine with

$$\int_\mathcal{V} \left(\phi\nabla^2\psi + \nabla\phi\boldsymbol{\cdot}\nabla\psi\right)d^3x=\oint_\mathcal{S}\phi\frac{\partial \psi}{\partial n} da$$

found earlier and the fact that the dot product commutes to eliminate the $\nabla\psi\boldsymbol{\cdot}\nabla\phi$ term.
|}

Assume that $\psi(\mathbf{x})=1/|\mathbf{x}-\mathbf{x'}|$ and 

1. explain why it follows that

$$\int_\mathcal{V} \left(-4\pi\phi(\mathbf{x'})\delta(\mathbf{x}-\mathbf{x'})+\frac{\rho(\mathbf{x'})/\epsilon_o}{|\mathbf{x}-\mathbf{x'}|}\right)d^3x'=\oint_\mathcal{S}\left(\phi\frac{\partial}{\partial n'}\frac{1}{|\mathbf{x}-\mathbf{x'}|}-\frac{1}{|\mathbf{x}-\mathbf{x'}|}\frac{\partial \phi}{\partial n'}\right) da'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$\phi(\mathbf{x})$ is a scalar function that is created by a continuous scalar volume charge density $\rho(\mathbf{x})$ implies that it satisfies Poisson's equation $\nabla^2\phi=-\rho/\epsilon_0$.

With a change to a primed integration variable, we need to replace $\nabla$ with $\nabla'$ and swap $\mathbf{x}$ and $\mathbf{x}'$ in the integrand. Then we can use

$$\nabla'^2 \left(\frac{1}{|\mathbf{x}'-\mathbf{x}|}\right) = -4\pi\delta(\mathbf{x}'-\mathbf{x}) = -4\pi\delta(\mathbf{x}-\mathbf{x}')$$

and

$$\frac{1}{|\mathbf{x}'-\mathbf{x}|}=\frac{1}{|\mathbf{x}-\mathbf{x}'|}$$
|}

Explain why

2. the integration in these equations were changed to be over primed variables; and

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
This was done so that the result after integration depends on $\mathbf{x}$ - usually primed variables are used for the location of charges and unprimed at the location of the potential.
|}

3. the integrals in this equation have an integration variable and another variable.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

|}

Also,

4. can the integral on the RHS can be written with $\phi(\mathbf{x'})$ instead of $\phi$?; and

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Yes. I raised this question because it is something that you should notice - in various place in Jackson, he'll explicitly give the dependence of some function and not other. For example, in equation 1.42, he uses $\partial \Phi/\partial n'$ and $\Phi(\mathbf{x}')$, but for consistency perhaps $\partial \Phi(\mathbf{x}')/\partial n'$ should have been written.
|}

5. give an example geometry where you can explain what $\frac{\partial}{\partial n'}\frac{1}{|\mathbf{x}-\mathbf{x'}|}$ means.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
If the geometry is a point charge at $\mathbf{x}'=0$, then on a sphere centered on the origin it is proportional to $E_r$, the electric field in the radial direction (In this case $n'=r'$).
|}

6. Are there any conditions required to justify re-writing the last equation as

$$\phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_\mathcal{V}\frac{\rho(\mathbf{x'})}{|\mathbf{x}-\mathbf{x'}|}d^3x'-\frac{1}{4\pi}\oint_\mathcal{S}\left(\phi\frac{\partial}{\partial n'}\frac{1}{|\mathbf{x}-\mathbf{x'}|}-\frac{1}{|\mathbf{x}-\mathbf{x'}|}\frac{\partial \psi}{\partial n'}\right) da'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
By the property of the delta function that $\delta(\mathbf{x}-\mathbf{x}')=0$ when $\mathbf{x} \ne \mathbf{x}'$

$$\int_\mathcal{V} -4\pi\phi(\mathbf{x'})\delta(\mathbf{x}-\mathbf{x'})\thinspace d^3x'=0$$

if $\mathbf{x}$ is outside the volume $\mathcal{V}$ because $\delta(\mathbf{x}-\mathbf{x'})$ will always be zero.

So that constraint is that $\mathbf{x}$ is in $\mathcal{V}$.
|}

7. Explain the conditions under which this equation reduces to 

$$\phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_\mathcal{V} \frac{\rho(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|}d^3x'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
This will be true if the charges in the system and a surface can be selected so the RHS is zero or if the surface is chosen to be so far away from any charges so that the integral approaches zero. Jackson notes on pg. 37 that the electric field must fall of faster than $|\mathbf{x}-\mathbf{x}'|^{-1}$. This claim is justified in the solution to the first problem in this HW.

Can you think of a distribution of charges and a surface that is not at infinity so that the RHS is zero? 
|}

8. Give an example of a charge distribution $\rho$ which for which this equation is valid.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

|}

## 1-D

### Parallel Plates with Charged Slab I

Equation 1.44 of Jackson states that the potential within a volume $\mathcal{V}$ enclosed by surface $\mathcal{S}$ can be computed using

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\Psi(\mathbf{x}')\frac{\partial G_D}{\partial n'} da'$$

provided that a Green function $G_D$ is known that satisfies

$$\nabla'^2G_D=-4\pi\delta(\mathbf{x}-\mathbf{x}')\qquad\text{for}\thinspace\mathbf{x}'\thinspace\thinspace\text{in}\thinspace\thinspace\mathcal{V}$$

and

$$G_D(\mathbf{x},\mathbf{x}') = 0\qquad\text{for}\thinspace\mathbf{x}'\thinspace\thinspace\text{on}\thinspace\thinspace\mathcal{S}$$

Previously, Green functions were found using the method of images. In this problem, you will find the Green function using an alternative method.

Consider two infinite, parallel, and grounded conducting sheets in the $x=0$ and $x=d$ plane. In the $x=x'$ plane, there is an infinite non-conducting sheet with surface charge density $\sigma'$.

1. Find the potentials to the left, $\psi_l$, and right, $\psi_r$, of the non-conducting sheet using any method.

2. Write the potential $\psi(x)$ for $0\le x\le d$ as a single function using $\psi_l$ and $\psi_r$ and the Heavyside step function $\Theta$.

3. Show that $\psi(0)=0$, $\psi(d)=0$, and $\nabla'^2\psi \sim \delta(x-x')$ and so this $\psi$ is proportional to $G_D$, and find the proportionality constant.

Now that $G_D$ is known, the potential between the two conducting planes given any charge distribution $\rho$ can be computed using

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\Psi(\mathbf{x}')\frac{\partial G_D}{\partial n'} da'$$

Conceptually, one can see that the first integral is a weighted sum of $G_D$, which is proportional to the potential for a single sheet of charge between the plates at $x'$. This integral sums the potentials for a continuous set of sheets.

4. Suppose the conducting planes are grounded and a non-conducting slab with charge density $\rho_o$ exists between them. Use the above equation to find $\Psi(\mathbf{x})$ between the conducting planes. 

Notes: You will need to use the fact that $\Theta$ modifies the limits of integration, $d\Theta(x)/dx=\delta(x)$, and $d\Theta(-x)/dx=-\delta(x)$. You can check your answer either using Gauss' law or the boundary value method to find $\Psi(x)$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Let subscript $l$ refer to quantities for $x\lt x'$ and subscript $r$ refer to quantities for $x\gt x'$.

1.

One can answer this question by assuming a surface charge of $\sigma_l$ and $\sigma_r$ is induced on the plates at $x=0$ and $x=w$. Then use the formula $\sigma/2\epsilon_o$ for the electric field of the sheets of charge at $x=0$, $x=x'$, and $x=w$ to get the total field $E_l$ and $E_r$.  The two unknowns, $\sigma_l$ and $\sigma_r$, can be found by using the fact that the electric field in either of the conductors is zero - this yields $\sigma' = -(\sigma_l+\sigma_r)$, which is expected because the net charge in the universe is zero. The second equation needed to find $\sigma_l$ and $\sigma_r$ in terms of $\sigma'$ is

$$\psi(w)-\psi(0) = 0 = -\int_0^w E\thinspace dx=-\int_0^{x'}E_ldx-\int_{x'}^wE_rdx$$

Some students wrote their final answers in terms of $\sigma_l$ and $\sigma_r$. These were not parameters given in the problem statement and so such a solution is incomplete.

Alternatively, one can use the fact that $\nabla^2 \psi(x)=0$ has solutions of the form $\psi=a+bx$, the two boundary conditions and the continuity and jump conditions at $x=x'$.

$$\psi_l=A_l+B_lx$$

$$\psi_r=A_r+B_rx$$

Boundary conditions:

$$\psi_l(0)=0\Rightarrow A_l=0$$

$$\psi_r(w)=0=A_r+B_rw\Rightarrow A_r=-B_rw$$

This leaves

$$\psi_l=B_lx$$

$$\psi_r=B_r(x-w)$$

Continuity:

$$\psi_l(x')=\psi_r(x')\Rightarrow B_lx'=B_r(x'-w)$$

Jump:

$$\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$$

$$-B_r+B_l=\frac{\sigma'}{\epsilon_o}\Rightarrow B_l=B_r+\frac{\sigma'}{\epsilon_o}$$

The three equations left are

$$A_r=-B_rw$$

$$B_lx'=B_r(x'-w)$$

$$B_l=B_r+\frac{\sigma'}{\epsilon_o}$$

Solving gives

$$B_l=-\frac{\sigma'}{\epsilon_o}\left(\frac{x'}{w}-1\right)$$

$$B_r=-\frac{\sigma'}{\epsilon_o}\frac{x'}{w}$$

So the final solution is

$$\psi_l=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x'}{w}\right)x$$

$$\psi_r=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x}{w}\right)x'$$

Note that swapping $x$ and $x'$ in $\psi_l$ gives the equation for $\psi_r$, and vice-versa. That is, $\psi_l(x',x)=\psi_r(x,x')$.

2.

$$\psi=\psi_l(x)\Theta(x'-x)+\psi_r(x)\Theta(x-x')$$

Checks: 
* When $x\lt x'$, $\Theta(x'-x)=1$ and $\Theta(x-x')=0$, giving $\psi=\psi_l$.
* When $x\gt x'$, $\Theta(x'-x)=0$ and $\Theta(x-x')=1$, giving $\psi=\psi_lr$.

3.

$$\frac{d\psi}{dx} = \psi_l(x)\frac{d}{dx}\Theta(x'-x) + \Theta(x'-x)\frac{d\psi_l(x)}{dx} + \psi_r(x)\frac{d}{dx}\Theta(x-x')+\Theta(x-x')\frac{d\psi_r(x)}{dx}$$

If one plots $\psi(x)$, you will see that its derivative has a jump downwards at $x=x'$ of $\sigma'/\epsilon_o$ and so we expect the terms in $d\psi/dx$ with the derivative of the Heavyside step function, which is the delta function, to be zero. So the two terms involving derivatives of $\Theta$ will be addressed first.

The first term can be rewritten using

$$\frac{d}{dx}\Theta(x'-x)=-\delta(x'-x)=-\delta(x-x')$$

The first equality follows from the identity given in the problem statement: $d\Theta(-x)/dx=-\delta(x)$. The second equality is a standard delta function identity.

The second term is

$$\frac{d}{dx}\Theta(x-x')=\delta(x-x')$$

The following two equalities follow from the fact that $\delta(x-x')$ is zero except at $x=x'$:

$$-\psi_l(x)\delta(x-x')=-\psi_l(x')\delta(x-x')$$

$$\psi_r(x)\delta(x-x')=\psi_r(x')\delta(x-x')$$

As a result of these considerations, the two terms in $d\psi/dx$ involving derivatives of $\Theta$ cancel, leaving

$$\frac{d\psi}{dx} = \Theta(x'-x)\frac{d\psi_l(x)}{dx} +\Theta(x-x')\frac{d\psi_r(x)}{dx}$$

Straightforward calculation and use of the same identities as above gives

$$\frac{d^2\psi}{dx^2}=-\frac{\sigma'}{\epsilon_o}\delta(x-x')$$

This matches expectations. For a sheet of charge in the $x=x'$ plane, the volume charge density is

$$\rho=\sigma'\delta(x-x')$$

and Poisson's equation is

$$\nabla^2\psi=-\frac{\rho}{\epsilon_o}$$

(Recall that the units of $\delta(x)$ are inverse length. This follows from part of the definition of the delta function: $\int\delta(x)dx=1$).

We need $G_D$ such that

$$\nabla'^2G_D=-4\pi\delta(\mathbf{x}-\mathbf{x}')\qquad\text{for}\thinspace\mathbf{x}'\thinspace\thinspace\text{in}\thinspace\thinspace\mathcal{V}$$

The units of $\delta(\mathbf{x})$ are 1/length$^3$. This follows from part of the definition of the 3-D delta function: $\int\delta(\mathbf{x})dx=1$. It is somewhat unconventional for a function with a scalar argument to have different units than when it has a vector argument and so some authors use $^3\delta(\mathbf{x})$ instead of $\delta(\mathbf{x})$. 

In one dimension, $\delta(\mathbf{x}-\mathbf{x}')=\delta(x-x')/A$, so

$$\nabla'^2G_D=-4\pi\delta(x-x')/A$$

where $A$ is the area of the sheets. 

The $A$ here plays a role similar to the $4\pi b^2$ found in the example done in class for the Green function associated with the interior of a sphere of radius $b$. 

Due to the property $G_D(x,x')=G_D(x',x)$, we can equivalently write 

$$\nabla^2G_D=-4\pi\delta(x-x')$$

Several students thought that $\nabla'^2G_D$ in the problem statement was a typo and that it should have been $\nabla^2G_D$. Because $G_D(x,x')=G_D(x,x')$, either can be used. I used the primed version to be consistent with the derivation of equation 1.42 of Jackson, which uses the primed version in equation 1.39.

----

If you are uncomfortable with the appearance of $A$ here, go back to the derivation of equation 1.42 of Jackson, but repeat assuming $\psi$ and $\phi$ in equation 1.35 only on $x$. Another way of concluding (\nabla'^2G_D=-4\pi\delta(x-x')/A$ is to integrate $\nabla'^2G_D(x,x')=-4\pi\delta(\mathbf{x}-\mathbf{x}')=-4\pi\delta(x-x')\delta(y-y')\delta(z-z')$ over the non-varying dimensions :

$$\int\int dy'dz'\nabla'^2G_D(x,x')=-4\pi\int \int dy'dz'\delta(x-x')\delta(y-y')\delta(z-z')=-4\pi\delta(x-x')$$

$$AG_D(x,x')=-4\pi\delta(x-x')$$

----

Comparison of 

$$\nabla'^2G_D=-4\pi\delta(x-x')/A$$

with 

$$\frac{d^2\psi}{dx^2}=-\frac{\sigma'}{\epsilon_o}\delta(x-x')$$

gives

$$G_D(x,x') = \frac{4\pi\epsilon_o}{A\sigma'}\psi$$

4.

Now that we have $G_D$ for this geometry, we can use it for any $\rho$ and any boundary condition. Take the volume $\mathcal{V}$ to have a volume of $Aw$. Its surface has 6 faces. Four of the faces have normal directions that are perpendicular to the $\hat{\mathbf{x}}$ direction and so $\partial G_D/\partial n'=0$ on these faces (e.g.,  $\partial G_D/\partial y'=\partial G_D/\partial z'=0$). 

In the new problem, we are given that $\psi=0$ at $x=0$ and $x=d$ and so $\psi=0$ on the two faces with a normals in the $\pm x$ direction. As a result, the surface integral term in

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\Psi(\mathbf{x}')\frac{\partial G_D}{\partial n'} da'$$

is zero. This leaves

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Note
|-
|
It is at this point that we can recognize that because $G_D$ is proportional to $\psi$, this integral represents the summation of the potentials due to sheets of charge that are continuously distributed between $0$ and $w$ such that they form a continuous charge density $\rho$. In fact, without knowledge of Green's functions, one may have concluded that to find the potential due to a continuous $\rho$, one only needed to do a weighted sum of potentials due a single sheet of charge at $x'$. That is, you could use the replacement $\sigma'=\rho(x\thinspace dx'$ and then $\Psi(x)=\int_0^w (\psi(x')/\sigma')\rho(x\thinspace dx'$.
|}

One can also check this equation by using $\rho=\sigma'\delta(x-x')$ and $G_D$ found above and verifying that the resulting $\Psi$ matches the potential $\psi$ used to form $G_D$.

Rewriting the Green function

$$G_D(x,x') = \frac{4\pi\epsilon_o}{A\sigma'}\psi$$

Using

$$\psi=\psi_l(x)\Theta(x'-x)+\psi_r(x)\Theta(x-x')$$

and

$$\psi_l=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x'}{w}\right)x$$

$$\psi_r=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x}{w}\right)x'$$

gives

$$G_D(x,x') = \frac{4\pi}{Aw}\left[(w-x')x\Theta(x'-x)+(w-x)x'\Theta(x-x')\right]$$

Using $\rho=\rho_o$ and $G_D$ in

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'$$

gives

$$\Psi(x)=\frac{\rho_o}{w\epsilon_o}\int_0^w \left[(w-x')x\Theta(x'-x)+(w-x)x'\Theta(x-x')\righ\thinspace dx'$$

The $\Theta$ function modifies the limits of integration

$$\Psi(x)=\frac{\rho_o}{w\epsilon_o} \left[\int_x^w(w-x'\thinspace dx' +\int_0^x(w-x)\thinspace dx'\right]$$

and integration gives

$$\Psi(x) = \frac{\rho_ow^2}{2\epsilon_o}\left[\frac{x}{w}-\frac{x^2}{w^2}\right]$$

As a final check, note that $\Psi(0)=\Psi(w)=0$ and $d^2\Psi/x^2=-\rho_o/\epsilon_o$.

(For practice with the $\Theta$ function, try this problem using $\rho=\rho_o\Theta(x-w/2)$ so that only half of the space is filled with a charged slab. In this case, there will be two $\Psi(x)$ functions, one for $x\lt w/2$ and the other for $x\gt w/2$. One student noted that the problem statement did not say that $\rho_o$ filled the space and tried to solve this assuming a conducting slab with an arbitrary thickness - however, the slab thickness was not given as a parameter in the problem statement so it is safe to assume that $\rho_o$ fills the space.)

An alternative way of computing $\Psi$ is to start with

$$\frac{d^2\Psi}{dx^2} = -\frac{\rho_o}{\epsilon_o}$$

Direct integration gives

$$\Psi(x) = -\frac{\rho_o}{\epsilon_o}\frac{x^2}{2} + C_1x + C_0$$

Using $\Psi(0)=\Psi(w)=0$ to find $C_0$ and $C_1$ gives

$$\Psi(x) = \frac{\rho_ow^2}{2\epsilon_o}\left[\frac{x}{w}-\frac{x^2}{w^2}\right]$$

Alternatively, one can solve this problem using Gauss' law to find the electric field (it is easiest to use a Gaussian cylinder centered on $x=w/2$ with a height of $w-2x$).
|}

<div style="page-break-before: always"> </div>

### Parallel Plates with Charged Slab II

Due on April 8th before class starts.

In [[#HW_5|HW #5]], you found $G_D(x,x')$ and used it to find the potential $\Phi$, the potential between the conductors, when the space between the conductors was filled with a non-conducting slab with a uniform charge density - $\rho(x) = \rho_o$.

1. Find $\Phi$ using $G$ from [[#HW_5|HW #5]] and equation 1.44 of Jackson.
1. Find $\Phi$ using Gauss' law and $\psi(b)-\psi(a)=\int_a^b \mathbf{E}\cdot d\mathbf{l}$. Provide diagrams and address all surfaces of your Gaussian surface. Do not use the $\Phi$ found in part 1.
1. Compute the surface charge density on the conductor at $x=0$ using $d\Phi/dn=-\sigma/\epsilon_o$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
In the following, subscript $r$ corresponds to potentials and fields for $0\lt x\le d/2$; subscript $r$ corresponds to $d/2\le x\lt d$. For surface charge densities, the subscript indicates the surface at $x=0$ or $x=d$.

'''Boundary Value Method'''

The following solution is written in dimensionless form using the replacements

$\psi \rightarrow \psi/(\rho_od^2/\epsilon_o)$, $x\rightarrow x/d$, $E \rightarrow E/(\rho_od/\epsilon_o)$, and $\sigma \rightarrow \sigma/(\rho_od)$.

Two solutions are computed. For $0\le x\le d/2$, we need to solve Poisson's equation. For $d/2\le x\le d$, we need to solve Laplace's equation. The two solutions are connected using boundary conditions at $x=d/2$.

The Poisson equation $\nabla^2\psi_l=-1$ has the general solution

$$\psi_l = -\frac{1}{2}x^2 + Ax + B$$

Laplace's equation $\nabla^2\psi_r=0$ has the general solution

$$\psi_r = Cx + D$$

Boundary conditions:
1. $\psi_l(0) = 0$
1. $\psi_r(d) = 0$
1. $\psi_l(1/2) = \psi_r(1/2)$
1. $\left[-\partial \psi_r/\partial x + \partial \psi_l/\partial x\right]_{x=1/2}=0$

BC 1. gives $B=0$; BC 2. gives $D=-C$. The potentials can then be written as

$$\psi_l = -\frac{1}{2}x^2 + A\qquad\quad \psi_r = C(x - 1)$$

BC 3. gives

$$-\frac{1}{8}+A\frac{1}{2} = -C\frac{1}{2}\qquad\Rightarrow\qquad \frac{1}{4}-A = C$$

BC 4. gives

$$\frac{1}{2} - A + C = 0\qquad\Rightarrow\qquad -\frac{1}{2} + A = C$$

After solving for $A$ and $C$ using these last two equations,

$$\psi_l(x)=\frac{x}{2}\left(\frac{3}{4}-x\right)$$

$$\psi_r(x)=\frac{1}{8}(1-x)$$

This potential is plotted in [https://www.mathcha.io/editor/kMNEMierUZnHDQYLZBsDZ1B36TLgxqBxh168Mvn Figure 3.]

'''Gauss' Law Method'''

The electric field will be in $x$ direction because conducting planes are large.

Dotted lines in [https://www.mathcha.io/editor/kMNEMierUZnHDQYLZBsDZ1B36TLgxqBxh168Mvn Figure 2.] are a side view of Gaussian cylinders with caps having area $A$. The electric field is parallel to the curved surface of the cylinder so the surface integral for the flux involves only the caps:

$$\oint \mathbf{E}\cdot d\mathbf{a}=\int_{l\thinspacecap}\mathbf{E}\cdot d\mathbf{a}+\int_{r\thinspacecap}\mathbf{E}\cdot d\mathbf{a}=\frac{Q_{encl}}{\epsilon_o}$$

Gaussian surfaces are shown in [https://www.mathcha.io/editor/kMNEMierUZnHDQYLZBsDZ1B36TLgxqBxh168Mvn Figure 2.]

Gaussian surface 1.

$$\epsilon_oE_{lc}A + \epsilon_oE_lA = \sigma_lA + \rho_oxA$$

$E_{lc}$, the electric field inside the left conductor, is zero so this simplifies to

$$1.\quad\epsilon_oE_l = \sigma_l + \rho_ox$$

Gaussian surface 2.

$$\epsilon_oE_{lc}A + \epsilon_oE_rA = \sigma_lA + \rho_o\frac{d}{2}A$$

Using $E_{lc}=0$ this simplifies to

$$2.\quad\epsilon_oE_r = \sigma_l + \rho_o\frac{d}{2}$$

Gaussian surface 3.

$$\epsilon_oE_{lc}A + \epsilon_oE_{rc}A = \sigma_lA + \rho_o\frac{d}{2}A + \sigma_rA$$

$E_{rc}$, the electric field inside the right conductor, is zero so this simplifies to

$$3.\quad 0 = \sigma_l + \rho_o\frac{d}{2} + \sigma_r$$

The electric field is related to a potential difference by

$$\psi(b)-\psi(a)=-\int_a^b \mathbf{E}\cdot d\mathbf{l}$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Note
|-
|
Quite often I see:

$$\psi = -\int \mathbf{E}\cdot d\mathbf{l} = -\int_a^b \mathbf{E}\cdot d\mathbf{l}$$

This is not correct. Either use the indefinite integral

$$\psi = -\int \mathbf{E}\cdot d\mathbf{l}$$

and solve for the constant of integration using the potential at a location where it is known or use the definite integral 

$$\psi(b)-\psi(a)=-\int_a^b \mathbf{E}\cdot d\mathbf{l}$$

or

$$\psi(x)-\psi(a)=-\int_a^x \mathbf{E}\cdot d\mathbf{l}$$

both of which has no constant of integration.

Also, avoid writing $\psi$ with no argument; use $\psi(x)$ to indicate a potential that depends on position and $\psi(b)$ to indicate the potential at a fixed position, where $b$ is a constant.
|}

The potential difference between the conducting plates is

$$\psi(d) - \psi(0) = -\int_0^dE(\thinspace dx = -\int_0^{d/2}E_l(\thinspace dx - \int_{d/2}^dE\thinspace dx$$

Both plates are grounded so $\phi(0)=\phi(d)=0$ and

$$0 - 0 = -\int_0^{d/2}E_l(\thinspace dx - \frac{d}{2}E_r$$

where the fact that $E_r$ is constant from equation 2. was used. Substituting $E_l$ and $E_r$ found using Gaussian surfaces 1. and 2. gives

$$0 = -\left[\sigma_lx + \rho_o\frac{x^2}{2}\right]_0^{d/2} - \frac{d}{2}\left(\sigma_l + \rho_o\frac{d}{2}\right)$$

This gives

$$\sigma_l=-\frac{3}{8}\rho_od$$

Using $0 = \sigma_l + \frac{1}{2}\rho_od + \sigma_r$ found using Gaussian surface 3.,

$$\sigma_r=-\frac{1}{8}\rho_od$$

Substitution of $\sigma_l$ into equations 1. and 2. gives

$$\epsilon_oE_l = -\frac{3}{8}\rho_od+ \rho_ox$$

$$\epsilon_oE_r = -\frac{3}{8}\rho_od + \frac{1}{2}\rho_od=\frac{1}{8}\rho_od$$

Because the functional form electric field changes at $x=d/2$, we need to find expressions for the potential in each region.

For $x \le d/2$, $\psi_l(x)-\psi(0) = \psi_l(x)=-\int_0^x E_l(x\thinspace dx'$. Integration gives

$$\psi_l(x)=\frac{\rho_o}{\epsilon_o}\frac{x}{2}\left(\frac{3}{4}d-x\right)\qquad x\le d/2$$

For $x \ge d/2$, $\psi_r(x)-\psi(0) = -\int_0^{d/2} E_l(x\thinspace dx'-\int_{d/2}^x E\thinspace dx'$. Integration gives

$$\psi_r(x)=\frac{\rho_o}{\epsilon_o}\frac{d}{8}(d-x)\qquad d/2 \le x\le d$$

The potential has a maximum inside the charged slab at $x=3d/8$.

Checks:

* Just outside of conductor, $\mathbf{E}\cdot \hat{\mathbf{n}} = \sigma/\epsilon_o$ so we expect $E_l(0)=\sigma_l/\epsilon_o$, $E_r(d)=-\sigma_r/\epsilon_o$.
* $E_r$ is constant - this is expected because $\boldsymbol{\nabla}\cdot \mathbf{E} = -\rho/\epsilon_o$ and $\rho=0$ in that region; because problem is 1-D, $\boldsymbol{\nabla}=d/dx$ giving $d E_r/dx = 0\Rightarrow E_r=const$.
* $\psi_l$ and $\psi_r$ satisfy $\psi_l(0)=0$ and $\psi_r(d)=0$ and $\psi_l(d/2)=\psi_r(d/2)$.
* The meaning of $x=3d/8$ - at this value of $x$, the amount of charge to the left is zero: $\sigma_lA+3\rho_oAd/8=0$ as is the amount of charge to the right: $\rho_oAd/8+\sigma_rA+=0$. The slope of the potential is zero and this corresponds to a net force of zero on a test charge and  hence an electric field of zero, which was found.

'''Gauss' Law + Reciprocity Method'''

The reciprocity equation stated in problem 1.12 of Jackson can be used to determine the charge density $\sigma_l$ on the left conductor (see [[#HW_2|HW #2]]). In this case, steps 3. and 4. in the Gauss' Law method are not needed. One can use the equations for $E_r$ and $E_l$ from Gaussian surfaces 1. and 2. in the Gauss' Law method, which depend on only one unknown: $\sigma_l$. The potentials are then found in the same way as before, using

For $x \le d/2$

$$\psi_l(x)-\psi(0) = -\int_0^x E_l dx$$

For $x \ge d/2$

$$\psi_r(x)-\psi(0) = -\int_0^{d/2} E\thinspace dx-\int_{d/2}^x E\thinspace dx$$

'''Green Function Method'''

From HW 5.1, with the replacement of $w$ with $d$,

$$G_D(x,x') = \frac{4\pi}{Ad}\Big[(d-x')x\Theta(x'-x)+(d-x)x'\Theta(x-x')\Big]$$

Let $\mathcal{V}$ be the volume between the plates. On four of the surfaces of $\mathcal{V}$, $\partial G/\partial n'=0$. On two of the surfaces, $\Psi=0$. As a result, the second term in

$$\Psi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G_D(\mathbf{x},\mathbf{x}')\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\Psi(\mathbf{x}')\frac{\partial G_D}{\partial n'} da'$$

is zero leaving. $G$ does not depend on $y$ and $z$, so this simplifies to

$$\Psi(x)=\frac{A}{4\pi\epsilon_o}\int_0^dG_D(x,x')\rho(x') dx'$$

Using $\rho(x')=\rho_o\Theta(d/2-x')$, the limits of integration are modified

$$\Psi(x)=\frac{A\rho_o}{4\pi\epsilon_o}\int_0^{d/2}G_D(x,x') dx'$$

Substitution of $G_D(x,x')$ in this equation gives

$$\Psi(x)=\frac{\rho_o}{d\epsilon_o}\int_0^{d/2}\Big[(d-x')x\Theta(x'-x)+(d-x)x'\Theta(x-x')\Big] dx'$$

The arguments to the $\Theta$ depend on $x$. By plotting $\Theta(x'-x)$ and $\Theta(x-x')$, one can see that that the limits of integration will depend on $x$.

If $x \gt d/2$, and for the limits of integration that correspond to $x'=[0,d/2]$,

$\Theta(x'-x)=0$ and $\Theta(x-x')=1$ for all $x'$.

Calling the potential for $x \gt d/2$ $\Psi_r$, the required integration is of the second term in $G$:

$$\Psi_r(x)=\frac{\rho_o}{d\epsilon_o}\int_0^{d/2}(d-x)\thinspace dx'$$

$$\Psi_r(x)=\frac{\rho_o}{\epsilon_o}\frac{d}{8}(d-x)$$

If $x \lt d/2$, and for the limits of integration that correspond to $x'=[0,d/2]$, 

$\Theta(x'-x)=1$ only when $x'\gt x$ and

$\Theta(x-x')=1$ only when $x'\lt x$. 

Using this to modify the limits of integration gives the required integration of

$$\Psi_l(x)=\frac{\rho_o}{d\epsilon_o}\left[\int_x^{d/2}(d-x'\thinspace dx'+\int_0^{x}(d-x)\thinspace dx'\right]$$

$$\Psi_l(x)=\frac{\rho_o}{\epsilon_o}\frac{x}{2}\left(\frac{3}{4}d-x\right)$$

The surface charge densities can be computed and compared with previous answers:

$$\sigma_l=-\epsilon_o\frac{\partial \Psi_l}{\partial x}=-\frac{3}{8}\rho_od$$

$$\sigma_r=\epsilon_o\frac{\partial \Psi_r}{\partial x}=-\frac{1}{8}\rho_od$$

The motivation for asking for the charge densities was as a hint of a way to check your answer.
|}

## Parallel Plates with Charged Slab III

#1-d-cartesian-green-function&l=775&c=1

## 1-D Spherical -- Outer boundary at $\infty$

#1-d-spherical-green-function&l=942&c=1

## 2-D

### Long Tube with Sheet of Charge

#long-rectangular-tube-with-sheet-of-charge&l=1240&c=1

### Long Tube with Line of Charge

See HW 6.1

### U-Shaped Channel 

A U-shaped, conducting, and grounded channel is shown in Fig. 1a; its cross-section is shown in Fig. 1b. The channel is infinite in the $\pm z$ and the top and bottom parts extend to $x=+\infty$.

An infinitely long (in the $\pm z$-direction) non-conducting sheet of charge with a surface charge density of $\sigma'$ is placed inside the tube at $x=d$ as shown.

[[Image:Uchannel2.png|500px]]

1. Find $\psi(x,y)$

2. Find an equation for the surface charge density at $(x,y)=(0,1/2)$ in the form of an infinite series.

3. For $d=0$, uses Gauss' law to find an expression for the surface charge density at $(x,y)=(0,1/2)$ that is not in the form of an infinite series. Provide a diagram and discuss all surfaces of your Gaussian surface.

4. Find $\psi(x,y)$ when an infinitely long (in the $\pm z$-direction) non-conducting slab of charge with a volume charge density $\rho'$ fill the region between $x=0$ to $x=d$ and $y=0$ to $y=1$

Extra credit: Show that the result of 2. evaluated at $d=0$ is equivalent to the result of 3.

Note: Initial version had $x'$ in part 3. and extra credit statement instead of $d$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
In the following, I used $x'$ instead of $d$ for the location of $\sigma'$. The motivation for using $d$ in the problem statement was to make sure that you knew to change $d$ to $x'$ in $\psi$ when doing the integral for part 4.

Justifications for steps that are the same as used in the previous problem are not repeated.

Outside of the channel, the potential is zero. (The conductor shields the outside from electric fields.) To see this formally, consider a [https://www.mathcha.io/editor/K4BjWfWBUm3TGdOEdHkNBgDcZzznM2CwVxxdl large sphere that encloses the channel] but has a slot corresponding to the surface of the channel. Laplace's equation is satified in the shaded volume. The part of the volume that touches the channel is at a potential of zero. As the radius of the sphere approaches infinity, the surface of the sphere is far away from all charges and so the potential on the outer surface is zero. The potential $\psi=0$ satisfies Laplace's equations and the boundary conditions on the surface of the volume, so the solution for the potential in the volume is zero. 

1.

$$\psi_l(x,y) = \sum_{n=1}^{\infty} A_n\sin(n\pi y)\sinh(n\pi x)$$

$$\psi_r(x,y) = \sum_{n=1}^{\infty} B_n\sin(n\pi y)e^{-n\pi x}$$

$$\psi_l(x',y) = \psi_r(x',y)$$

$$\sum_{n=1}^{\infty} \sin(n\pi y)\Big[A_n\sinh(n\pi x')-B_ne^{-n\pi x'}\Big] = 0$$

$$A_n = B_n\frac{e^{-n\pi x'}}{\sinh(n\pi x')}$$

$$\psi_l = \sum_{n=1}^{\infty} B_ne^{-n\pi x'}\frac{\sinh(n\pi x)}{\sinh(n\pi x')}\sin(n\pi y)$$

$$\psi_r = \sum_{n=1}^{\infty} B_ne^{-n\pi x}\sin(n\pi y)$$

$$\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$$

$$\sum_{n=1}^{\infty} B_n\sin(n\pi y)\left[n\pi e^{-n\pi x'}+n\pi e^{-n\pi x'}\frac{\cosh(n\pi x')}{\sinh(n\pi x')}\right]=\frac{\sigma'}{\epsilon_o}$$

Using $\sinh(u)+\cosh(u)=e^u$, this can be written as

$$\sum_{n=1}^{\infty} B_n\left(\frac{n\pi }{\sinh(n\pi x')}\right)\sin(n\pi y)=\frac{\sigma'}{\epsilon_o}$$

Multiply both sides by $\sin(l\pi \thinspace dy$ and integrate from $y=0$ to $y=1$ and use

$$
\int_0^1\sin(l\pi y)\sin(n\pi \thinspace dy=
\begin{cases}
\frac{1}{2} & \text{if $n=l$}\\
0 & \text{otherwise}
\end{cases}
$$

$$
\int_0^1\sin(l\pi \thinspace dy=
\begin{cases}
\frac{2}{l\pi} & l=1,3,...\\
0 & \text{otherwise}
\end{cases}
$$

$$\psi_l = \frac{4\sigma'}{\pi^2\epsilon_o}\sum_{n=1,3,...}^{\infty} \frac{e^{-n\pi x'}}{n^2} \sinh(n\pi x)\sin(n\pi y)$$

$$\psi_r = \frac{4\sigma'}{\pi^2\epsilon_o}\sum_{n=1,3,...}^{\infty} \frac{e^{-n\pi x}}{n^2} \sinh(n\pi x')\sin(n\pi y)$$

Notice that $\psi_l(x,y;x')=\psi_r(x',y;x)$.

2.

$$\sigma_l(y) = -\epsilon_o\frac{\partial \psi_l}{\partial x}\Bigg|_{x=0}$$

$$\sigma_l(y) = -\frac{4\sigma'}{\pi}\sum_{n=1,3,...}^{\infty} e^{-n\pi x'} \cosh(n\pi 0) \sin(n\pi y) $$

$$\sigma_l(1/2; x'=0) = -\frac{4\sigma'}{\pi}\sum_{n=1,3,...}^{\infty} e^{-n\pi 0}{\cosh(n\pi 0)} \sin(n\pi/2) $$

$$\sigma(1/2; x'=0) = -\frac{4\sigma'}{\pi}\sum_{l=0}^{\infty} \frac{(-1)^l}{2l+1}$$

This sum is a well-known way to generate $\pi$ and it evaluates to $\pi/4$ giving

$$\sigma(1/2; x'=0) = -\sigma'$$

3.

A [https://www.mathcha.io/editor/K4BjWfWBUm3TGdOEdHkNBgDcZzznM2CwVxxdl Gaussian cylinder] centered on $y=1/2$ with one end-cap in the conductor and the other at any $x$ has an enclosed charge of $\sigma'A + \sigma(1/2)$. When $x'=0$, one can compute the field using $\psi_r$ and show that $E_x(x,y)=E_y(x,y)=0$ and so there is no flux through the cylinder. Gauss' law then gives

$$0 = \sigma'A + \sigma A$$

$$\sigma = -\sigma'\qquad\text{(for all }y\text{)}$$

When the sheet of charge is next to the left surface, the surface charge density on that surface is equal and opposite to the surface charge density on the charged sheet. The field everywhere is zero.

If $x'\ne 0$, one would need to account for the flux through the curved surface because $\mathbf{E}\ne 0$ and Gauss' law will not give a simple answer as was the case here.

4.

$$G=\frac{4\pi\epsilon_o}{\sigma' A}[\psi_l(x,x')\Theta(x'-x) + \psi_r(x,x')\Theta(x-x')]$$

If the volume is the volume inside the channel, then the potential is zero on three surfaces of this volume; $\partial G/\partial z$ is zero on two surfaces. The fact that $\partial G/\partial x=0$ on the surface at $x=\infty$ can be shown by direct calculation.

$$\Phi(x) = \frac{1}{4\pi\epsilon_o}\int_0^{\infty} G(x,x')\rho(x\thinspace d^3x'$$

Using

$$\rho(x')=\rho_o\Theta(d-x')$$

this is

$$\Phi(x) = \frac{1}{4\pi\epsilon_o}\int_0^{\infty} G(x,x')\rho(x\thinspace d^3x'$$

Using $G$ in terms of $\psi_l$ and $\psi_r$, this is

$$\Phi(x) = \frac{\rho_o}{\epsilon_o}\int_0^d \Big[\psi_l(x,x')\Theta(x'-x) + \psi_r(x,x')\Theta(x-x')\Bi\thinspace dx'$$

$$x\lt d$$

$$\Phi(x) = \frac{\rho_o}{\epsilon_o}\left[\int_0^d \psi_l(x,x\thinspace dx' + \int_0^x \psi_r(x,x\thinspace dx'\right]$$

$$\Phi(x) = \frac{4\rho_o}{\pi^3\epsilon_o}\sum_{n=1,3,...}^{\infty}\frac{\sin(n\pi y)}{n^3}[1-e^{-n\pi x} - e^{-n\pi d}\sinh(n\pi x)]$$

$$x\gt d$$

$$\Phi(x) = \frac{\rho_o}{\epsilon_o}\int_0^d \psi\thinspace dx'$$

$$\Phi(x) = \frac{4\rho_o}{\pi^3\epsilon_o}\sum_{n=1,3,...}^{\infty}\frac{\cosh(n\pi d)-1}{n^3}e^{-n\pi x}\sin(n\pi y)$$

## Long Cylinder 

For a long, grounded, and hollow cylinder with radius $b$ aligned with, and centered on, the $z$-axis,

1. find $G(s,\phi;s',\phi')$ using the solution to an appropriate method of images problem (as was done in [[S2020/Problems#Sphere|HW 7.2.1]] for a sphere);
1. find $G(s,\phi;s',\phi')$ by finding equations for the potential outside of the cylinder when it is surrounded by a co-aligned cylindrical shell of radius $s'$ with a charge density that is proportional to $\delta(\phi-\phi')$ (similar to what was done in [[S2020/Problems#Sphere|HW 7.2.2]] for a sphere); and
1. use Equation 1.44 of Jackson and a Green function to find the potential outside of the cylinder when it is held at a potential of $V_u$ for $0\lt \phi \lt \pi$ and $V_l$ for $\pi \lt \phi\lt 2\pi$.

4. Find the potential outside of the cylinder for the boundary potential given in part 3. using the boundary value method.

## 3-D

### Infinite Dome or Infinite Plane

#green-function-for-infinite-dome&l=1063&c=1

## Green Functions 

Green's theorem (second identity) derived earlier is

$$\int_{\mathcal{V}} \left(\phi\nabla^2\psi -\psi\nabla^2\phi\right)d^3x=\oint_{\mathcal{S}}\left(\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}\right) da$$

Assume that $\phi$ is an electric potential associated in a volume $\mathcal{V}$ with a continuous scalar volume charge density $\rho$ in $\mathcal{V}$ and charges on the surface of $S$ of $\mathcal{V}$ held at a known potential, Now, instead of using

$$\psi(\mathbf{x})=\frac{1}{|\mathbf{x}-\mathbf{x}'|}$$

use

$$\psi(\mathbf{x})=\frac{1}{|\mathbf{x}-\mathbf{x}'|}+F(\mathbf{x},\mathbf{x}')$$

9. What is the constraint on $F$ so that one can write

$$\int_{\mathcal{V}} \left(-4\pi\phi(\mathbf{x'})\delta(\mathbf{x}-\mathbf{x}')+\psi(\mathbf{x}')\rho(\mathbf{x'})/\epsilon_o\right)d^3x'=\oint_{\mathcal{S}}\left(\phi\frac{\partial \psi}{\partial n'}-\psi\frac{\partial \phi}{\partial n'}\right) da'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

$$\nabla^2F(\mathbf{x},\mathbf{x}')=0$$

Writing the LHS integral with primed integration variables and explicitly writing out the functional dependence gives

$$I = \int_{\mathcal{V}} \left[\phi(\mathbf{x'})\nabla'^2\psi(\mathbf{x'}) -\psi(\mathbf{x'})\nabla'^2\phi(\mathbf{x'})\right]d^3x'$$

In primed coordinates

$$\psi(\mathbf{x}')=\frac{1}{|\mathbf{x}'-\mathbf{x}|}+F(\mathbf{x}',\mathbf{x})$$

We need to evaluate $\nabla'^2\psi(\mathbf{x'})$ in the integral, which gives

$$\nabla'^2\psi(\mathbf{x'})=\nabla'^2\frac{1}{|\mathbf{x}'-\mathbf{x}|}+\nabla'^2F(\mathbf{x'},\mathbf{x})=-4\pi\delta(\mathbf{x}'-\mathbf{x})+\nabla'^2F(\mathbf{x}',\mathbf{x})$$

With $\nabla'^2\phi(\mathbf{x'})=-\rho(\mathbf{x'})/\epsilon_o$ and $\nabla'^2F(\mathbf{x}',\mathbf{x})=0$, we can write

$$I = \int_{\mathcal{V}} \left[\phi(\mathbf{x'})\nabla'^2\psi(\mathbf{x'}) -\psi(\mathbf{x'})\nabla'^2\phi(\mathbf{x'})\right]d^3x$$

as

$$I=\int_{\mathcal{V}} \left[-4\pi\phi(\mathbf{x'})\delta(\mathbf{x}-\mathbf{x'})+\psi(\mathbf{x}')\rho(\mathbf{x'})/\epsilon_o\right]d^3x'$$
|}

10. What is an additional constraint on $F$ so that one can write

$$\int_{\mathcal{V}}\left[-4\pi\phi(\mathbf{x'})\delta(\mathbf{x}-\mathbf{x'})+\psi(\mathbf{x}')\rho(\mathbf{x'})/\epsilon_o\right]d^3x'=\oint_{\mathcal{S}}\phi\frac{\partial \psi}{\partial n'} da'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$$F(\mathbf{x}',\mathbf{x})=-\frac{1}{|\mathbf{x}'-\mathbf{x}|}\quad\mbox{for}\thinspace\mathbf{x}'\mbox{on}\thinspaceS$$

This corresponds to $\psi(\mathbf{x}')=0$ on $S$.

The integral

$$\oint_{\mathcal{S}}\psi\frac{\partial \phi}{\partial n'}da'$$

must be zero. One way for this to be true is for $\psi(\mathbf{x}')$ to be zero on $S$, 

$$\psi(\mathbf{x}')=0=\frac{1}{|\mathbf{x}'-\mathbf{x}|}+F(\mathbf{x}',\mathbf{x})$$

so that

$$F(\mathbf{x}',\mathbf{x})=-\frac{1}{|\mathbf{x}'-\mathbf{x}|}$$

on $S$. Note that this gives $\psi(\mathbf{x}')=0$ on $S$, but inside of $\mathcal{V}$, $\psi(\mathbf{x}')$ is in general zero.
|}

Evaluation of the first term in the volume integral and rearrangement gives

$$\phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}\psi(\mathbf{x}')\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\phi\frac{\partial \psi}{\partial n'} da'$$

11. Explain how this equation justifies the statement that if one knows how charge is distributed inside of a volume and something about the potential $\phi$ on the surface of the volume, one can compute the potential everywhere inside of the volume.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
This equation was derived under the assumption that $\mathbf{x}$ was inside $V$. The first term involves charges inside the volume; the second term involves the potential on the surface of the volume. According to this equation, we don't need information about the charges outside the volume to compute the potential inside of the volume! (Provided that we know ${\partial \psi}/{\partial n}$ on the surface.)

Note that there is an additional constraint. We need to have a function $F$ with the two properties identified above.

In summary, one can compute the potential inside of a volume $V$ given
1. ${\partial \psi}/{\partial n}$ on the surface of the volume;
1. $\rho$ inside the volume;
1. a function $F$ that has the property $\nabla^2F(\mathbf{x})=0$ and $F(\mathbf{x})=-\frac{1}{|\mathbf{x}-\mathbf{x}'|}$ for $\mathbf{x}$ on $\mathcal{S}$.

Finding the function $F$ is not trivial. It happens that one method of finding this function, which allows us to solve many electrostatic problems, is to solve a specific electrostatic problem involving a point charge and a grounded conductor. If we can solve that specific problem, we can then solve many any problem where we are given ${\partial \psi}/{\partial n}$ on the surface of a volume and $\rho$ inside the volume.

Keep in mind that "solve" in the previous paragraph means that we can find the potential using integration. In many cases the integrals do not have a known analytic solution and must be solved numerically.
|}

Consider flat and infinite plane.  

12. What is $F$ and $\mathbf{x}'$ in the equation

$$\psi(\mathbf{x})=\frac{1}{|\mathbf{x}-\mathbf{x}'|}+F(\mathbf{x},\mathbf{x}')$$

that gives $\psi(\mathbf{x})=0$ on the surface of the plane and $\nabla^2F=0$ above the plane? Recall that you found a function that had this property in a previous homework problem in which you computed the potential when a point charge was placed at a distance $d$ above an infinite, flat, and grounded plane. For generality, assume the point charge is at $\mathbf{x}'=x'\hat{\mathbf{x}}+y'\hat{\mathbf{y}}+z'\hat{\mathbf{z}}$ instead of $z_o\hat{\mathbf{z}}$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$$F(\mathbf{x},\mathbf{x}') = \frac{1}{\sqrt{(x-x')^2 + (y-y')^2 + (z+z')^2}}$$

$$\nabla^2F = -4\pi\delta(x-x')\delta(y-y')\delta(z+z')=0\quad\text{for}\thinspacez\gt 0$$
|}

This function $\psi(\mathbf{x},\mathbf{x}')$ that has above-identified properties is called a Green function for an infinite plane geometry and is re-named to as $G(\mathbf{x},\mathbf{x}')$ in what follows. This function was derived with the aid of the solution to the problem of a point charge above an infinite and grounded conducting plane. The power of knowing the Green function is that it can be used to solve for the potential in a different problem - a problem where the potential is known on an infinite plane and the charge density above the plane is zero.

Because the charge density in the different problem is zero, the first integral is zero in

$$\phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G(\mathbf{x}',\mathbf{x})\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\phi\frac{\partial G(\mathbf{x}',\mathbf{x})}{\partial n'} da'$$

and one only needs to be given the potential on the plane, $\phi(x,y,z=0)$, and to evaluate the integral

$$\phi(\mathbf{x})=-\frac{1}{4\pi}\oint_{\mathcal{S}}\phi\frac{\partial G(\mathbf{x},\mathbf{x}')}{\partial n'} da'$$

to find the potential above the plane.

Note that $n=-z$ because the volume is the half-space for which $z\gt 0$ and the normal direction always points outwards from the volume.

Using for $G(\mathbf{x},\mathbf{x}')$ the function $\psi(\mathbf{x},\mathbf{x}')$ found previously when $F$ was found, 

13. compute $\frac{\partial G(\mathbf{x},\mathbf{x}')}{\partial n'}$ at $z'=0$ and show that given $\phi(x,y,z=0)$, one can write

$$\phi(x,y,z)=\frac{1}{4\pi}\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}\phi(x',y',z'=0)\frac{2z}{\left((x-x')^2+(y-y')^2+z^2\right)^{3/2}} dx'dy'$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
The derivative calculation is straight-forward and was done in a previous problem. Starting with

$$\phi(\mathbf{x})=\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G(\mathbf{x}',\mathbf{x})\rho(\mathbf{x'}) d^3x'-\frac{1}{4\pi}\oint_{\mathcal{S}}\phi\frac{\partial G(\mathbf{x}',\mathbf{x})}{\partial n'} da'$$

The first term on the right-hand side is zero assuming that there are no other charges in the system - we are only given a plane with the potential specified on the surface.

We are given $\phi$ in the $z=0$ plane - and this plane does not form a closed surface. To close the surface, consider the system to be a hemisphere with the flat part in the $z=0$ plane. The integral given above is over the flat part of the hemisphere. To write the above equation, one must assume the potential on the hemisphere is zero (this is not often explicitly stated when this problem is given). This is consistent with $G$, which has the property of being zero for large $r$. 
|}

14. Show that if the potential is in the plane is given by $\phi(x,y,z=0)=V_o$ for $x^2+y^2\le a^2$ and  $\phi(x,y,z=0)=0$ otherwise, then the potential along the $z-$axis is

$$\phi(z)=V_o\left(1-\frac{z}{\sqrt{z^2+a^2}}\right)$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

Set $x=y=0$ and use polar coordinates with a radial coordinate $s'=\sqrt{x'^2+y'^2}$.

$$\phi(z)=\frac{1}{4\pi}\int_{0}^{2\pi}\int_{0}^{a}Vo\frac{2z}{\left(s'^2+z^2\right)^{3/2}} s'ds'd\phi'$$
$$\phi(z)=V_oz\int_{0}^{a}\frac{s'ds'}{\left(s'^2+z^2\right)^{3/2}} s'ds'=-\frac{V_oz}{\sqrt{s'^2+z^2}}\Bigg|_{s'=0}^{a}$$
$$\phi(z)=V_o\left(\frac{z}{|z|}-\frac{z}{\sqrt{z^2+a^2}}\right)$$

For $z\gt 0$, $z/|z|=1$, which gives

$$\phi(z)=V_o\left(1-\frac{z}{\sqrt{z^2+a^2}}\right)$$
|}

15. Show that for the same boundary potential  $\phi(x,y,z=0)$ and for $r^2\equiv x^2+y^2+z^2\gg a^2$, the off-axis potential can be approximated as

$$\phi(x,y,z)\approx\frac{V_oa^2}{2}\frac{z}{r^3}\left(1-\frac{3a^2}{4r^2}\right)$$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
To show this, re-write

$$\frac{1}{\left((x-x')^2+(y-y')^2+z^2\right)^{3/2}}$$

as 

$$\frac{1}{\left(r^2+s'^2-2xx'-2yy'\right)^{3/2}}$$

factor out $r$

$$\frac{1}{r^3}\frac{1}{\left(1+(s'/r)^2-2(x/r)(x'/r)-2(y/r)(y'/r)\right)^{3/2}}$$

For the integration, $s'$, $x'$, and $y'$ are $\le a$ so $s'/r\ll 1$ as is $x'/r$ and $y'/r$. The terms $y/r$ and $x/r$ can vary from $-1$ to $1$. Defining

$$\delta = (s'/r)^2-2(x/r)(x'/r)-2(y/r)(y'/r)$$

gives

$$\frac{1}{r^3}\frac{1}{\left(1+\delta\right)^{3/2}}$$

$\delta \ll 1$ as argued above. The binomial expansion (or Taylor series expansion) gives

$$\frac{1}{r^3}\frac{1}{\left(1+\delta\right)^{3/2}}\simeq \frac{1}{r^3}\left(1-\frac{3}{2}\delta\right)+...$$

Using this, the integral equation

$$\phi(x,y,z)=\frac{1}{4\pi}\int_{0}^{2\pi}\int_{0}^{a}V_o\frac{2z}{\left((x-x')^2+(y-y')^2+z^2\right)^{3/2}} s'ds'd\phi'$$

becomes

$$\phi(x,y,z)\simeq\frac{1}{4\pi}\int_{0}^{2\pi}\int_{0}^{a}V_o\frac{2z}{r^3} \left(1-\frac{3}{2}\delta\right) s'ds'd\phi'$$

or

$$\phi(x,y,z)\simeq \frac{V_o}{2}\frac{z}{r^3}\int_{0}^{2\pi}\int_{0}^{a}\left(1-\frac{3}{2}\delta\right) s'ds'$$

$$\delta = (s'/r)^2-2(x/r)(x'/r)-2(y/r)(y'/r)$$

After integrating over $\phi'$, only the first term remains because $x'=s'\cos\phi$ and $y'=s'\cos\phi$.

$$\phi(x,y,z)\simeq V_o\frac{z}{r^3}\int_{0}^{a}\left(1-\frac{3}{2}\frac{s'^2}{r^2}\right) s'ds'$$

integration gives

$$\phi(x,y,z)\approx\frac{V_oa^2}{2}\frac{z}{r^3}\left(1-\frac{3a^2}{4r^2}\right)$$

|}

For the $z$-axis solution of

$$\phi(z)=V_o\left(1-\frac{z}{\sqrt{z^2+a^2}}\right)$$

suppose a point charge is placed at $z=d$. It may seem that by superposition, the potential on the $z$-axis would be

$$\phi(z)=\frac{1}{4\pi\epsilon_o}\frac{1}{|z-d|}+V_o\left(1+\frac{z}{\sqrt{z^2+a^2}}\right)$$

However, the correct additional term is not $\frac{1}{4\pi\epsilon_o}\frac{1}{|z-d|}$ but is rather that obtained from evaluating

$$\frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}\psi(\mathbf{x}')\rho(\mathbf{x'}) d^3x'$$

with $\rho(\mathbf{x'})=q\delta(x)\delta(y)\delta(z-d)$, and $\psi=G$. Evaluation gives

$$\frac{q}{4\pi\epsilon_o}\frac{1}{|z-d|}-\frac{q}{4\pi\epsilon_o}\frac{1}{|z+d|}$$

16. Explain this.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
With the addition of the point charge, charges will appear on the conducting plane. The simple addition of the potential due only the point charges does not account for the charges that are induced on the conducting plane. Adding

$$\frac{1}{4\pi\epsilon_o}\frac{1}{|z-d|}-\frac{1}{4\pi\epsilon_o}\frac{1}{|z+d|}$$

is equivalent to the superposition of the potential created by the disk at potential $a$ and the potential due to a point charge above an infinite plane.
|}

## Between Spherical Shells

1. Show the steps required to obtain equation 3.114 from equation 2.16 (both in Jackson 3rd edition).
1. Show that equation 3.114 can be obtained using the same technique used to find the Green function in the previous problem (the Long Tube problem). Do this by assuming a shell of charge at $r=r'$ with density $\sigma'(\theta,\phi)$ and finding the potential in two regions: $a \le r \lt r'$ and $r\gt r'$. To obtain 3.114 of Jackson, you will need to use $\sigma'(\theta,\phi)=q\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')/4\pi r'^2$.
1. Use equation 3.114 and equation 1.44 of Jackson to find the potential outside of a sphere of radius $a$ for which the upper hemisphere ($z\gt 0$) is held at a potential of $V_o$ and the lower hemisphere ($z\lt 0$) is held at $-V_o$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
1.

Equation 2.16 is

$$G(\mathbf{x},\mathbf{x}')=\frac{1}{|\mathbf{x}-\mathbf{x}'|}  - \frac{a}{x'}\frac{1}{\left|\mathbf{x}-\frac{a^2}{x'^2}\mathbf{x}'\right|}$$

where $x'\equiv |\mathbf{x}'|$ and so it has the same meaning as $r'$ used in Chapter 3. I am not sure why he did not use $r'$ in equation 2.16 and in Chapter 3 he switches to using $|\mathbf{x}'|=r'$. (This is why using a vector named $\mathbf{x}$ is an awkward choice of notation. When using cartesian coordinates is $x$ $|\mathbf{x}|$ or $\sqrt{x^2+y^2+z^2}$?)

The first term in $G$ is the same as equation 3.70:

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r_\lt^{l}}{r_\gt^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

Treating the second term requires some effort. First, define $\mathbf{y}\equiv (a^2/r'^2)\mathbf{x}'$ so that $|\mathbf{y}|=(a^2/r'^2)|\mathbf{x}'|=a^2/r'$.

<code>!!!</code>Next, consider $\frac{1}{\left|\mathbf{x}-\mathbf{y}'\right|}$. The angle between $\mathbf{x}$ and $\mathbf{y}'$ is the same as the angle between  $\mathbf{x}$ and $\mathbf{x}'$ because $\mathbf{y}'$ is a multiple of $\mathbf{x}'$. For this reason, the primed angular terms will be the same as in equation 3.70. Whe using equation 3.70, there are two cases

$$r\gt |\mathbf{y}'|\quad\Rightarrow\quad r \gt \frac{a^2}{r'}\quad\text{or}\quad rr'\gt a^2$$

In this case, $r_{\gt}=r$ and $r_{\lt} = a^2/r'$.

The other case is

$$r\lt |\mathbf{y}'|\quad\Rightarrow\quad r \lt \frac{a^2}{r'}\quad\text{or}\quad rr'\lt a^2$$

In this case, $r_{\gt}=a^2/r'$ and $r_{\lt} = r$.

The Green function applies to two domains: $0\le r\le a$ and $r \gt a$ and $r'$ covers the same domain as $r$.

We want the Green function for the domain $r \gt a$, which corresponds to the case $rr'\gt a^2$ for which $r_{\gt}=r$ and $r_{\lt} = a^2/r'$. Therefore, for $r\gt a$, $1/\left|\mathbf{x}-\mathbf{y}'\right|$

is

$$\frac{1}{|\mathbf{x}-\mathbf{y}'|} = \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{(a^2/r')^{l}}{r^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

and so

$$G(\mathbf{x},\mathbf{x}')=\frac{1}{|\mathbf{x}-\mathbf{x}'|}  - \frac{a}{r'}\frac{1}{\left|\mathbf{x}-\mathbf{y}'\right|} $$

is

$$G(\mathbf{x},\mathbf{x}')= \sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\left(\frac{r_\lt^{l}}{r_\gt^{l+1}}-\frac{a}{r'}\frac{(a^2/r')^{l}}{r^{l+1}}\right)Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

or

$$G(\mathbf{x},\mathbf{x}')= 4\pi\sum_{l,m} \frac{1}{2l+1}\left[\frac{r_\lt^{l}}{r_\gt^{l+1}}-\frac{1}{a}\left(\frac{a^2}{rr'}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

2.

The general solution to $\nabla^2\Phi(r,\theta,\phi)=0$ is

$$\Phi(r,\theta,\phi)=\sum_{l,m}^l \left(A_{lm}r^l+\frac{B_{lm}}{r^{l+1}}\right)Y_{lm}(\theta,\phi)$$

$\nabla^2\Phi(r,\theta,\phi)=0$ in two regions: the inner, $i$, for which $a\le r\lt r'$ and the outer, $o$, for which $r\gt r'$

In order to match the boundary condition that $\Phi^o(r\rightarrow\infty,\theta,\phi)\rightarrow 0$, the constants for $r^l$ must be zero, so the equation in the outer region simplifies to

$$\Phi^o(r,\theta,\phi)=\sum_{l,m} \frac{B^o_{lm}}{r^{l+1}}Y_{lm}(\theta,\phi)$$

The inner solution is

$$\Phi^i(r,\theta,\phi)=\sum_{l,m} \left(A^i_{lm}r^l+\frac{B^i_{lm}}{r^{l+1}}\right)Y_{lm}(\theta,\phi)$$

The boundary condition $\Phi^i(a,\theta,\phi)=0$ gives

$$1.\quad B^i_{lm}=-A^i_{lm}a^{2l+1}$$

The continuity condition $\Phi^i(r',\theta,\phi)=\Phi^o(r',\theta,\phi)$ gives

$$B_{lm}^o=A_{lm}^ir'^{2l+1}+B_{lm}^i$$

which, when combined with 1. gives

$$2.\quad B^o_{lm}=A^i_{lm}\left(r'^{2l+1}-a^{2l+1}\right)$$

And so the inner potential simplifies to

$$\Phi^i(r,\theta,\phi)=\sum_{l,m} A^i_{lm}\left(r^l-\frac{a^{2l+1}}{r^{l+1}}\right)Y_{lm}(\theta,\phi)$$

At this point, $\Phi^o$ will be kept in terms of $B^o_{lm}$. The jump condition is

$$\frac{\sigma'}{\epsilon_o}=\left[-\frac{\partial \Phi^o}{\partial r}+\frac{\partial \Phi^i}{\partial r}\right]_{r=r'}$$

With

$$\frac{\partial \Phi^o}{\partial r}=\sum_{l,m}-(l+1)\frac{B^o_{lm}}{r^{l+2}}Y_{lm}(\theta,\phi)$$

and

$$\frac{\partial \Phi^i}{\partial r}=\sum_{l,m} A^i_{lm}\left(lr^{l-1}+(l+1)\frac{a^{2l+1}}{r^{l+2}}\right)Y_{lm}(\theta,\phi)$$

the jump condition is

$$\frac{\sigma'}{\epsilon_o}=\sum_{l,m}\left[(l+1)\frac{B^o_{lm}}{r'^{l+2}}+\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)A^i_{lm}\right]$$

where $\sigma'(\theta,\phi)=q\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')/4\pi r'^2$ from the problem statement.

Multiply both sides by $Y^*_{l'm'}(\theta,\phi)d\Omega$ and integrate over the solid angle. The left-hand-side is

$$
\begin{array}
&\displaystyle\int \frac{\sigma'}{\epsilon_o}Y^*_{l'm'}(\theta,\phi)d\Omega & = \displaystyle\int \frac{q}{4\pi\epsilon_o r'^2}\delta(\cos\theta-\cos\theta')\delta(\phi-\phi') Y^*_{l'm'}(\theta,\phi)d(\cos\theta) d\phi\\
& =\frac{q}{4\pi\epsilon_or'^2}Y^*_{l'm'}(\theta',\phi')
\end{array}
$$

The right-hand-side is

$$\sum_{l,m}\left[(l+1)\frac{B^o_{lm}}{r'^{l+2}}+\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)A^i_{lm}\right]\int Y^*_{l'm'}Y^*_{lm}d\Omega$$

With, $\int Y^*_{l'm'}Y^*_{lm}d\Omega=\delta_{ll'}\delta_{mm'}$, it reduces to

$$(l+1)\frac{B^o_{l'm'}}{r'^{l+2}}+\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)A^i_{l'm'}$$

This leaves

$$\frac{Y^*_{lm}(\theta',\phi')}{4\pi\epsilon_or'^2}=(l+1)\frac{B^o_{lm}}{r'^{l+2}}-\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)A^i_{lm}$$

Using the relationship found earlier

$$2.\quad B^o_{lm}=A^i_{lm}\left(r'^{2l+1}-a^{2l+1}\right)$$

$$
\begin{align}
\frac{Y^*_{lm}(\theta',\phi')}{4\pi\epsilon_or'^2} & =(l+1)\frac{A^i_{lm}\left(r'^{2l+1}+a^{2l+1}\right)}{r'^{l+2}}-\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)A^i_{lm}\\
& = \left[(l+1)\frac{\left(r'^{2l+1}-a^{2l+1}\right)}{r'^{l+2}}+\left(lr'^{l-1}+(l+1)\frac{a^{2l+1}}{r'^{l+2}}\right)\right]A^i_{lm}\\
& = \left[(l+1)\frac{r'^{2l+1}}{r'^{l+2}}+lr'^{l-1}\right]A^i_{lm}\\
& =A_{lm}^i(2l+1)r'^{l-1}\\
\end{align}
$$

Thus,

$$A_{lm}^i = \frac{qY^*_{lm}(\theta',\phi')}{4\pi\epsilon_o(2l+1)r'^{l+1}}$$

Using 1. and 2. gives

$$B_{lm}^i = -\frac{qY^*_{lm}(\theta',\phi')}{4\pi\epsilon_o(2l+1)r'^{l+1}}a^{2l+1} \qquad \quad B_{lm}^o = \frac{qY^*_{lm}(\theta',\phi')}{4\pi\epsilon_o(2l+1)r'^{l+1}}(r'^{2l+1}-a^{2l+1})$$

Using these in the equations for $\Phi$ that we left off with of

$$\Phi^i(r,\theta,\phi)=\sum_{l,m} A^i_{lm}\left(r^l-\frac{a^{2l+1}}{r^{l+1}}\right)Y_{lm}(\theta,\phi)$$

$$\Phi^o(r,\theta,\phi)=\sum_{l,m} \frac{B^o_{lm}}{r^{l+1}}Y_{lm}(\theta,\phi)$$

gives

$$\Phi^i(r,\theta,\phi)=\sum_{l,m} \frac{q}{4\pi\epsilon_o(2l+1)}\left(r^l-\frac{a^{2l+1}}{r^{l+1}}\right)\frac{1}{r'^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$$\Phi^o(r,\theta,\phi)=\sum_{l,m} \frac{q}{4\pi\epsilon_o(2l+1)r'^{l+1}}\frac{r'^{2l+1}-a^{2l+1}}{r^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$\Phi^o$ can be written in a form that reveals the fact that $\Phi^o(r,r')=\Phi^i(r',r)$

$$\Phi^o(r,\theta,\phi)=\sum_{l,m} \frac{q}{4\pi\epsilon_o(2l+1)}\left(r'^{l}-\frac{a^{2l+1}}{r'^{l+1}}\right)\frac{1}{r^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

The equations have the symmetry of a Dirichlet Green function and the radial term also matches Equation 3.115 of Jackson (which follows trivially from 3.114). The scaling factor between $\Phi$ and $G$ is found by noting that

$$\nabla^2G=-4\pi\delta(\mathbf{x}-\mathbf{x}')$$

using the spherical representation of $\delta(\mathbf{x}-\mathbf{x}')$ is

$$\nabla^2G=-4\pi\frac{\delta(r-r')}{r'^2}\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')$$

We solved

$$\nabla^2\Phi=-\frac{\rho}{\epsilon_o}$$

with, to start,

$$\rho=\frac{q}{4\pi r'^2}\delta(r-r')=\sigma'\delta(r-r')$$

Then $\sigma'$ was replaced with $q\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')/4\pi r'^2$ giving

$$\rho=q\frac{\delta(r-r')}{4\pi r'^2}\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')$$

and so the Poisson equation that we solved

$$\nabla^2\Phi=-\frac{q}{4\pi\epsilon_o}\frac{\delta(r-r')}{ r'^2}\delta(\cos\theta-\cos\theta')\delta(\phi-\phi')$$

Comparing the equations for and $\nabla^2G$ and $\nabla^2\Phi$ gives

$$\frac{G}{4\pi} = \frac{4\pi\epsilon_o}{q} \Phi$$

Using this gives the Green function associated with $\Phi$:

$$G(r,\theta,\phi)=4\pi\sum_{l,m} \frac{1}{2l+1}\left(r^l-\frac{a^{2l+1}}{r^{l+1}}\right)\frac{1}{r'^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)\qquad r\lt r'$$

$$G(r,\theta,\phi)=4\pi\sum_{l,m} \frac{1}{2l+1}\left(r'^{l}-\frac{a^{2l+1}}{r'^{l+1}}\right)\frac{1}{r^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)\qquad r\gt r'$$

Which can be rearranged to the form of equation 3.114 of Jackson.

$$G(r,\theta,\phi)=4\pi\sum_{l,m} \frac{1}{2l+1}\left[\frac{r^l}{r'^{l+1}}-\frac{1}{a}\left(\frac{a^2}{rr'}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)\qquad r\lt r'$$

$$G(r,\theta,\phi)=4\pi\sum_{l,m} \frac{1}{2l+1}\left[\frac{r'^l}{r^{l+1}}-\frac{1}{a}\left(\frac{a^2}{rr'}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)\qquad r\gt r'$$

3.

Key steps given only for now. See previous problems with similar steps for justifications.

$$G = G_{r\lt r'}\Theta(r'-r) + G_{r\gt r'}\Theta(r-r')$$

$$\frac{\partial G}{\partial n'} = -\frac{\partial G}{\partial r'}=-\frac{\partial G_{r\lt r'}}{\partial r'}\Theta(r'-r)-\frac{\partial G_{r\gt r'}}{\partial r'}\Theta(r-r')$$

Keep first term because $r'=a$ means $r\ge a$.

$$\frac{\partial G}{\partial n'}=-\frac{\partial G_{r\gt r'}}{\partial r'}=-4\pi\sum_{l,m} \frac{1}{2l+1}\frac{\partial}{\partial r'}\left[\frac{r'^l}{r^{l+1}}-\frac{1}{a}\left(\frac{a^2}{rr'}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$$\frac{\partial G}{\partial n'}=-4\pi\sum_{l,m} \frac{1}{2l+1}\left[\frac{lr'^{l-1}}{r^{l+1}}+(l+1)\frac{1}{a}\left(\frac{a^2}{rr'^2}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$$\frac{\partial G}{\partial n'}\Bigg|_{r'=a}=-4\pi\sum_{l,m} \frac{1}{2l+1}\left[\frac{la^{l-1}}{r^{l+1}}+(l+1)\frac{1}{a}\left(\frac{a^2}{ra^2}\right)^{l+1}\right]Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$$\frac{\partial G}{\partial n'}\Bigg|_{r'=a}=-4\pi\sum_{l,m} \frac{a^{l-1}}{r^{l+1}}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)$$

$$\Psi(\mathbf{x})=-\frac{1}{4\pi}\oint_{\mathcal{S}} \Psi(\mathbf{x}')\frac{\partial G}{\partial n'}\Bigg|_{r'=a}da'$$

$G$ is proportional to potential and the surface charge density on the conductors is proportional to $\partial \Psi/\partial r$ at $r=a$; this equations is equivalent to computing the potential due to the charges on the conductor.

$$\Psi(\mathbf{x})=-\frac{1}{4\pi}\int_0^{2\pi}\int_{0}^{\pi}\Psi(a)\frac{\partial G}{\partial n'}\Bigg|_{r'=a}a^2\sin\thet\thinspace d\theta'd\phi'$$

$$\Psi(\mathbf{x})=-\frac{1}{4\pi}\int_0^{2\pi}d\phi'\left[\int_{0}^{\pi/2}V_o\frac{\partial G}{\partial n'}\Bigg|_{r'=a}\sin\thet\thinspace d\theta'-\int_{\pi/2}^{\pi}V_o\frac{\partial G}{\partial n'}\Bigg|_{r'=a}\sin\thet\thinspace d\theta'\right]$$

$$\Psi(\mathbf{x})=V_o\sum_{l,m} \left(\frac{a}{r}\right)^{l+1}Y_{lm}(\theta,\phi)\int_0^{2\pi}d\phi'\left[\int_{0}^{\pi/2}Y^*_{lm}(\theta',\phi')\sin\thet\thinspace d\theta'-\int_{\pi/2}^{\pi}Y^*_{lm}(\theta',\phi')\sin\thet\thinspace d\theta'\right]$$

$$\Psi(\mathbf{x})=V_o\sum_{l,m}\left(\frac{a}{r}\right)^{l+1}f(l)e^{im\phi}P_{lm}(\theta,\phi)\int_0^{2\pi}d\phi'\left[\int_{0}^{\pi/2}f(l)e^{-im\phi'}P^l_{m}\sin\thet\thinspace d\theta'-\int_{\pi/2}^{\pi}e^{-im\phi'}P^l_{m}\sin\thet\thinspace d\theta'\right]$$

Eqn. 3.53

$$Y_{lm}(\theta,\phi)= f(l)P^l_m(\cos\theta)e^{im\phi}$$

$$f(l) = \sqrt{\frac{2l+1}{4\pi}\frac{(l-m)!}{(l+m)!}}$$

$$\Psi(\mathbf{x})=V_o\sum_{l,m}\left(\frac{a}{r}\right)^{l+1}e^{im\phi}P_{l}^m(\theta,\phi)I_{lm}$$

$$I_{lm} \equiv [f(l)]^2\int_0^{2\pi}d\phi'\left[\int_{0}^{\pi/2}f(l)e^{-im\phi'}P_l^{m}(\cos\theta')\sin\thet\thinspace d\theta'-\int_{\pi/2}^{\pi}e^{-im\phi'}P^m_{l}(\cos\theta')\sin\thet\thinspace d\theta'\right]$$

$$I_{lm} =  [f(l)]^2\int_0^{2\pi}e^{-im\phi'}d\phi'\left[\int_{0}^{\pi/2}P_l^{m}(\cos\theta')-\int_{\pi/2}^{\pi}P_l^{m}(\cos\theta')\right]\sin\thet\thinspace d\theta'$$

$$I_{lm} =  [f(l)]^2\int_0^{2\pi}e^{-im\phi'}d\phi'\left[\int_{0}^{1}P^m_{l}(x)dx-\int_{-1}^{0}P^m_{l}(x)dx\right]$$

$I_{lm}=0$ for $m\ne 0$.

$$I_{l} = \frac{(2l+1)}{2}\left[\int_{0}^{1}P_{l}(x)dx-\int_{-1}^{0}P_{l}(x)dx\right]$$

$I_l=A_l$ with $A_l$ given by eqn. 3.26; $A_0=0$, $A_1=3/2$, $A_2=0$, $A_3=-7/8$, ...

$$\Psi(r,\theta)=V_o\sum_{l=1,3,...} \frac{a^{l+1}}{r^{l+1}}P_{l}(\theta)A_{l}$$

$$\Psi(r,\theta)\simeq V_o\left[\frac{3}{2}\left(\frac{a}{r}\right)^2P_1(\cos\theta)-\frac{7}{8}\left(\frac{r}{a}\right)^4P_3(\cos\theta)+\frac{11}{16}\left(\frac{r}{a}\right)^6P_5(\cos\theta)\right]$$

Same as eqn. 3.36 with replacement of $(r/a)^l$ with $(a/r)^{l+1}$.  Far away, the system looks like a dipole (due to opposite-sign charge density on each hemisphere), so we expect only odd $l$ terms, as found.
|}

\newpage

# BV

## 1-D

See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.md#1-D).

In many of these problems, one can guess the solution and use a uniqueness argument to justify that it is the solution. In this assignment, I want to see the steps for a non-guess solution (using what I called "the boundary value" method in class).

Problems of this type are not addressed in much detail in Jackson; I recommend Griffiths and/or a mathematical physics textbook.

In these problems, "Find $\Psi(\rho)$ or $\Psi(r)$" means to find the potential for all $\rho$ and $r$.

## Spherical -- Potentials Given 

1. Derive the general solution of $\nabla^2\Psi(r) = 0$ in spherical coordinates.

Two concentric and conducting spherical shells of radius $b$ and $c$ have potentials $\Psi(r=b)=V_b$ and $\Psi(r=c)=V_c$ after they were connected to a battery.

2. Find $\Psi(r)$ using the boundary value method.

3. Compare the answer from 2. to an answer obtained using a non-boundary-value method (assume the potential induces a charge, use Gauss' law to find $E_r$, and then integrate $E_r$).

**Solution**

This is a somewhat basic problem, and I wanted you to solve it before considering some of the subtitles discussed below. Quite often we solve these basic problems without much thought about the details. When considering more complex boundary value problems, understanding the details of the basic problems is important. (I previously emphasized this with respect to solving Gauss' law problems.)

1\. In spherical coordinates,

$\displaystyle\nabla^2\Psi(r)=\frac{1}{r^2}\frac{\partial \Psi}{\partial r}\left(r^2\frac{\partial \Psi}{\partial r}\right)=\frac{1}{r^2}\frac{d \Psi}{dr}\left(r^2\frac{d \Psi}{dr}\right)$

where the partial derivatives can be turned into total derivatives becuase the potential only depends on $r$.

$\displaystyle\frac{1}{r^2}\frac{d \Psi}{dr}\left(r^2\frac{d \Psi}{dr}\right)=0 \Rightarrow \left(r^2\frac{d \Psi}{dr}\right) = A\Rightarrow \frac{d \Psi}{dr} = Ar^2$

where $A$ is a constant.  Integration gives

$\displaystyle\Psi = A + \frac{B}{r}$

Some students found the solution for $\nabla^2\Psi(r,\theta) = 0$, but technically this was not asked for (and was not needed for parts 2. and 3.)

2\. $\Psi_1 = V_b$

$\Psi_2(r) = V_b + (V_c-V_b)\frac{\frac{1}{r}-\frac{1}{b}}{\frac{1}{c}-\frac{1}{b}}$

$\Psi_3(r) = V_c + (V_R-V_c)\frac{\frac{1}{r}-\frac{1}{c}}{\frac{1}{R}-\frac{1}{c}}$

where $\Psi_3(R)\equiv V_R$. If $R\gg c$ and $V_R=0$, then

$\Psi_3(r) = V_c\thinspace\frac{c}{r}$

If $V_R=V_c$, then

$\Psi_3(r) = V_c$

Call the region $b\le r\le c$ region 2. Then

$\Psi_2(b)=V_b=A+\frac{B}{b}$

$\Psi_2(c)=V_c=A+\frac{B}{c}$

$\Psi_2(r) = V_b + (V_c-V_b)\frac{\frac{1}{r}-\frac{1}{b}}{\frac{1}{c}-\frac{1}{b}}$

Using

$\sigma_{b+}=-\epsilon_o\frac{\partial \Psi_2}{\partial r}\Bigg|_{r=b}$

$\sigma_{c-}=+\epsilon_o\frac{\partial \Psi_2}{\partial r}\Bigg|_{r=c}$

where $b+$ means the outer surface of the shell with radius $b$ and $c-$ means the inner surface of the shell with radius $c$, it can be shown that $\sigma_{c-} c^2=-\sigma_{b+} b^2$. This means that $Q_{b+}=-Q_{c-}$.

The charge on the outer surface of the shell at $b$ is

$Q_{b+}=\sigma_{b+}4\pi b^2=4\pi\epsilon_o(V_b-V_c)\frac{1}{\frac{1}{b}-\frac{1}{c}}$

which is negative if $V_c > V_b$.

Call the region $r\le b$ region 1. Then

$\Psi_1 = A + \frac{B}{r}$

Typically we say $B=0$ so the solution does not "blow up".  There are two other ways to justify $B=0$. First, with $A=V_b$ and $B=0$, the potential satisfies the boundary condition at $r=b$ and $\Psi_1=V_b$ gives $\nabla^2\Psi_1=0$. By the uniqueness theorem, $\Psi=V_b$ is the solution. Second, if $B\ne 0$, $\nabla^2\Psi_1=-4\pi\delta(\mathbf{r})= -B\delta(r)/r^2$. Because, $\nabla^2\Psi=-\rho/\epsilon_o$, a non-zero $B$ means $\rho=\epsilon_oB\delta(r)/r^2$, which is the charge density for a point charge at the origin. But no point charge was given to exist there, so $B$ must be zero.

As mentioned on Piazza, I intentionally did not give a boundary condition for $r>c$ in the hopes that the question would be raised and so that I could make the point that a boundary value problem needs a ''closed'' surface (I won't take off if you didn't catch this, as mentioned earlier, this basic problem was given so the subtleties discussed here are easier to understand). Ideally, you realized that there is not a unique solution unless you specify the potential for $r>c$. This issue is discussed in section 1.9 of Jackson, which concludes with the statement that "electrostatic problems are specified by Dirichlet or Neumann boundary conditions on a '''closed'' surface''' So to have a unique solution for $r>c$, we must specify a boundary and information about the potential in that region''". Most students assumed the potential $V_{R}=0$ or $V_R=V_c$, where $R\gg c$. The general solution in this region can be written down using the solution for $\Psi_1$:

$\Psi_3(r) = V_c + (V_R-V_c)\frac{\frac{1}{r}-\frac{1}{c}}{\frac{1}{R}-\frac{1}{c}}$

One could also specify $d\Psi/dr$ on the boundary at $r=R$. Solving for $A$ and $B$ assuming the potential is given at $r=c$ as $V_c$ and $d\Psi/dr$ is given at $r=R$ gives

$\Psi(r)=V_c+R^2\left(\frac{1}{c}-\frac{1}{r}\right)\frac{d\Psi}{dr}\Bigg|_{r=R}$

3. In the Gauss' law method, one assumes charges of $Q_b$ and $Q_c$. The geometry is un-changed by a rotation by $\theta$ and $\phi$ and so the field and thus charge density on the surfaces must be independent of $\theta$ and $\phi$. The field can be argued to be radial in this case because for each charge on a sphere there will be another charge which exactly cancels its non-radial component, so $E_{\theta}=E_{\phi}=0$. These arguments allow writing $\mathbf{E}(r,\theta,\phi)=E_r(r)\hat{\mathbf{r}}$. Using a spherical Gaussian surface of radius $r$ for $r\lt b$, $\hat{\mathbf{n}}=\hat{\mathbf{r}}$

$\oint\mathbf{E}\cdot \hat{\mathbf{r}}\thinspace r^2 d\Omega=E_r(r)\thinspace r^2\thinspace 4\pi$

Because $Q_{encl}=0$, this gives $E_r(r)=0$ for $r\ne 0$. For r=0$, Gauss' law gives $E_r=0/0$. However, one can argue that $E_r=0$ by the cancellation discussed above.

For $b\lt r \lt c$, $Q_{encl}=Q_b$ and

$E_r(r)=\frac{1}{4\pi\epsilon_o}\frac{Q_b}{r^2}$

For $r \gt c$, $Q_{encl}=Q_b+Q_c$ and

$E_r(r)=\frac{1}{4\pi\epsilon_o}\frac{Q_b+Q_c}{r^2}$

To find the potential, integrate from $R$ to $r$

$\Psi_3(r) - \Psi(R) = -\int^{r}_{R} E_r\thinspace dr$

$\Psi_3(r) = \Psi(R) + \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(\frac{1}{R}-\frac{1}{r} \right)\quad r\gt c$

Integration from $r=c$ to $r$ gives

$\Psi_2(r)-V_c=\frac{Q_b}{4\pi\epsilon_o}\left(\frac{1}{r}-\frac{1}{c} \right)$

or

$$\Psi_2(r)=V_c+\frac{Q_b}{4\pi\epsilon_o}\left(\frac{1}{r}-\frac{1}{c} \right)\quad b\lt r\lt c$$

$Q_b$ can be solved for using $V(b)=V_b$, giving

$$Q_b=4\pi\epsilon_o\frac{V_b-V_c}{\left(\frac{1}{b}-\frac{1}{c} \right)}$$

This matches $Q_{b+}$ computed using the boundary value method. Using $Q_b$ in the equation for $\Psi_2$ gives

$\Psi_2(r)=V_c+(V_c-V_b)\frac{\left(\frac{1}{r}-\frac{1}{c} \right)}{\left(\frac{1}{c}-\frac{1}{b} \right)}\quad b\lt r\lt c$

Integration from $b$ to $r$ gives

$\Psi_1(r)-V_b=0\Rightarrow \Psi_1(r)=V_b\quad r\lt b$

In summary, thus far we have

$\Psi_1(r)=V_b\quad r\lt b$

$\Psi_2(r)=V_c+(V_c-V_b)\frac{\left(\frac{1}{r}-\frac{1}{c} \right)}{\left(\frac{1}{c}-\frac{1}{b} \right)}\quad b\lt r\lt c$

$\Psi_3(r) = V_R + \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(\frac{1}{R}-\frac{1}{r} \right)\quad r\gt c$

where 

$Q_b=4\pi\epsilon_o\frac{V_b-V_c}{\left(\frac{1}{b}-\frac{1}{c} \right)}$

If $V_R=V_c$, the equation for $\Psi_3$ evaluated at $r=c$ gives $Q_b=-Q_c$, and so

$\Psi_3=V_c$

In this case, all of the charge on the shell at $c$ is on its inner surface. If $V_R=0$ and $R\gg c$, then we get 

$\Psi_3(c) = V_c = \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(-\frac{1}{c} \right)$

or

$Q_b+Q_c = -cV_c4\pi\epsilon_o$

and finally

$\Psi_3(r) = V_c\frac{c}{r}\quad r\gt c$

Note that here $Q_c$ is the charge on the inner and outer surface of the shell of radius $c$; in the boundary value method solution, I only computed the charge on the inner part of the shell with radius $c$. One could compute the charge on the outer part of the shell with radius $c$ using the boundary value method and show that $Q_{c+}+Q_{c-}$ equals the $Q_c$ found above. 

Physically, if the shell at $r=R$ is not at $V_c$, extra charge will need to be on the outer surface of the shell at $r=c$ in order to make the electric field in the shell at $r=R$ zero.

Finally, note that this problem is equivalent to the problem of two spherical capacitors in series and could have been solved simply by using the formula for the capacitance of a spherical capacitor.

## Spherical -- $\sigma$ Given 

A non-conducting spherical shell of radius $b$ has a uniform surface charge density of $\sigma_o$. 

1. Find $\Psi(r)$ using the boundary value method.

2. Compare the answer from 1. to an answer obtained using a non-boundary-value method.

**Solution**

This again is somewhat of a basic problem; the motivation for assigning it will become clear when the Green function approach is used.

There were several common errors. Several students noted that $\Psi(\infty)=0$ was required. It is not required. What is required is that the "boundary" at infinity is given a potential (so that you have a fully specified boundary value problem). One can also set $\Psi(0)=0$ - in this case, you are implicitly specifying the potential at the boundary at infinity. As mentioned in the solution to the previous problem, to solve a boundary value problem, you need to know the potentials on the surfaces of a volume.

Another error was sloppy usage of

$$\Psi(r)=-\int E_rdr$$

Without limits, integration gives a constant that must be solved for. Quite often, no discussion was given about the integration constant. I generally use limits and always write

$$\Psi(b)-\Psi(a)=-\int_{a}^b E_rdr$$

so that there is no constant of integration that needs to be considered.

1. 

Outside (o) and inside (i), the potentials can be written as

$$\Psi_i = A_i + \frac{B_i}{r}$$

$$\Psi_o= A_o + \frac{B_o}{r}$$

At $r=b$, $\Psi_i=\Psi_o$, giving

$$A_i + \frac{B_i}{b} = A_o + \frac{B_o}{b}$$

At $r=b$, 

$$-\frac{d\Psi_o}{dr}\Bigg|_{r=b}+\frac{d\Psi_i}{dr}\Bigg|_{r=b}=\frac{\sigma_o}{\epsilon_o}$$

giving

$$+\frac{B_o}{b^2} - \frac{B_i}{b^2}=\frac{\sigma_o}{\epsilon_o}$$

We have two equations and four unknowns. $B_o$ can be argued to be zero using any of the arguments in the previous problem. This leaves the two equations

$$A_i = A_o + \frac{B_o}{b}$$

$$\frac{B_o}{b^2} =\frac{\sigma_o}{\epsilon_o}$$

$$\Psi_i=A_i$$

$$\Psi_o=A_i+\frac{\sigma_ob}{\epsilon_o}\left(\frac{b}{r}-1\right)$$

The fact that one unknown remains follows from the fact that a reference potential was not given. We can choose the location and value of the reference potential to be anything. $\Psi=0$ at $r=0$ gives

$$\Psi_i=0$$

$$\Psi_o=\frac{\sigma_ob}{\epsilon_o}\left(\frac{b}{r}-1\right)$$

$\Psi_o=0$ at $r=\infty$ gives

$$\Psi_i=\frac{\sigma_ob}{\epsilon_o}$$

$$\Psi_o=\frac{\sigma_o}{\epsilon_o}\frac{b^2}{r}$$

2.

From Gauss' law,

$$E_i=0$$

$$E_o=\frac{\sigma_o}{\epsilon_o}\frac{b^2}{r^2}$$

$$\Psi(r)-\Psi(\infty)=-\int_{\infty}^rE_odr$$

This gives

$$\Psi(r)=\Psi(\infty)+\frac{\sigma_o}{\epsilon_o}\frac{b^2}{r}$$

and matches the result from 1. if we set $\Psi(\infty)=0$. Because the electric field is zero for $r\lt b$, the potential will not change and must match that at $r=b$. Another way to show this is

$$\Psi(r)-\Psi(b)=-\int_b^{r}E_idr=0 \Rightarrow \Psi(r)=\Psi(b)$$

If we choose $\Psi(0)=0$, then $\Psi(b)=0$ based on arguments given above and

$$\Psi(r)-\Psi(b)=\Psi(r)=-\int_b^rE_odr=\frac{\sigma_ob}{\epsilon_o}\left(\frac{b}{r}-1\right)$$

which matches the result from part 1.
|}


## 2-D

## Cartesian

See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.html)

See [HW #4](hw.md#2-d-cartesian-boundary-value-problem) and references therein.

## Cylindrical -- $\sigma$ given

#2-d-cylindrical-boundary-value-problem&l=1272&c=1

## Cylinder -- $\mathbf{E}(\infty)$ given

A long conducting cylinder of radius $b$ has its centerline along the $z$--axis. There is an external electric field of $\mathbf{E}=E_o\hat{\mathbf{x}}$.

Find $\psi(s,\phi)$

## Cylinder -- $\psi$ given

A long conducting cylinder of radius $b$ has its centerline along the $z$--axis. The cylinder is held at a potential of $V_o\sin^2\phi$.

Find $\psi(s,\phi)$

## Spherical -- $\psi$ given I.

A non-conducting spherical shell of radius $b$ has on its surface of $V_o\cos\theta$.

Find $\Psi(r,\theta)$.

**Solution**

1\. Using $\psi=0$ at the origin,

$\psi(r,\theta) = 
\begin{cases}
\displaystyle V_o\frac{r}{b}\cos\theta & r \le b \\ \\
\displaystyle V_o\frac{b^2}{r^2}\cos\theta & r \ge b
\end{cases}
$

## Spherical -- $\psi$ given II.

Find $\Phi(r,\theta)$ if  $\Phi(r=b,\theta)=V_1\cos\theta+V_2\cos^2\theta$.

**Solution**

(Partial solution)

Note that we could compute the potential due to the $V_2$ term and add the result of the previous problem. 

Need to write $V_2\cos^2\theta$ in terms of Legendre polynomials. Noting that $P_2=\frac{1}{2}(3\cos^2\theta - 1)$, $\cos^2\theta = \frac{2P_2+1}{3}$. Using this and $P_1(\cos\theta)=\cos\theta$, the boundary condition can be re-written as

$\displaystyle\Phi(r=b,\theta)=\frac{V_2}{3} + V_1P_1(\cos\theta) + \frac{2V_2}{3}P_2(\cos\theta)$

Inside the sphere, look for solutions in the form

$\displaystyle\Phi^i(r,\theta) = \sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)$

Outside, use 

$\displaystyle\Phi^o(r,\theta) = \sum_{l=0}^{\infty}\frac{B_l}{r^{l+1}}P_l(\cos\theta)$

At $r=b$,

$\Phi^o(b,\theta)=\Phi^i(b,\theta)$

$\displaystyle\sum_{l=0}^{\infty}A_lb^lP_l(\cos\theta) = \sum_{l=0}^{\infty}\frac{B_l}{b^{l+1}}P_l(\cos\theta)$

This gives

$B_l=A_lb^{2l+1}$

Written out explicitly, this is

$B_0=A_0b$

$B_1=A_1b^3$

$B_2=A_2b^5$

$...$

One can use either $\Phi^i$ or $\Phi^o$ at $r=b$ along with the boundary condition

$\displaystyle\Phi(r=b)=\frac{V_2}{3} + V_1P_1(\cos\theta) + \frac{2V_2}{3}P_2(\cos\theta)$

Using $\Phi^i$,

$\displaystyle\Phi^i(b,\theta)=\sum_{l=0}^{\infty}A_lb^lP_l(\cos\theta)=\frac{V_2}{3} + V_1P_1(\cos\theta) + \frac{2V_2}{3}P_2(\cos\theta)$

To find the coefficients, it is often easier to write out a few terms in the sum and match terms (make sure that you know why this works):

$$
\begin{align*}
&& A_0P_0                   && + && A_1bP_1  && + &&  A_2b^2P_2            &&\quad +   &&\quad A_3b^3P_3 &&\quad+&&\quad ... && = && \\
&& \frac{V_2}{3}P_0   && + && V_1P_1    && + && \frac{2V_2}{3}P_2   &&\quad+    && \quad 0                &&\quad +            && \quad ...              &&   &&
\end{align*}
$$

## Spherical -- $\sigma$ given

A non-conducting sphere of radius $r_o$ has a surface charge density of $(3/2)\sigma_2\sin^2\theta$. Find the potential inside and outside of the sphere assuming that at $r\gg r_o$, $\Psi=0$. In your calculations, use $\epsilon_o=1$.

First, write $\sigma$ in terms of Legendre polynomials:

$\sigma = \frac{3\sigma_2}{2}\sin^2\theta=\frac{3}{2}\sigma_2(1-\cos^2\theta)=\frac{3}{2}\sigma_2-\frac{3}{2}\sigma_2\cos^2\theta$

Given that $P_2 = \frac{3\cos^2\theta-1}{2}$, we can write $\cos^2\theta = \frac{2P_2+1}{3}$ and

$\displaystyle \sigma = \frac{3\sigma_2}{2} - \frac{3\sigma_2}{2}\left(\frac{2P_2+1}{3}\right) = \frac{3\sigma_2}{2} - \frac{\sigma_2}{2} - \sigma_2P_2 = \sigma_2P_0 - \sigma_2P_2$

The net charge on the sphere is not zero because the integral of $\sigma$ over the surface is non-zero, so we expect a $1/r$ term for the potential outside of it (the "monopole" term). (The integral of $\sigma$ over the surface is $4\pi r_o^2\sigma_2$ - the $P_2$ term integrates to zero).

The general solution to $\nabla^2\Phi(r,\theta)=0$ is

$\displaystyle\Phi(r,\theta) = \sum_{l=0}^{\infty}\left(a_lr^{l}+\frac{b_l}{r^{l+1}}\right)P_l(\cos\theta)$

Based on previous experience, look for solutions for the potential outside (o) and inside (i) of the form

$\Phi^o = \frac{A_o}{r}P_0 + \frac{A_2}{r^3}P_2$

$\Phi^i = B_oP_0 + B_2r^2P_2$

I've dropped the $P_1$ term and the higher-order terms and to shorten the solution. You can include both and follow the steps in a previous homework solution to show that the omitted terms are zero.

Note that $\Psi_o$ is zero for $r\gg r_o$ as required by the boundary condition given in the problem statement.

The two conditions that need to be satisfied are continuity

$\Phi^o(r_o,\theta) = \Phi^i(r_o,\theta)$

and the perpendicular electric field jump condition

$\displaystyle\left[-\frac{\partial \Phi_o}{\partial r} + \frac{\partial \Phi_i}{\partial r}\right]_{r=r_o} = \frac{\sigma}{\epsilon_o}$

Many students wrote an equation of the form $E_o-E_i=\sigma/\epsilon_o$. This is not technically correct. The correct version is $E_{\perp o}-E_{\perp i}=\sigma/\epsilon_o$, which is equivalent to equation 1.22 of Jackson 3rd edition. I went over the derivation of this equation in class and showed how Gauss' law gives $E_{\perp o}-E_{\perp i}=\sigma/\epsilon_o$ and $E_{\parallel  o}-E_{\parallel i}=0$. See also the derivation associated with equations 2.31 and 2.32 of Griffiths 4th edition.

The continuity condition

$\Phi_o(r_o,\theta) = \Phi_i(r_o,\theta)$

gives

$\displaystyle\frac{A_o}{r_o}P_0 + \frac{A_2}{r_o^3}P_2 = B_oP_0 + B_2r^2_oP_2$

So

$B_o=A_o/r_o\qquad B_2=A_2/r_o^5$

The perpendicular electric field jump condition

$\displaystyle\left[-\frac{\partial \Phi_o}{\partial r} + \frac{\partial \Phi_i}{\partial r}\right]_{r=r_o} = \frac{\sigma}{\epsilon_o}$


gives

$\displaystyle\frac{A_o}{r_o^2}P_o + 3\frac{A_2}{r_o^4}P_2 + 2B_2r_oP_2 = \frac{\sigma_2}{\epsilon_o}P_0 - \frac{\sigma_2P_2}{\epsilon_o}$

So 

$A_o=\sigma_2r_o^2/\epsilon_o\qquad 3A_2+2r_o^5B_2=-r_o^4\sigma_2/\epsilon_o$

Using $B_o=A_o/r_o$ from the continuity condition and $A_o=\sigma_2r_o^2/\epsilon_o$ gives

$B_o = \sigma_2r_o/\epsilon_o$

Using $B_2=A_2/r_o^5$ from the continuity condition and $3A_2+2r_o^5B_2=-r_o^4\sigma_2/\epsilon_o$ gives

$3A_2+2r_o^4B_2=2A_2+3A_2=-r_o^4\sigma_2/\epsilon_o$

and finally

$A_2=-\frac{\sigma_2}{5\epsilon_o}r_o^4\qquad B_2=-\frac{\sigma_2}{5r_o\epsilon_o}$

The final answer is (using $P_0=1$)

$\displaystyle\Phi^o = \frac{\sigma_2r_o}{\epsilon_o}\left(\frac{r_o}{r} - \frac{1}{5}\frac{r_o^3}{r^3}P_2\right)$

$\displaystyle\Phi^i = \frac{\sigma_2r_o}{\epsilon_o}\left(1 - \frac{1}{5}\frac{r^2}{r_o^2}P_2\right)$

----

Note that the first term in $\Phi_o$

$\displaystyle\frac{\sigma_2r_o^2}{\epsilon_o}\frac{1}{r}$

can be written as

$\displaystyle\frac{4\pi\sigma_2r_o^2}{4\pi\epsilon_o}\frac{1}{r}=\frac{kQ}{r}$

confirming that the existence of a $1/r$ term for $\Phi_o$ that expected for a sphere with a uniform charge density of $\sigma_2$. (For large $r$, the $1/r$ term dominates and the potential is near that for a uniformly charged sphere.)

As a final check, note that

$\displaystyle\Phi^o(r_o,\theta) = \frac{\sigma_2r_o}{\epsilon_o}\left(1 - \frac{1}{5}P_2\right)$

$\displaystyle\Psi^i(r_o,\theta) = \frac{\sigma_2r_o}{\epsilon_o}\left(1 - \frac{1}{5}P_2\right)$

so the continuity condition is satisfied. Also, the perpendicular electric field jump condition

$\displaystyle\left[-\frac{\partial \Phi^o}{\partial r} + \frac{\partial \Phi^i}{\partial r}\right]_{r=r_o} = \frac{\sigma}{\epsilon_o}$

evaluated with the potentials

$\displaystyle\Phi^o = \frac{\sigma_2r_o}{\epsilon_o}\left(\frac{r_o}{r} - \frac{1}{5}\frac{r_o^2}{r^3}P_2\right)$

$\displaystyle\Phi^i = \frac{\sigma_2r_o}{\epsilon_o}\left(1 - \frac{1}{5}\frac{r^2}{r_o^2}P_2\right)$

and $\sigma = \sigma_2P_0 - \sigma_2P_2$ results in

$\displaystyle\frac{\sigma_2r_o}{\epsilon_o}\left(\frac{1}{r_o}P_0 + \frac{1}{5}\frac{3}{r_o}P_2\right) +  \frac{\sigma_2r_o}{\epsilon_o}\frac{1}{5}\frac{2}{r_o}P_2= \frac{\sigma_2}{\epsilon_o}P_0 - \frac{\sigma_2}{\epsilon_o}P_2$

and so the jump condition is satisfied.

## Spherical -- $\mathbf{E}(\infty)$ given

See example in Griffiths

## Spherical -- $\psi$ given

See example in Griffiths

\newpage

# Dielectric

## Long Dielectric Cylinder 

An infinitely long dielectric cylinder of radius $b$ is placed into a vacuum region of space with an initially uniform electric field $E_o\hat{\mathbf{x}}$. The cylinder is parallel to and centered on the $z-$axis.

The cylinder has a dielectric constant of $\epsilon$. Find the potential inside and outside of the dielectric.

----
In class, I mentioned that one could "guess" which terms in the general solution to $\nabla^2\psi(s,\phi)=0$ of

$$
\begin{align}
\psi(s,\phi)  = {} &  A_o+a_o\ln s\\
& +\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)s^n\\
& +\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)s^{-n}
\end{align}
$$

to keep and start the solution at that point. For this problem, start with the general solution and provide justification for constants that are zero. In the equations above, $s$ is the radial cylindrical coordinate and $\phi$ is the cylindrical angular coordinate.

----

**Solution**

Most students were able to get the correct answer, which is not surprising because this is a problem from Griffiths for which solutions can be found easily. The reason that I asked for justifications was to make sure that you understood the solutions that you were reading and/or could spot errors or poor logic. This was an opportunity to clarify your logic in solving these types of problems. Unfortunately, many students still used specious logic found on a Google search of "dielectric cylinder in a uniform electric field".

This is a problem with the logic of "the potential does not blow up" at infinity fails. The potential does "blow up" because it has a term proportional to $s$.

A common comment was that the condition $\epsilon/\epsilon_o=-1$ implied a set of coefficients were zero because $\epsilon$ had to be greater than zero. I wondered why this statement was made so frequently in student answers and I found a similar statement [https://physicspages.com/pdf/Griffiths%20EM/Griffiths%20Problems%2004.22.pdf here]. I accepted this because technically it is a valid statement, but there is a more general reason that applies. (One could be given a non-physical problem in which $\epsilon$ was negative and the set of coefficients would still be zero.) This is discussed in my solution.

In the following, I give two solutions to this problem. The first is the type of solution that I was looking for. The second is a brief solution that uses some intuition that is gained from solving these types of problems to make large steps with the only mathematical justification being that the guesses gave a solution that satisfied the boundary conditions and Laplace's equation and therefore it is the solution as a result of the uniqueness of solutions to Laplace's equation. You should be able to do these types of problems in both ways. Quite often on more complex problems, you can't rely on shortcuts of the type taken here and you need a solid understanding of the mathematical justifications for each step.

----

'''First Solution'''

To be posted.

----

'''Second Solution'''

For large $s$, we expect $\psi\rightarrow V_o - E_os\cos\theta$. Because there is a cosine term for large $s$, we expect a cosine term in the outer and inner solution (based on experience with the analogous sphere-in-a-dielectric problem). So we make an attempt for a solution using the following forms for the potential.

$$\psi_o=V_o+\frac{B_1}{s}\cos\phi-E_os\cos\phi$$

$$\psi_i=A_o+A_1s\cos\phi$$

The boundary condition

$\psi_o(s)=\psi_i(s)$

gives

$$A_o=V_o\quad \text{and}\quad A_1=B_1/a^2-E_o$$

The boundary condition

$$D_{os}-D_{is}=0$$

corresponds to

$$-\epsilon_o\frac{\partial \psi_o}{\partial s}+\epsilon\frac{\partial \psi_i}{\partial s} = 0$$

and this gives

$$B_1=-s_o^2E_o-\epsilon_rA_1s_o^2$$

which when combined with $A_1=B_1/a^2-E_o$ gives

$$B_1=\frac{1-\epsilon_r}{1+\epsilon_r}E_os_o^2$$

and

$$A_1=-\frac{2E_o}{\epsilon_r+1}$$

So the potentials are

$$\psi_o=V_o+E_o\frac{\epsilon_r-1}{\epsilon_r+1}\frac{s_o^2}{s}\cos\phi-E_os\cos\phi$$

$$\psi_i=V_o-\frac{2E_o}{\epsilon_r+1}s\cos\phi$$

Note when $\epsilon_r\rightarrow \infty$, is consistent with the solution for a conducting cylinder. For $s_o\rightarrow 0$ the solution is consistent with the solution for a line of charge with $\lambda=0$ (because all of the polarized charges are on top of each other) in an electric field $E_o\hat{\mathbf{x}}$: the inner potential, which corresponds to $\psi_i(0,\theta)$ in this limit) is $V_o$ and the outer potential is the external potential. The dielectric does not contribute to the electric field because the bound charges are on top of each other at the origin.

## Spherical Dielectric with Cavity 

A spherical dielectric with permittivity $\epsilon$, inner radius $b$, and outer radius $c$ is centered on the origin. Inside and outside of the dielectric the permittivity is $\epsilon_o$.

There is an external electric field of $E_o\hat{\mathbf{z}}$. 

Find the electric field in all regions of space.

**Solution**
See the analogous magnetism example in Jackson 5.12. All of the mathematical steps are the same and the solution to this problem can be obtained by the replacement of constants.

\newpage

# Monopole

## Monopole Expansion Using "Standard" Method 

1. Write down the potential $\psi$ as a function of $(x,y,z)$ for a point charge $q$ located at $(x,y,z)=(0,0,z')$ using $kq=1$.

2. Write out the first three terms in the Taylor series expansion of $\psi$ for $z'/r \ll 1$.

3. Show that your result is consistent with equation 3.38 of Jackson 3rd edition:

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$$

where $r_{<}$ ( $r_{<}$) is the smaller (larger) of $|\mathbf{x}|$ and $|\mathbf{x}'|$ and $\gamma$ is the angle between $\mathbf{x}$ and $\mathbf{x}'$.

4. Show how your result consistent with equation 3.95 of Griffiths 4th edition (by using the delta function to represent the charge density):

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

which was derived assuming that the maximum value of $r'$ for which $\rho\ne 0$ is much less than $r$ and $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$.

'''Optional Problem'''

Repeat the above for a point charge located at $(x,y,z)=(0,y',0)$.

**Solution**

1.

$$\psi = \frac{1}{|\mathbf{x}-\mathbf{x}'|} =\frac{1}{\sqrt{x^2+y^2+(z-z')^2}}$$

2.

For the case $r\gg z'$, factor out $r$ and re-write in a form that is straightforward to expand as a Taylor series

$$
\begin{align}
\frac{1}{|\mathbf{x}-\mathbf{x}'|} &=\frac{1}{\sqrt{x^2+y^2+(z-z')^2}}\\
&=\frac{1}{\sqrt{x^2+y^2+z^2+z'^2-2zz'}}&&\text{Expand }(z-z')^2\\
&=\frac{1}{|r|\sqrt{1+z'^2/r^2-2zz'/r^2}}&&\text{Using}\thinspacer^2=x^2+y^2+z^2\thinspace\text{and factoring out}\thinspacer\\
&=\frac{1}{r\sqrt{1+z'^2/r^2-2(z'/r)\cos\theta}}&&\text{Using}\thinspacez=r\cos\theta\text{ and }|r|=r\\
& =\frac{1}{r\sqrt{1+\delta}}&&\text{Defining }\delta\equiv z'^2/r^2-2(z'/r)\cos\theta
\end{align}
$$

For $\delta<1$, the binomial function $(1+\delta)^{-1/2}$ can be expanded as a Taylor series, the result of which is

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\delta+\frac{3}{8}\delta^2-\frac{5}{16}\delta^3+...$$

Evaluating terms of order $\delta^2$ and lower using $\delta = z'^2/r^2-2(z'/r)\cos\theta$ gives

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\left(z'^2/r^2-2(z'/r)\cos\theta\right)+\frac{3}{8}\left(z'^2/r^2-2(z'/r)\cos\theta\right)^2+...$$

This can be written in terms of a power series ordered by powers of $z'/r$ giving the result

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\frac{1}{r}\left(1+\frac{z'}{r}\cos\theta+\left(\frac{z'}{r}\right)^2\frac{1}{2}\left(3\cos^2\theta-1\right)-\left(\frac{z'}{r}\right)^3\frac{3}{2}\cos\theta+\frac{3}{8}\left(\frac{z'}{r}\right)^4...\right)$$

The first three terms are identified as $P_0,P_1,$, and $P_2$. The last two terms are parts of $P_4$ and $P_5$ - the full $P_4$ and $P_5$ appear if the $\delta^3$ term is expanded.  Therefore the two expressions are consistent up to $l=2$.

3.

The above equation is to be compared with

$$\sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)=\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)$$

which, given the problem statement and the assumption that $z' < r$, we identify $r_{>}$ as $r$, $r_{<}$ as $z'$. The angle $\gamma$ between $r$ and $r'$ is the same as the spherical polar angle $\theta$ when $r'$ is aligned with the $z$-axis. With this,

$$\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)=\frac{1}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^l P_l(\cos \theta)$$

Therefore the two expressions are consistent up to $l=2$.

The steps above can be repeated by factoring out $z'$ and using $\delta \equiv r^2/z'^2-2(r/z')\cos\theta$ for the case $z'\gg r$.

4.

Note that there is a complication introduced by choosing the location of the charge to be $z'$ when using Griffiths equation 3.95. (If I had stated that the charge was located at $z_o$ instead of $z'$, we would not have this problem.) In the integral

$$\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

the dummy index is also primed. In this problem, the location of the charge is $\mathbf{r}'=(0,0,z')$, so the charge density can be written as

$$\rho(\mathbf{r})=q\delta(x)\delta(y)\delta(z-z')$$

Plugging this into the expression for the delta function would give

$$\rho({\mathbf{r}'})=q\delta(x')\delta(y')\delta(z'-z')=q\delta(x')\delta(y')\delta(0)$$

This does not make sense because the charge density should be zero everywhere except for at the point $(0,0,z')$.

To circumvent this issue, choose the dummy integration index to be double primed (or use $z_o$ as the location of the charge instead of $z'$). If the dummy index is double-primed, then

<nowiki>
$$\rho({\mathbf{r}^{\prime\prime}})=q\delta(x^{\prime\prime})\delta(y^{\prime\prime})\delta(z^{\prime\prime}-z')$$

which corresponds to the charge density of a point charge at a fixed location $z'$. Then

$$\rho({\mathbf{r}''})=q\delta(x'')\delta(y'')\delta(z''-z')$$

which corresponds to the charge density of a point charge at a fixed location $z'$. Then

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r'')^nP_n(\cos\alpha)\rho(\mathbf{r}'')d\tau''$$

Using $\alpha=\theta$ and factoring out (\q$ and $P_l(\cos(\theta))$ and using $kq=1$ gives

$$\psi(\mathbf{r})=\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}P_n(\cos\theta)\int\int\int(x''^2+y''^2+z''^2)^{n/2}\rho(\mathbf{r}'')dx''dy''dz''$$

The integral evaluates to

$$
\begin{align}
& \int\int\int(x'^2+y'^2+z'^2)^{n/2} q\delta(x'')\delta(y'')\delta(z''-z') dx''dy''dz''=\\
& \int\int(y''^2+z''^2)^{n/2} q\delta(y'')\delta(z''-z') dy'dz' = \\
& \int(z''^2)^n q\delta(z''-z') dz''=\\
& z'^{n}
\end{align}
$$
</nowiki>

The final result is

$$\psi = \frac{1}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^l P_l(\cos \theta)$$

which is the same as found earlier.

'''Optional'''

For the case the charge at $(0,y',0)$, one needs to note that $y=r\sin\theta\sin\phi=r\cos\gamma$ and follow the same steps, for $y'\ll r$ factor out $r$ and for $y'\gg r$ factor out $y'$. For the case $r\gg y'$, the expansion should yield

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\frac{1}{r}\left(1+\frac{y'}{r}\cos\gamma+\left(\frac{y'}{r}\right)^2\frac{1}{2}\left(3\cos^2\gamma-1\right)-\left(\frac{y'}{r}\right)^3\frac{3}{2}\cos\gamma+\frac{3}{8}\left(\frac{y'}{r}\right)^4...\right)$$

and one makes the identification that $r_{>}$ is $r$, $r_{<}$ is $y'$ and concludes that this is consistent with Jackson's equation 3.38.

----

Having done the derivation for charges at specific points, one can then follow the same steps to find the result for an arbitrary location in space $r'$ for the charge.

$$
\begin{align}
\frac{1}{|\mathbf{x}-\mathbf{x}'|} &=\frac{1}{\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}}\\
&=\frac{1}{\sqrt{x^2+y^2+z^2+x'^2+y'^2+z'^2-2xx'-2yy'-2zz'}}\\
&=\frac{1}{r\sqrt{1+r'^2/r^2-2(xx'+yy'+zz')/r^2}}\\
&=\frac{1}{r\sqrt{1+r'^2/r^2-2(r'/r)\cos\gamma}}\\
\end{align}
$$

$$r^2=x^2+y^2+z^2$$

$$r'^2=x'^2+y'^2+z'^2$$

$$\cos\gamma=\frac{\mathbf{r}\cdot\mathbf{r'}}{rr'}=\frac{xx'+yy'+zz'}{rr'}$$

$$\delta = r'^2/r^2-2(r'/r)\cos\gamma$$

For $r \gg r'$,

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\delta+\frac{3}{8}\delta^2-\frac{5}{16}\delta^3+...$$

$$\frac{1}{r\sqrt{1+r'^2/r^2-2(r'/r)\cos\gamma}}=\frac{1}{r}\left(1+\frac{r'}{r}\cos\gamma+\left(\frac{r'}{r}\right)^2\frac{1}{2}\left(3\cos^2\gamma-1\right)+\left(\frac{r'}{r}\right)^3\frac{1}{2}\left(5\cos^3\gamma-3\cos\gamma\right)+...\right)$$

$$\frac{1}{r}\sum_{l=0}^\infty \left(\frac{r'}{r}\right)^l P_l(\cos \gamma)$$

This process can be repeated using $r' \gg r$ giving

$$\frac{1}{r'}\sum_{l=0}^\infty \left(\frac{r}{r'}\right)^l P_l(\cos \gamma)$$

The equations for $r \gg r'$ and $r'\gg r$ can be combined into one equation

$$\sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)=\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)$$

using the convention that $r_{>}$ is the larger of $r$ & $r'$ and $r_{<}$ is the smaller of $r$ and $r'$.
|}

$# Monopole Expansion Using the Azimuthal Symmetry Trick 

In section 3.3 of Jackson 3rd edition, he notes that for a problem with azimuthal symmetry, the general solution to Laplace's equation in spherical coordinates is

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

The coefficients $A_l$ and $B_l$ in the expansion can be found using a trick, provided that $\psi(z)$ is known as a power series for a charge distribution that is independent of the spherical angle $\phi$ (so $\psi$ has azimuthal symmetry). Using this trick, he finds $\psi(r,\theta)$ for a point charge at $\mathbf{x}'$ by noting that $\psi(z)$ for a charge located on the $z-$axis is easily converted to a power series using a Taylor series expansion. (He uses the same trick to find  $\psi(r,\theta)$ for a ring of charge in the $x-y$ plane and centered on the $z-$axis.)

1. In a few sentences, explain the justification for why the trick works.

2. Use the trick to find the coefficients $A_l$ and $B_l$ for a charge: $q$ at $z'= d$ using $kq=1$. (That is, repeat Jackson's derivation, but fill in the missing steps and write it in a way that makes sense to you.)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
1.

The justification is that due to the uniqueness of solutions to Laplace's equation, there must exist a single solution (single set of coefficients $A_l$ and $B_l$) for all space in the general solution so the coefficients $a_l$ and $b_l$ in an expansion of the potential in the form of $\psi(z)=\sum_{l=0}^{\infty} a_lz^l + b_l/z^{l+1}$ that applies to the $z-$axis must be the same as $A_l$ and $B_l$. 

Suppose for a given charge configuration, one can find a solution for the potential on the $z$-axis as a power-series 

$$\psi(z)=\sum_{l=0}^{\infty} \left(a_lz^l + \frac{b_l}{z^{l+1}}\right)$$

and the charge configuration has azimuthal symmetry. The general solution to Laplace's equation for a potential that does not depend on $\phi$ is $\nabla^2\psi(r,\theta)=0$ is

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

Setting $r=z$, $\theta=0$, and noting that $P_l(1)=0$, this equation becomes

$$\psi(r=z,\theta=0)=\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)$$

The equations for $\psi(z)$ in terms of $a_l$ & $b_l$ and $A_l$ & $B_l$ both satisfy Laplace's equation. If solutions to Laplace's equations are unique, then $A_l=a_l$ and $B_l=b_l$.
|}

$# Dipole Expansion 

Point charges $q=\pm 1$ are located at $(x,y,z)=(0,0,\pm z')$ and $kq=1$.

Find the potential in three ways

1. Using the azimuthal symmetry trick
1. Using equation 3.38 of Jackson 3rd edition (quoted in a previous problem)
1. Using equation 3.95 of Griffiths 4th edition (quoted in a previous problem)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
1.

First, consider the $z>0$ case, so $|z|=z$.

Using $q/4\pi\epsilon_o=1$

$$\psi(z)=\frac{1}{\sqrt{(z-z')^2}}-\frac{1}{\sqrt{(z+z')^2}}=\frac{1}{|z-z'|}-\frac{1}{|z+z'|}$$

For $z'\lt z$,

$$
\begin{align}
\frac{1}{|z-z'|}=\frac{1}{|z|}\frac{1}{(1-z'/z)}&=\frac{1}{z}\left(1 + \frac{z'}{z} + \left(\frac{z'}{z}\right)^2 + \left(\frac{z'}{z}\right)^3 + \left(\frac{z'}{z}\right)^4 + ... \right)\\
\frac{1}{|z+z'|}=\frac{1}{|z|}\frac{1}{(1+z'/z)}&=\frac{1}{z}\left(1 - \frac{z'}{z} + \left(\frac{z'}{z}\right)^2 - \left(\frac{z'}{z}\right)^3 + \left(\frac{z'}{z}\right)^4 + ... \right)\\
\end{align}
$$

Combining these two equations gives

$$\psi(z)=\frac{1}{|z-z'|}-\frac{1}{|z+z|}=\frac{2z'}{z^2}+\frac{2z'^3}{z^4}+\frac{2z'^5}{z^6}+...$$

This is to be compared to the general solution to Laplace's equation 

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

for $\theta=0$. Using this, $r=z$, and $P_l(\cos 0)=P_l(1)=1$,

$$\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)=A_o+A_1z+A_2z^2+...+\frac{B_o}{z}+\frac{B_1}{z^2}+\frac{B_2}{z^3}+\frac{B_3}{z^4}+...$$

If the two $\psi(z)$ potential equations are to match, $A_l=0$ for all $l$ and $B_1=2z'$, $B_3=2z'^3$, $B_5=2z'^5$, $...$ for $l=1,3,5,...$, and $B_l=0$ otherwise. 

$$
\begin{align}
\psi(\mathbf{x}) & = \frac{2z'}{r^2}P_1(\cos\theta)+\frac{2z'^3}{r^4}P_3(\cos\theta)+\frac{2z'^5}{r^6}P_5(\cos\theta)+...\\
& = \frac{2}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)
\end{align}
$$

When $z<z'$, a power series form of the potential can be found by repeating the above steps with $z$ and $z'$ interchanged. The result is then this last equation with $r$ and $z'$ swapped:

$$\psi(\mathbf{x})=\frac{2}{z'}\sum_{l=0}^\infty \left(\frac{r}{z'}\right)^{2l+1}P_l(\cos\theta)$$

Note that the above was done under the assumption that $z>0$. If $z < 0$, we would need to make two changes: (1) $|z|=-z$ and (2) $\theta=\pi$. The results are the same. However, this calculation actually does not need to be done or considered because we have already found a general solution.

2.

This could also have been shown using equation 3.38 of Jackson (shown here for $r>r'$)

$$\frac{1}{|\mathbf{x}-\mathbf{x_+}|}=\sum_{l=0}^\infty \frac{r^l_{+}}{r^{l+1}} P_l(\cos \gamma_+)$$

$$\frac{1}{|\mathbf{x}-\mathbf{x_-}|}=\sum_{l=0}^\infty \frac{r^l_{-}}{r^{l+1}} P_l(\cos \gamma_-)$$

Where  $r_{+}=r_{-}=z'$, $\gamma_+$ is the angle from the $+q$ charge at $\mathbf{x}_+ = z'\hat{\mathbf{z}}$ to $\mathbf{x}$ and $\gamma_-$ is the angle from the $-q$ charge at $\mathbf{x}_- = -z'\hat{\mathbf{z}}$ to $\mathbf{x}$.

Using, $\gamma_+ = \theta$, $\gamma_++\gamma_-=\pi \Rightarrow \gamma_-=\pi-\theta$, and $P_l(x)=-P_l(-x)$ for $l=1,3,...$ and $P_l(x) = P_l(-x)$ otherwise:

$$\begin{eqnarray}
\frac{1}{|\mathbf{x}-\mathbf{x_+}'|}-\frac{1}{|\mathbf{x}-\mathbf{x_-}'|} & = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} P_l(\cos \theta)-\sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} P_l(\cos (\pi-\theta))\\
& = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} \Big[P_l(\cos \theta) - P_l(\cos (\pi-\theta))\Big]\\
& = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} \Big[P_l(\cos \theta) - P_l(-\cos \theta)\Big]\\
& = & \sum_{l=1,3,...}^\infty \frac{z^{'l}}{r^{l+1}} 2P_l(\cos \theta)\\
& = & \sum_{l=0}^\infty \frac{z^{'2l+1}}{r^{2l+2}} 2P_l(\cos \theta)\\
& = & \frac{2}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)
\end{eqnarray}$$

For $r < z'$, all of the above steps apply and the result is the above equation with $r$ and $z'$ swapped.

3. 

In this case, the charge density in primed coordinates is (using $d\equiv z'$ to avoid issue noted in problem 1)

$$\rho({\mathbf{r}}')=q\delta(x')\delta(y')\delta(z'-d)-q\delta(x')\delta(y')\delta(z'+d)$$

or

$$\rho({\mathbf{r}}')=\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta')-\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)$$

The following charge density could also be used

$$\rho({\mathbf{r}}')=\frac{q}{r'^2\sin\theta'}\delta(r'-d)\delta(\theta')\delta(\phi')-\frac{q}{r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)\delta(\phi')$$

(In fact, we could use $\delta(\phi'-\delta)$, where $\delta$ is arbitrary.)

As noted in class, one should check that this charge density gives $\int \rho(\mathbf{r}')r'^2\sin\theta'dr'd\theta'd\phi'=q-q$. Also note that the second term has $\delta(r'-d)$ and not $\delta(r'+d)$, which is a common error; $r'$ must be greater than zero, so $\delta(r'+d)$ corresponds to a charge at $r'=-d$.

In general, $\alpha$ depends on the primed coordinates

$$\cos \alpha = \frac{\mathbf{r}\cdot \mathbf{r}'}{r\thinspacer'}=\sin\theta\sin\theta'\cos\phi\cos\phi' + \sin\theta\sin\theta'\sin\phi\sin\phi'+\cos\theta\cos\theta'$$

which can also be written as

$$\cos \alpha = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$$

We need to evaluate

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

In spherical coordinates, $d\tau'=r'^2\sin\theta'dr'd\theta'd\phi'$. The integral to evaluate is 

$$\int(r')^nP_n(\cos\alpha)\left[\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta')-\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)\right]r'^2\sin\theta'dr'd\theta'd\phi'$$

After cancellation

$$\frac{q}{2\pi}\int(r')^nP_n(\cos\alpha)\left[\delta(r'-d)\delta(\theta')-\delta(r'-d)\delta(\theta'-\pi)\right]dr'd\theta'd\phi'$$

Integration over $r'$ gives

$$\frac{q}{2\p\thinspace d^{\thinspacen}\int P_n(\cos\alpha)\left[\delta(\theta')-\delta(\theta'-\pi)\right]d\theta'd\phi'$$

Recalling that

$$\cos \alpha = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$$

and using

$$P_l(\cos\alpha)\delta(\theta') = P_l(\sin(\theta)\sin 0\cos(\phi-\phi')+\cos\theta\cos 0)=P_l(\cos\theta)$$

$$P_l(\cos\alpha)\delta(\theta-\pi) = P_l(\sin(\theta)\sin 0\cos(\phi-\phi')+\cos\theta\cos \pi)=P_l(-\cos \theta)$$

allows the integration over $\theta$ to be evaluated as

$$\frac{q}{2\p\thinspace d^{\thinspacen}\int P_n(\cos\alpha)\left[\delta(\theta')-\delta(\theta'-\pi)\right]d\theta'=\frac{q}{2\pi}d^{\thinspacen}[P_n(\cos\theta)-P_n(-\cos\theta)]\int d\phi'$$

Integration over $\phi'$ leaves

$\thinspace d^{\thinspacen}[P_n(\cos\theta)-P_n(-\cos\theta)]$$

Thus, 

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

simplifies to

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{d^{\thinspacen}}{r^{n+1}}[P_n(\cos\theta)-P_n(-\cos\theta)]$$

for $\pm q$ at $z=\pm d$

The $n=0, 2, ...$ Legendre polynomials are even functions, so $P_n(x)=P_n(-x)$. The $n=1, 3, ...$ Legendre polynomials are odd functions, os $P_n(x)=-P_n(-x)$. As a result, 

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{n=1,3,...}^{\infty}\frac{d^{\thinspacen}}{r^{n+1}}[2P_n(\cos\theta)]$$

or, using $n=2l+1$ and switching replacing $d$ with $z'$

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{z'^{2l+1}}{r^{2l+2}}[2P_l(\cos\theta)]=\frac{q}{4\pi\epsilon_0}\frac{2}{r}\sum_{l=0}^{\infty}\left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)$$

which matches the earlier results. This process can be repeated for $r\lt z'$ and the result is the above equation with $r$ and $z'$ swapped.
|}

$# Line of Charge 

Due on April 22nd before class starts.

A line of charge with a charge density of $\lambda$ is on the $z$-axis and extends from $z=-1$ to $z=1$. 

1. For $r\gt 1$, find the coefficients $A_l$ and $B_l$ for the potential expressed in the form

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

where $r$ and $\theta$ are the radial and polar angles in spherical coordinates.

2. For $(y,z)=(1,1)$, <span style="background-color:yellow">Correction: $(s,z)=(1,1)$</span> compute the ratio of the exact potential with the potential found from the above equation using only the $l=0, 1$, and $2$ terms.

1. See midterm

2.

$(s,z)=(1,1) \Rightarrow (r,\theta) = (\sqrt{2},\pi/4)$.

Using $P_2(x)=(3x^2-1)/2$,

$$P_2(\cos(\pi/4))=P_2(1/\sqrt{2})=\frac{1}{2}(3/2-1)=\frac{1}{4}$$

and so

$$
\begin{align}
\psi(1,1) & \approx k\lambda\left(\frac{2}{\sqrt{2}} + \frac{2}{3}\frac{1}{\sqrt{2}^3}P_2(1/\sqrt{2})\right) \\
& = k\lambda\sqrt{2}\left(1 + \frac{1}{24}\right)\\
& = 1.4371k\lambda
\end{align}
$$

2.

$$\psi(s,z) = k\int_{-1}^1\frac{\lambda dz'}{\sqrt{(z-z')^2 + s^2}}$$

This integral can be looked up or solved using trigonometric substitutions. The result is

$$\psi(s,z) = k\lambda\ln\left[\frac{1+z+\sqrt{(1+z)^2 + s^2}}{z-1+\sqrt{(z-1)^2 + s^2}}\right]$$

$$\psi(1,1) \approx 1.4436k\lambda$$

$$\frac{\psi_{approx}}{\psi_{exact}}\simeq 1.02$$

The following is a Python script that can be used to explore the accuracy using NumPy's Legendre polynomial functions.

```Python
import numpy as np

z = 1
s = 1

N = (1+z)+ np.sqrt((1+z)**2 + s**2)
D = -(1-z) + np.sqrt((1-z)**2 + s**2)
psi_e = np.log(N/D)

r = np.sqrt(s**2 + z**2)
x = z/np.sqrt(s**2 + z**2)
psi_a = 2/r + ((2/3)/np.power(r,3))*(1/2)*(3*x**2-1)

print('Exact: {0:.4f}; Approximate: {1:.4f}; Approximate/Exact: {2:.4f}'
      .format(psi_e, psi_a, psi_a/psi_e))

1. Compute solution out to l = 10
c = np.zeros(10)
for k in range(1,10,2):
    c[k-1] = (2/k)/np.power(r,k)
    
l = np.polynomial.legendre.legval(x,c)
print(l)
```

\newpage

# Legendre Polynomials

http://web.uconn.edu/~ch351vc/Leg3/node1.html

http://bolvan.ph.utexas.edu/~vadim/classes/17f/mme.pdf


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

This form of  $1/|\mathbf{x}-\mathbf{x}'|$ with $\gamma = \theta$ follows from Taylor series expansion of $1/|z-z'|$, the general solution of $\nabla^2\Psi(r,\theta)=0$, and the uniqueness of solutions to Laplace's equation. ("Azimuthal symmetry trick"; See Section 3.3 of Jackson).  The result is

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

 Note that in this derivation, the constraint is ${r'}\gt {r}$ or ${r} \gt {r'}$.

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

$\displaystyle I(\mathbf{x}) = \int_0^{\infty}(r')^l\frac{q}{r'^2}\delta(r'-y_o)r'^2dr'\int_0^{2\pi}\int_0^\pi\delta(\theta'-\pi/2)\delta(\phi'-\pi/2)P_l\big(\cos(\gamma(\theta,\phi,\theta',\phi')\big)\sin\theta'd\theta'd\phi'
$

$\displaystyle = qy_o^l\int_0^{2\pi}\int_0^\pi\delta(\theta'-\pi/2)\delta(\phi'-\pi/2)P_l\big(\cos(\gamma(\theta,\phi,\theta',\phi')\big)\sin\theta'd\theta'd\phi'$

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

\newpage

# Spherical Harmonics/Associated Legendre Functions

$$
\frac{1}{|\mathbf{x}-\mathbf{x}'|} =
\begin{cases}
\displaystyle\sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r'^{l}}{r^{l+1}}Y^*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)  & \mbox{if } r \gt r' \\ \\
\displaystyle\sum_{l=0}^\infty \sum_{m=-l}^l \frac{4\pi}{2l+1}\frac{r^{l}}{r'^{l+1}}Y^*\_{lm}(\theta',\phi')Y_{lm}(\theta,\phi) & \mbox{if } r \lt r'
\end{cases}
$$

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

$# Comparison of Legendre and Spherical Harmonic Forms

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
\Phi_{l=1}(r,\theta,\phi) = \frac{1}{4\pi\epsilon_0}\frac{1}{r^2}\int r'\big(\sin\theta\sin\theta'\cos(\phi-\phi') + \cos\theta\cos\theta'\big) \rho(r',\theta',\phi')r'^2\sin\theta dr' d\theta' d\phi'
$

Spherical Harmonic:

$\displaystyle\Phi_{l=1} = \frac{1}{3\epsilon_o}\frac{Y_{lm}(\theta,\phi)}{r^{l+1}}\left[q^\*\_{11} + q_{10} + q_{11}\right]$

$\displaystyle q_{lm} = \int (r')^lY^*_{lm}(\theta',\phi')\rho(r',\theta',\phi')r'^2\sin\theta dr' d\theta' d\phi'$

To plot $\Phi$ for a grid of $(r,\theta,\phi)$ values, one integration is needed for each grid point for Legendre form. In the spherical harmonic form, three integrations are needed. Then for each grid point, only evaluation of $Y_{lm}(\theta,\phi)/r^{l+1}$ is needed.  

If only one value of $(r,\theta,\phi)$ is needed, 3x as many integrations needed for spherical harmonic form over Legendre form