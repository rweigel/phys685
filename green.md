
#green-s-reciprocity-theorem

#green-s-reciprocity-use&l=589&c=1

#green-s-identity-derivation&l=663&c=1

#alternative-derivation-of-reciprocity-for-continuous-rho&l=697&c=1

#jackson-equation-1-42&l=1017&c=1

#1-d-cartesian-green-function&l=775&c=1

#1-d-spherical-green-function&l=942&c=1


#long-rectangular-tube-with-sheet-of-charge&l=1240&c=1

#green-function-for-infinite-dome&l=1063&c=1

## Green Function Method 

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

1.## Preliminaries 

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

## 1-D Green Function 

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

## Parallel Plates with Charged Slab 

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

## U-Shaped Channel 

Due on April 15th before class starts.

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
|}