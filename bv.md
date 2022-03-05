# 1-D

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

1.

In spherical coordinates,

$$\nabla^2\Psi(r)=\frac{1}{r^2}\frac{\partial \Psi}{\partial r}\left(r^2\frac{\partial \Psi}{\partial r}\right)=\frac{1}{r^2}\frac{d \Psi}{dr}\left(r^2\frac{d \Psi}{dr}\right)$$

$$\frac{1}{r^2}\frac{d \Psi}{dr}\left(r^2\frac{d \Psi}{dr}\right)=0 \Rightarrow \left(r^2\frac{d \Psi}{dr}\right) = A\Rightarrow \frac{d \Psi}{dr} = Ar^2$$

where $A$ is a constant.  Integration gives

$$\Psi = A + \frac{B}{r}$$

Some students found the solution for $\nabla^2\Psi(r,\theta) = 0$, but technically this was not asked for (and was not needed for parts 2. and 3.)

2.

Answer:

$$\Psi_1 = V_b$$

$$\Psi_2(r) = V_b + (V_c-V_b)\frac{\frac{1}{r}-\frac{1}{b}}{\frac{1}{c}-\frac{1}{b}}$$

$$\Psi_3(r) = V_c + (V_R-V_c)\frac{\frac{1}{r}-\frac{1}{c}}{\frac{1}{R}-\frac{1}{c}}$$

where $\Psi_3(R)\equiv V_R$. If $R\gg c$ and $V_R=0$, then

$$\Psi_3(r) = V_c\thinspace\frac{c}{r}$$

If $V_R=V_c$, then

$$\Psi_3(r) = V_c$$

----
Call the region $b\le r\le c$ region 2. Then

$$\Psi_2(b)=V_b=A+\frac{B}{b}$$

$$\Psi_2(c)=V_c=A+\frac{B}{c}$$

$$\Psi_2(r) = V_b + (V_c-V_b)\frac{\frac{1}{r}-\frac{1}{b}}{\frac{1}{c}-\frac{1}{b}}$$

Using

$$\sigma_{b+}=-\epsilon_o\frac{\partial \Psi_2}{\partial r}\Bigg|_{r=b}$$

$$\sigma_{c-}=+\epsilon_o\frac{\partial \Psi_2}{\partial r}\Bigg|_{r=c}$$

where $b+$ means the outer surface of the shell with radius $b$ and $c-$ means the inner surface of the shell with radius $c$, it can be shown that $\sigma_{c-} c^2=-\sigma_{b+} b^2$. This means that $Q_{b+}=-Q_{c-}$.

The charge on the outer surface of the shell at $b$ is

$$Q_{b+}=\sigma_{b+}4\pi b^2=4\pi\epsilon_o(V_b-V_c)\frac{1}{\frac{1}{b}-\frac{1}{c}}$$

which is negative if $V_c > V_b$.

Call the region $r\le b$ region 1. Then

$$\Psi_1 = A + \frac{B}{r}$$

Typically we say $B=0$ so the solution does not "blow up".  There are two other ways to justify $B=0$. First, with $A=V_b$ and $B=0$, the potential satisfies the boundary condition at $r=b$ and $\Psi_1=V_b$ gives $\nabla^2\Psi_1=0$. By the uniqueness theorem, $\Psi=V_b$ is the solution. Second, if $B\ne 0$, $\nabla^2\Psi_1=-4\pi\delta(\mathbf{r})= -B\delta(r)/r^2$. Because, $\nabla^2\Psi=-\rho/\epsilon_o$, a non-zero $B$ means $\rho=\epsilon_oB\delta(r)/r^2$, which is the charge density for a point charge at the origin. But no point charge was given to exist there, so $B$ must be zero.

As mentioned on Piazza, I intentionally did not give a boundary condition for $r>c$ in the hopes that the question would be raised and so that I could make the point that a boundary value problem needs a ''closed'' surface (I won't take off if you didn't catch this, as mentioned earlier, this basic problem was given so the subtleties discussed here are easier to understand). Ideally, you realized that there is not a unique solution unless you specify the potential for $r>c$. This issue is discussed in section 1.9 of Jackson, which concludes with the statement that "electrostatic problems are specified by Dirichlet or Neumann boundary conditions on a '''closed'' surface''' So to have a unique solution for $r>c$, we must specify a boundary and information about the potential in that region''". Most students assumed the potential $V_{R}=0$ or $V_R=V_c$, where $R\gg c$. The general solution in this region can be written down using the solution for $\Psi_1$:

