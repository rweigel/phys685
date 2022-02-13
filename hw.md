# HW 1.

Due on Feb. 2nd at 4:30 pm. Please turn in a physical copy unless you are absent, in which case you may send me an electronic copy.

## Notation and Delta Function

For a volume charge density $\rho$, the electric field at $\mathbf{r}$ is given by

$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\epsilon_o}\int\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}\rho(\mathbf{r}')\thinspace d\tau'$$

where $\textbf{\char"0509}=\mathbf{r}-\mathbf{r}'$ and $\mathbf{r}'$ is the location of a charge.

1. For a point charge $Q$ at the origin, $\rho(\mathbf{r})=Q\delta(x)\delta(y)\delta(z)$. Evaluate the above integral using cartesian coordinates and unit vectors and this $\rho$.
2. For a point charge $Q$ at $\mathbf{r}'$, $\rho(\mathbf{r})=Q\delta(x-x')\delta(y-y')\delta(z-z')$. Evaluate the above integral using cartesian coordinates and unit vectors and this $\rho$.

**Solution**

1\.

$$\begin{align}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}Q\delta(x')\delta(y')\thinspace dx'dy' \\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y')dy'\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}\delta(x')\thinspace dx'\\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y')dy'\frac{(x-0)\xhat+(y-y')\yhat}{\sqrt{(x-0)^2 + (y-y')^2}^3}\\\\
= & \frac{Q}{4\pi\epsilon_o}\frac{(x-0)\xhat+(y-0)\yhat}{\sqrt{(x-0)^2 + (y-0)^2}^3}\\\\
= & \frac{Q}{4\pi\epsilon_o}\frac{x\xhat+y\yhat}{\sqrt{x^2 + y^2}^3}
\end{align}
$$

The generalization to the 3-D problem given is straightforward.

2\.

Here $x', y'$, and $z'$ are fixed points in space. Normally when given a charge density, we replace $x, y, z$ with $x',y',z'$. If we did that here, we would have $\rho(\mathbf{r}')=Q\delta(0)\delta(0)\delta(0)$, which does not depend on primed coordinates. To work around this issue, change the integration variables to be double primes. As before, in two dimensions,

$$
\begin{align}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x'')\xhat+(y-y'')\yhat}{\sqrt{(x-x'')^2 + (y-y'')^2}^3}Q\delta(x''-x')\delta(y''-y')\thinspace dx''dy'' \\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y''-y')dy''\int\frac{(x-x'')\xhat+(y-y'')\yhat}{\sqrt{(x-x'')^2 + (y-y'')^2}^3}\delta(x''-x')\thinspace dx''\\\\
\end{align}
$$

In the integral above, the $x'$ is a constant with respect to integration (in the same way that in $\int\delta(x-a)dx$, $a$ is a constant) and so we replace $x''$ with this constant value.

