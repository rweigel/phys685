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

$$\begin{align*}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}Q\delta(x')\delta(y')\thinspace dx'dy' \\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y')dy'\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}\delta(x')\thinspace dx'\\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y')dy'\frac{(x-0)\xhat+(y-y')\yhat}{\sqrt{(x-0)^2 + (y-y')^2}^3}\\\\
= & \frac{Q}{4\pi\epsilon_o}\frac{(x-0)\xhat+(y-0)\yhat}{\sqrt{(x-0)^2 + (y-0)^2}^3}\\\\
= & \frac{Q}{4\pi\epsilon_o}\frac{x\xhat+y\yhat}{\sqrt{x^2 + y^2}^3}
\end{align*}
$$

The generalization to the 3-D problem given is straightforward.

2\.

Here $x', y'$, and $z'$ are fixed points in space. Normally when given a charge density, we replace $x, y, z$ with $x',y',z'$. If we did that here, we would have $\rho(\mathbf{r}')=Q\delta(0)\delta(0)\delta(0)$, which does not depend on primed coordinates. To work around this issue, change the integration variables to be double primes. As before, in two dimensions,

$$
\begin{align*}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x'')\xhat+(y-y'')\yhat}{\sqrt{(x-x'')^2 + (y-y'')^2}^3}Q\delta(x''-x')\delta(y''-y')\thinspace dx''dy'' \\\\
= & \frac{Q}{4\pi\epsilon_o}\int\delta(y''-y')dy''\int\frac{(x-x'')\xhat+(y-y'')\yhat}{\sqrt{(x-x'')^2 + (y-y'')^2}^3}\delta(x''-x')\thinspace dx''\\\\
\end{align*}
$$

In the integral above, the $x'$ is a constant with respect to integration (in the same way that in $\int\delta(x-a)dx$, $a$ is a constant) and so we replace $x''$ with this constant value.