$$\Psi_3(r) = V_c + (V_R-V_c)\frac{\frac{1}{r}-\frac{1}{c}}{\frac{1}{R}-\frac{1}{c}}$$

One could also specify $d\Psi/dr$ on the boundary at $r=R$. Solving for $A$ and $B$ assuming the potential is given at $r=c$ as $V_c$ and $d\Psi/dr$ is given at $r=R$ gives

$$\Psi(r)=V_c+R^2\left(\frac{1}{c}-\frac{1}{r}\right)\frac{d\Psi}{dr}\Bigg|_{r=R}$$

----

3. 

In the Gauss' law method, one assumes charges of $Q_b$ and $Q_c$. The geometry is un-changed by a rotation by $\theta$ and $\phi$ and so the field and thus charge density on the surfaces must be independent of $\theta$ and $\phi$. The field can be argued to be radial in this case because for each charge on a sphere there will be another charge which exactly cancels its non-radial component, so $E_{\theta}=E_{\phi}=0$. These arguments allow writing $\mathbf{E}(r,\theta,\phi)=E_r(r)\hat{\mathbf{r}}$. Using a spherical Gaussian surface of radius $r$ for $r\lt b$, $\hat{\mathbf{n}}=\hat{\mathbf{r}}$

$$\oint\mathbf{E}\cdot \hat{\mathbf{r}}\thinspacer^2 d\Omega=E_r(r)\thinspacer^2\thinspace4\pi$$

Because $Q_{encl}=0$, this gives $E_r(r)=0$ for $r\ne 0$. For $r=0$, Gauss' law gives $E_r=0/0$. However, one can argue that $E_r=0$ by the cancellation discussed above.

For $b\lt r \lt c$, $Q_{encl}=Q_b$ and

$$E_r(r)=\frac{1}{4\pi\epsilon_o}\frac{Q_b}{r^2}$$

For $r \gt c$, $Q_{encl}=Q_b+Q_c$ and

$$E_r(r)=\frac{1}{4\pi\epsilon_o}\frac{Q_b+Q_c}{r^2}$$

To find the potential, integrate from $R$ to $r$

$$\Psi_3(r) - \Psi(R) = -\int^{r}_{R} E_r\thinspace dr$$

$$\Psi_3(r) = \Psi(R) + \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(\frac{1}{R}-\frac{1}{r} \right)\quad r\gt c$$

Integration from $r=c$ to $r$ gives

$$\Psi_2(r)-V_c=\frac{Q_b}{4\pi\epsilon_o}\left(\frac{1}{r}-\frac{1}{c} \right)$$

or

$$\Psi_2(r)=V_c+\frac{Q_b}{4\pi\epsilon_o}\left(\frac{1}{r}-\frac{1}{c} \right)\quad b\lt r\lt c$$

$Q_b$ can be solved for using $V(b)=V_b$, giving

$$Q_b=4\pi\epsilon_o\frac{V_b-V_c}{\left(\frac{1}{b}-\frac{1}{c} \right)}$$

This matches $Q_{b+}$ computed using the boundary value method. Using $Q_b$ in the equation for $\Psi_2$ gives

$$\Psi_2(r)=V_c+(V_c-V_b)\frac{\left(\frac{1}{r}-\frac{1}{c} \right)}{\left(\frac{1}{c}-\frac{1}{b} \right)}\quad b\lt r\lt c$$

Integration from $b$ to $r$ gives

$$\Psi_1(r)-V_b=0\Rightarrow \Psi_1(r)=V_b\quad r\lt b$$

In summary, thus far we have

$$\Psi_1(r)=V_b\quad r\lt b$$

$$\Psi_2(r)=V_c+(V_c-V_b)\frac{\left(\frac{1}{r}-\frac{1}{c} \right)}{\left(\frac{1}{c}-\frac{1}{b} \right)}\quad b\lt r\lt c$$

$$\Psi_3(r) = V_R + \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(\frac{1}{R}-\frac{1}{r} \right)\quad r\gt c$$