$$
\begin{align}\mathbf{E}(\mathbf{r}) = & \frac{Q}{4\pi\epsilon_o}\int\delta(y''-y')dy''\frac{(x-x')\xhat+(y-y'')\yhat}{\sqrt{(x-x')^2 + (y-y'')^2}^3}\\\\
=& \frac{Q}{4\pi\epsilon_o}\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}
\end{align}
$$

In class, I used an alternative approach where I replaced $x',y',z'$ with $a_x, a_y, a_z$ and integrated over $x',y',z'$ so that I needed to evaluate

$$
\begin{align}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}Q\delta(x'-a_x)\delta(y'-a_y)\thinspace dx'dy'
\end{align}
$$

The result of integration is

$$
\mathbf{E}(\mathbf{r}) = \frac{Q}{4\pi\epsilon_o}\frac{(x-a_x)\xhat+(y-a_y)\yhat}{\sqrt{(x-a_x)^2 + (y-a_y)^2}^3}
$$

To finish the problem, I replaced $a_x,a_y,a_z$ with the variables given in the problem of $x',y',z'$ to get the same answer as when integration was done over double primed variables.

## Delta Function I

1. Suppose $I = \int_{-2}^{2}g(x)dx$. Find $\int_{-1}^{1}g(2x)dx$ and $\int_{-1}^{1}g(-2x)dx$ in terms of $I$. Show graphically why the result makes sense
using $g(x)=x^2$.

2. Show that $\int \delta(bx)f(x)dx = \frac{f(0)}{|b|}$. (That is, show that $\delta(bx)=\delta(x)/|b|$).

**Solution**

1\.

$\displaystyle \int_{-1}^{1}g(2x)dx=\int_{-1}^{1}g(-2x)dx=I/2$

2\.

The generalization of the previous result is if $I = \int_{-a}^{b}g(x)dx$, then for $\alpha \gt 0$

$\displaystyle \int_{-a/\alpha}^{b/\alpha}g(\alpha x)dx=\int_{-a/\alpha}^{b/\alpha}g(-\alpha x)dx=\frac{I}{\alpha}$.

In the case that $a=b=\infty$ and a finite integral, it follows that $\int g(bx)dx=\int \frac{g(x)}{|b|}dx$, which applies to $g(x)=\delta(x)$ and thus whe have shown $\delta(bx)=\delta(x)/|b|$.

Griffiths 4th Edition example 1.15 gives an alternative solution. Another approach is to think of this as a transformation of variables problem in which the Jacobian, which involves the absolute value, is computed.

## Delta Function II

1. Find $\int \delta(a + bx)f(x)dx$ using either
   1. identity 5. on page 26 of Jackson, 3rd Edition or
   2. using the substition $u=a+bx$.

2. Prove identity 5. on Page 26 of Jackson 3rd edition

   $\displaystyle \delta(f(x))=\sum_i\frac{\delta(x-x_i)}{\left|\frac{df}{dx}(x_i)\right|}$

   where $f(x)$ is assumed to have only simple zeros, located at $x=x_i$. Do this by either
   1. explaing the omitted explanations in [Dennery and Krzywicki 1967, page 237](https://drive.google.com/drive/folders/0013X5HELBJvBlCsQGFauVVDEFczCLV0y9D) or
   2. Taylor series expanding $f(x)$ around the points $x_i$ where $g(x_i)=0$.

**Solution**

1.1 To avoid confusion with the $f(x)$ in the given equation, re-write the identity as

$\displaystyle \delta(g(x))=\sum_i\frac{\delta(x-x_i)}{\left|\frac{dg}{dx}(x_i)\right|}$

Here $g(x)=a+bx$, which has a single zero at $x_1=-a/b$. $dg/dx=b$, so 

$\displaystyle \delta(g(x))=\frac{\delta(x-x_1)}{|\frac{dg}{dx}(x_1)|}=\frac{\delta(x-x_1)}{|b|}=\frac{\delta(x+a/b)}{|b|}$

and so

$\displaystyle \int \delta(a + bx)f(x)dx=\int dx \frac{\delta(x+a/b)}{|b|} f(x)=\frac{f(-a/b)}{|b|}$

1.2 With the substitution,

$\displaystyle \int \delta(u)\frac{f((u-b)/a)}{b}du=\frac{f(-b/a)}{b}$

for positive $b$ and $f(-b/a)/(-b)$ for negative $b$, so the integral is $f(-b/a)/|b|$ as before.

## Divergence Theorem

1. Find the electric field $\mathbf{E}$ due to a non-conducting sphere with a uniform volume charge density $\rho_o$ and radius $b$ that is centered on the origin.
2. Show by direct calculation that

   $$\oint_{\mathcal{S}}\mathbf{E}\bfcdot d\mathbf{a} = \int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

   when the volume of integration $\mathcal{V}$ is a sphere centered on the origin with

   1. radius $b/2$
   2. radius $2b$

**Solution**

As mentioned in class, this is somewhat of a simple problem but was given to motivate the use of the Dirac delta function. What I said in class is briefly summarized at the end.

1\. The electric field is

$$\mathbf{E}(r \le b) = \frac{\rho_o}{3\epsilon_o}r\thinspace \mathbf{\hat{r}}=\frac{q}{4\pi\epsilon_o}\frac{r}{b^3}\mathbf{\hat{r}}$$

$$\mathbf{E}(r \ge b) = \frac{\rho_o}{3\epsilon_o}\frac{b^3}{r^2}\thinspace \mathbf{\hat{r}}=\frac{q}{4\pi\epsilon_o}\frac{1}{r^2}\mathbf{\hat{r}}$$

where $q=\rho_o\thinspace 4\pi b^3/3$ was used.

2\.

In the following,

$$A.\qquad\boldsymbol{\nabla}\cdot (f(r)\thinspace \hat{\mathbf{r}})=\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2f(r)\right)$$

is used. This follows from the identity for the divergence in spherical coordinates.

----

For $r\le b$ and $\mathcal{S}$ a spherical surface of radius $r$:

$$\oint_{\mathcal{S}}\mathbf{E}(r\le b)\bfcdot \hat{\mathbf{n}}\thinspace da =  \int_0^{2\pi}\int_0^\pi\left(\frac{\rho_o}{3\epsilon_o}r\thinspace \hat{\mathbf{r}}\right)\bfcdot\hat{\mathbf{r}}\thinspace r^2\sin\theta\thinspace d\theta\thinspace d\phi=\frac{\rho_o}{\epsilon_o}\frac{4\pi r^3}{3}=\frac{q}{\epsilon_o}$$

The divergence of $\mathbf{E}$ is, using $A.$,

$$\boldsymbol{\nabla}\cdot \mathbf{E}(r\le b)= \boldsymbol{\nabla}\cdot \left(\frac{\rho_o}{3\epsilon_o}r\thinspace \hat{\mathbf{r}}\right) = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\left(\frac{\rho_o}{3\epsilon_o}r\right)\right)= \frac{\rho_o}{\epsilon_o}$$

