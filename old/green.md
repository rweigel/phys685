
# Reciprocity -- Discrete

#green-s-reciprocity-theorem

#green-s-reciprocity-use&l=589&c=1

# Reciprocity -- Continuous

#green-s-identity-derivation&l=663&c=1

#alternative-derivation-of-reciprocity-for-continuous-rho&l=697&c=1

# Green Function Solution General Equation I

#jackson-equation-1-42&l=1017&c=1

# Green Function Solution General Equation II

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

## Preliminaries 

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

# 1-D

## Parallel Plates with Charged Slab I

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

## Parallel Plates with Charged Slab II

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

# 2-D

## Long Tube with Sheet of Charge

#long-rectangular-tube-with-sheet-of-charge&l=1240&c=1

## Long Tube with Line of Charge

See HW 6.1

## U-Shaped Channel 

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

# 3-D

## Infinite Dome or Infinite Plane

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