where 

$$Q_b=4\pi\epsilon_o\frac{V_b-V_c}{\left(\frac{1}{b}-\frac{1}{c} \right)}$$

If $V_R=V_c$, the equation for $\Psi_3$ evaluated at $r=c$ gives $Q_b=-Q_c$, and so

$$\Psi_3=V_c$$

In this case, all of the charge on the shell at $c$ is on its inner surface. If $V_R=0$ and $R\gg c$, then we get 

$$\Psi_3(c) = V_c = \frac{Q_b+Q_c}{4\pi\epsilon_o}\left(-\frac{1}{c} \right)$$

or

$$Q_b+Q_c = -cV_c4\pi\epsilon_o$$

and finally

$$\Psi_3(r) = V_c\frac{c}{r}\quad r\gt c$$

Note that here $Q_c$ is the charge on the inner and outer surface of the shell of radius $c$; in the boundary value method solution, I only computed the charge on the inner part of the shell with radius $c$. One could compute the charge on the outer part of the shell with radius $c$ using the boundary value method and show that $Q_{c+}+Q_{c-}$ equals the $Q_c$ found above. 

Physically, if the shell at $r=R$ is not at $V_c$, extra charge will need to be on the outer surface of the shell at $r=c$ in order to make the electric field in the shell at $r=R$ zero.

Finally, note that this problem is equivalent to the problem of two spherical capacitors in series and could have been solved simply by using the formula for the capacitance of a spherical capacitor.
|}

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

## Cylindrical -- $\sigma$ Given 

A non-conducting and infinitely long cylindrical shell of radius $b$ has a surface charge density of $\sigma=\sigma_o\sin\thinspace2\phi$.

1. Find $\Psi(\rho)$ using the boundary value method.

In class, I did the a problem for $\sigma=\sigma_o\cos\thinspace\phi$. In justifying dropping the $\rho^n$ and $\ln\rho$ terms, I mentioned that this was justified because the potential should go to zero as $\rho\rightarrow \infty$. What I neglected to mention is that this is because for large $\rho$, the system appears as a line of charge with linear charge density, $\lambda$, and $\lambda=0$ for the given $\sigma$. This can be seen by computing the linear charge density $\lambda = \int_0^{2\pi} \sigma b d\phi$.

2. Repeat 2. assuming $\sigma=\sigma_1 + \sigma_o\sin\thinspace2\phi$. In this case, the $A'_o\ln\rho$ term cannot be dropped; $A'_o$ is determined from the requirement that for large $\rho$, the potential should be that for a line of charge with linear denstiy $\lambda$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|

I'll solve part 2., which reduced to part 1. if $\sigma_1=0$. Some students had difficulty with part 2. even though they got part 1. The short-cut answer it to solve part 2. using superposition of two boundary value problems, one being the solution to part 1. and the other being the solution to a uniformly charged cylinder.

2.

The general solution to Laplace's equation in cylindrical coordinates for a problem with azimuthal symmetry is

$$\psi=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)\rho^n+a_o\ln\rho+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)\rho^{-n}$$

We can conclude that the $\rho^n$ terms are zero for the potential outside of the cylinder because at large $\rho$ the cylinder will be approximately that for a line of charge, for which potential will be proportional to $\overline{\lambda}\ln\rho$ for large $\rho$, where $\overline{\lambda}$ is the azimuthally averaged surface charge density: $\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$. That is, for large $\rho$, the potential should be the same as that when all of the charge on the cylinder is collapsed onto a line, for which the potential is $\psi=const-(\overline{\lambda}/2\pi\epsilon_o)\ln\rho$, giving $a_o=-\overline{\lambda}/2\pi\epsilon_o$ and $A_o=const$. The constant $A_o$ is determined by defining a reference potential. For example, if $\psi(\rho_r)=V_r$, then $V_r=A_o-\overline{\lambda}\ln\rho_r/2\pi\epsilon_o$ and the terms $A_o+a_o\ln\rho$ combine to form

$$A_o+a_o\ln\rho=V_r-(\overline{\lambda}/2\pi\epsilon_o)\ln(\rho/\rho_r)$$

**Note**

----

This is related to the problem that arises if one attempts to use