as expected from Gauss' law in differential form ($\boldsymbol{\nabla}\cdot \mathbf{E}=\rho/\epsilon_o$ with $\rho=\rho_o$). Therefore, for $r\le b$:

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x=\int_{\mathcal{V}} \frac{\rho_o}{\epsilon_o}\thinspace d^3x=\frac{\rho_o}{\epsilon_o}\frac{4\pi r^3}{3}=\frac{q}{\epsilon_o}$$

Conclusion: for $r\le b$,

$$\oint_{\mathcal{S}}\mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da = \int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

----

For $r\gt b$ and $\mathcal{S}$ a spherical surface of radius $r$:

$$\oint_{\mathcal{S}}\mathbf{E}(r\ge b)\cdot \hat{\mathbf{n}}\thinspace da =  \int_0^{2\pi}\int_0^\pi\left(\frac{\rho_o}{3\epsilon_o}\frac{b^3}{r^2}\thinspace \hat{\mathbf{r}}\right)\cdot\hat{\mathbf{r}}\thinspace r^2\sin\theta\thinspace d\theta\thinspace d\phi = \int_0^{2\pi}\int_0^\pi\left(\frac{\rho_o}{3\epsilon_o}b^3\right)\sin\theta\thinspace d\theta\thinspace d\phi=\frac{\rho_o}{\epsilon_o}\frac{4\pi b^3}{3}=\frac{q}{\epsilon_o}$$

The divergence is

$$\boldsymbol{\nabla}\cdot \mathbf{E}(r\ge b)=\frac{\rho_o b^3}{3\epsilon_o} \boldsymbol{\nabla}\cdot \frac{\hat{\mathbf{r}}}{r^2} = \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\left(\frac{\rho_o b^3}{3\epsilon_o}\frac{1}{r^2}\right)\right)=\frac{\rho_o b^3}{3\epsilon_o}\frac{1}{r^2}\frac{\partial}{\partial r}\left(1\right)=0$$

also as expected from Gauss' law in differential form ($\boldsymbol{\nabla}\cdot \mathbf{E}=\rho/\epsilon_o$ with $\rho=0$). Important: the last equality in the above equation is only true when $r\ne 0$; when $r=0$, the result is $0/0$. This issue is considered later in this solution.

One must split the volume integral into two integrals, one for $r\le b$ and the other for $r\gt b$ to account for the divergence being different in the two regions. As shown earlier, in the region $r\gt b$, the divergence is zero. 

$$
\begin{array}{ll}
\displaystyle\int\_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x& = & 
\displaystyle\int\_{\mathcal{V\_{r\le b}}} \boldsymbol{\nabla} \cdot \mathbf{E}(r\le b)\thinspace d^3x & + &  \displaystyle\int\_{\mathcal{V\_{r\ge b}}} \boldsymbol{\nabla} \cdot \mathbf{E}(r\ge b)\thinspace d^3x\\\\
& = &  \displaystyle\int_{\mathcal{V\_{r\le b}}} \frac{\rho_o}{\epsilon_o}\thinspace d^3x & + &  \displaystyle\int_{\mathcal{V\_{r\ge b}}}0\thinspace d^3x\\\\
& = & \frac{\rho_o}{\epsilon_o}\frac{4\pi b^3}{3} & + & 0\\\\
& = & \frac{q}{\epsilon_o}
\end{array}
$$

Conclusion: for $r\gt b$,

$$\oint_{\mathcal{S}}\mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da = \int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

----

_Motivation for this problem_

I gave this problem as a lead-in/follow-up for my discussion of the motivation for the delta function. For a point charge, the integrand of

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x$$

with

$$\mathbf{E}_p=\frac{q}{4\pi\epsilon_o}\frac{\hat{\mathbf{r}}}{r^2}$$

is zero everywhere except at the origin ($r=0$) where it is indeterminate in the form of $0/0$ because

$$
\displaystyle \boldsymbol{\nabla}\cdot \mathbf{E}_p = \frac{q}{4\pi\epsilon_o} \boldsymbol{\nabla}\cdot \frac{\hat{\mathbf{r}}}{r^2} = \frac{q}{4\pi\epsilon_o}\frac{1}{r^2}\frac{\partial}{\partial r}\left(1\right) = \begin{cases}
0/0 & \text{if }r = 0 \\ 
0   & \text{if }r\ne 0
\end{cases}
$$

However,

$$\oint_{\mathcal{S}}\mathbf{E}_p\cdot \hat{\mathbf{n}}\thinspace da =\frac{q}{\epsilon_o}$$

does not have an indeterminacy. Therefore, the divergence theorem

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x=\oint_{\mathcal{S}}\mathbf{E}_p\cdot \hat{\mathbf{n}}\thinspace da$$

applied to $\mathbf{E}$ for a point charge gives

$$\text{indeterminate integral}=\frac{q}{\epsilon_o}$$

In this problem, it has been shown that if a point charge $q$ is modeled as having a uniform density for $r\le b$ and having zero density for $r\gt b$, then the indeterminacy problem can be avoided and

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x = \oint_{\mathcal{S}}\mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da$$

