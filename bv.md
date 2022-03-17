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


# 2-D

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