$$V=\frac{1}{4\pi\epsilon_o}\int \frac{dq}{|\mathbf{r}-\mathbf{r'}|}$$

to compute the potential for an infinite line of charge. The derivation of this equation assumes that the potential is zero at large $\mathbf{r}$. Using Gauss' law, one can show that this is not the case - $E_{\rho}=\frac{\lambda}{2\pi\epsilon_o}\frac{1}{\rho}$ and so $\psi = \psi_o - \frac{\lambda}{2\pi\epsilon_o}\ln\rho$, where $\psi_o$ is a constant. We can't choose $\psi(\rho=\infty)=0$ because it gives $\psi_o=\infty$. So to compute the electric field for an infinite line of charge, one must either use the integral equation for the electric field or Gauss' law.

----


Outside the cylinder, the general form is then

$$\psi_o=A_o'+a_o\ln\rho+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)\rho^{-n}$$

I've kept the $\ln\rho$ term. In the following, I'll show how the values of $A_o'$ and $a_o$ given above follow from an alternative argument. 

Inside the cylinder, the potential should be finite and so the $\ln\rho$ and $\rho^{-n}$ terms are dropped. (If the cylinder had a constant charge density, we would expect the potential to be constant inside of the cylinder and would keep only the $A_o$ term.)

Inside the cylinder, the general form is then

$$\psi_i=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)\rho^n$$

The two boundary conditions are

$$\psi_o(b)=\psi_i(b)$$

and

$$(\partial \psi_o/\partial \rho-\partial \psi_i/\partial \rho)\Bigm\lvert_{\rho=b}=-\sigma/\epsilon_o$$

(Make sure that you know how to derive the above boundary condition.)

The boundary condition

$$\psi_o(b)=\psi_i(b)$$

gives

$$A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)b^n$$

This equation gives

$$A_o'+ a_o\ln b = A_o$$

and

$$A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$$

from "matching terms", which means integrating both sides by  $\int_0^{2\pi}d\phi$, $\int_0^{2\pi}\cos n'\phi\thinspace d\phi$ and $\int_0^{2\pi}\sin n'\phi\thinspace d\phi$, with $n'$ being an integer greater than zero, and using 

$$\int_0^{2\pi}\cos n\thinspace d\phi = 0$$

$$\int_0^{2\pi}\sin n\thinspace d\phi = 0$$

$$\int_0^{2\pi}\cos n'\phi\cos n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$$

$$\int_0^{2\pi}\sin n'\phi\sin n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$$

$$\int_0^{2\pi}\cos n'\phi\sin n\phi\thinspace d\phi = 0$$

To determine the relationship between the coefficients quoted above, it is often easier to write out the first few terms in the sums

$$A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\cos n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\cos n\phi)b^n$$

in alignment as

$$
\begin{align}
&& A_o'+a_o\ln b &&+ && (a_1\cos \phi+b_1\sin \phi)b^{-1} &&+ && (a_2\cos 2\phi+b_2\sin 2\phi)b^{-2}  && +&& ... && \\
= && A_o && + && (A_1\cos \phi+B_1\sin \phi)b^{1} &&+ && (A_2\cos 2\phi+B_2\sin 2\phi)b^{2} && +&& ... &&
\end{align}
$$

and then read off the matching terms

$$A_o'+a_o\ln b = A_o$$

$$a_1/b = A_1b$$

$$b_1/b = B_1b$$

$$a_2/b^2 = a_2b^2$$

$$b_2/b^2 = B_2b^2$$

$$a_3/b^3 = a_3b^2$$

$$b_3/b^3 = B_3b^2$$

$$...$$

in order to conclude the general result stated earlier of

$$A_o'+ a_o\ln b = A_o$$

$$A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$$

The boundary condition

$$(\partial \psi_o/\partial \rho-\partial \psi_i/\partial \rho)\Bigm\lvert_{\rho=b}=-\sigma/\epsilon_o$$

gives

$$
\begin{align}
&& a_o/b &&  - &&(a_1\cos \phi+b_1\sin \phi)b^{-2} &&-&&2(a_2\cos 2\phi+b_2\sin 2\phi)b^{-3} &&+ &&... \\
&&           && - && (A_1\cos \phi+B_1\sin \phi) &&-&& 2(A_2\cos 2\phi+B_2\sin 2\phi)b^{1} &&+&& ... &&\\
=&& -(\sigma_1/\epsilon_o)&& && && && -(\sigma_o/\epsilon_o)\sin\thinspace2\phi
\end{align}
$$