for all $r$ and for arbitrarily small (but non-zero) $b$ (but see also 'other notes' below). That is, the divergence theorem gives the correct answer for a solid ball of charge that is arbitrarily small but not zero.

Although the divergence theorem does not apply for $\mathbf{E}_p$, to avoid having to think about a solid ball with arbitrarily small but non zero radius is to use it with the convention that

$$\boldsymbol{\nabla}\cdot \mathbf{E}_p=\frac{q}{4\pi\epsilon_o}\boldsymbol{\nabla}\cdot \frac{\hat{\mathbf{r}}}{r^2}=\frac{q}{\epsilon_o}\delta(\mathbf{\mathbf{r}})$$

where the function $\delta(\mathbf{\mathbf{r}})$ is zero everywhere except at $\mathbf{r}=\mathbf{0}$ and integrates to 1 when the volume of integration includes $\mathbf{r}=\mathbf{0}$.

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x=\int_{\mathcal{V}}\frac{q}{4\pi\epsilon_o}\boldsymbol{\nabla}\cdot \frac{\hat{\mathbf{r}}}{r^2}\thinspace d^3x=\int_{\mathcal{V}}\frac{q}{\epsilon_o}\delta(\mathbf{\mathbf{r}})\thinspace d^3x=\frac{q}{\epsilon_o}$$

That is,

$$\boldsymbol{\nabla}\cdot \frac{\hat{\mathbf{r}}}{r^2}=4\pi\delta(\mathbf{\mathbf{r}})$$

When you see the delta function used in an integration, you should think back to this problem and realize that the delta function is being used instead of modeling the electric field as a point charge $q$ as having a uniform density for $r\lt b$ and zero density for $r\gt b$.

Griffiths takes a different approach to motivating the introduction of the delta function. He notes that the indeterminate integral of the divergence

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x=\text{indeterminate integral}$$

must be equal to $q/\epsilon_o$ because of the divergence theorem (which technically does not apply because of the singularity in $\mathbf{E}$ at $r=0$):

$$\oint_{\mathcal{S}}\mathbf{E}_p\cdot \hat{\mathbf{n}}\thinspace da = \frac{q}{\epsilon_o}\quad\Rightarrow\quad\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x=\frac{q}{\epsilon_o}$$

He then notes that $\hat{\mathbf{r}}/r^2$ has the property that its divergence

$$\boldsymbol{\nabla}\cdot\frac{\hat{\mathbf{r}}}{r^2}$$

1. is zero everywhere except at the origin (where it is interminate)
2. integrates to a constant ($4\pi$) over any volume $\mathcal{V}$ that includes $r=0$ (based on the assumption that the divergence theorem applies and resolves the indeterminacy)

That is, although

$$\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x$$

has an indeterminate integrand at $r=0$, the divergence theorem must be true, and so this integral must be equal to the surface integral, which is $\frac{q}{\epsilon_o}$. Therefore,

$$\boldsymbol{\nabla}\cdot \mathbf{E}_p=\frac{q}{\epsilon_o}\delta(\mathbf{\mathbf{r}})$$

where the function $\delta(\mathbf{r})$ is defined to be zero unless $r=0$ and integrates over a volume that includes $\mathbf{r}=\mathbf{0}$ to 1. This explanation is somewhat awkward because it asserts that the divergence theorem must be correct even though the field $\mathbf{E}_p$ does not satisfy the requirements for the divergence theorem to apply. (The requirements for the divergence theorem to apply are that the components of the vector field and their derivatives are continuous.)

In summary, the integral

