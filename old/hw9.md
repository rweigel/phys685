# HW 9

## Force on Current Loop 

The circular loop with radius $b$ lies in the $z=d$ plane ($d\gt 0$), and the $z$ axis passes through its center. There is a current $I$ in the loop in the direction shown in the following figure.

<img src="figures/loop.svg"/>

A magnetic dipole at the origin creates a magnetic field of

$$\mathbf{B}=\frac{\mu_o}{4\pi}\frac{m_o}{r^3}\left(2\cos\theta\hat{\mathbf{r}}+\sin\theta\hat{\boldsymbol{\theta}}\right)$$

1\. Use eqn 5.12 in Jackson 3rd ed. ($\mathbf{F}=\int \mathbf{J}(\mathbf{x})\times \mathbf{B}(\mathbf{x})d^3x$) to find the force on the loop in cartesian coordinates.

2\. Find the force on the loop in cartesian coordinates using eqn 5.69 of Jackson 3rd ed. ($\mathbf{F}=\boldsymbol{\nabla}(\mathbf{m}\cdot\mathbf{B})$).

3\. Write your answer to 1. as a power series in terms of powers of $b/d$ (assume $b/d\ll 1)$ (if 1. and 2. don't match).

**Solution**

%There were several common errors. 

%1. Some reported a force that depended on $r$ and $\theta$ either explicity or implicitly because their unit vectors appeared in their answer. It does not make sense for the force on an object to depend on a coordinate. It should depend on the parameters given in the problem. In addition, the force depended on a coordinate, we would write $\mathbf{F}(\mathbf{x})=\int \mathbf{J}\times \mathbf{B}d^3x'$, which we don't - see the previous problem.
%1. When computing the gradient of a function that involved $r$, $r$ was treated as a constant. More on this in the solution.
%1. The wrong delta function representation of $\mathbf{J}$. You know that you need to get $\int \mathbf{I}\times \mathbf{B} dl$ after evaluating the delta function in the volume integral given, so this could have been used as a check that you had the correct delta function representation of $\mathbf{J}$.

1\.


Many students had questions about representing $\mathbf{J}$ with a delta function. As a guide, recall that you know that after application of the delta function

$$\mathbf{F}=\int \mathbf{J}\times \mathbf{B}\thinspace d^3x$$

should be

$$\mathbf{F}=\int \mathbf{I}\times\mathbf{B}\thinspace dl$$

where $\mathbf{B}$ is evaluated at the location of the differential elements $dl$. It is easier to find the delta representation of $\mathbf{J}$ in cylindrical coordinates, but most attempted modifying Jackson's equation 5.33 for a current loop of radius $a$ in the $x$-$y$ plane and centered on the origin:

$$J_{\phi}=I\sin\theta\thinspace\delta(\cos\theta)\frac{\delta (r-a)}{a}$$

where

$$\mathbf{J}=J_{\phi}(-\sin\phi\thinspace\hat{\mathbf{x}}+\cos\phi\thinspace\hat{\mathbf{y}})$$

By delta function identity #5 on page 26 of Jackson 3rd Edition, $J_{\phi}$ above is equivalent to 

$$J_{\phi}=I\delta(\theta-\pi/2)\frac{\delta (r-a)}{a}$$

You can (correctly) guess and that show that for this problem, replacing $\pi/2$ with $\theta_o$ and $a$ with $r_o$,  where $\tan\theta_o=b/d$ and $r_o=\sqrt{d^2+b^2}$ will result the volume integral $\int \mathbf{J}\times \mathbf{B}\thinspace d^3x$ reducing to the line integral $\int \mathbf{I}\times\mathbf{B}\thinspace dl$.


----

_Note_

Several students asked how to derive Jackson's equation or the guessed modified equation, so I'll derive it here. A student also mentioned that they found [a post on StackExchange](https://physics.stackexchange.com/questions/128732/describing-a-circular-current-loop-as-delta-functions), but that it didn't quite help. We need to find

$$\mathbf{J} = J(r,\theta)(-\sin\phi\thinspace\hat{\mathbf{x}}+\cos\phi\thinspace\hat{\mathbf{y}})$$

where $J(r,\theta)$ has the property that it is zero except for $(r,\theta)$ on the loop. $\delta(r-r_o)$ is zero except on the surface of a sphere of radius $r_o$ and $\delta(\theta-\theta_o)$ is zero except on the surface of a cone with apex angle $\theta_o$. The product of these two delta functions (corresponding to the intersection of these two surfaces) is non-zero only at positions on the loop. As in charge distribution problems, we need to find a constant $C$ in

$$J(r,\theta)=C\delta(r-r_o)\delta(\theta-\theta_o)$$

where $\tan\theta_o=b/d$ and $r_o=\sqrt{d^2+b^2}$. To determine $C$, note that integrating $J$ over all space is equivalent to multiplying the current by the length of the wire it flows through.

$$2\pi b I = \int J\thinspace d^3x=C\int \delta(r-r_o)\delta(\theta-\theta_o)\sin\theta\thinspace r^2\thinspace dr\thinspace d\theta\thinspace d\phi$$

$$2\pi b I = C2\pi\sin\theta_o r_o^2\Rightarrow C = \frac{bI}{r_o^2\sin\theta_o }$$

$$J(r,\theta)=\frac{I b}{\sin\theta_o r_o^2}\delta(r-r_o)\delta(\theta-\theta_o)=\frac{I}{r_o}\delta(r-r_o)\delta(\theta-\theta_o)$$

where $b = r_o\sin\theta_o$ was used for the last equality. When $\theta_o=\pi/2$, $r_o=b$ we recover Jackson's equation.

----

$$
\begin{align*}
\mathbf{F} & = \int \mathbf{J}\times \mathbf{B}d^3x\\
& = \int  J(r,\theta)(-\sin\phi\hat{\mathbf{x}}+\cos\phi\hat{\mathbf{y}})\times \mathbf{B}(r,\theta)r^2\sin\theta d\theta d\phi\\
& = \int  \frac{I}{r_o}\delta(r-r_o)\delta(\theta-\theta_o)(-\sin\phi \hat{\mathbf{x}}+\cos\phi\hat{\mathbf{y}})\times \mathbf{B}(r,\theta)r^2\sin\theta d\theta d\phi\\
& = \int I (-\sin\phi\hat{\mathbf{x}}+\cos\phi\hat{\mathbf{y}})\times \mathbf{B}(r_o,\theta_o) r_o\sin\theta_o d\phi\\
& = \int I (-\sin\phi\hat{\mathbf{x}}+\cos\phi\hat{\mathbf{y}})\times \mathbf{B}(r_o,\theta_o) b d\phi
\end{align*}
$$

Note that with $dl=b d\phi$ the last integral above can be written as 

$$
\mathbf{F} = \int \mathbf{I}\times \mathbf{B}(r_o,\theta_o)dl
$$

Evaluating the cross product gives (see the note below for a more straightforward approach)

$$
\begin{align*}
(-\sin\phi\thinspace\hat{\mathbf{x}}+\cos\phi\thinspace\hat{\mathbf{y}})\times \mathbf{B}(r_o,\theta_o)
&=
\hat{\boldsymbol{\phi}}\times \frac{\mu_o}{4\pi}\frac{m_o}{r^3}\left(2\cos\theta\hat{\mathbf{r}}+\sin\theta\hat{\boldsymbol{\theta}}\right)\\
&=
\frac{\mu_oI}{4\pi}\frac{m_o}{r^3}(2\cos\theta\hat{\boldsymbol{\phi}}\times\hat{\mathbf{r}}+\sin\theta\hat{\boldsymbol{\phi}}\times\hat{\boldsymbol{\theta}})\\
&=
\frac{\mu_oI}{4\pi}\frac{m_o}{r^3}(2\cos\theta\hat{\boldsymbol{\theta}}-\sin\theta\hat{\mathbf{r}})\end{align*}
$$

Non-cartesian vectors must be converted to cartesian prior to integration. Use the spherical-to-cartesian transformation matrix

$$\begin{bmatrix}{\hat{\boldsymbol{r}}} \\ {\hat{\boldsymbol{\theta }}} \\ {\hat{\boldsymbol{\phi }}}\end{bmatrix} = \begin{bmatrix}\sin \theta\cos \phi & \sin\theta \sin\phi & \cos\theta \\ \cos\theta \cos\phi & \cos\theta \sin\phi & -\sin\theta \\ -\sin\phi & \cos\phi & 0 \end{bmatrix} \begin{bmatrix}{\hat{\mathbf{x}}} \\ {\hat{\mathbf{y}}} \\{\hat{\mathbf{z}}}\end{bmatrix}$$

to write the spherical unit vectors $\hat{\boldsymbol{\theta}}$ and $\hat{\mathbf{r}}$ using cartesian unit vectors and then integrate with respect to $d\phi$. The integrals multiplied by $\xhat$ and $\yhat$ should evaluate to zero. The result is

$$\mathbf{F}=-\frac{3}{2}\frac{\mu_om_oIdb^2}{(b^2+d^2)^{5/2}}\hat{\mathbf{z}}$$

----

_Note_

One can get equivalent results by converting $\mathbf{B}$ into cartesian using the above matrix and doing the cross product with $\mathbf{J}$ written with cartesian unit vectors. The components of $B$ in cartesian coordinates, with $r=\sqrt{x^2+y^2+z^2}$, are

$$B_x=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{(x^2+y^2+z^2)^{5/2}}=\frac{\mu_oI\pi a^2}{4\pi}\frac{3xz}{r^5}$$

$$B_y=\frac{\mu_oI\pi a^2}{4\pi}\frac{3yz}{r^5}$$

$$B_z=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

----

_Checking answer_

The problem statement asked for it to be solved starting with a general equation. However, there is an easier way to get the solution.

Compute the horizontal, $B_s$, and vertical, $B_z$, magnetic field at all points on the loop. (Equations for both are given above.) Then compute the horizontal and vertical forces created by these two fields individually. 

That is, use $\mathbf{I}\times\mathbf{B}=\mathbf{I}\times (B_s\hat{\mathbf{s}} + B_z\zhat)=(\mathbf{I}\times B_s \hat{\mathbf{s}}) + (\mathbf{I}\times B_z\zhat)$ with $\mathbf{I}=-I\hat{\boldsymbol{\phi}}$ and take the cross products of the cylindrical unit vectors.

From $\mathbf{I}\times B_z\zhat$, $B_z$ results in a horizontal force of $-IdlB_z(r_o,\theta_o)\hat{\mathbf{s}}$ on each $dl$.  This horizontal force averages to zero because the total vertical force is obtained by using $dl=bd\phi$ and integrating over $\phi$ from $0$ to $2\pi$ and the integral of $\hat{\mathbf{s}}$ is zero. This should be clear from a diagram that this force tends to compress the ring as its direction is towards the center of the ring all $dl$.

From $\mathbf{I}\times B_s\zhat$, $B_s$ results in a vertical force of $-IdlB_s\hat{\mathbf{z}}$ on each $dl$.


$$\int_0^{2\pi}-IB_sbd\phi\hat{\mathbf{z}}$$

The magnitude of horizontal field is $B_s=\sqrt{B_x^2+B_y^2}$ and $B_x$ and $B_y$ given earlier. Neither depend on $\phi$. We have

$$B_s(x,y)=\sqrt{B_x^2+B_y^2}=\frac{\mu_o}{4\pi}\frac{3m_oz}{r^5}\sqrt{x^2+y^2}$$

On the loop, $z=d$, $x^2+y^2=b^2$, and $r^2=b^2+d^2$. Putting this all together gives a net force of

$$\mathbf{F}=-\frac{3}{2}\frac{\mu_om_oIdb^2}{(b^2+d^2)^{5/2}}\hat{\mathbf{z}}$$

----

2\.

$$\mathbf{m}=Ib^2\hat{\mathbf{z}}$$

$$\mathbf{m}\cdot\mathbf{B}=Ib^2B_z$$

From above,

$$B_z=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

The formula 

$$\mathbf{F}=\boldsymbol{\nabla}(\mathbf{m}\cdot\mathbf{B})$$

was derived by expanding $\mathbf{B}$ about around a point near a current loop and under the assumption that the change in $\mathbf{B}$ was small over the area of the loop and so the result must be evaluated at a point near the current loop, for which I use $(x,y,z)=(0,0,d)$. Jackson states that $\mathbf{B}$ is expanded about a "suitable origin" but does not elaborate on what constitutes suitableness. By default, it makes the most sense to expand about the center of the current distribution, but if the field changes more rapidly on one part of the current distribution, one may get a more accurate answer if the expansion is performed where the field changes the most. (However, if the answer strongly depends on the origin, probably this approximate formula should not be used.)

Using $\mathbf{m}=I\mathbf{a}=-I\pi b^2\zhat$,

$$\boldsymbol{\nabla}(\mathbf{m}\cdot\mathbf{B})=\boldsymbol{\nabla}\left[(-I\pi b^2\zhat)\bfcdot \mathbf{B}\right]=-I\pi b^2\boldsymbol{\nabla}B_z=-I\pi b^2\zhat\frac{\partial B_z}{\partial z}$$

It is import to not plug in values for $r$ and $z$ prior to computing the derivative (if constants are used for both, one gets a force of zero). The formula for $\mathbf{F}$ given above was derived under the assumption that the result of the gradient is evaluated at the point as opposed to the argument of the gradient being evaluated at a point. That is, one needs to substitute values for the variables after the derivatives are computed. (Think of finding the slope of $y=x^2$ at $x=2$. You don't first set $x=2$, giving $y=4$ and $dy/dx = 0$).


After computing the derivative using

$$B_z(x,y,z)=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

with $r=\sqrt{x^2+y^2+z^2}$ and setting $(x,y,z)=(0,0,d)$ the result is

$$\mathbf{F}=-\frac{3}{2}\frac{\mu_om_oIb^2}{d^4}\hat{\mathbf{z}}$$

If interested, try evaluating the gradient of $B_z$ about a different location, say $0,b,z_o$ -- you should get the same result to first order in a $b/d$  expansion. However, there will be a net force in the $y$-direction, which does not match the exact result. Therefore this choice of origin seems not "suitable". But to know it was not suitable, we had to know the exact result! As a result, I would argue that the approximate formula for an arbitrary current distribution is mostly useful for interpretation rather than calculation;  $\mathbf{F}=\boldsymbol{\nabla}(\mathbf{m}\cdot\mathbf{B})$ means a gradient in its argument will result in a force.

The most common error students made was setting $r=\sqrt{b^2+d^2}$ in

$$B_z(x,y,z)=\frac{\mu_oI\pi a^2}{4\pi}\frac{3z^2-r^2}{r^5}$$

instead of using $r = \sqrt{x^2+y^2+z^2}$.

An alternative approach is to use the fact that the force of the dipole at the origin on the ring will be equal and opposite to the force of the ring on the dipole at the origin. Using the dipole moment of $m_o\zhat$ for the dipole at the origin and the $\mathbf{B}$ due to the ring at the origin will give a force that matches the answer to part 1. The reason we get two different answers is the equation for $\mathbf{F}$ was derived under the assumption that $\mathbf{B}$ is nearly constant in the region of the current distribution. The field due to the dipole at the origin is not constant in the region of the ring. However, the field due to the ring is constant over the current distribution of the dipole at the origin because the dipole at the origin is infinitesimal (a "perfect" magnetic dipole). (We are not told that the dipole at the origin is a perfect dipole, but it must be because the equation for its field is the same as that for a perfect dipole.)

3.

The result from 1. was

$$\mathbf{F}=-\frac{3}{2}\frac{\mu_om_oIdb^2}{(b^2+d^2)^{5/2}}\hat{\mathbf{z}}$$

or, after factoring out a $d^5$ in the denominator,

$$\mathbf{F}=-\frac{3}{2}\frac{\mu_om_oIb^2}{d^4\left(1+\left(\frac{b}{d}\right)^2\right)^{5/2}}\hat{\mathbf{z}}\simeq -\frac{3}{2}\frac{\mu_om_oIb^2}{d^4}\hat{\mathbf{z}}\left(1-\frac{5}{2}\frac{b^2}{d^2}\right)$$

which matches the result from 3. in the limit that $b/d\rightarrow 0$, as expected because the relevant length scales that determine how much $\mathbf{B}$ changes over the loop are the distance of the loop from the dipole to the length scale of the loop.


## Surface Current on Cylinder 

A hollow and open-ended cylinder of height $2h$ and radius $b$ is centered on the origin and aligned with the $z$-axis. The curved surface of the cylinder has a surface current of $K_o\hat{\boldsymbol{\phi}}$.

<img src="figures/cylinder_surface_current.svg"/>

1\. Find $\mathbf{B}(z)$ using the Biot--Savart formula.

2\. Use the formula

$$\frac{1}{\sqrt{1-2ut+t^2}}=\sum_{l=0}^{\infty}P_l(u)t^l$$

to express $B_z(z)$ as a power series involving the Legendre polynomials, $P_l$, and $z^l$.

**Solution**

1\.

$$\mathbf{B}(\mathbf{x})=\frac{\mu_o}{4\pi}\int\frac{\mathbf{K}\times (\mathbf{x}-\mathbf{x'})}{|\mathbf{x}-\mathbf{x'}|^3}da'$$

Using

$\mathbf{x}'=b\hat{\mathbf{s}'} + z'\zhat = b\cos\phi'\xhat + b\sin\phi'\yhat+z'\zhat$,

$\mathbf{x}=z\zhat$, and

$\mathbf{K}=K_o\hat{\boldsymbol{\phi'}}=K_o(-\sin\phi'\xhat+\cos\phi'\yhat)$

The numerator of the integrand is

$$\mathbf{K}\times (\mathbf{x}-\mathbf{x'})=K_o\hat{\boldsymbol{\phi'}}\times(b\hat{\mathbf{s}'} + z'\zhat)=K_ob\zhat+K_oz'\hat{\mathbf{s}'}$$

and the denominator is

$$|\mathbf{x}-\mathbf{x'}|^3=\left(b^2+(z-z')^2\right)^{3/2}$$

$$\mathbf{B}(z)=\frac{\mu_o K_o b}{4\pi}\int_0^{2\pi}\int_{-h}^{h}\frac{1}{\left(b^2+(z-z')^2\right)^{3/2}} bd\phi' dz'(K_ob\zhat+K_oz'\hat{\mathbf{s}'})$$

The integral of $\hat{\mathbf{s}'}$ over $\phi'=0$ to $2\pi$ will be zero and this is expected based on cancellation symmetry (for each $dI_1$ on the surface, there is another $dI_2$ whos horizontal field cancels that from $dI_1$). This leaves

$$B_z(z)=\frac{\mu_o K_o b }{4\pi}2\pi b\int_{-h}^{h}\frac{1}{\left(b^2+(z-z')^2\right)^{3/2}}  dz'$$

Alterntatively, one may arrive at this by starting with the equation for the field due to a loop in the $x$--$y$ plane and centered on the origin, which is 

$$B_z(z)=\frac{\mu_o}{4\pi}\frac{2\pi b^2 I}{(b^2 + z^2)^{3/2}}$$

To find the field due to a cylinder, let $z\rightarrow z-z'$ and $I\rightarrow dI=K_odz'$ and integrate:

$$B_z(z)=\frac{\mu_o}{4\pi}\int_{-h}^{h} \frac{2\pi b^2 K_odz'}{(b^2+(z-z')^2)^{3/2}}$$

Integration gives

$$B_z(z) = \frac{\mu_oK_o}{2}\left[\frac{z+h}{\sqrt{b^2+(z+h)^2}}-\frac{z-h}{\sqrt{b^2+(z-h)^2}}\right]$$


_Checks_:

1. For $z=0$ and $h\ll b$, the equivalent system is a loop of current in the $x$--$y$ plane with a total current of $I=K_o 2h$. This matches the answer of the simple problem of finding the magnetic field at the center of a current loop carrying a current $I$. Alternatively, it is the result one finds using $z=0$ and $h\ll b$ in the starting equation of

    $$B_z(z) = \frac{\mu_oK_o}{2}\left[\frac{z+h}{\sqrt{b^2+(z+h)^2}}-\frac{z-h}{\sqrt{b^2+(z-h)^2}}\right]$$

2. For $h\gg b$, the system approaches an infinite solenoid, and the solution should be independent of $z$ near the center. Setting $b=0$ and $z=0$ in the above equation gives 
 
    $$B_z(z) = \frac{\mu_oK_o}{2}\left[\frac{h}{|h|}-\frac{-h}{|-h|}\right]=\mu_oK_o$$

    which is the field inside an ideal solenoid.
    
    More formally, one could use the conditions $b/h\ll 1$ and $z/h \ll 1$ and the binomial expansion of the exact formula for $B_z(z)$). See the next part of the problem.

2\. We need to expand

$$B_z(z) = \frac{\mu_oK_o}{2}\left[\frac{z+h}{\sqrt{b^2+(z+h)^2}}-\frac{z-h}{\sqrt{b^2+(z-h)^2}}\right]$$

Let $B_z(z)=B_z^+-B_z^-$. Expanding the square in the denominator of $B_z^+$ gives
 
$$B_z^+(z) = \frac{\mu_oK_o}{2}\left[\frac{z+h}{\sqrt{b^2+h^2+2zh+z^2}}\right]$$

Factoring out $b^2+h^2$ in the denominator gives

$$B_z^+(z) = \frac{\mu_oK_o}{2\sqrt{b^2+h^2}}\left[\frac{z+h}{\sqrt{1+2zh/(b^2+h^2)+z^2/(b^2+h^2)}}\right]$$

Defining $t=z/\sqrt{b^2+h^2}$ gives

$$B_z^+(z) = \frac{\mu_oK_o}{2\sqrt{b^2+h^2}}(z+h)\left[\frac{1}{\sqrt{1+2ht/\sqrt{b^2+h^2}+t^2}}\right]$$

Defining $u=-h/\sqrt{b^2+h^2}$ (note that $u$ is related to the angle $\alpha$ from the $z$--axis to the rim of the cylinder: $\cos\alpha = -u = h/\sqrt{b^2+h^2}$), we have

$$B_z^+(z) = \frac{\mu_oK_o}{2\sqrt{b^2+h^2}}(z+h)\left[\frac{1}{\sqrt{1-2ut+t^2}}\right]$$

Using the given formula,

$$B_z^+(z) = \frac{\mu_oK_o}{2\sqrt{b^2+h^2}}(z+h)\sum_{l=0}^{\infty}P_l(u)t^l$$

or, using $z=t\sqrt{b^2+h^2}$,

$$B_z^+(z) = \frac{\mu_oK_o}{2\sqrt{b^2+h^2}}(t\sqrt{b^2+h^2}+h)\sum_{l=0}^{\infty}P_l(u)t^l$$

which simplifies to

$$B_z^+(z) = \frac{\mu_oK_o}{2}(t-u)\sum_{l=0}^{\infty}P_l(u)t^l$$

$B_z^-(z)$ is obtained by replacing $u$ with $-u$ in the expression for $B_z^+(z)$. Then 

$$B_z(z)=B_z^+(z)-B_z^-(z) = \frac{\mu_oK_o}{2}\left[(t-u)\sum_{l=0}^{\infty}P_l(u)t^l-(t+u)\sum_{l=0}^{\infty}P_l(-u)t^l\right]$$

or

$$\frac{B_z(z)}{\mu_oK_o}= \frac{1}{2}\left[(t-u)\sum_{l=0}^{\infty}P_l(u)t^l-(t+u)\sum_{l=0}^{\infty}P_l(-u)t^l\right]$$

To simplify, use $P_l(-u)=P_l(u)$ for $l=0, 2, ...$ and $P_l(-u)=-P_l(u)$ for $l=1,3,...$. Then

$$\frac{B_z(z)}{\mu_oK_o}= -u\sum_{l=0,2,...}^{\infty}P_l(u)t^l+\sum_{l=1,3,...}^{\infty}P_l(u)t^{l+1}$$

Shift the index on second sum so $t^l$ appears in both sums:

$$\frac{B_z(z)}{\mu_oK_o}= -u\sum_{l=0,2,...}^{\infty}P_l(u)t^l+\sum_{l=2,4,...}^{\infty}P_{l-1}(u)t^{l}$$

Remove $l=0$ from first sum so both sums are over the same $l$--values:

$$\frac{B_z(z)}{\mu_oK_o}=-u- \sum_{l=2,4,..}^{\infty}uP_l(u)t^l+\sum_{l=2,4,...}^{\infty}P_{l-1}(u)t^{l}$$

Combine sums:

$$\frac{B_z(z)}{\mu_oK_o}=-u+ \sum_{l=2,4,..}^{\infty}\big(P_{l-1}(u)-uP_l(u)\big)t^{l}$$

Using $\cos\alpha = -u$ gives

$$\frac{B_z(z)}{\mu_oK_o}=\cos\alpha+ \sum_{l=2,4,..}^{\infty}\big(P_{l-1}(-\cos\alpha)+\cos\alpha P_l(-\cos\alpha)\big)t^{l}$$

Using $P_l(-u)=P_l(u)$ for $l=0, 2, ...$ and $P_l(-u)=-P_l(u)$ for $l=1,3,...$ gives

$$\boxed{\frac{B_z(z)}{\mu_oK_o}=\cos\alpha+ \sum_{l=2,4,..}^{\infty}\big(\cos\alpha P_l(\cos\alpha)-P_{l-1}(\cos\alpha)\big)t^{l}}$$

where $t=z/\sqrt{b^2+h^2}$. The answer only contains terms proportional to $z^2$, $z^4$, ....

%Replace $l$ with $2l+2$ so the sum over $l=0,1,...$:

%$$\frac{B_z(z)}{\mu_oK_o}=-u+ \sum_{l=0}^{\infty}\big(P_{2l+1}(u)-uP_{2l+2}(u)\big)t^{2l+2}$$

%Rewrite using $t=z/\sqrt{b^2+h^2}$ and $u=-h/\sqrt{b^2+h^2}$ and use $\cos\alpha=-u$:

%$$\frac{B_z(z)}{\mu_oK_o}=\cos\alpha + \sum_{l=0}^{\infty}\big(P_{2l+1}(-\cos\alpha)+\cos\alpha P_{2l+2}(-\cos\alpha)\big)t^{2l+2}$$

%Use $P_l(-u)=P_l(u)$ for $l=0, 2, ...$ and $P_l(-u)=-P_l(u)$:

%$$\boxed{\frac{B_z(z)}{\mu_oK_o}=\cos\alpha + \sum_{l=0}^{\infty}\Big(\cos\alpha P_{2l+2}(\cos\alpha)-P_{2l+1}(\cos\alpha)\Big)\left(\frac{z}{\sqrt{b^2+h^2}}\right)^{2l+2}}$$

With this magnetic field, one can obtain the solution for the magnetic field inside of cylinder.

Inside of the cylinder, $\nabla^2\Phi_m=0$ is satisfied, where $\mathbf{B}=-\boldsymbol{\nabla}\Phi_m$. The problem has azimuthal symmetry and so $\Phi_m$ must be expressible in form

$$\Phi_m(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

Using $\Phi_m(z)=\sum_{l=0}^{\infty}z^lA_l$ and

$$B_z(z)=-\frac{\partial \Phi_m(z)}{\partial z} = -\sum_{l=0}^{\infty}lz^{l-1}A_l=-A_1-2A_2z-3A_3z^2+...$$

%$$\frac{B_z(z)}{\mu_oK_o}=\cos\alpha + \sum_{l=0}^{\infty}\Big(\cos\alpha P_{2l+2}(\cos\alpha)-P_{2l+1}(\cos\alpha)\Big)\left(\frac{z}{\sqrt{b^2+h^2}}\right)^{2l+2}$$

The first four $A$ coefficients are

$$A_1=-\mu_oK_o\cos\alpha$$

$A_2=0$

$$A_3=-\frac{\mu_oK_o}{3}\frac{\cos\alpha P_2(\cos\alpha)-P_1(\cos\alpha)}{b^2+h^2}$$

$$A_4=0$$

Or, in general

$A_1=-\mu_oK_o\cos\alpha$

and for $l=3,5,...$,

$$A_l=-\frac{\mu_oK_o}{l}\frac{\cos\alpha P_{l-1}(\cos\alpha)-P_{l-2}(\cos\alpha)}{(b^2+h^2)^{(l-1)/2}}$$

One can then use

$$\mathbf{B}(r,\theta) = -\mathbf{\nabla}\Phi_m(r,\theta)=-\mathbf{\nabla}\sum_{l=0}^{\infty}A_lr^lP_l(\cos\theta)$$

to arrive at an expression for $\mathbf{B}$ inside the cylinder. Technically the solution is valid for $r\lt b$ (required for Laplace's equation to be true), and $r\lt \sqrt{b^2+h^2}$ (required for the power series expansion). So the solution is valid inside the cylinder and inside a dome on both ends of the cylinder.

$$
\mathbf{B}(r,\theta) = 
-\mathbf{\nabla} \Phi_m(r,\theta) = 
-
{\partial \Phi_m \over \partial r}\hat{\mathbf r}
-
{1 \over r}{\partial \Phi_m \over \partial \theta}\hat{\boldsymbol \theta}=
-B_r\hat{\mathbf r}-B_\theta\hat{\boldsymbol \theta}
$$

$$\Phi_m(r,\theta)=\sum_{l=0}^{\infty}r^lA_lP_l(\cos\theta)=A_0+rA_1P_1(\cos\theta)+r^2A_2P_2(\cos\theta)+...$$

$$B_r=-{\partial \Phi_m \over \partial r}\hat{\boldsymbol \theta}=-A_1P_1(\cos\theta)-2rA_2P_2(\cos\theta)+...$$

$$B_\theta=-{1 \over r}{\partial \Phi_m \over \partial \theta}\hat{\boldsymbol \theta}=-\frac{1}{r}\left(rA_1\frac{d P_1(\cos\theta)}{d\theta}+r^2A_2\frac{d P_2(\cos\theta)}{d\theta}+...\right)$$

%$$A_1=-\cos\alpha$$

%$$A_2=0$$

%$$A_3=\frac{P_1(d)/d-P_2(d)}{3}$$

%$$A_4=0$$

%$$A_5=\frac{P_3(d)/d-P_4(d)}{5}$$

%$$...$$

%or

%$$P_l=\frac{P_{l-2}(d)/d-P_{l-1}(d)}{l}\quad l=3,5,...$$

%$$P_l=0\quad l=2,4,...$$

%Similar to electrostatic problems, the constant $A_o$ is arbitrary and cannot be fixed unless one is given $\Phi_m$ at a location in space.


_Alternative Method 2._

See http://dx.doi.org/10.1119/1.4906516, which uses a method that is similar to Method 1., but a general relationship was not derived.

_Alternative Method 3._

Use $J_{\phi}=I\sin(\theta'-\theta_o)\delta(r'-r_o)/r_o$ with $r_o=\sqrt{z^2+b^2}$ and $\tan\theta_o=b/z$ and follow the steps needed to arrive at Equation 5.44 of Jackson, which is the vector potential due to a ring in the $x-y$ plane and centered on the $z$-axis.  The equation will be valid for a ring that is shifted by a distance $z$. Set $I=K_odz$ and integrate from $z=-L$ to $z=L$. One will need to use equation 5.47 and integration by parts.

## Reading

Read 5.6--5.12 of Jackson and Chapter 6 of Griffiths, and be prepared to ask questions during class. (Questions on Discord are also welcome).