$$
\begin{align*}\mathbf{E}(\mathbf{r}) = & \frac{Q}{4\pi\epsilon_o}\int\delta(y''-y')dy''\frac{(x-x')\xhat+(y-y'')\yhat}{\sqrt{(x-x')^2 + (y-y'')^2}^3}\\\\
=& \frac{Q}{4\pi\epsilon_o}\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}
\end{align*}
$$

In class, I used an alternative approach where I replaced $x',y',z'$ with $a_x, a_y, a_z$ and integrated over $x',y',z'$ so that I needed to evaluate

$$
\begin{align*}\mathbf{E}(\mathbf{r}) = & \frac{1}{4\pi\epsilon_o}\int\int\frac{(x-x')\xhat+(y-y')\yhat}{\sqrt{(x-x')^2 + (y-y')^2}^3}Q\delta(x'-a_x)\delta(y'-a_y)\thinspace dx'dy'
\end{align*}
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

\newpage

# HW 2.

## Representing $\rho$ Using $\delta$ and $\Theta$

The step (or Heavyside step) function, $\Theta$, is defined by

$$
\Theta(x) = \begin{cases} 1 & x > 0\\ 0 & x \le 0\end{cases}
$$

$\Theta$ can be used to to express a charge density in a compact mathematical form. For example, instead of stating "a uniformly charged sphere centered on the origin, with total charge $Q$, and radius $b$", we can write $\rho(x,y,z)=\frac{Q}{(4/3)\pi b^3}\Theta(b-r)$. When this density is integrated over all space, the result is $Q$:

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

**Solution**

1. As mentioned in class, an easy way to solve this is to write $f(x)$ as the sum of two step functions. One shifted to the left by $b$, corresponding to $\Theta(x+b)$; the other shifted to the right and inverted, corresponding to $\Theta(x-b)$. Thus,

   $f(x) = \Theta(x+b) - \Theta(x-b)$.
   
   Other solutions:

   $f(x) = \Theta(b-|x|)$
   
   $f(x)=\Theta(b^2-x^2)=\Theta[(b-x)(b+x)]$
   
   $f(x) = \Theta(b+x) - \Theta(x-b)$

   It may be interesting to use $d\Theta/dx=\delta(x)$ develop an identity for $\Theta(f(x))$ similar to identity 5. on page 26 of Jackson 4th Edition.

   Checks:
   * when $x=0$, $f(x) = \Theta(b) - \Theta(-b) = 1-0 = 1$
   * when $x=2b$, $f(x) = \Theta(3b) - \Theta(b) = 1-1 = 0$
   * when $x=-2b$, $f(x) = \Theta(-b) - \Theta(-3b) = 0-0 = 0$

2. We want a charge distribution that is localized at a cylindrical radial distance $b$. $\rho(s) = C\delta(s-b)$ has this feature, where $C$ is a constant. We also need the integral of this charge density over all space to equal the total charge on the cylinder, which is $Q=\lambda_o h$ assuming that the length of the cylinder is $h$. Thus, we need to find $C$ such that

   $\displaystyle Q=\lambda_o h = \int \rho(\mathbf{x})d^3x$
   
   $\displaystyle Q=\lambda_o h = \int_{-h/2}^{h/2}\int_{0}^{2\pi}\int_{0}^\infty C\delta(s-b) sdsd\phi dz$   

   $\displaystyle Q=\lambda_o h = 2\pi hC\int_{0}^\infty \delta(s-b) sds=2\pi h C b \quad\Rightarrow\quad C=\lambda_o/2\pi b$

  and so
  
  $\displaystyle \rho(\mathbf{x}) = \frac{\lambda_o}{2\pi b}\delta(s-b)$

  Equivalently, we can write

  $\displaystyle \rho(\mathbf{x}) = \frac{\lambda_o}{2\pi s}\delta(s-b)$

  because $\delta(s-b)/s=\delta(s-b)/b$, which follows from the fact that the delta function is only non-zero at $s=b$.
  
3. Here we apply the result from part 1. with the replacement of $b$ in that problem with $h/2$:

    $\displaystyle \rho(\mathbf{x}) = \frac{\lambda_o}{2\pi b}\delta(s-b)[\Theta(x+h/2) - \Theta(x-h/2)]$

## Green's Reciprocity Theorem

For discrete charges, Green's Reciprocity Theorem for $N$ charges is

$$\sum_{i=1}^{N}\Phi\_i q'\_i=\sum_{i=1}^{N}\Phi'\_i q\_i$$

Consider charges $q_1,q_2$, and $q_3$ at locations $x_1,x_2$, and $x_3$, respectively, on the $x$-axis. At these locations, the potentials are $\Phi_1,\Phi_2,$ and $\Phi_3$, respectively.

If a new system of charges $q'_1,q'_2$, and $q'_3$ is created by placing them at the same locations $x_1,x_2$, and $x_3$, respectively, the potentials at these locations are $\Phi'_1,\Phi'_2,$ and $\Phi'_3$, respectively.

Show that 

$$\sum_{i=1}^{3}\Phi\_i q'\_i=\sum_{i=1}^{3}\Phi'\_i q\_i$$

**Solution**

The physical interpretation of Green's Reciprocity theorem is that the work required to put charges an unprimed set of charges at $x_1,x_2,x_3$ under the influence of only the electric field of a primed set of charges $x_1,x_2,x_3$ must be the same as the work required to put a primed set of charges at $x_1,x_2,x_3$ under the influence of only the electric field of an unprimed set of charges at $x_1,x_2,x_3$.

Using

$\displaystyle\Phi_i=\sum_{\substack{j=1\\j\ne i}}^N \frac{q_j}{|x_j-x_i|}=\sum_{\substack{j=1\\j\ne i}}^N \frac{q_j}{d_{ji}}$

gives, for $N=3$, the left-hand side terms in $\sum\_{i=1}^{3}\Phi\_i q'\_i=\sum\_{i=1}^{3}\Phi'\_i q\_i$

$
\begin{array}{rc}
\Phi\_1q'\_1 & = & 0 & + &  \frac{q\_2q'\_1}{d\_{21}} & + & \frac{q\_3q'\_1}{d\_{31}}  \\ \\
\Phi\_2q'\_2 & = & \frac{q\_1q'\_2}{d\_{12}} & + & 0 & + & \frac{q\_3q'\_2}{d\_{32}} \\ \\
\Phi\_3q'\_3 & = & \frac{q\_1q'\_3}{d\_{13}} & + & \frac{q\_2q'\_3}{d\_{23}} & + & 0 &
\end{array}
$

The right-hand side terms in $\sum_{i=1}^{3}\Phi\_i q'\_i=\sum\_{i=1}^{3}\Phi'\_i q\_i$ can be expanded as

$
\begin{array}{rc}
\Phi'\_1q\_1 & = & 0 & + &  \frac{q'\_2q\_1}{d\_{21}} & + & \frac{q'\_3q\_1}{d\_{31}}  \\ \\
\Phi'\_2q\_2 & = & \frac{q'\_1q\_2}{d\_{12}} & + & 0 & + & \frac{q\_2q'\_3}{d\_{32}} \\ \\
\Phi'\_3q\_3 & = & \frac{q'\_1q\_3}{d\_{13}} & + & \frac{q'\_2q\_3}{d\_{23}} & + & 0 &
\end{array}
$

In the above, the left-- and right--hand sides of the equation to prove were written in the form of a matrix. In this form, one can see that the matrices are transposes of each other. If we sum all elements in a matrix, the result is the same if we sum all elements of that matrix transposed.

More generally, one can use

$\displaystyle \sum_{i=1}^{N} q\_i\Phi'\_i = \sum_{i=1}^{N} q\_i \sum_{\substack{j=1\\j\ne i}}^N \frac{q'\_j}{d\_{ij}}=\sum_{i=1}^{N}\sum\_{\substack{j=1\\j\ne i}}^N \frac{ q'\_j q_i}{d\_{ij}}$

Repeating with the primed and unprimed swapped and starting with a dummy index of $j$ instead of $i$, we have

$\displaystyle \sum_{j=1}^{N} q'\_j\Phi\_j = \sum_{j=1}^{N} q'\_j \sum_{\substack{i=1\\i\ne j}}^N \frac{q\_i}{d\_{ji}}=\sum_{j=1}^{N}\sum\_{\substack{i=1\\i\ne j}}^N \frac{ q'\_j q_i}{d\_{ij}}$

Where in the last step, $d_{ji}=d_{ij}$ was used.

One can think of $q'\_j q_i/d\_{ij}$ as elements in a matrix. The equations

$\displaystyle\sum_{i=1}^{N}\sum\_{\substack{j=1\\j\ne i}}^N \frac{ q'\_j q_i}{d\_{ij}}$ and $\displaystyle \sum_{j=1}^{N}\sum\_{\substack{i=1\\i\ne j}}^N \frac{ q'\_j q_i}{d\_{ij}}$

both result in the sum of all elements of a matrix excluding the diagonals. The only difference is the order in which the elements of the matrix are summed. For a continuous charge distribution, we would use the fact that the order of integration could be changed to arrive at the result $\int dq \Phi'(x) d^3x = \int dq' \Phi(x') d^3x'$.

## Green's Reciprocity Use

1. In class, I partially did problem 1.13 of Jackson 3rd Edition (I only found the net charge on the upper of the plate). Find the net charge on the lower plate. Justify your steps at the level of detail given in class. (I stated an easy way of finding the net charge induced on the lower plate, but I want you to do it the long way, which requires steps similar to the ones used in class.)
2. A point charge at a distance $r$ from the origin is between two grounded spherical conducting shells of radius $b$ and $c$ that are centered on the origin. Find the net charge induced on the surfaces at $b$ and $c$.

For discussion during the next class: In my solution to part 1., I used the continous form of reciprocity. Could I have solved it using the discrete form?

**Solution**

1.

Let the unprimed system have a conducting plate in $z=0$ plane held at $\Phi=0$ and a conducting plate in the $z=d$ plane held at at $\Phi=V_o$.

Let the unprimed system have a conducting plate in the $z=0$ plane held at at $\Phi'=0$, a conducting plate in the $z=d$ plane held at $\Phi'=0$, and a point charge $q'$ at $(x,y,z)=(x_o,0,0)$.

One can use the equation from problem 1.11 of Jackson or start with

$\displaystyle\int_{all\thinspace space}\rho'\Phi\thinspace d^3x = \int_{all\thinspace space}\rho\Phi'\thinspace d^3x$

and split the charge density into surface and volume charge densities $\sigma$ and $\rho_v$, where the subscript $v$ means charge not on the conducting surfaces $\mathcal{S}$:

$\displaystyle\int_{all\thinspace space}\rho_v'\Phi\thinspace d^3x+\int_{\mathcal{S}}\sigma'\Phi\thinspace da = \int_{all\thinspace space }\rho_v\Phi'\thinspace d^3x+\int_{\mathcal{S}}\sigma\Phi'\thinspace da$

The first term on RHS is zero because $\rho_v=0$ (there are no charges in the unprimed system between the plates). The second term on the RHS is zero becuase $\Phi'=0$ on conducting surfaces.

The first term on the LHS reduces to $q'\Phi(x_o)$ becuase $\rho_v'=q'\delta(x-x_o)\delta(y)\delta(z)$ (the notation $\rho_v'=q'\delta(\mathbf{x}-\mathbf{x_o}')$ is also acceptable; this gives $\Phi(\mathbf{x_o})$, which is the same things as $\Phi(x_o)$ notationally). 
The potential between the plates in the unprimed system is

$\displaystyle\Phi(x)=V_o\frac{x}{d}$

and so the first term on the LHS is $q'V_ox_o/d$.

The second term on LHS is composed of integrals over the top and bottom surfaces (assuming all of the charges in the primed system are on the plates or at $x_o$; this is discussed below). Given that $\Phi=0$ on bottom surface, we are left with an integral over upper surface ($u$) for which $\Phi=V_o$.

$$\int_{\mathcal\thinspace u}\sigma'V_o\thinspace da=V_o\int_{\mathcal\thinspace u}\sigma'\thinspace da=V_oq'_u$$

The equation 

$\displaystyle\int_{all\thinspace space}\rho_v'\Phi\thinspace d^3x+\int_{\mathcal{S}}\sigma'\Phi\thinspace da = \int_{all\thinspace space }\rho_v\Phi'\thinspace d^3x+\int_{\mathcal{S}}\sigma\Phi'\thinspace da$

thus reduces to 

$\displaystyle q'V_ox_o/d + V_oq'_u = 0 \Rightarrow \boxed{q'_u=-q\frac{x_o}{d}}$

One can reverse the potentials on the unprimed system to arrive at the charge $q'_l$ on the lower primed surface, which is

$\boxed{q'_l=q'\left(\frac{x_o}{d}-1\right)}$

Note also that the assumption that the total charge in the universe is zero

$q'_u+q'_l+q=0$

could have also been used to find $q'_l$ given $q'_u$. 

----

Note: In the solution, I assumed all free charges were on the upper and lower surfaces and there were no charges on far-away surfaces; this statement is justified post hoc by uniqueness and because computing $q'_u$ and $q'_l$ in this way gave $q'_u+q'_l+q=0$. To avoid this assumption, one would need to use equation 1.35 of Jackson with the volume being the volume between the plates. Curiously, in problem 1.11, Jackson suggests using equation 1.35 to come up with what he calls Green's reciprocation theorem, seemingly so it could be applied in problem 1.12. However, the equation in problem 1.11 does not directly apply because the surface of the volume between the plates is not all conductor (only the top and bottom parts of the volume are conductors, the sides of this volume are not). One is left with having to use equation 1.35 and the argument that because the problem is 1-dimensional, the derivatives of the potential with respect to the normal on the side surfaces of the volume are zero.

----

2.

The procedure here is nearly identical to part 1. The potential between the sphere in the unprimed system when the potential at $r=b$ is $V_o$ and the potential at $r=c$ is zero is

$\displaystyle\Phi(r)=V_o\frac{b}{c-b}\left(\frac{c}{r}-1\right)$

which can be found by solving the boundary value problem

$\Phi(c)=0\quad \Phi(b)=V_o$

$\displaystyle\nabla^2\Phi = \frac{1}{r^2}\frac{d^2 (r^2\Phi)}{dr^2}= 0 \quad \Rightarrow \quad \Phi = A + B/r$

to find $A$ and $B$ or by assuming a charge $Q$ on the outer sphere and $-Q$ on the inner sphere and using Gauss' law to find $E_r$ and then $V(c)-V(b)=-\int_b^cE_r\thinspace dr$ (the $Q$ will cancel). The final result is

$\displaystyle q'_{r=b}=-V_o\frac{q'b}{c-b}\left(\frac{c}{r_o}-1\right)$

$\displaystyle q'_{r=c}=+V_o\frac{q'c}{c-b}\left(\frac{b}{r_o}-1\right)$

## Green's Identity Derivation 

In one of the steps required to derive his identities (discussed in 1.8 of Jackson, 3rd Edition), Green said: "Consider the divergence of a scalar function $f$ multiplied by a vector function $\mathbf{A}$".

1. Show that

$$\mathbf{\nabla}\bfcdot (f\mathbf{A}) = f\thinspace \mathbf{\nabla}\bfcdot \mathbf{A} + \mathbf{A}\bfcdot(\mathbf{\nabla}f)$$

2. Show that

   $$\int_{\mathcal{V}} f\thinspace\mathbf{\nabla}\bfcdot \mathbf{A}\thinspace d^3x = -\int_{\mathcal{V}}\mathbf{A}\bfcdot(\mathbf{\nabla}f)\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\bfcdot\hat{\mathbf{n}}\thinspace da$$

  where $\mathcal{V}$ is the volume enclosed by the surface $\mathcal{S}$, $\hat{\mathbf{n}}$ is the normal to a differential area element $da$ on $\mathcal{S}$, and $d^3x$ is a differential volume element.

3. Verify the result in 2. by using an $f$, $\mathbf{A}$ and $\mathcal{V}$ of your choosing.

**Solution**

1\. This can be shown by writing $\boldsymbol{\nabla}$ and $\mathbf{A}$ in cartesian coordinates.

2\. The divergence theorem

$\displaystyle\oint_{\mathcal{S}}\mathbf{U}\cdot d\mathbf{a}=\int_{\mathcal{V}}\boldsymbol{\nabla}\cdot \mathbf{U}\thinspace d^3x$

using $\mathbf{U}=f\mathbf{A}$ on the LHS and $\mathbf{U}=f(\mathbf{\nabla}\cdot \mathbf{A}) + \mathbf{A}\cdot(\mathbf{\nabla}f)$ the the RHS gives

$\displaystyle\oint_{\mathcal{S}}f\mathbf{A}\cdot d\mathbf{a}=\int_{\mathcal{V}}\Big[\boldsymbol{\nabla}\cdot f(\mathbf{\nabla}\cdot \mathbf{A}) + \mathbf{A}\cdot(\mathbf{\nabla}f)\big]\thinspace d^3x$

and rearrangement gives

$\displaystyle\int_{\mathcal{V}} f(\mathbf{\nabla}\cdot \mathbf{A})\thinspace d^3x = -\int_{\mathcal{V}}\mathbf{A}\cdot(\mathbf{\nabla}f)\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\cdot\hat{\mathbf{n}}\thinspace da$

Note that when $\mathbf{A}=A_x(x)\hat{\mathbf{x}}$, $f=f(x)$, and $\mathcal{V}$ is a cube, this reduces to the integration by parts formula.

## Alternative Derivation of Reciprocity for Continuous $\rho$

Consider the integral

$$I = \int_{\mathcal V} \mathbf{E}\bfcdot\mathbf{E}'d^3x$$

1. Use $\mathbf{E}=-\mathbf{\nabla}\Phi$ and the result derived in the previous problem to re-write this equation in terms of a volume integral + a surface integral.

2. Repeat 1. using $\mathbf{E}'=-\mathbf{\nabla}\Phi'$

3. Show how the results from 1. and 2. can be used to show

$$\int_{all\space space}\Phi'\rho\thinspace d^3x = \int_{all\space space}\Phi\rho'\thinspace d^3x$$

which was a result derived in class last week using the discrete form of Green's reciprocity theorem.

**Solution**

%From HW #2, derived using a vector identity + the divergence theorem (Several students did not cite this result from HW #2. As a general rule, if a step is not obvious, the justification or a citation to an equation in a book needs to be provided; otherwise it can appear as if you are omitting justification because you don't know what it is.):

The identity from the previous problem is

$$\int_{\mathcal{V}} f(\mathbf{\nabla}\cdot \mathbf{A})\thinspace d^3x = -\int_{\mathcal{V}}\mathbf{A}\cdot(\mathbf{\nabla}f)\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\cdot\hat{\mathbf{n}}\thinspace da$$

or, switching locations of the volume integrals,

$$\int_{\mathcal{V}}\mathbf{A}\cdot(\mathbf{\nabla}f)\thinspace d^3x= -\int_{\mathcal{V}} f(\mathbf{\nabla}\cdot \mathbf{A})\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\cdot\hat{\mathbf{n}}\thinspace da$$

Using $f=\Phi'$ and $\mathbf{A}=\mathbf{E}$ in the identity and $\mathbf{E}'=\boldsymbol{\nabla} \Phi'$ gives

$$I=\int_{\mathcal{V}}\mathbf{E}\cdot(\mathbf{\nabla}\Phi')\thinspace d^3x= -\int_{\mathcal{V}} \Phi'(\mathbf{\nabla}\cdot \mathbf{E})\thinspace d^3x+\oint_{\mathcal{S}} \Phi'\mathbf{E}\cdot\hat{\mathbf{n}}\thinspace da$$

Using $f=\Phi$ and $\mathbf{A}=\mathbf{E}'$ in the identity and $\mathbf{E}=\boldsymbol{\nabla} \Phi$ gives

$$I=\int_{\mathcal{V}}\mathbf{E}'\cdot(\mathbf{\nabla}\Phi)\thinspace d^3x= -\int_{\mathcal{V}} \Phi(\mathbf{\nabla}\cdot \mathbf{E}')\thinspace d^3x+\oint_{\mathcal{S}} \Phi\mathbf{E}'\cdot\hat{\mathbf{n}}\thinspace da$$

(The two equations for $I$ must be equal because the integrands on the left--hand side integrals are the same because $\mathbf{E}\bfcdot\mathbf{\nabla}\Phi'= \mathbf{E}\bfcdot\mathbf{E}'=\mathbf{E}'\bfcdot\mathbf{E}=\mathbf{E}'\bfcdot\mathbf{\nabla}\Phi$.)

Equating the two equations for $I$ gives

$$-\int_{\mathcal{V}} \Phi'(\mathbf{\nabla}\cdot \mathbf{E})\thinspace d^3x+\oint_{\mathcal{S}} \Phi'\mathbf{E}\cdot\hat{\mathbf{n}}\thinspace da=-\int_{\mathcal{V}} \Phi(\mathbf{\nabla}\cdot \mathbf{E}')\thinspace d^3x+\oint_{\mathcal{S}} \Phi\mathbf{E}'\cdot\hat{\mathbf{n}}\thinspace da$$

If the volume is all space, the area of $\mathcal{S}$ becomes infinite. If all of the charges that make up $\rho$ and $\rho'$ are confined to be in a sphere centered at the origin with a finite radius, then as the radius of $\mathcal{S}\rightarrow\infty$, $\mathbf{E}\rightarrow \hat{\mathbf{r}}/r^2$ and $\Phi\rightarrow 1/r$ and similar for $\mathbf{E}'$ and $\Phi'$.  (You needed to provide some sort of justification similar to this in you solution - saying the potential and field approaches zero is not sufficient because the surface becomes infinite and you are left with $\infty\cdot 0$). So for $\mathcal{S}$ being a spherical surface with large $r$

$$\oint_{\mathcal{S}} \Phi\mathbf{E}'\cdot\hat{\mathbf{n}}\thinspace da\simeq\int_0^{2\pi}\int_0^{\pi}\frac{QQ'}{r^3}\thinspace r^2\sin\theta\thinspace d\theta\thinspace d\phi=4\pi \frac{QQ'} r$$

Where $Q$ and $Q'$ are the total charges in the unprimed and primed system respectively. As a result of this argument, the surface integrals can be dropped and $\mathcal{V}$ can be replaced with $all\text{ } space$ and we are left with

$$\int_{{all\space space}} \Phi'(\mathbf{\nabla}\cdot \mathbf{E})\thinspace d^3x = \int_{{all\space space}} \Phi(\mathbf{\nabla}\cdot \mathbf{E}')\thinspace d^3x$$

Finally, using $\boldsymbol{\nabla}\bfcdot\mathbf{E} = -\nabla^2\Phi=\rho/\epsilon_o$ and $\boldsymbol{\nabla}\bfcdot\mathbf{E}' = -\nabla^2\Phi'=\rho'/\epsilon_o$ gives

$$\int_{all\space space}\Phi'\rho\thinspace d^3x = \int_{all\space space}\Phi\rho'\thinspace d^3x$$


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

\newpage

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

# HW 4

## Green function for infinite dome

In class, I showed how to find the potential $\psi$ due to a point charge inside of a grounded, conducting, and closed dome when the radius of the dome is infinite. The potential was found using the method of images. (A dome is a hemisphere plus a cap.) 

Use this $\psi$ and equation 1.35 of Jackson (or equation 1.42; $\psi$ is proportional to a Green function) to find the potential $\Phi$ for the following problem:

An conducting dome has its base in the $x-y$ plane and the radius of the dome is infinite. There are no charges inside of the dome. The boundary of the dome is grounded except for the region between $x^2 + y^2 < b$, which is held at a potential of $V_o$.

1. Find the potential $\Phi(z)$ inside of the dome (the integral required to find $\Phi(x,y,z)$ requires an approximation of the integrand or numerical integration and will be considered in the future).
2. Find the potential $\Phi(z)$ inside of the dome when $b/z \ll 1$. Do this by Taylor series expanding $\Phi(z)$ for small $b/z$. Does the answer make sense?
3. Sketch the electric field lines inside of the dome.

Note that a related problem (but with a different Green function) considered in 2.6 of Jackson.

## 2--D Cartesian Boundary Value Problem

Review Griffiths 3.3.1 (3rd and 4th edition). You should be able to quickly derive the potential for Figure 3.20 (3rd and 4th edition) when any one of the sides is at $V_o$ and the other three are grounded. See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.html).

Suppose the sides of Figure 3.20 of Griffiths 3rd or 4th edition are held at $V_l$, $V_r$, $V_t$, and $V_b$, where $l=$left, $r=$right, $t=$top, and $b=$bottom. Find the potential inside the rectangular pipe.

Hints:

1. The total potential will be the the sum of the potentials from four different problems (1)
 $V_l$ non--zero and all other sides zero, (2) $V_r$ non--zero and all other sides zero, etc. I will ask you to explain why in class.
2. You can build the solution to three of the four problems described in the first hint using a transformation of coordinate system and the solution to one of the problems.

## 2--D Spherical Boundary Value Problem

In 2.7 of Jackson 3rd edition, he solves for the potential outside of a sphere with hemispheres held at $\pm V$ using a Green function. In example 3.7 of Griffiths 4th edition (example 3.6 in 3rd edition), he describes how to solve for the potential outside of a sphere with a potential of $V(\theta)$ on its surface. As a result, Jackson's example is related to Griffiths' example.

Study these two examples and be prepared to answer questions (such as how they are related) about them in class.