$$\int_{\mathcal{V}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

is indeterminant when $\mathbf{E}\sim \hat{\mathbf{r}}/r^2$ and $\mathcal{V}$ includes $r=0$. If we model a point charge as having a uniform density for $r\le b$, and zero density for $r\gt b$, where $b\ne 0$ is smaller than any length scale in the problem, the indeterminacy is removed. Instead of two integrations, one for $r \le b$ and the other for $r\gt b$, we can simply replace $\boldsymbol{\nabla}\cdot \mathbf{E}_p$ with $(q/\epsilon_o)\delta(\mathbf{\mathbf{r}})$; the result of any integration will be the same.

----

A second motivation for using the delta function is that we often want to do an integral of the form

$$\int_{\mathcal{V}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}_p\thinspace d^3x$$

(Recall that $f(\mathbf{r})$ means $f(x,y,z)$). As before, integral is indeterminate because $\boldsymbol{\nabla} \cdot (\hat{\mathbf{r}}/r^2)$ is 0/0 at $r=0$. To work around this problem, we can again model the point charge as having a uniform density for $r\le b$ and zero density for $r\gt b$. Then 

$$\int_{\mathcal{V}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x=\int\_{\mathcal{V_{r\le b}}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\_b\thinspace d^3x+\int_{\mathcal{V_{r\gt b}}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}_b\thinspace d^3x$$

The second integral is identically zero because $\boldsymbol{\nabla}\cdot\mathbf{E}_b=0$ for $r\gt b$. If $f(\mathbf{r})$ can be expanded as a Taylor series

$$f(\mathbf{r})\simeq f(\mathbf{0}) + \mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]_{\mathbf{r}=0}\;+\;...$$

then

$$
\begin{array}{ll}
\displaystyle\int\_{\mathcal{V\_{r\le b}}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x & = & \displaystyle\int\_{\mathcal{V\_{r\le b}}} \left(f(\mathbf{0})+\mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]\_{\mathbf{r}=0}\thickspace+\thickspace ...\right)\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x\\
& = & \displaystyle\int\_{\mathcal{V\_{r\le b}}} f(\mathbf{0})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x+\displaystyle\int\_{\mathcal{V\_{r\le b}}} (\mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]\_{\mathbf{r}=0}\thickspace+\thickspace...)\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x\\
& = & f(\mathbf{0})\displaystyle\int\_{\mathcal{V\_{r\le b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x+\displaystyle\int\_{\mathcal{V\_{r\le b}}} \left(\mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]\_{\mathbf{r}=0}\thickspace+\thickspace ...\right)\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x\\
& = & \frac{q}{\epsilon\_o}f(\mathbf{0})\thickspace+\thickspace\frac{q}{\epsilon\_o}\displaystyle\int\_{\mathcal{V\_{r\le b}}} \left(\mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]\_{\mathbf{r}=0}\thickspace+\thickspace ...\right)d^3x\\
\end{array}
$$

The second and higher-order terms in the last equation approach zero as $b\rightarrow 0$.  To see this, note that for small enough $b$,

$$\frac{q}{\epsilon_o}\displaystyle\int_{\mathcal{V_{r\le b}}} f(\mathbf{r})\thinspace d^3x\rightarrow \frac{4\pi}{3}b^3\left<f(\mathbf{0})\right>$$

where the $\left<\right>$ is the average in $\mathcal{V}$ in a sphere of radius $b$. Therefore,

$$\frac{q}{\epsilon_o}\displaystyle\int_{\mathcal{V_{r\le b}}} \mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]_{\mathbf{r}=0}\thinspace d^3x\xrightarrow[b\rightarrow 0]{} \frac{q}{\epsilon_o}\frac{4\pi}{3}b^3\left<\mathbf{r}\cdot\left[\boldsymbol{\nabla}f\thinspace \right]_{\mathbf{r}=0}\right>\xrightarrow[b\rightarrow 0]{}  0$$

The same argument applies to the higher-order terms in the Taylor series expansion.

Prior to the introduction of the delta function by Dirac in the 1930s, the above argument was used when an integral of the form

$$\displaystyle\int_{\mathcal{V}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

was encountered and $\mathbf{E}$ was that for a point charge and $\mathcal{V}$ that included the location of the point charge.

With the introduction of the Dirac delta, one can simply use $\boldsymbol{\nabla}\cdot \mathbf{E}=\frac{q}{\epsilon_o}\delta(\mathbf{\mathbf{r}})$ to get the same result without needing to think about the above steps:

$$
\displaystyle \int_{\mathcal{V}} f(\mathbf{r})\boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x = \int_{\mathcal{V}} f(\mathbf{r})\frac{q}{\epsilon_o}\delta(\mathbf{\mathbf{r}})\thinspace d^3x = \begin{cases}
f(\mathbf{0})\frac{q}{\epsilon_o} & \text{if }\mathcal{V}\text{ includes } r = 0 \\ 
0 & \text{otherwise}
\end{cases}
$$

That is, using the delta function for the divergence of $\mathbf{E}$ due to a point charge will give us the same answer as if we had modeled the point charge as having a uniform density for $r\le b$, zero density for $r\gt b$, Taylor series expanded $f(\mathbf{r})$, and then let $b\rightarrow 0$. 

----

_Other notes_

In the above, I showed that the divergence theorem gave the correct result for $\mathbf{E}$ and any $r$ by direct calculation. However, the divergence theorem

$$\oint_{\mathcal{S}}\mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da = \int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$$

requires that within $\mathcal{V}$, the components of $\mathbf{E}$ and their derivatives are continuous. In $\mathbf{E}$, $E_r$ is continuous, but $\partial E_r/\partial r$ is not. So it appears that direct calculation for $r\gt b$ gave a result that was consistent with the divergence theorem even though the assumptions required to apply the divergence theorem are not satisfied. To see why this occurred, use the divergence theorem in the two parts of $\mathcal{V}$ where the divergence theorem applies for $\mathbf{E}$. 

First, consider the application of the divergence theorem for the volume between $r=0$ and $r=b$.

$$\int_{\mathcal{V_{r \le b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x = \int_\mathcal{S_{r=b}} \mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da $$

The outward normal to $\mathcal{S_{r=b}}$ for $\mathcal{V_{r \le b}}$ is $+\hat{\mathbf{r}}$, so

$$I.\quad \int_{\mathcal{V_{r \le b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x =\int_\mathcal{S_{r=b}} \mathbf{E}\cdot \hat{\mathbf{r}}\thinspace da$$

Next, consider the application of the divergence theorem for the volume between $r=b$ and $r=2b$ (the result will apply to any $r\gt b$). In this case, there is an inner and outer surface and so the surface integral has two parts.

$$\int_{\mathcal{V_{b \le r \le 2b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x= \oint_\mathcal{S_{r=b}} \mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da + \oint_\mathcal{S_{r=2b}} \mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da$$

The outward normal to $\mathcal{S_{r=b}}$ for this volume is $-\hat{\mathbf{r}}$ and the outward normal to $\mathcal{S_{r=2b}}$ is $+\hat{\mathbf{r}}$, so

$$II.\quad \int_{\mathcal{V_{b \le r \le 2b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x=-\oint_\mathcal{S_{r=b}} \mathbf{E}\cdot \hat{\mathbf{r}}\thinspace da + \oint_\mathcal{S_{r=2b}} \mathbf{E}\cdot \hat{\mathbf{r}}\thinspace da$$

Using $I.$ and $II.$ with the volume integral expressed in two parts

$$\int_{\mathcal{V_{r \le 2b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x=\int_{\mathcal{V_{r \le b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x + \int_{\mathcal{V_{\thinspace b \le r \le 2b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x $$

gives

$$\int_{\mathcal{V_{r \le 2b}}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x = \int_{\mathcal{S_{r=2b}}}\mathbf{E}\cdot \hat{\mathbf{n}}\thinspace da$$

(The surface integrals at $r=b$ cancel because their normal directions are in opposite directions.)

\newpage

## Related Problems

You do not need to turn these problems in. If you turn in these problems, I'll provide feedback.

These are problems that either I discussed in class or are related to the topic covered in class. I place them here for your reference. Some of the problems listed may not have been covered in class but may serve as exam practice problems.


###

Evaluate

$\displaystyle\lim_{n \to \infty}\Bigg[\int xD_n(x-1)dx\Bigg]$

using

$\displaystyle
D_n(x) = \begin{cases}
   n &\text{if } |x| \lt \frac{1}{2n} \\
   0 &\text{ otherwise}
\end{cases}
$

Repeat this problem using $D_n = \sqrt{\frac{n}{\pi}}e^{-nx^2}$

###

Evaluate

$\displaystyle\lim_{n \to \infty}\Bigg[\int f(x)D_n(x)dx\Bigg]$

using

$\displaystyle
D_n(x) = \begin{cases}
   n &\text{if } |x| \lt \frac{1}{2n} \\
   0 &\text{ otherwise}
\end{cases}
$

by writing $f(x)$ as a Taylor series expansion around $x=0$.

###

A straight 1-D rod of mass $M$ with a uniform mass density and length $a/n$ ($n=1, 2, ...$) is aligned with the $x$--axis and centered on $x=a$. Find the center of mass by evaluating

$\displaystyle \overline{x}\_n = \frac{1}{M}\int_{\text{rod}} x\lambda_n(x) dx$

###

Find the moment of inertia about the $y$--axis of the rod in the previous problem in terms of $a$, $n$, and $M$ by evaluating

$\displaystyle I\_n = \int_{\text{rod}} x^2\lambda_n(x)dx$

Explain why the value of $I_n$ for $n\to \infty$ makes sense.

###

A spherical shell has a net charge $Q$ uniformly distributed on its surface.

Find $\rho$ in terms of the delta function.

### Divergence Theorem

Show by direct calculation that

$$\oint_{\mathcal{S}}\mathbf{A}\bfcdot d\mathbf{a} = \int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{A}\thinspace d^3x$$

is satisfied when $\mathbf{A}=A_x(x)\xhat$ and $\mathcal{V}$ is an origin--centered cube of side length $b$ with its sides parallel to the coordinate planes.
   
### Divergence Theorem

Solve II-27 and II-28 of [Schey, 2005](https://drive.google.com/drive/folders/001s8T-MO_G7YfPuAiHesVK3yFNy82noAsg?usp=sharing).

# HW 2.

## Representing $\rho$ Using $\delta$ and $\Theta$

The step (or Heavyside step) function, $\Theta$, is defined by

$$
\Theta(x) = \begin{cases} 1 & x > 0\\ 0 & x \le 0\end{cases}
$$

$\Theta$ can be used to to express a charge density in a compact mathematical form. For example, instead of stating "a uniformly charged sphere centered on the origin, with total charge $Q$, and radius $b$", we can write $\rho(x,y,z)=\frac{Q}{(4/3)\pi b^3}\Theta(b-r)$. We can verify that when this density is integrated over all space, the result is $Q$:

$\displaystyle\int\rho(\mathbf{x})\thinspace d^3x=\frac{Q}{(4/3)\pi b^3}\int_{0}^{2\pi}d\phi\int_{0}^{\pi}\sin\theta d\theta\int_{0}^{\infty}\Theta(b-r)r^2dr
$

Because $\Theta(b-r)=0$ for $r\ge b$ and $\Theta(b-r)=1$ for $r\lt b$, the limits on the $r$ integral can be modfied and the $\Theta$ function removed:

$\displaystyle\int\rho(\mathbf{x})\thinspace d^3x=\frac{Q}{(4/3)\pi b^3}\int_{0}^{2\pi}d\phi\int_{0}^{\pi}\sin\theta d\theta\int_{0}^{b}r^2dr
$

The integrals above evaluate to the volume of a sphere of radius $b$ so that 

$\displaystyle\int\rho(\mathbf{x})\thinspace d^3x=Q$


%$\displaystyle\phantom{\int\rho(\mathbf{x})\thinspace d^3x}=\frac{Q}{b^3}\int_{-b}^{b}dz\int_{-b}^{b}dy\int_{-b}^{b}dx
%$

%$\displaystyle\phantom{\int\rho(\mathbf{x})\thinspace d^3x}=\frac{Q}{b^3}b^3$

1. Write the piecewise function $
f(x) = \begin{cases} 1 & |x| \lt b\\ 0 & |x| \ge b\end{cases}$ using one or more $\Theta$ functions.
1. Find the volume charge density $\rho$ in cylindrical coordinates in terms of $\delta$ and/or $\Theta$ for an infinitely long cylinder of radius $b$ with a charge density per unit length of $\lambda_o$ uniformly distributed on its surface. Assume that the cylinder's centerline is along the $z$-axis.
2. Repeat 2. assuming the cylinder is finite and extends from $z=-h/2$ to $z=h/2$.

## Green's Reciprocity Theorem

For discrete charges, Green's Reciprocity Theorem for $N$ charges is

$$\sum_{i=1}^{N}\Phi\_i q'\_i=\sum_{i=1}^{N}\Phi'\_i q\_i$$

Consider charges $q_1,q_2$, and $q_3$ at locations $x_1,x_2$, and $x_3$, respectively, on the $x$-axis. At these locations, the potentials are $\Phi_1,\Phi_2,$ and $\Phi_3$, respectively.

If a new system of charges $q'_1,q'_2$, and $q'_3$ is created by placing them at the same locations $x_1,x_2$, and $x_3$, respectively, the potentials at these locations are $\Phi'_1,\Phi'_2,$ and $\Phi'_3$, respectively.

Show that 

$$\sum_{i=1}^{3}\Phi\_i q'\_i=\sum_{i=1}^{3}\Phi'\_i q\_i$$

## Green's Reciprocity Use

1. In class, I partially did problem 1.13 of Jackson 3rd Edition (I only found the net charge on the upper of the plate). Find the net charge on the lower plate. Justify your steps at the level of detail given in class. (I stated an easy way of finding the net charge induced on the lower plate, but I want you to do it the long way, which requires steps similar to the ones used in class.)
2. A point charge at a distance $r$ from the origin is between two grounded spherical conducting shells of radius $b$ and $c$ that are centered on the origin. Find the net charge induced on the surfaces at $b$ and $c$.

For discussion during the next class: In my solution to part 1., I used the continous form of reciprocity. Could I have solved it using the discrete form?

## Green's Identity Derivation 

In one of the steps required to derive his identities (discussed in 1.8 of Jackson, 3rd Edition), Green said: "Consider the divergence of a scalar function $f$ multiplied by a vector function $\mathbf{A}$".

1. Show that

$$\mathbf{\nabla}\bfcdot (f\mathbf{A}) = f\thinspace \mathbf{\nabla}\bfcdot \mathbf{A} + \mathbf{A}\bfcdot(\mathbf{\nabla}f)$$

2. Show that

   $$\int_{\mathcal{V}} f\thinspace\mathbf{\nabla}\bfcdot \mathbf{A}\thinspace d^3x = -\int_{\mathcal{V}}\mathbf{A}\bfcdot(\mathbf{\nabla}f)\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\bfcdot\hat{\mathbf{n}}\thinspace da$$

  where $\mathcal{V}$ is the volume enclosed by the surface $\mathcal{S}$, $\hat{\mathbf{n}}$ is the normal to a differential area element $da$ on $\mathcal{S}$, and $d^3x$ is a differential volume element.

3. Verify the result in 2. by using an $f$, $\mathbf{A}$ and $\mathcal{V}$ of your choosing.

## Alternative Derivation of Reciprocity for Continuous $\rho$

Consider the integral

$$I = \int_{\mathcal V} \mathbf{E}\bfcdot\mathbf{E}'d^3x$$

1. Use $\mathbf{E}=-\mathbf{\nabla}\Phi$ and the result derived in the previous problem to re-write this equation in terms of a volume integral + a surface integral.

2. Repeat 1. using $\mathbf{E}'=-\mathbf{\nabla}\Phi'$

3. Show how the results from 1. and 2. can be used to show

$$\int_{all\space space}\Phi'\rho\thinspace d^3x = \int_{all\space space}\Phi\rho'\thinspace d^3x$$

which was a result derived in class last week using the discrete form of Green's reciprocity theorem.

## Related Problems

You do not need to turn these problems in. If you turn in these problems, I'll provide feedback.

These are problems that either I discussed in class or are related to the topic covered in class. I place them here for your reference. Some of the problems listed may not have been covered in class but may serve as exam practice problems.

### Divergence

Find $\int_{\mathcal{V}} \boldsymbol{\nabla} \cdot \mathbf{E}\thinspace d^3x$, where $\mathbf{E}$ is the electric field due to a point charge $q$ at $\mathbf{x}'$ and $\mathcal{V}$ is a sphere centered on the origin with radius $b \gt |\mathbf{x}'|$.

### Point Charge Outside of Conducting Sphere

A point charge is at a distance $r$ from the center of a conducting sphere of radius $b \lt r$. Use reciprocity to find the potential on the surface of the sphere.

### Delta and $\Theta$

1. Find the volume charge density $\rho$ in cylindrical coordinates in terms of $\delta$ and/or $\Theta$ for a uniformly charged disk of radius $b$ with charge density $\sigma_o$ that lies in the $x-y$ plane and is centered on the origin. Use $s$ for the radial coordinate in cylindrical coordinates.
2. Use identity 5. on page 26 of Jackson to convert this to spherical coordinates. Use $r$ for the radial coordinate in spherical coordinates.

# HW 3

## 1-D Cartesian Green Function

Two infinite and grounded conducting sheets are in the $x=0$ and $x=w$ plane. In the $x=x'$ plane, there is an infinite non-conducting sheet with surface charge density $\sigma'$.

1. Find the potential, $\psi_l(x)$, on the left ($0\le x\le x'$) and to the right ($x'\le x\le w$), $\psi_r(x)$, of the non-conducting sheet using any method (Gauss's law or the boundary value method can be used; you should be able to do it using both methods, but you need to only show your work using one method).

2. Write the potential $\psi(x)$ for $0\le x\le w$ as a single function using $\psi_l$ and $\psi_r$ and the Heavyside step function $\Theta$. (In the future this $\psi$ (with $\sigma'/\epsilon_o$ set to 1), will be called a Green function, which is the motivation for the title of this problem.)

3. Show that $\nabla^2\psi(x) = -\frac{\sigma'}{\epsilon_o}\delta(x-x')$. You will need to use the fact that $d\Theta(x)/dx=\delta(x)$, and $d\Theta(-x)/dx=-\delta(x)$. Also compute $\nabla'^2\psi(x)$, where the prime means to take derivatives with respect to primed variables. (This may seem odd because $x'$ was defined to be a constant; here you are being asked to treat it as a variable. You should get an answer that is proportional to $\delta(x-x')$).

As discussed in class, the motivation for solving this problem is that its potential, $\psi$, can be used in Green's second identity (eqation 1.35), which is a form of reciprocity, to solve the most general problem for this geometry. The most general problem is to find the potential $\Phi(x)$ when $\rho=\rho(x)$ between $x=a$ and $x=b$, the left plane is grounded, and the right plane is at potential $V_o$. Instead of using $\psi$ found above to solve the most general problem, first use it to solve an easier problem:

4. Use Equation 1.35 and $\psi(x)$ to find the potential $\Phi(x)$ when $\rho(x)=0$ between the conductors and $\Phi(0)=0$ and $\Phi(w)=V_o$. Include a sketch or a sentence where you define $\mathcal{V}$ and $\mathcal{S}$ when you use Equation 1.35. There will be a subtilty with notation here -- if you use Equation 1.35 as written, you'll end up with $\Phi(x')$ and not the desired $\Phi(x)$.

%5. Suppose the conducting planes are grounded and a non-conducting slab with charge density $\rho_o$ exists between them. Use the above equation to find $\Psi(\mathbf{x})$ between the conducting planes. 

## 1-D Spherical Green Function

Two conducting and grounded spherical shells of radius $b$ and $c$ are centered on the origin, and $c\gt b$.

A nonconducting spherical shell is centered on the origin and has a charge density of $\sigma'$ and radius $r'$, with $b \lt r' \lt c$.

1. Find $\psi_i(r)$, the potential between the inner conducting shell and the charged shell and $\psi_o(r)$, the potential between the charged shell and the outer conducting shell. (Read the subscript $i$ as "inner" and $o$ as "outer".)
2. Find the surface charge densities on the inner and outer conductor.
3. Verify that Gauss's law is satisfied for a Gaussian sphere centered on the origin and with a radius that is between the charged shell and the outer conducting shell.
2. Write the potential $\psi(r)$ for $b\le r\le c$ as a single function using $\psi_i$ and $\psi_o$ and the Heavyside step function $\Theta$.

## Jackson Equation 1.42

Before stating Equation 1.42, Jackson (3rd edition) notes that with Equation 1.35 and 1.39, it is simple to obtain a generalization of Equation 1.36.

Show the "simple" steps need to arrive at Equation 1.42.

Be very careful with notation. You'll need to think a bit about the justification and validity of swapping $x$ and $x'$ and/or changing the dummy variable used in integration. When you do either of these, provide a justification so that I know you are not applying the "answer operator".