This gives

$$a_o/b=-\sigma_1/\epsilon_o$$

$$-a_1/b^2-A_1=0$$

$$-b_1/b^2-B_1=0$$

$$-2a_2/b^3-2A_2b = 0$$

$$-2b_2/b^3-2B_2b = -\sigma_o/\epsilon_o$$

$$-3a_3/b^4-3A_3b^2 = 0$$

$$-3b_3/b^4-3B_3b^2 = 0$$

$$...$$

The equation $a_o=-b\sigma_1/\epsilon_o$ from the second boundary condition combines with $A_o'+a_o\ln b = A_o$ from the first boundary condition to give

$$A_o=A_o'-(b\sigma_1/\epsilon_o)\ln b$$

The equation $a_1/b = A_1b$ from the first boundary condition combines with $-a_1/b^2-A_1=0$ from the second boundary condition to give

$$2A_1=0$$

which is only possible if $A_1=0$.  Similarily, all terms except $b_2$ and $B_2$ are zero.

The equation $b_2/b^2 = B_2b^2$ from the first boundary condition and $-2b_2/b^3-2B_2b = -\sigma_o/\epsilon_o$ combine to give

$$B_2=+\sigma_o/4b\qquad\qquad b_2=b^3\sigma_o/4$$

The final result is

$$\psi_i=A_o'-(b\sigma_1/\epsilon_o)\ln b+\frac{\sigma_o}{4\epsilon_0}\frac{\rho^2}{b}\sin 2\phi$$

$$\psi_o=A_o'-(b\sigma_1/\epsilon_o)\ln \rho+\frac{\sigma_o}{4\epsilon_0}\frac{b^3}{\rho^2}\sin 2\phi$$

If the reference potential is chosen to be zero at $\rho=0$, then $A_o'=(b\sigma_1/\epsilon_o)\ln b$ and

$$\psi_i=\frac{\sigma_o}{4\epsilon_0}\frac{\rho^2}{b}\sin 2\phi$$

$$\psi_o=(b\sigma_1/\epsilon_o)\ln (b/\rho)+\frac{\sigma_o}{4\epsilon_0}\frac{b^3}{\rho^2}\sin 2\phi$$

Earlier it was argued that for large $\rho$, the $\psi_o$ should approach

$$\psi_o(\rho\rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln\rho$$

where 

$$\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$$

Using

$$\sigma=\sigma_1 + \sigma_o\sin\thinspace2\phi$$

gives

$$\overline{\lambda}=2\pi b\sigma_1$$

and so the computed value of $\psi_o$ of

$$\psi_o=(b\sigma_1/\epsilon_o)\ln (b/\rho)+\frac{\sigma_o}{4\epsilon_0}\frac{b^3}{\rho^2}\sin 2\phi=(b\sigma_1/\epsilon_o)\ln b-(b\sigma_1/\epsilon_o)\ln \rho+\frac{\sigma_o}{4\epsilon_0}\frac{b^3}{\rho^2}\sin 2\phi$$

matches the limit

$$\psi_o(\rho\rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln\rho=const-(\sigma_1b/\epsilon_o)\ln\rho$$

----

*Alternative Solution*

In the following, \(s_o\) is used in place of \(b\) to avoid confusion with \(b_n\).

----

$$
\begin{align}
\psi_o(s,\phi)  = {} &  A^o_o+a^o_o\ln s\\
& +\sum_{n=1}^\infty (A^o_n\cos n\phi+B^o_n\sin n\phi)s^n\\
& +\sum_{n=1}^\infty (a^o_n\cos n\phi+b^o_n\sin n\phi)s^{-n}
\end{align}
$$

A common error is to assert \(A^o_n=B^o_n=0\) for all \(n\) because the potential does not "blow up". Here that logic fails as it would give \(A^o_1=0\). (This is in part why I discourage using the "blow up" logic in solutions and why I asked you to provide justifications.) 

The electric field is given as \(\mathbf{E}=E_o\hat{\mathbf{x}}\). Using \(\psi=\int \mathbf{E}\cdot d\mathbf{l}\) with \(d\mathbf{l}=\hat{\mathbf{x}}dx\) gives a potential of \(\psi(x)=-E_ox+V_o\), where \(V_o\) is a constant of integration. In cylindrical coordinates this is \(\psi=-E_os\cos\phi+V_o\). We will assume that for large \(s\), the potential approaches this functional form. (At the end of this solution, we consider an alternative justification for this assumption than the usual "if it satisfies ... and unique ... it is the solution" justification; if there were a line of charge in the system parallel to the \(z\)-axis, this assumption would not be valid.) Therefore, our outer boundary condition is

$$\psi^o(s\rightarrow \infty,\phi) \rightarrow E_os\cos\phi+V_o$$

For large \(s\), the general form of the potential reduces to

$$\psi^o(s\rightarrow \infty,\phi) \rightarrow A^o_o+a^o_o\ln s +\sum_{n=1}^\infty (A^o_n\cos n\phi+B^o_n\sin n\phi)s^n$$

(Technically we should write the solution in terms of  \(s' = s/b\) and consider \(s'\rightarrow \infty\) because \(\infty\) is dimensionless).  Combining these two equations gives

$$I.\quad E_os\cos\phi+V_o = A^o_o+a^o_o\ln s +\sum_{n=1}^\infty (A^o_n\cos n\phi+B^o_n\sin n\phi)s^n$$

Integration of both sides of \(I.\) over \(\phi = [0,2\pi]\) gives

$$V_o = A^o_o + a^o_o\ln s$$

or

$$V_o - A^o_o = a^o_o\ln s$$

The only way for this to be true for arbitrary \(s\) is if \(a^o_o=0\), which implies \(A_o=V_o\). 

Multiplication of \(I.\) by \(\cos\phi\) and integration over \(\phi = [0,2\pi]\) gives

$$-E_o = A^o_1$$

Multiplication of \(I.\) by \(\cos n'\phi\) for \(n'\gt 1\) and integration over \(\phi = [0,2\pi]\) gives

and \(A^o_n=0\) for \(n\gt 1\). 

Multiplication of \(I.\) by \(\sin n'\phi\) for \(n'\gt 1\) and integration over \(\phi = [0,2\pi]\) gives

and \(B^o_n=0\) for \(n\ge 1\). (That \(B^o_n=0\) could also be justified by a symmetry argument - the potential should have the property that \(\psi(x,y)=\psi(x,-y)\), or equivalently, \(\psi(s,\phi)=\psi(s,-\phi)\)). This leaves

$$\psi^o(s,\phi) = V_o-\frac{E_o}{s}\cos\phi+\sum_{n=1}^\infty (a^o_n\cos n\phi+b^o_n\sin n\phi)s^n$$

As noted earlier, because the system is invariant under the transformation \(\phi\rightarrow -\phi\) from which it follows that \(b^o_n=0\), leaving

$$\psi^o(s,\phi) = V_o-E_os\cos \phi+\frac{A^o_1}{s}\cos\phi+\sum_{n=1}^\infty (a^i_n\cos n\phi)s^{-n}$$

(If we had not used the symmetry argument to assert \(b^o_n=0\), we could still find it to be zero later using the method used to show \(B^o_n=0\).)

The fact that we cannot say anything about \(a^i_n\) is reflective of the fact that we have not addressed any constraints on the potential for non-large \(s\).

The starting equation for the inner solution is the same as that for the outer solution:

----
----

$$
\begin{align}
\psi_i(s,\phi)  = {} &  A^i_o+a^i_o\ln s\\
& +\sum_{n=1}^\infty (A^i_n\cos n\phi+B^i_n\sin n\phi)s^n\\
& +\sum_{n=1}^\infty (a^i_n\cos n\phi+b^i_n\sin n\phi)s^{-n}
\end{align}
$$

The continuity condition is

$$\psi_o(s_o,\phi)=\psi_i(s_o,\phi)$$

$$
\begin{align}
II.\quad V_o+ E_os_o\cos \phi +\frac{A^o_1}{s}\cos\phi = {} &  A^i_o+a^i_o\ln s_o\\
& +\sum_{n=1}^\infty (A^i_n\cos n\phi+B^i_n\sin n\phi)s_o^n\\
& +\sum_{n=1}^\infty (a^i_n\cos n\phi+b^i_n\sin n\phi)s_o^{-n}
\end{align}
$$

Integration of both sides of \(II.\) over \(\phi = [0,2\pi]\) gives

$$V_o=A^i_o + a^i_o\ln s_o$$

Multiplication of \(II.\) by \(\cos\phi\) and integration over \(\phi = [0,2\pi]\) gives

$$E_os_o+\frac{A^o_1}{s_o}=A^i_1s_o+\frac{a^i_1}{s_o}$$

Multiplication of \(II.\) by \(\cos n'\phi\) for \(n'\gt 1\) and integration over \(\phi = [0,2\pi]\) gives

$$0 = A^i_ns_o^n + \frac{a^i_n}{s_o^n}\quad n'\gt 1$$

Multiplication of \(II.\) by \(\sin n'\phi\) for \(n'\ge 1\) and integration over \(\phi = [0,2\pi]\) gives

$$0 = B^i_nb^n+\frac{b^i_n}{s_o^n}\quad n'\ge 1$$

----
----

The boundary condition \(\epsilon_2 E_{2\perp}-\epsilon_1E_{1\perp}=\sigma_f\) evaluated at \(s=s_o\), written in terms of potentials, and with \(\sigma_f=0\) is

$$\epsilon_o\frac{\partial \psi_o}{\partial s}\Bigg|_{s=s_o}=\epsilon\frac{\partial \psi_i}{\partial s}\Bigg|_{s=s_o}$$

$$
\begin{align}
III.\quad (\epsilon_o/\epsilon)E_o\cos \phi-\frac{A_1^o}{s_o^2}\cos\phi  = {} &  \frac{a^i_o}{s_o}\\
& +\sum_{n=1}^\infty n(A^i_n\cos n\phi+B^i_n\sin n\phi)s_o^{n-1}\\
& -\sum_{n=1}^\infty n(a^i_n\cos n\phi+b^i_n\sin n\phi)s_o^{-n-1}
\end{align}
$$

Integration of both sides of \(III.\) over \(\phi = [0,2\pi]\) gives

$$a^i_o=0$$

Multiplication of \(III.\) by \(\cos\phi\) and integration over \(\phi = [0,2\pi]\) gives

$$\frac{\epsilon_o}{\epsilon}E_o-\frac{\epsilon_o}{\epsilon}\frac{A_1^o}{s^2_o}=A^i_1 - \frac{a^i_1}{s_o^2}$$

Multiplication of \(III.\) by \(\cos n'\phi\) for \(n'\gt 1\) and integration over \(\phi = [0,2\pi]\) gives

$$0 = nA^i_ns_o^{n-1} - \frac{na^i_n}{s_o^{n+1}}\quad n\gt 1$$

When this is combined with the earlier condition

$$0 = A_ns_o^n + \frac{a_n}{s_o^n}\quad n\gt 1$$

yields

$$0 = -n\frac{a^i_n}{s_o^{2n}}s_o^{n-1} - \frac{na^i_n}{s_o^{n+1}}\quad n\gt 1$$

which simplifies to

$$0 = \frac{a^i_n}{s^{n+1}_o} \quad n\gt 1$$

So \(a^i_n=0\) for \(n\gt 1\) and because \(a^i_o=0\) was found earlier, only \(a^o_1\) is unknown.

Multiplication of \(III.\) by \(\sin n'\phi\) for \(n' \ge 1\) and integration over \(\phi = [0,2\pi]\) gives

$$0 = nB^i_ns_o^{n-1} - \frac{nb^i_n}{s_o^{n+1}}\quad n\ge 1$$

This combined with

$$0 = B_nb^n+\frac{b_n}{s_o^n}\quad n\ge 1$$

from the continuity condition gives \(b^i_n=0\) for \(n\ge 1\).

This leaves

$$\psi_i = V_o-A_1^i s\cos\phi+\frac{a_1^i}{s}\cos\phi$$

$$\psi_o = V_o-E_os\cos\phi + \frac{A_1^o}{s}\cos\phi$$

and two equations that have not been used:

$$E_os_o+\frac{A^o_1}{s_o}=A^i_1s_o+\frac{a^i_1}{s_o}$$

$$\frac{\epsilon_o}{\epsilon}E_o-\frac{\epsilon_o}{\epsilon}\frac{A_1^o}{s^2_o}=A^i_1 + \frac{a^i_1}{s_o^2}$$

It would appear that there are three unknowns in these two equations. Normally we would say that \(a_1^i=0\) because the solution does not "blow up" at the origin. There is also a mathematical justification. Poisson's equation in cylindrical coordinates for a potential with no \(z\)-dependence is

$$\frac{1}{s}\frac{\partial}{\partial s}\left(s\frac{\partial \psi}{\partial s}\right) + \frac{1}{s^2}\frac{\partial^2\psi}{\partial \phi^2}=-\frac{\rho}{\epsilon_o}$$

or

$$s\frac{\partial}{\partial s}\left(s\frac{\partial \psi}{\partial s}\right) + \frac{\partial^2\psi}{\partial \phi^2}=-\frac{\rho}{\epsilon_o}$$

If \(s=0\), \(\phi\) is continuous near \(s=0\), and \(\rho=0\) (corresponding to no line of charge along the \(z\)-axis and passing through the origin) this reduces to

$$\frac{\partial^2\psi}{\partial \phi^2}=0\qquad \Rightarrow\qquad\frac{\partial \psi}{\partial \phi}\Bigg|_{s=0}=const$$

(If one inspects the derivation for the equation of the general equation for the potential (e.g., [http://faculty.washington.edu/blayneh/cylcoord.pdf]) used at the starting point in this problem, you will note that the general form of the solution is actually only valid for \(s\gt 0\)). As a result, we actually need to consider three regions for the solution, with the additional "region" being \(s=0\). 

The additional condition is then

$$\frac{\partial \psi_i}{\partial \phi}\Bigg|_{s\rightarrow 0} = const$$

As a result,

$$\frac{\partial \psi_i}{\partial \phi}\Bigg|_{s\rightarrow 0} = \left[A_1^i s\sin\phi-\frac{a_1^i}{s}\sin\phi\right]_{s\rightarrow 0}=const$$

For this condition to hold, \(a^i_1=0\) and the remaining equations are the same as found in the first solution to this problem.

As noted earlier, technically we were only told that the dielectric was placed in a region of space where the electric field was \(\mathbf{E}=E_o\hat{\mathbf{x}}\). From a physical perspective, it seems reasonable to conclude that the presence of the dielectric will not alter this electric field for large enough \(s\), which was used to justify the condition \(\psi^o(s\rightarrow \infty,\phi) \rightarrow E_os\cos\phi+V_o\). If we did not make this assumption, the only reduction from the general solution to the potential would be that from the symmetry argument that \(\psi(s,\phi)=\phi(s,-\phi)\), from which it follows that \(b_n=B_n=0\). The outer potential is then

$$
\begin{align}
\psi_o(s,\phi)  = {} &  A^i_o+a^i_o\ln s+\sum_{n=1}^\infty (A^i_n\cos n\phi)s^n+\sum_{n=1}^\infty (a^i_n\cos n\phi)s^{-n}
\end{align}
$$

It is left as an exercise to show how one can arrive at the same solution found earlier without using the assumption \(\psi^o(s\rightarrow \infty,\phi) \rightarrow E_os\cos\phi+V_o\).


# 2-D

## Cartesian

See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.html)

See [HW #4](hw.md#2-d-cartesian-boundary-value-problem) and references therein.

## Cylindrical -- $\sigma$ given

#2-d-cylindrical-boundary-value-problem&l=1272&c=1

## Spherical -- Potential Given 

A non-conducting spherical shell of radius $b$ has on its surface of $V_o\cos\theta$.

Find $\Phi(r,\theta)$.

**Solution**

1\. Using $\Phi=0$ at the origin,

$\Phi(r,\theta) = 
\begin{cases}
\displaystyle V_o\frac{r}{b}\cos\theta & r \le b \\ \\
\displaystyle V_o\frac{b^2}{r^2}\cos\theta & r \ge b
\end{cases}
$

## Spherical -- Potential Given 

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

## Spherical $\sigma$ given

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
