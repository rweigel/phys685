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

**Solution**

1\. One can answer this question by assuming a surface charge of $\sigma_l$ and $\sigma_r$ is induced on the plates at $x=0$ and $x=w$. Then use the formula $\sigma/2\epsilon_o$ for the electric field of the sheets of charge at $\sigma_l$ at $x=0$, $\sigma'$ at $x=x'$, and $\sigma_r$ at $x=w$ to get the total field $E_l$ and $E_r$.  The two unknowns, $\sigma_l$ and $\sigma_r$, can be found by using the fact that the electric field in either of the conductors is zero - this yields $\sigma' = -(\sigma_l+\sigma_r)$, which is expected because the net charge in the universe is zero. The second equation needed to find $\sigma_l$ and $\sigma_r$ in terms of $\sigma'$ is

$\displaystyle\psi(w)-\psi(0) = 0 = -\int_0^w E\thinspace dx=-\int_0^{x'}E_ldx-\int_{x'}^wE_rdx$

Alternatively, one can use the fact that $\nabla^2 \psi(x)=0$ has solutions of the form $\psi=A+Bx$, the two boundary conditions and the continuity and jump conditions at $x=x'$.

$\psi_l=A_l+B_lx\qquad\psi_r=A_r+B_rx$

Boundary conditions:

$\psi_l(0)=0\Rightarrow A_l=0$

$\psi_r(w)=0=A_r+B_rw\Rightarrow A_r=-B_rw$

This leaves

$\psi_l=B_lx$ and $\psi_r=B_r(x-w)$

Continuity:

$\psi_l(x')=\psi_r(x')\Rightarrow B_lx'=B_r(x'-w)$

Jump:

The jump condition follows from Gauss's law with a Gaussian cylinder with one end cap to the left of $x'$ and the other to the right. It also follows from integrating $\nabla^2\psi=d(d\psi/dx)/dx=-\sigma'\delta(x-x')/\epsilon_o$ once with respect to $x$.
The condition is

$\displaystyle E_r-E_l=\frac{\sigma'}{\epsilon_o}$

or

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

$\displaystyle-B_r+B_l=\frac{\sigma'}{\epsilon_o}\Rightarrow B_l=B_r+\frac{\sigma'}{\epsilon_o}$

The three equations left are

$A_r=-B_rw\qquad B_lx'=B_r(x'-w)\qquad B_l=B_r+\frac{\sigma'}{\epsilon_o}$

Solving gives

$\displaystyle B_l=-\frac{\sigma'}{\epsilon_o}\left(\frac{x'}{w}-1\right)$ and $B_r=-\frac{\sigma'}{\epsilon_o}\frac{x'}{w}$

So the final solution is

$\boxed{\displaystyle\psi_l=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x'}{w}\right)x\quad\quad\displaystyle\psi_r=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x}{w}\right)x'}$

Note that swapping $x$ and $x'$ in $\psi_l$ gives the equation for $\psi_r$, and vice-versa. That is, $\psi_l(x',x)=\psi_r(x,x')$.

2\.

$\boxed{\psi=\psi_l(x)\Theta(x'-x)+\psi_r(x)\Theta(x-x')}$

Checks: 
* When $x\lt x'$, $\Theta(x'-x)=1$ and $\Theta(x-x')=0$, giving $\psi=\psi_l$.
* When $x\gt x'$, $\Theta(x'-x)=0$ and $\Theta(x-x')=1$, giving $\psi=\psi_r$.

3\.

$\begin{array}{ll}
\displaystyle\frac{d\psi}{dx} & = \displaystyle\thickspace \psi_l(x)\frac{d}{dx}\Theta(x'-x) + \Theta(x'-x)\frac{d\psi_l(x)}{dx} \\\\
& \displaystyle+\thickspace\psi_r(x)\frac{d}{dx}\Theta(x-x')+\Theta(x-x')\frac{d\psi_r(x)}{dx}
\end{array}
$

If one plots $\psi(x)$, you will see that its derivative has a jump downwards at $x=x'$ of $\sigma'/\epsilon_o$ and so we expect the terms in $d\psi/dx$ with the derivative of the Heavyside step function, which is the delta function, to be zero. So the two terms involving derivatives of $\Theta$ will be addressed first.

The first term can be rewritten using

$\displaystyle\frac{d}{dx}\Theta(x'-x)=-\delta(x'-x)=-\delta(x-x')$

The first equality follows from the identity given in the problem statement: $d\Theta(-x)/dx=-\delta(x)$. The second equality is a standard delta function identity.

The second term is

$\displaystyle\frac{d}{dx}\Theta(x-x')=\delta(x-x')$

The following two equalities follow from the fact that $\delta(x-x')$ is zero except at $x=x'$:

$\psi_l(x)\delta(x-x')=\psi_l(x')\delta(x-x')$

$\psi_r(x)\delta(x-x')=\psi_r(x')\delta(x-x')$

Given that $\psi_r(x')=\psi_l(x')$, the two terms in $d\psi/dx$ involving derivatives of $\Theta$ cancel, leaving

$\displaystyle\frac{d\psi}{dx} = \Theta(x'-x)\frac{d\psi_l(x)}{dx} +\Theta(x-x')\frac{d\psi_r(x)}{dx}$

Straightforward calculation and use of the same identities as above gives

$\displaystyle\frac{d^2\psi}{dx^2}=-\frac{\sigma'}{\epsilon_o}\delta(x-x')$

This matches expectations. For a sheet of charge in the $x=x'$ plane, the volume charge density is

$\rho=\sigma'\delta(x-x')$

and Poisson's equation is $\displaystyle\nabla^2\psi=-\frac{\rho}{\epsilon_o}$

(Recall that the units of $\delta(x)$ are inverse length. This follows from part of the definition of the delta function: $\int\delta(x)dx=1$).

4\. Equation 1.35 with $\phi$ replaced with $\Phi$ is

$$\int_{\mathcal{V}} \left(\Phi\nabla^2\psi -\psi\nabla^2\Phi\right)d^3x=\oint_{\mathcal{S}}\left(\Phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \Phi}{\partial n}\right) da$$

Let $\mathcal{V}$ be the volume spanned by $x=[0,w]$, $y=[0,b]$, and $z=[0,b]$, where $b$ is arbitrary. This volume has six surfaces and so the surface integral will have six parts.

In the volume integral, the term with $\nabla^2\Phi=0$ because there is no charge in the volume of the $\Phi$ system. Subtitution of $\nabla^2\psi=-(\sigma'/\epsilon_o)\delta(x-x')$ gives

$\displaystyle (\sigma'/\epsilon_o)\int_{\mathcal{V}} \Phi\delta(x-x')d^3x=\oint_{\mathcal{S}}\left(\Phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \Phi}{\partial n}\right) da$

Integration over $x$ gives

$\displaystyle -\frac{\sigma'}{\epsilon_o}\Phi(x')\int dydz=\oint_{\mathcal{S}}\left(\Phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \Phi}{\partial n}\right) da$

Of the six sides of the surface, $\Phi=0$ on all except the one in the $x=w$ plane for which the outward normal is $n=x$. So

$\displaystyle\oint_{\mathcal{S}}\Phi\frac{\partial \psi}{\partial n}da=\int V_o\left[\frac{\partial \psi_r}{\partial x}\right]_{x=w}dydz=V_o\int \left[-\frac{\sigma'}{\epsilon_o}\frac{x'}{w}\right]dydz=-V_o \frac{\sigma'}{\epsilon_o}\frac{x'}{w}\int dydz$

where $\psi_r=\frac{\sigma'}{\epsilon_o}\left(1-\frac{x}{w}\right)x'$ found in part 1. was used.

One could assert that we expect $\Phi$ to depend only on $x$, so $\frac{\partial \Phi}{\partial n}=0$ on the other four faces, for which $n=-y,y,-z,z$. Alternatively, one can use symmetry make the same conclusion:

----

The sides of $\mathcal{V}$ that are in the $x=0$ and $x=w$ plane have $\psi=0$, so two of the surface integrals of $\oint \psi\frac{\partial \Phi}{\partial n} da$ are zero. 

On the surface in the $y=0$ plane, $n = -y$, so we need to evaluate

$-\displaystyle \int_0^w\int_0^b \Psi(x,0,z)\frac{\partial \Phi}{\partial z}\Bigg|_{y=0}dxdz$

On the surface in the $y=b$ plane, $n = y$, so we need to evaluate

$\displaystyle \int_0^w\int_0^b \psi(x,b,z)\frac{\partial \Phi}{\partial z}\Bigg|_{y=b}dxdz$

Because the geometry is invariant with respect to $y$, the two partial derivatives are equal and the sum of these two surface integrals is zero. An idential argument can be made for the surfaces at $z=0$ and $z=b$.

----

All of the parts of the volume and surface integrals have not been evaluated and so equation 1.35 reduces to

$\displaystyle -\frac{\sigma'}{\epsilon_o}\Phi(x')\int dydz = -V_o \frac{\sigma'}{\epsilon_o}\frac{x'}{w}\int dydz$

or

$\displaystyle \Phi(x')=V_o\frac{x'}{w}$

In the problem statement $\Phi(x)$ was requested. In the above equation, we have $\Phi$ as a function of $x'$, which was a constant in the $\psi$ problem. Given that both $x'$ $0$ and $w$, we can find any value of $\Phi$ in this range by solving a problem with $x'$ set to that value. Thus, we can equivantly replace $x'$ with $x$ and so we have shown  

$\displaystyle \Phi(x)=V_o\frac{x}{w}$

## 1-D Spherical Green Function

Two conducting and grounded spherical shells of radius $b$ and $c$ are centered on the origin, and $c\gt b$.

A nonconducting spherical shell is centered on the origin and has a charge density of $\sigma'$ and radius $r'$, with $b \lt r' \lt c$.

1. Find $\psi_i(r)$, the potential between the inner conducting shell and the charged shell and $\psi_o(r)$, the potential between the charged shell and the outer conducting shell. (Read the subscript $i$ as "inner" and $o$ as "outer".)
2. Find the surface charge densities on the inner and outer conductor.
3. Verify that Gauss's law is satisfied for a Gaussian sphere centered on the origin and with a radius that is between the charged shell and the outer conducting shell.
2. Write the potential $\psi(r)$ for $b\le r\le c$ as a single function using $\psi_i$ and $\psi_o$ and the Heavyside step function $\Theta$.

**Solution**

1\.

Instead of starting with $\psi_i=A_i+B_i/r$ and $\psi_o=A_o+B_o/r$, we immediately write

$\displaystyle\psi_i=C_i\left(\frac{1}{r}-\frac{1}{b}\right)$ and $\displaystyle\psi_o=C_o\left(\frac{1}{r}-\frac{1}{c}\right)$

because we know the potential must have a $1/r$ dependence and the above two equations satisfy $\psi_i(b)=0$ and $\psi_o(c)=0$. What is left then is to use the conditions $\psi_i(r')=\psi_o(r')$ and $E_o(r')-E_i(r')=\sigma'/\epsilon_o$ to find the two unknows $C_i$ and $C_o$. The result is

$\displaystyle\psi_i=-\frac{\sigma'r'^2}{\epsilon_o}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)\left(\frac{1}{r}-\frac{1}{b}\right)$

$\displaystyle\psi_o=-\frac{\sigma'r'^2}{\epsilon_o}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)\left(\frac{1}{r}-\frac{1}{c}\right)$
 
Written in terms of the total charge $q'$ on the shell with charge density $\sigma'$ at $r=r'$, this is

$\displaystyle\psi_i=-\frac{q'}{4\pi\epsilon_o}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)\left(\frac{1}{r}-\frac{1}{b}\right)$

$\displaystyle\psi_o=-\frac{q'}{4\pi\epsilon_o}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)\left(\frac{1}{r}-\frac{1}{c}\right)$

As before, there is symmetry with respect to swapping the spatial coordinate $r$ with a parameter $r'$: $\psi_i(r,r')=\psi_o(r',r)$ (note that this is only after writing the potentials in terms of the charge on the shell at $r=r'$).

2\. From Gauss's law, near the surface of a conductor $\sigma=-\epsilon_o d\psi/dn$, where $n$ is in the direction perpendicular to the conductor and outwards. For the inner conductor, $n=r$; for the outer, $n=-r$. (Note that in Green's second identity, the convention is that $n$ is in the direction perpendicular to $\mathcal{V}$ and outwards.) Evaluation givves

$\displaystyle\sigma_i=-\frac{q'}{4\pi}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)\left[\frac{1}{b^2}\right]$

$\displaystyle\sigma_o=+\frac{q'}{4\pi}\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)\left[\frac{1}{c^2}\right]$

The charge induced on the inner and outer surface is

$\displaystyle q_i=-q'\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)$

$\displaystyle q_o=+q'\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)$

Checks:

1\. As $r'\rightarrow b$, $q_i\rightarrow -q'$ and $q_o\rightarrow 0$.

2\. As $r'\rightarrow c$, $q_i\rightarrow 0$ and $q_o\rightarrow -q'$.

3\. In HW #2.3.2, we found the charge induced when a point charge was at $r'$. We can use that answer and superposition to find the total charge induced if point charges are distributed uniformly on a sphere. This should match the total charge induced found in this problem. From #2.3.2, the answers were (with $r_o$ replaced with $r'$):

$\displaystyle q'_{r=b}=-\frac{q'b}{c-b}\left(\frac{c}{r'}-1\right)=-q'\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)$

$\displaystyle q'_{r=c}=+\frac{q'c}{c-b}\left(\frac{b}{r_o}-1\right)=+q'\left(\frac{1}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)$

The "superposition" argument requires a bit more justification. Consider two separate problems. In one problem there is $dq'$ at $(r',\theta',\phi')$; call the potential for this single $dq$ problem $\psi'(r,\theta,\phi;r',\theta',\phi')$. This potential will satisfy

$\nabla^2\psi'(r,\theta,\phi;r',\theta',\phi')=-dq'\delta(\mathbf{r}-\mathbf{r}')$ with $\psi'=0$ at $r=b$ and $\psi'=0$ at $r=c$

In another problem, there is $dq''$ at $(r',\theta'',\phi'')$; call the potential for this single $dq''$ problem $\psi(r,\theta,\phi;r'',\theta'',\phi'')$. This potential will satisy

$\nabla^2\psi''(r,\theta,\phi;r'',\theta'',\phi'')=-dq'\delta(\mathbf{r}-\mathbf{r}'')$ with $\psi''=0$ at $r=b$ and $\psi''=0$ at $r=c$

The sum $\psi' + \psi''$ satisfies

$\nabla^2(\psi'+\psi'')=-dq'\delta(\mathbf{r}-\mathbf{r}')-dq'\delta(\mathbf{r}-\mathbf{r}'')$ with $\psi'+\psi''=0$ at $r=b$ and $\psi'+\psi''=0$ at $r=c$

This argument can be extended for an arbitrary number of differential charges on a sphere of radius $r'$.

We can conclude that the sum of the potentials for isolated charges at any position on a surface of radius $r'$ and $r''$ satsifies Poisson's equation and the boundary conditions, which is the same condictions that we require for the combined charge problem. The charge density obeys superposition: $\sigma/epsilon_o = -d\psi/dn =  -(d\psi'/dn + d\psi''/dn)$ so that the charge densities on the conductors for two charge case is the sum of the charge densities for from each individual case.

Another way of justifying superposition is to note that for the isolated $dq'$ problem, the net force on the charges induced on the conductors is zero. If $dq''$ is introduced the net force on all of the induced charges will still be zero.

## Jackson Equation 1.42

Before stating Equation 1.42, Jackson (3rd edition) notes that with Equation 1.35 and 1.39, it is simple to obtain a generalization of Equation 1.36.

Show the "simple" steps need to arrive at Equation 1.42.

Be very careful with notation. You'll need to think a bit about the justification and validity of swapping $x$ and $x'$ and/or changing the dummy variable used in integration. When you do either of these, provide a justification so that I know you are not applying the "answer operator".


**Solution**

In [HW 3.1](#1-d-spherical-green-function), the use of Green's second identity resulted in a potential that depended on the primed variable because integration was performed over an unprimed area or volume. In that problem, an argument was given for why the prime variable could be simply replaced with the unprimed variable. In principle, one could always use the approach used in  [HW 3.1](#1-d-spherical-green-function) to find $\Phi(\mathbf{x}')$ and then make an argument for why $\Phi(\mathbf{x})$ is the equation for $\Phi(\mathbf{x}')$ with the prime removed. In this problem, we follow Jackson's logic for Equation 1.42 for which the result of integration is $\Phi(\mathbf{x})$, which depends on the unprimed variable.

Equation 1.35 is

$\displaystyle\int_V \left(\phi\nabla^2\psi -\psi\nabla^2\phi\right)d^3x=\oint_S\left(\phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \phi}{\partial n}\right) da$


Using, $\phi=\Phi(\mathbf{x})$, $\displaystyle\psi=G(\mathbf{x},\mathbf{x}')$, and $\displaystyle\nabla^2\Phi=-\frac{\rho}{\epsilon_o}$ gives

$\displaystyle\int_{\mathcal{V}} \left(\Phi(\mathbf{x})\nabla^2G(\mathbf{x},\mathbf{x}') + G(\mathbf{x},\mathbf{x}')\frac{\rho(\mathbf{x})}{\epsilon_o}\right)d^3x=\oint_{\mathcal{S}}\left(\Phi(\mathbf{x})\frac{\partial G(\mathbf{x},\mathbf{x}')}{\partial n}-G(\mathbf{x},\mathbf{x}')\frac{\partial \Phi(\mathbf{x})}{\partial n}\right) da$

We want the result after integration to depend on $\mathbf{x}$, so change the integration variable to be primed. The derivatives must also be changed to be primed and $G(\mathbf{x},\mathbf{x}')$ must be replaced with $G(\mathbf{x}',\mathbf{x})$.

$\displaystyle\int_{\mathcal{V}} \left(\Phi(\mathbf{x}')\nabla'^2G(\mathbf{x}',\mathbf{x}) + G(\mathbf{x}',\mathbf{x})\frac{\rho(\mathbf{x}')}{\epsilon_o}\right)d^3x'=\oint_{\mathcal{S}}\left(\Phi(\mathbf{x}')\frac{\partial G(\mathbf{x}',\mathbf{x})}{\partial n'}-G(\mathbf{x}',\mathbf{x})\frac{\partial \Phi(\mathbf{x}')}{\partial n'}\right) da'$

Equation 1.39,

$\displaystyle\nabla'^2G(\mathbf{x},\mathbf{x}')=-4\pi\delta(\mathbf{x}-\mathbf{x}')$

can be used to evaluate the first term in the volume integral, where the prime means the partial derivatives are taken with respect to primed coordinates. The first term evaluates to

$\displaystyle\int_{\mathcal{V}}\Phi(\mathbf{x}')\left(-4\pi\delta(\mathbf{x}-\mathbf{x}')\right)d^3x'=-4\pi\Phi(\mathbf{x})$

with this and rearrangement, we can write

$\displaystyle \Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\int_{\mathcal{V}}G(\mathbf{x}',\mathbf{x})\rho(\mathbf{x}')d^3x'+\frac{1}{4\pi}\oint_S\left(G(\mathbf{x}',\mathbf{x})\frac{\partial \Phi(\mathbf{x}')}{\partial n'}-\Phi(\mathbf{x}')\frac{\partial G(\mathbf{x}',\mathbf{x})}{\partial n'}\right) da'$

To get equation 1.42, one must justify

$G(\mathbf{x},\mathbf{x}')=G(\mathbf{x}',\mathbf{x})$

For a general function, say, $g(x,y) = xy^2$, $g(x,y) = xy^2\ne g(y,x) = yx^2$. Showing $G(\mathbf{x},\mathbf{x}')=G(\mathbf{x}',\mathbf{x})$ in general is non-trivial and Jackson problem 1.14 gives a suggestion for the proof, and a footnote on page 40 gives a reference of the proof for 1.14(b). So ideally one would have cited the statement on page 40 of Jackson to justify the use of $G(\mathbf{x},\mathbf{x}')=G(\mathbf{x}',\mathbf{x})$.

\newpage

# HW 4

## Green function for infinite dome

In class, I showed how to find the potential $\psi$ due to a point charge inside of a grounded, conducting, and closed dome when the radius of the dome is infinite. The potential was found using the method of images. (A dome is a hemisphere plus a cap.) 

Use this $\psi$ and equation 1.35 of Jackson (or equation 1.42; $\psi$ is proportional to a Green function) to find the potential $\Phi$ for the following problem:

An conducting dome has its base in the $x-y$ plane and the radius of the dome is infinite. There are no charges inside of the dome. The boundary of the dome is grounded except for the region between $x^2 + y^2 < b$, which is held at a potential of $V_o$.

1. Find the potential $\Phi(z)$ inside of the dome (the integral required to find $\Phi(x,y,z)$ requires an approximation of the integrand or numerical integration and will be considered in the future).
2. Find the potential $\Phi(z)$ inside of the dome when $b/z \ll 1$. Do this by Taylor series expanding $\Phi(z)$ for small $b/z$. Does the answer make sense?
3. Sketch the electric field lines inside of the dome.

Note that a related problem (but with a different Green function) considered in 2.6 of Jackson.

**Solution**

1\. The potential that satisfies the boundary conditions in the limit that that that the radius of the dome is much larger than $r'$ is

$\displaystyle\psi = \frac{kq}{\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}}-\frac{kq}{\sqrt{(x-x')^2+(y-y')^2+(z+z')^2}}$

This equation was derived using the method of images in class and is the same equation that solves the problem for a point charge at $\mathbf{x}'$ above an infinite grounded plane in the $x$-$y$ plane. $\psi$ satisfies the boundary conditions that when $z=0$, $\psi(x,y,0)=0$ and when $r'\gg r$, $\psi=0$ (showing the latter requires re--writing the denominators in terms of $r'$ and $r$).

Given that we are only interested in the potential along the $z$--axis, we can set $x'=y'=0$. (In 2.6 of Jackson, he does this after the integral required to find $\Phi(x,y,z)$ is found.) We then have

$\displaystyle\psi = \frac{kq}{\sqrt{x^2+y^2+(z-z')^2}}-\frac{kq}{\sqrt{x^2+y^2+(z+z')^2}}$

Green's second identity (Equation 1.35) with $\Phi$ in place of $\phi$ is

$\displaystyle\int_\mathcal{V} \left(\Phi\nabla^2\psi -\psi\nabla^2\Phi\right)d^3x=\oint_\mathcal{S}\left(\Phi\frac{\partial \psi}{\partial n}-\psi\frac{\partial \Phi}{\partial n}\right) da$

In this problem $\mathcal{V}$ is the volume of the dome and $\mathcal{S}$ has two surfaces -- a large disk in the $x$--$y$ plane and the curved part of the dome.

The Laplacian of $\psi$ can be written down by inspection. The charge density is that for point charges at $(x,y,z)=(0,y,\pm z')$, so

$\displaystyle\nabla^2\psi=-\frac{q}{\epsilon_o}\big[\delta(x)\delta(y)\delta(z-z')+\delta(x)\delta(y)\delta(z+z')\big]$


$\displaystyle\int_\mathcal{V} \Phi\nabla^2\psi d^3x=-\frac{q}{\epsilon_o}\int_\mathcal{V} \Phi\big[\delta(x)\delta(y)\delta(z-z')+\delta(x)\delta(y)\delta(z+z')\big]d^3x$

$\delta(z+z')$ is zero in $\mathcal{V}$ because $z$ and $z'$ are positive in $\mathcal{V}$. The integral simplifies to  

$\displaystyle\int_\mathcal{V} \Phi\nabla^2\psi d^3x=-\frac{q}{\epsilon_o}\int_\mathcal{V} \Phi \delta(x)\delta(y)\delta(z-z')d^3x=-\frac{q}{\epsilon_o}\Phi(0,0,z')=\frac{q}{\epsilon_o}\Phi(z')$.

Inside $\mathcal{V}$, we were given that there are no charges, so $\nabla^2\Phi=0$. Therefore, the left-hand side of Equation 1.35 reduces to $-(q/\epsilon_o)\Phi(z')$.

On $\mathcal{S}$, $\psi=0$, so the second surface integral is zero. We are left with

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=\oint_\mathcal{S}\Phi\frac{\partial \psi}{\partial n} da$

The surface is composed of the two parts -- the curved part and its base. On the curved part, $\Phi=0$ was given. On the base, $\Phi=0$ for $x^2+y^2\lt b^2$ and $\Phi=V_o$ otherwise. As a result, the surface integral reduces to

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=\int_\mathcal{x^2+y^2\lt b^2}V_o\frac{\partial \psi}{\partial n} da$.

In cylindrical coordinates, we have

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=V_o\int_{0}^{2\pi}\int_0^b\frac{\partial \psi}{\partial n} sdsd\phi$

The outward normal to $\mathcal{V}$ is -$z$, so

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=-V_o\int_{0}^{2\pi}\int_0^b\frac{\partial \psi}{\partial z} sdsd\phi$

What remains is to evaluate the partial derivative (and recall that ${\partial \psi}/{\partial z}$ in the integral means ${\partial \psi}/{\partial z}|_{\text{on }\mathcal{S}}$). In this problem, "$\text{on }\mathcal{S}$" corresponds to $z=0$.)

$\displaystyle\frac{\partial \psi}{\partial z}\Bigg|_{z=0}=2kq\frac{z'}{\sqrt{s^2+z'^2}^3}$

Evaluation of the integral gives

$\displaystyle -\frac{q}{\epsilon_o}\Phi(z')=-4\pi kqV_o\left[\frac{z'}{|z'|}-\frac{z'}{\sqrt{b^2+z'^2}}\right]$

Cancelling constants and using $z'/|z'|=1$ for $z'\gt 0$ gives

$\displaystyle \Phi(z')=V_o\left[1-\frac{z'}{\sqrt{b^2+z'^2}}\right]$

Using the same arguments used in [HW 3.1](#1-d-cartesian-green-function), we can replace $z'$ with $z$, leaving

$\displaystyle \Phi(z)=V_o\left[1-\frac{z}{\sqrt{b^2+z^2}}\right]$

2\. The solution can also be written (for $z>0$) as

$\displaystyle \Phi(z)=V_o\left[1-\frac{1}{\sqrt{1+\frac{b^2}{z^2}}}\right]$

Using [the binomial expansion](https://rweigel.github.io/phys305/binomial_expansion.html), 

$\displaystyle \Phi(z)=V_o\left[1-\left(1-\frac{1}{2}\left(\frac{b}{z}\right)^2 + ... \right)\right]$

To lowest order in $b/z$, 

$\displaystyle \Phi(z) \simeq \frac{V_o}{2}\left(\frac{b}{z}\right)^2 \qquad z\gg b$

For large $z$, the (positive) charge on the disk appears as a point charge at the origin. As a result, we may expect that the potential will fall off as $1/z$. Here the potential falls off more slowly. The reason is that there is also a contribution from the negative charges in the plane for $s\gt b$. As a result, for large $z$, the system appears to have zero charge at the origin and so there is no $1/z$ term. (The interpretation of the power series expansion of potential will be covered in more detail later.)

3\. This was discussed in class. In general, it is easiest to draw equipotential lines starting with one near the boundary. Then, draw electric field lines that are perpendicular to the equipotential lines.

## 2--D Cartesian Boundary Value Problem

Review Griffiths 3.3.1 (3rd and 4th edition). You should be able to quickly derive the potential for Figure 3.20 (3rd and 4th edition) when any one of the sides is at $V_o$ and the other three are grounded. See also [my PHYS 305 notes](https://rweigel.github.io/phys305/boundary_value_problems.html).

Suppose the sides of Figure 3.20 of Griffiths 3rd or 4th edition are held at $V_l$, $V_r$, $V_t$, and $V_b$, where $l=$left, $r=$right, $t=$top, and $b=$bottom. Find the potential inside the rectangular pipe.

Hints:

1. The total potential will be the the sum of the potentials from four different problems (1)
 $V_l$ non--zero and all other sides zero, (2) $V_r$ non--zero and all other sides zero, etc. I will ask you to explain why in class.
2. You can build the solution to three of the four problems described in the first hint using a transformation of coordinate system and the solution to one of the problems.

**Solution**

_Note: Diagram and solution below assumes width is $b$ and height is $a$. Diagram in Griffiths has width of $2b$ and height of $2a$._

The potential inside of the long (in $z$ direction) duct with cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

is

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

The geometry for the $V_l$ case is

<img src="figures/square_duct2.svg"/>

The choice of coordinate system for $I.$ was arbitrary and we can translate the duct used for $I.$ to the left by $b/2$ and down by $a/2$ so that the position of the duct is the same as that in Figure 3.20 of Griffiths.

This is effected by replacing $x$ with $x+b/2$ and $y$ with $y+a/2$ in $I.$:

$\qquad\displaystyle \psi_l(x,y)=\frac{4V_l}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b/2-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi (y/a-1/2))$

Check: When $y=\pm a/2$, $\psi_l=0$ and when $x=b/2$, $\psi_l=0$.

To find $\psi_r$, replace $x$ with $-x$ and $V_l$ with $V_r$ in the equation for $\psi_l$:

$\qquad\displaystyle \psi_r(x,y)=\frac{4V_r}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b/2+x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi (y/a-1/2))$

Check: When $y=\pm a/2$, $\psi_r=0$ and when $x=-b/2$, $\psi_l=0$.

To find $\psi_t$, swap $a$ and $b$, $x$ and $y$, and $V_r$ with $V_t$  in the equation for $\psi_r$:

$\qquad\displaystyle \psi_r(x,y)=\frac{4V_t}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (a/2+y)/b]}{n\sinh(n\pi a/b)}\right)\sin(n\pi (x/b-1/2))$

Check: When $x=\pm b/2$, $\psi_t=0$ and when $y=-a/2$, $\psi_t=0$.

To find $\psi_t$, replace $y$ with $-y$, and $V_t$ with $V_b$ in the equation for $\psi_t$:

$\qquad\displaystyle \psi_b(x,y)=\frac{4V_b}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (a/2-y)/b]}{n\sinh(n\pi a/b)}\right)\sin(n\pi (x/b-1/2))$

Check: When $x=\pm b/2$, $\psi_t=0$ and when $y=a/2$, $\psi_t=0$.

The total potential can be written as

$\psi = \psi_l+\psi_r+\psi_t+\psi_b$

This potential satisifes Laplaces's equation and the boundary conditions for the case where all four sides are at a different potential.

## 2--D Spherical Boundary Value Problem

In 2.7 of Jackson 3rd edition, he solves for the potential outside of a sphere with hemispheres held at $\pm V$ using a Green function. In example 3.7 of Griffiths 4th edition (example 3.6 in 3rd edition), he describes how to solve for the potential outside of a sphere with a potential of $V(\theta)$ on its surface. As a result, Jackson's example is related to Griffiths' example.

Study these two examples and be prepared to answer questions (such as how they are related) about them in class.

\newpage

# HW 5

## Limit Check

The potential inside of the long (in $z$ direction) duct with cross-section is shown in the following figure

<img src="https://rweigel.github.io/phys305/figures/Boundary_Value_Problems_2D_Left.svg"/>

can be written as

$I.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)$

In Example 3.3 of Griffiths, he finds the potential for a long duct with one open face. The diagram for that example is similar to the above except there is no conductor on the right side and $b=\infty$. The solution he finds is

$II.\qquad\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\frac{e^{-n\pi x/a}}{n}\sin(n\pi y/a)$

1\. Show that the infinite $b$ solution ($II.$) matches the finite $b$ solution ($I.$) in the limit that $a/b \ll 1$. (You do not need to derive $I.$ or $II.$, but should be able to.)

2\. In the limit that $b/a \ll 1$, it would seem that near the center of the duct ($y=a/2$), the system appears as two infinite parallel conducting plates held at different potentials, which is a 1-D problem solved before. Show that in the limit $b/a \ll 1$, equation $I.$ reduces to the solution for an infinite conducting plate in the $x=0$ plane held at $V_o$ and a grounded infinite conducting plate in the $x=b$ plane. (You'll need to use $e^u\simeq 1 + u$ for $u\ll1$ multiple times and also the [Gregory and Leibniz formula for $\pi$](https://mathworld.wolfram.com/PiFormulas.html)).

**Solution**

1\. We need to show that 

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}$ reduces to $\displaystyle e^{-n\pi x/a}$ when $a/b\ll 1$, or, equivalently, $b/a \gg 1$

Re-writing the numerator and denominator in terms of exponentials

$\sinh[n\pi (b-x)/a]=\frac{1}{2}\left(e^{n\pi (b-x)/a}-e^{-n\pi (b-x)/a}\right)=\frac{1}{2}e^{n\pi b/a}\left(e^{-n\pi x/a}-e^{-2n\pi b/a}e^{n\pi x/a}\right)$

$\sinh(n\pi b/a)=\frac{1}{2}\left(e^{n\pi b/a}-e^{-n\pi b/a}\right)=\frac{1}{2}e^{n\pi b/a}\left(1-e^{-2n\pi b/a}\right)$

gives

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}=\frac{e^{-n\pi x/a}-e^{-2n\pi b/a}e^{n\pi x/a}}{1-e^{-2n\pi b/a}}$

In the numerator, the term $e^{-2n\pi b/a}e^{n\pi x/a} \rightarrow 0$ as $b/a \rightarrow \infty$ for $x=[0,b]$.

In the denominator, the term $e^{-2n\pi b/a}\rightarrow 0$ as $b/a \rightarrow \infty$.

As a reuslt, the ratio approaches $\displaystyle e^{-n\pi x/a}$ as expected.

2\. We need to show that near $y=a/2$, the sum in $II.$ approaches $\frac{\pi}{4}(1-x/b)$ so that $V(x,a/2)\rightarrow V_o(1-x/b)$.

In the middle of the duct, $y=a/2$ so we replace $\sin(n\pi y/a)$ with 
$\sin(n\pi/2)=(-1)^{n}$ for $n=1,3,...$. Using $\sinh x=(e^x-e^{-x})/2$ and $e^x\simeq 1-x$ for $x\ll 1$ gives

$\displaystyle\frac{\sinh[n\pi (b-x)/a]}{\sinh(n\pi b/a)}\simeq \frac{1+n\pi(b-x)/a - (1-n\pi(b-x)/a)}{1+n\pi b/a-(1-n\pi b/a)}=1-\frac{x}{b}$

We are left with

$\displaystyle V(x,y)=\frac{4V_o}{\pi}\sum_{n=1,3,...}^\infty\left(\frac{\sinh[n\pi (b-x)/a]}{n\sinh(n\pi b/a)}\right)\sin(n\pi y/a)\simeq \frac{4V_o}{\pi}\left(1-\frac{x}{b}\right)\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}$

From [mathworld.wolfram.com](https://mathworld.wolfram.com/PiFormulas.html),

$\frac{\pi}{4}=\sum_{k=1}^\infty \frac{(-1)^{k+1}}{2k-1}$

Using $n=2k-1$, we can re-write this as 

$\frac{\pi}{4}=\sum_{n=1,3,...}^\infty \frac{(-1)^{(n+3)/2}}{n}$

Finally, for $n=1,3,...$, $(-1)^{(n+3)/2}=1,-1,1,...=(-1)^{n}$ and so

$\frac{\pi}{4}=\sum_{n=1,3,...}^\infty \frac{(-1)^{(n+3)/2}}{n}=\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}$

Thus,

$\displaystyle V(x)\simeq \frac{4V_o}{\pi}\left(1-\frac{x}{b}\right)\sum_{n=1,3,...}^\infty \frac{(-1)^{n}}{n}=\frac{4V_o}{\pi}\frac{\pi}{4}\left(1-\frac{x}{b}\right)=V_o\left(1-\frac{x}{b}\right)$

## Long Rectangular Duct with Sheet of Charge 

An infinitely long, hollow, and conducting duct is parallel to the $z$-axis and has sides bounded by $0\le x \le 1$ and $0\le y\le 1$. All sides are grounded. An infinitely long non-conducting sheet of charge with surface charge density $\sigma'$ is in the $x=x'$ plane between $y=0$ and $y=1$. See the left part of the figure below.

<img src="figures/square_duct.svg"/>

1\. Find equations $\psi_l(x,y)$, the potential for $x\lt x'$, and $\psi_r(x,y)$, the potential for $x\gt x'$. Based on the discussion in class, we can easily write down equations for $\psi_l$ and $\psi_r$ that are zero on the conducting walls:

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

where $n$ is an integer, matches the boundary conditions on the walls of the conductor. You need to find $A_n$ and $B_n$ such that the two conditions

$\psi_l(x',y)=\psi_r(x',y)$

and

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

are satisfied.

2\. Write a single equation for the potential $\psi(x,y)$ using $\psi_l$, $\psi_r$, and the Heavyside step function $\Theta$.

The Green function is $G=(4\pi\epsilon_o/A\sigma')\psi$, where $A=\int_0^1dy\int_{0}^L dz$ and $L$ is the length of the duct. (You may want to verify this.)

3\. Use $\psi(x,y)$ and Green's second identity (Equation 1.35 of Jackson), or equivalently, the Green function stated above and equation 1.42 of Jackson to find the potential when the duct is filled with a nonconducting material with a uniform charge density $\rho_o$ as shown in the right part of the figure above.

----

Note: In problem 2.15 of Jackson, he gives the Green function for the case where a line of charge parallel to the $z$-axis passes through $(x,y)=(x',y')$. That problem is a bit more complicated than the problem considered here. In problem 2.16, of Jackson, he states the result of using the Green function from problem 2.15 to find the potential for the configuration in part 3. above.

----

**Solution**

1\. Both

$\psi_l=\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$

and

$\psi_r=\sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x-1))$

satisfy $\partial^2 \psi/\partial^2 x+\partial^2 \psi/\partial^2 y=0$ and the boundary conditions

$\psi_l(0,y)=0 \quad \psi_l(x,0)=0 \quad \psi_l(x,1)=0$

$\psi_r(1,y)=0 \quad \psi_r(x,0)=0 \quad \psi_r(x,1)=0$

The equations for $\psi_l$ and $\psi_r$ could have been derived using the above six boundary equations and starting with 

$\psi_l=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[A_n\sinh(n\pi x)+a_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\sin(n\pi y)\Big[B_n\sinh(n\pi x)+b_n\cosh(n\pi x)\Big]$

or most generally

$\psi_l=\sum_{n=0}^{\infty}\Big[A^l_n\sin(n\pi y)+B^l_n\cos(n\pi y)\Big]\Big[C^l_n\sinh(n\pi x)+D^l_n\cosh(n\pi x)\Big]$

$\psi_r=\sum_{n=0}^{\infty}\Big[A^r_n\sin(n\pi y)+B^r_n\cos(n\pi y)\Big]\Big[C^r_n\sinh(n\pi x)+D^r_n\cosh(n\pi x)\Big]$

However, the result will be the same. In problems such as these, it is often easier to reason out what the form of the solution will be rather than starting from the most general equation. In this case, we need the $\sin$ solution in the $y$ direction because it can have zeros at two locations. The $\sinh(n\pi(x-1))$ term is justified because we know that $A\sinh x$ and $B\cosh x$ can be combined into a $C\sinh (x + \delta)$ with a "phase" shift $\delta$.

The continuity condition

$\psi_l(x',y)=\psi_r(x',y)$

gives

$\sum_{n=0}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x') = \sum_{n=0}^{\infty}B_n\sin(n\pi y)\sinh(n\pi(x'-1))$

It follows that

$\displaystyle B_n = \frac{\sinh(n\pi x')}{\sinh(n\pi(x'-1))}A_n$

The jump condition

$\displaystyle\left[-\frac{\partial \psi_r}{\partial x}+\frac{\partial \psi_l}{\partial x}\right]_{x=x'}=\frac{\sigma'}{\epsilon_o}$

gives

$\displaystyle\sum_{n=0}^{\infty}(n\pi)\sin(n\pi y)\Big[- B_n\cosh(n\pi(x'-1))+A_n\cosh(n\pi x')\Big]=\frac{\sigma'}{\epsilon_o}$

The term in square brackets

$-B_n\cosh(n\pi(x'-1)) + A_n\cosh(n\pi x')$

rewritten using the continuity relationship $B_n = A_n\sinh(n\pi x')/\sinh(n\pi(x'-1))$ is

$\displaystyle A_n\left[\cosh(n\pi x')-\frac{\sinh(n\pi x')\cosh(n\pi(x'-1))}{\sinh(n\pi(x'-1))}\right]$

or

$\displaystyle A_n\frac{\sinh(n\pi(x'-1))\cosh(n\pi x')-\sinh(n\pi x')\cosh(n\pi(x'-1))]}{\sinh(n\pi(x'-1))}$

The numerator simplifies to $\sinh(-n\pi)=-\sinh(n\pi)$. This can be seen by expanding the hyperbolic functions as exponentials or using the identity

$\sinh(\alpha-\beta)=\sinh(\alpha)\cosh(\beta)-\sinh(\beta)\cosh(\alpha)$

with $\alpha = n\pi (x' - 1)$ and $\beta = n\pi x'$.

The continuity condition equation thus simplifies to

$\displaystyle\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\sigma'}{\epsilon_o}$

Multiplication of this by $\sin(l\pi y) dy$ and integration from $y=0$ to $1$ and using

$\displaystyle\int_0^1\sin(l\pi y)\sin(n\pi y) dy=0\qquad\mbox{ for }l\ne n$

$\displaystyle\int_0^1\sin(l\pi y)\sin(n\pi y) dy=\frac{1}{2}\qquad\mbox{ for }l=n$

$\displaystyle\int_0^1\sin(l\pi y) dy=\frac{2}{l\pi}\quad\mbox{ for }l=1, 3, 5, ...$

gives (after changing the dummy index from $l$ to $n$),

$\displaystyle A_n = - \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{\sinh(n\pi(x'-1))}{\sinh(n\pi)}$

$\displaystyle B_n = - \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{\sinh(n\pi x')}{\sinh(n\pi)}$

for $n=1, 3, 5, ...$ and $A_n=B_l=0$ for $n = 2, 4, ...$.

$\boxed{\displaystyle \psi_l(x,x') = -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(x'-1))\sinh(n\pi x)\sin(n\pi y)}$

$\boxed{\displaystyle \psi_r(x,x')= -\sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi x')\sinh(n\pi (x-1))\sin(n\pi y)}$

or, using $-\sinh(x)=\sinh(x)$ and defining $x_{\lt}$ to the the smaller of $x$ and $x'$ and $x_{\gt}$ to the the larger of $x$ and $x'$,

$\displaystyle\psi(x,x') =  \sum_{n=1,3,...}^{\infty} \frac{4\sigma'}{n^2\pi^2\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi(1-x_{\gt}))\sinh(n\pi x_{\lt})\sin(n\pi y)$

or, in terms of $\Theta$,

$\displaystyle\psi(x,x') = \psi_l\Theta(x'-x)+\psi_r\Theta(x-x')$

----

2.Using $G(x)=(4\pi\epsilon_o/A\sigma')\psi(x)$ gives

$\displaystyle G(x,x') = \frac{4\pi\epsilon_o}{A\sigma'}\Big[\psi_l(x,x')\Theta(x'-x)+\psi_r(x,x')\Theta(x-x')\Big]$

----

3\. The surface integral in equation 1.44 of Jackson is zero (why?) leaving 

$\displaystyle\Phi(\mathbf{x}) = \frac{1}{4\pi\epsilon_o}\int_{\mathcal V} G(\mathbf{x},\mathbf{x}') \rho(\mathbf{x}')d^3x'$

$G$ does not depend on $y'$ or $z'$ and $\rho=\rho_o=const$, so integration over $y$ and $z$ gives

$\displaystyle\Phi(x) = \frac{\rho_oA}{4\pi\epsilon_o}\int_0^1 G(x,x') \thinspace dx'$

where $A$ is as defined in the problem statement. Using $G$ from part 2. gives

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_0^1  \Big[\psi_l(x,x')\Theta(x'-x)+\psi_r(x,x')\Theta(x-x')\Big]\thinspace dx'$

The step function modifies the limits of integration, so

$\displaystyle\Phi(x) = \frac{\rho_o}{\sigma'}\int_x^1  \psi_l(x,x')\thinspace dx'+\frac{\rho_o}{\sigma'}\int_0^x  \psi_r(x,x')\thinspace dx'$

The interpretation of this equation is that to find the potential at $x$,  sum over the potential due to differential sheets at different $x'$. The first integral is the potential just to the left of all differential sheets to the right of $x$. The second integral is the potential just to the right of all differential sheets to the left. This is the equation you would probably write down in order to compute the potential due to a slab if you did not know about Green functions -- the total potential is simply the sum of potentials due to all differential sheets.

The first integral requires the integration

$\displaystyle\int_x^1\sinh(n\pi(x'-1))\thinspace dx'=\frac{\cosh(0)-\cosh(n\pi(x-1))}{n\pi}$

The second integral requires the integration

$\displaystyle\int_0^x\sinh(n\pi x')\thinspace dx'=\frac{\cosh(n\pi x)-\cosh(0)}{n\pi}$

Using these, evaluation of the integrals gives

$\displaystyle\Phi(x) =-\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty}  \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\thickspace\Large{\times}
$

$\Big[\sinh(n\pi x)(1-\cosh[n\pi (x-1)])+\sinh[n\pi(x-1)](\cosh(n\pi x)-1))\Big]
$

Using again $\sinh(\alpha-\beta)=\sinh(\alpha)\cosh(\beta)-\sinh(\beta)\cosh(\alpha)$

with $\alpha=n\pi(x-1)$ and $\beta=n\pi$

$\displaystyle\Phi(x) = -\frac{4}{\epsilon_o\pi^3}\sum_{n=1,3,5,...}^{\infty} \frac{\sinh(n\pi y)}{n^3\sinh(n\pi)}\Big[-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]\Big]$

To combine $\sinh(n\pi x)+\sinh[n\pi(x-1)$ into one term, note that when expanded in terms of exponentials the following sum has four terms

$\sinh(u)+\sinh(u-1) = \frac{1}{2}\left(e^u-e^{-u}+e^{u-1}+e^{-(u-1)}\right)$

The following product has four terms

$\cosh\alpha\sinh\beta = \frac{1}{4}\left(e^{\alpha+\beta}-e^{-(\alpha+\beta)}+e^{\alpha-\beta}-e^{-(\alpha-\beta)}\right)$

Setting $\alpha + \beta = u$ and $\alpha-\beta=u-1$

gives $\alpha = u-1/2$ and $\beta=1/2$. Thus

$\displaystyle\sinh(n\pi x)+\sinh[n\pi(x-1)] = 2\cosh[n\pi(x-1/2)]\sinh(n\pi/2)$

and

$\displaystyle\frac{-\sin(n\pi)+\sinh(n\pi x)+\sinh[n\pi(x-1)]}{\sinh(n\pi)}=\Big[-1+\frac{\sinh(n\pi/2)}{\sinh(n\pi)}2\cosh[n\pi(x-1/2)]\Big]$

Finally, using

$\displaystyle\sin(2x)=2\cosh(x)\sinh(x) \Rightarrow \sinh(x)=2\cosh(x/2)\sinh(x/2)$

gives 

$\displaystyle\frac{\sinh(x/2)}{\sinh(x)}=\frac{1}{2\cosh(x/2)}$

and the final result of

$\displaystyle\Phi = \frac{4}{\pi^3\epsilon_o}\sum_{n=1,3,...}^{\infty}\frac{\sin(n\pi y)}{n^3}\left[1-\frac{\cosh[n\pi(x-1/2)]}{\cosh(n\pi/2)}\right]$

Defining $m = (n-1)/2$ gives the result of problem 2.16 of Jackson.

## 2-D Cylindrical Boundary Value Problem

A non-conducting and infinitely long cylindrical shell of radius $b$ has a surface charge density of $\sigma=\sigma_2\sin\thinspace2\phi$. 

1. Find $\psi(s,\phi)$ using the boundary value method. Note that the general solution to Laplace's equation in cylindrical coordinates for a problem with no $z$ dependence is

   $\psi=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi) s^n+a_o\ln s+\sum_{n=1}^\infty (a_n\cos n\phi+b_n \sin n\phi)s^{-n}$

2. Repeat 1. assuming $\sigma=\sigma_o + \sigma_2\sin\thinspace2\phi$. In this case, the $\ln s$ term cannot be dropped for the $s>b$ solution; $a_o$ is determined from the requirement that for large $s$, the potential should be that for a line of charge with linear density $\lambda$ that is the average of $\sigma$ over $\phi$.

%In class, I did the a problem for $\sigma=\sigma_o\cos\thinspace\phi$. In justifying dropping the $\rho^n$ and $\ln\rho$ terms, I mentioned that this was justified because the potential should go to zero as $\rho\rightarrow \infty$. What I neglected to mention is that this is because for large $\rho$, the system appears as a line of charge with linear charge density, $\lambda$, and $\lambda=0$ for the given $\sigma$. This can be seen by computing the linear charge density $\lambda = \int_0^{2\pi} \sigma b d\phi$.

**Solution**

I'll solve part 2., which reduces to part 1. if $\sigma_o=0$. I will also solve this the long way. After solving this problem the long way, you should be able to identify short--cuts, one of which is find the potnential due to a long and uniformly charged cylinder and adding the result to the answer of part 1.

We can conclude that the $ s ^n$ terms are zero for the potential outside of the cylinder because at large $ s $ the cylinder will be approximately that for a line of charge, for which potential will be proportional to $\overline{\lambda}\ln s $ for large $ s $, where $\overline{\lambda}$ is the azimuthally averaged surface charge density: $\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$. That is, for large $ s $, the potential should be the same as that when all of the charge on the cylinder is collapsed onto a line, for which the potential is $\psi=const-(\overline{\lambda}/2\pi\epsilon_o)\ln s $, giving $a_o=-\overline{\lambda}/2\pi\epsilon_o$ and $A_o=const$. The constant $A_o$ is determined by defining a reference potential $V_r$ at a reference point $s_r$. For example, if $\psi( s _r)=V_r$, then $V_r=A_o-\overline{\lambda}\ln s _r/2\pi\epsilon_o$ and the terms $A_o+a_o\ln s $ combine to form

$A_o+a_o\ln s =V_r-(\overline{\lambda}/2\pi\epsilon_o)\ln( s / s _r)$

----
**Note** For a line of charge, we can't choose a reference potential to be zero at infinity. This is related to the problem that arises if one attempts to use $V=\frac{1}{4\pi\epsilon_o}\int {dq}/{|\mathbf{r}-\mathbf{r'}|}$ to compute the potential for an infinite line of charge. The derivation of this integral assumes that the potential is zero at large $\mathbf{r}$. Using Gauss' law, one can show that this is not the case -- $E_{ s }=\frac{\lambda}{2\pi\epsilon_o}\frac{1}{ s }$ and so $\psi =  \psi_o  - \frac{\lambda}{2\pi\epsilon_o}\ln s $, where $ \psi^o $ is a constant. We can't choose $\psi( s =\infty)=0$ because it gives $ \psi_o =-\infty$. So to compute the potential for an infinite line of charge, one must either use the integral equation for the electric field or Gauss' law. See also 2.3.4 of Griffiths where he notes that the integral diverges for a charge distribution that extends to infinity.

----


Outside the cylinder, the general form is then

$ \psi^o =A_o'+a_o\ln s +\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi) s ^{-n}$

I've kept the $\ln s $ term. In the following, I'll show how the values of $A_o'$ and $a_o$ given above follow from an alternative argument than the one given above. 

Inside the cylinder, the potential should be finite and so the $\ln s $ and $ s ^{-n}$ terms are dropped. (If the cylinder had a constant charge density, we would expect the potential to be constant inside of the cylinder and would keep only the $A_o$ term.)

Inside the cylinder, the general form is then

$\displaystyle\psi^i=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi) s ^n$

The two boundary conditions are

$\psi^o (b,\phi)= \psi^i(b,\phi)$ and $\displaystyle \left[\partial  \psi^o /\partial  s -\partial  \psi^i/\partial  s \right]_{ s =b}=-\sigma/\epsilon_o$

(Make sure that you know how to derive the second boundary condition.)

The boundary condition $\psi^o (b,\phi)= \psi^i(b,\phi)$ gives

$\displaystyle A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\sin n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\sin n\phi)b^n$

This equation gives

$A_o'+ a_o\ln b = A_o$

and

$\displaystyle A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$

from "matching terms", which means integrating both sides by either $\cos n'\phi\thinspace d\phi$ or $\sin n'\phi\thinspace d\phi$, with $n'$ being an integer greater than zero, and integrating from $\phi=0$ to $2\pi$ and using 

$\displaystyle\int_0^{2\pi}\cos n\thinspace d\phi = 0;\qquad\displaystyle\int_0^{2\pi}\sin n\thinspace d\phi = 0;\qquad\displaystyle\int_0^{2\pi}\cos n'\phi\sin n\phi\thinspace d\phi = 0$

$\displaystyle\int_0^{2\pi}\cos n'\phi\cos n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$

$\displaystyle\int_0^{2\pi}\sin n'\phi\sin n\phi\thinspace d\phi = 0\text{ if } n'\ne n\text{ and } \pi \text{ if } n'=n$


Notice that in cylindrical problems we integrate over $\phi$, so the limits of integration are from $0$ to $2\pi$. In contrast, in spherical problems with a $\theta$ dependence, we integrate from $0$ to $\pi$.

To determine the relationship between the coefficients quoted above, it is often easier to write out the first few terms in the sums

$A_o'+a_o\ln b+\sum_{n=1}^\infty (a_n\cos n\phi+b_n\cos n\phi)b^{-n}=A_o+\sum_{n=1}^\infty (A_n\cos n\phi+B_n\cos n\phi)b^n$

in alignment as

$$
\begin{align*}
&& A_o'+a_o\ln b &&+ && (a_1\cos \phi+b_1\sin \phi)b^{-1} &&+ && (a_2\cos 2\phi+b_2\sin 2\phi)b^{-2}  && +&& ... && \\
= && A_o && + && (A_1\cos \phi+B_1\sin \phi)b^{1} &&+ && (A_2\cos 2\phi+B_2\sin 2\phi)b^{2} && +&& ... &&
\end{align*}
$$

and then read off the matching terms

$A_o'+a_o\ln b = A_o$

$a_1/b = A_1b\quad b_1/b = B_1b$

$a_2/b^2 = a_2b^2\quad b_2/b^2 = B_2b^2$

$a_3/b^3 = a_3b^2\quad b_3/b^3 = B_3b^2$

$...$

in order to conclude the general result stated earlier of

$A_o'+ a_o\ln b = A_o$

$A_n=a^{-2n}a_n\quad\quad B_n=a^{-2n}b_n\quad\quad n\ge 1$

The boundary condition

$\displaystyle\left[\partial  \psi^o /\partial  s -\partial  \psi^i/\partial  s \right]_{ s =b}=-\sigma/\epsilon_o$

gives

$$
\begin{align*}
&& a_o/b &&  - &&(a_1\cos \phi+b_1\sin \phi)b^{-2} &&-&&2(a_2\cos 2\phi+b_2\sin 2\phi)b^{-3} &&+ &&... \\
&&           && - && (A_1\cos \phi+B_1\sin \phi) &&-&& 2(A_2\cos 2\phi+B_2\sin 2\phi)b^{1} &&+&& ... &&\\
=&& -(\sigma_o/\epsilon_o)&& && && && -(\sigma_2/\epsilon_o)\sin\thinspace2\phi
\end{align*}
$$

This gives

$a_o/b=-\sigma_1/\epsilon_o$

$-a_1/b^2-A_1=0\quad -b_1/b^2-B_1=0$

$-2a_2/b^3-2A_2b = 0\quad -2b_2/b^3-2B_2b = -\sigma_2/\epsilon_o$

$-3a_3/b^4-3A_3b^2 = 0\quad -3b_3/b^4-3B_3b^2 = 0$

$...$

The equation $a_o=-b\sigma_o/\epsilon_o$ from the second boundary condition combines with $A_o'+a_o\ln b = A_o$ from the first boundary condition to give

$A_o=A_o'-(b\sigma_o/\epsilon_o)\ln b$

The equation $a_1/b = A_1b$ from the first boundary condition combines with $-a_1/b^2-A_1=0$ from the second boundary condition to give

$2A_1=0$

which is only possible if $A_1=0$.  Similarily, all terms except $b_2$ and $B_2$ are zero.

The equation $b_2/b^2 = B_2b^2$ from the first boundary condition and $-2b_2/b^3-2B_2b = -\sigma_o/\epsilon_o$ combine to give

$B_2=+\sigma_2/4b\qquad\qquad b_2=b^3\sigma_2/4$

The final result is

$\displaystyle\psi^i=A_o'-(b\sigma_o/\epsilon_o)\ln b+\frac{\sigma_2}{4\epsilon_0}\frac{ s ^2}{b}\sin 2\phi$

$\displaystyle\psi^o =A_o'-(b\sigma_o/\epsilon_o)\ln  s +\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi$

If the reference potential is chosen to be zero at $ s =0$, then $A_o'=(b\sigma_1/\epsilon_o)\ln b$ and

$\boxed{\displaystyle\psi^i=\frac{\sigma_2}{4\epsilon_0}\frac{ s ^2}{b}\sin 2\phi}$

$\boxed{\displaystyle\psi^o =(b\sigma_o/\epsilon_o)\ln (b/ s )+\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi}$

(In this problem, the reference potential was not given intentionally. Ideally you recognized that a reference potential was needed to fully specify the solution. Also note that we cannot specify a constant reference potential at any other $s$ because the potential depends on $\phi$.)

*Note*: Inspection of this answer suggests a faster way of solving the general problem of

$\sigma_o + \sigma_1\sin \phi + \sigma_2\sin 2\phi + ...$

or more generally,

$\sigma_o + \sigma_{1s}\sin \phi + \sigma_{1c}\cos\phi + \sigma_{2s}\sin 2\phi + \sigma_{2c}\cos 2\phi + ...$

First find the potential due to $\sigma_o$. Then, write $\psi^i$ and $\psi^o$ not as an infinite sum, but rather as a sum that involves only terms of $\sin n\phi$ and $\cos n\phi$ that appear in $\sigma$.

*Check*: Earlier it was argued that for large $ s $, $\psi^o $ should approach

$\psi^o ( s \rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln s $

where 

$\overline{\lambda}=\int_0^{2\pi}\sigma b d\phi$

Using $\sigma=\sigma_o + \sigma_2\sin\thinspace2\phi$ gives $\overline{\lambda}=2\pi b\sigma_o$ and so the computed value of $ \psi^o $ of

$\displaystyle\psi^o =(b\sigma_o/\epsilon_o)\ln (b/ s )+\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi=(b\sigma_o/\epsilon_o)\ln b-(b\sigma_o/\epsilon_o)\ln  s +\frac{\sigma_2}{4\epsilon_0}\frac{b^3}{ s ^2}\sin 2\phi$

matches the limit

$\psi^o ( s \rightarrow\infty,\phi) \rightarrow const-(\overline{\lambda}/2\pi\epsilon_o)\ln s =const-(b\sigma_o/\epsilon_o)\ln s$

\newpage

# HW 6

Due Sunday, March 13th at 11:59 pm. Email me a scan (if it is less than 10 pages), slide under my door (preferred), or bring to the next class (if you finish early).

# Long Tube with Line of Charge

1. Do problem [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge) with the modification that $\sigma'=\lambda'\delta(y-y')$ and show that how it can be used to arrive at the result quoted in problem 2.15(b) of Jackson.
1. Use your answer to part 1. and reciprocity to find the potential inside the tube when $\rho=0$ inside the tube, the side at $x=1$ is held at a potential of $V_o$, and the other three sides are grounded. (This is an analog to [HW #3.1.4](#1-d-cartesian-green-function) where we solved a problem that was easy to solve without reciprocity using reciprocity).

**Solution**

1\. The steps used to derive

$$B_n = \frac{\sinh(n\pi x')}{\sinh(n\pi(x'-1))}A_n$$

and

$$\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\sigma'}{\epsilon_o}$$

For this problem, replace $\sigma'$ with $\sigma'=\lambda'\delta(y-y')$ in the above equation.

$$\sum_{n=1}^{\infty} A_n \sin(n\pi y)\left[\frac{n\pi\sinh(n\pi)}{\sinh(n\pi(x'-1))}\right]=-\frac{\lambda'\delta(y-y')}{\epsilon_o}$$

Multiplication of both sides by $\sin(l\pi y) dy$ and integration from $y=0$ to $1$ and using

$$\int_0^1\sin(l\pi y)\sin(n\pi y) dy=0\qquad\mbox{ for }l\ne n$$

$$\int_0^1\sin(l\pi y)\sin(n\pi y) dy=\frac{1}{2}\qquad\mbox{ for }l=n$$

$$\int_0^1\sin(l\pi y) \delta(y-y') dy=\sin(l\pi y')$$

gives, after changing the dummy index from $l$ to $n$,

$$A_n = - \frac{2\lambda'}{n\pi\epsilon_o}\frac{\sinh(n\pi(x'-1))}{\sinh(n\pi)}\sin(n\pi y')$$

$$B_n = - \frac{2\lambda'}{n\pi \epsilon_o}\frac{\sinh(n\pi x')}{\sinh(n\pi)}\sin(n\pi y')$$

for $n=1, 2, 3 , ...$. Note that $n$ is not constrained to be odd as it was in [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge). The new result is

$$\psi_l = -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(x'-1)]\sinh(n\pi x)\sin(n\pi y)\sin(n\pi y')$$

$$\psi_r= -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh(n\pi x')\sinh[n\pi (x-1)]\sin(n\pi y)\sin(n\pi y')$$

or, using $-\sinh(x)=\sinh(-x)$ and defining $x_{\lt}$ to the the smaller of $x$ and $x'$ and $x_{\gt}$ to the the larger of $x$ and $x'$,

$$\psi =  \sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-x_{\gt})]\sinh(n\pi x_{\lt})\sin(n\pi y)\sin(n\pi y')$$

Using $G=(4\pi\epsilon_o/L_z\lambda')\psi$ gives

$$G =  8\sum_{n=1}^{\infty} \frac{1}{n}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-x_{\gt})]\sinh(n\pi x_{\lt})\sin(n\pi y)\sin(n\pi y')$$

This is the same equation as problem 2.15 of Jackson except that the $x$ and $y$ variables are swapped. Given the fact that the problem is unchanged if the coordinates on the diagram for [HW problem 5.2.1](#long-rectangular-tube-with-sheet-of-charge) are swapped, we are free to change replace $x$ with $y$ and vice-versa in our equation above and so we conclude that it follows from this geometrical symmetry that

$$G =  8\sum_{n=1}^{\infty} \frac{1}{n}\frac{1}{\sinh(n\pi)}\sinh[n\pi(1-y_{\gt})]\sinh(n\pi y_{\lt})\sin(n\pi x)\sin(n\pi x')$$

Alternatively, the equivalence can be proved using an identity such as equation 3.169 of Jackson.

2\. First, obtain an answer using the standard boundary value method. The potential

$$\Phi = \sum_{n=1}^{\infty}A_n\sin(n\pi y)\sinh(n\pi x)$$

satisfies the three boundary conditions for which the potential on the boundary is zero.

To determine $A_n$, multiply both sides by $\sin(l\pi y)dy$ and integrate from $y=0$ to $y=1$. This gives

$$A_n=\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\quad n=1,3,...$$

$$A_n=0\quad n=2,4,...$$

and so the answer we expect is

$$\Phi = \sum_{n=1,3,...}^{\infty}\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)$$

----

To solve this problem using $G$, we need to compute

$$\Phi(x,y) = -\frac{1}{4\pi}\oint_\mathcal{S} \Phi(x,x',y,'y) \frac{\partial G}{\partial n'}\Bigg|_{\mathcal{S}} da'$$

(You should be able to explain what happened to the other terms in 1.42 of Jackson, which the above is based on and also the justification for the following equation.)

For this problem, the required integration is
%<code>!!!</code>The surface $\mathcal{S}$ is the surface of the volume $\mathcal{V}$, which is the volume inside the tube. $\mathcal{S}$ has a cross-sectional area of 1x1 and a length of $L_z$. On the two open ends of the tube, $n'=\pm z'$ and $\partial G/\partial z'=0$. On three of the sides of the volume, $\Phi=0$. This leaves the side at $x=1$, which has an outward normal of $n=x$. The integration needed is thus

$$\Phi(x,y) = -\frac{1}{4\pi}\int_0^1\int_0^{L_z} \Phi(1,x,y,y') \frac{\partial G}{\partial x'}\Bigg|_{x'=1} dy'dz'$$

Using $\Phi(1,x,y,y')=V_o$ and the fact that integration over $z'$ gives $L_z$, we have

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\int_0^1\frac{\partial G}{\partial x'}\Bigg|_{x'=1} dy'$$

Using the relationship

$$G=\frac{4\pi\epsilon_o}{L_z\lambda'}\psi$$

this is

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\frac{4\pi\epsilon_o}{L_z\lambda'}\int_0^1\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1} dy'$$

Using $\psi = \psi_l\Theta(x'-x)+\psi_r\Theta(x-x')$,

$$\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1}= \Theta(1-x)\frac{\partial \psi_l}{\partial x'}\Bigg|_{x'=1}+\Theta(x-1)\frac{\partial \psi_r}{\partial x'}\Bigg|_{x'=1}$$

(The two other terms in $\partial \psi/\partial x'$ involving the derivative of $\Theta$ cancel; this was considered in a previous HW problem.) The second term in this equation is zero because the volume extends from $x=0$ to $x=1$ for which $\Theta(x-1)=0$. Also, in this range of $x$, $\Theta(1-x) = 1$. This leaves

$$\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1}= \frac{\partial \psi_l}{\partial x'}\Bigg|_{x'=1}$$

Using

$$\psi_l = -\sum_{n=1}^{\infty} \frac{2\lambda'}{n\pi\epsilon_o}\frac{1}{\sinh(n\pi)}\sinh[n\pi(x'-1)]\sinh(n\pi x)\sin(n\pi y)\sin(n\pi y')$$

gives

$$\frac{\partial \psi}{\partial x'}\Bigg|\_{x'=1}= -\sum_{n=1}^{\infty} \frac{2\lambda'}{\epsilon_o}\frac{1}{\sinh(n\pi)}\cosh(0)\sinh(n\pi 
x)\sin(n\pi y)\sin(n\pi y')$$

and the integral

$$\Phi(x,y) = -\frac{V_oL_z}{4\pi}\frac{4\pi\epsilon_o}{L_z\lambda'}\int_0^1\frac{\partial \psi}{\partial x'}\Bigg|_{x'=1} dy'$$

can be rewritten as

$$\Phi(x,y) = \sum_{n=1}^{\infty}\frac{2V_o}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)\int_0^1 \sin(n\pi y')  dy'$$

The integral is zero for $n=2, 4, ...$ and $2/n\pi$ for $n=1,3,...$. The final result is then

$$\Phi(x,y) = \sum_{n=1,3,...}^{\infty}\frac{4V_o}{n\pi}\frac{1}{\sinh(n\pi)}\sinh(n\pi x)\sin(n\pi y)$$

which is the same as the result found earlier.

# Azimuthal Symmetry

1\. Find $\Phi(r,\theta)$ for problem [HW 4.1](#green-function-for-infinite-dome) in terms of an infinite sum involving the Legendre polynomials. 

2\. Find the surface charge density on the part of the dome in the $x$--$y$ plane.

**Solution**

1\. Letting $V_o=1$ so that potential is units of $V_o$, the exact solution on the $z$--axis is

$$\Phi(z)=1-\frac{z}{\sqrt{b^2+z^2}}$$

which can be written as

$$\Phi(z)=1-\frac{z}{|z|}\frac{1}{\sqrt{1+\displaystyle\frac{b^2}{z^2}}}$$

or

$$\Phi(z)=1-\frac{z}{|b|}\frac{1}{\sqrt{1+\displaystyle\frac{z^2}{b^2}}}$$

I've kept the absolute values because in some problems, it matters. Here it does not because $b$ is by definition positive, and we are considering the solution for $z\gt 0$. We can thus write the exact solution as either

$$\Phi^o(z)=1-\frac{1}{\sqrt{1+\displaystyle\frac{b^2}{z^2}}}$$

or

$$\Phi^i(z)=1-\frac{z}{b}\frac{1}{\sqrt{1+\displaystyle\frac{z^2}{b^2}}}$$

Where the superscript indicates the equation will be used for either the outer ( $o$; $z\gt b$) or inner ($i$; $z\lt b$) solution.

[The binomial expansion](https://rweigel.github.io/phys305/binomial_expansion.html) has the form

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + \frac{n(n+1)}{2!}\delta^2- \frac{n(n+1)(n+2)}{3!}\delta^3...$$

For $n=1/2$, we have

$$\frac{1}{(1+\delta)^n} = 1 - \frac{1}{2}\delta + \frac{\frac{1}{2}\frac{3}{2}}{2}\delta^2- \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\delta^3...$$

Using $\delta=b/z$ gives

$$\frac{1}{(1+\delta)^n} = 1 - \frac{1}{2}\frac{b^2}{z^2} + \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}- \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}...$$

Using this in the $b/z$ expansion for $\Phi^o$ gives

$$\Phi^o(z)=1-\frac{1}{\sqrt{1+\frac{b^2}{z^2}}}= \frac{1}{2}\frac{b^2}{z^2} - \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}+ \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}+...$$

or

$\displaystyle\Phi^o(z)=\sum_{l=2,4,...}\frac{C_l}{z^l}\qquad$ with $\qquad\displaystyle C_l=(-1)^{(l/2+1)} \frac{(l-1) !!}{(l/2)!}\frac{b^l}{2^{l/2}}$

where the double factorial is similar to the usual factorial with every other term omitted: $n!!\equiv 1\cdot 3\cdot 5\cdot ... n$ for $n$ odd and $n!!\equiv 2 \cdot 4\cdot 6\cdot ... n$ for $n$ even.

For $z\lt b$, we have the same equation as above except with the $b$ and $z$ swapped.


We know that the potential for a charge distribution with azimuthal symmetry can be written in the form

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

This equation must match a power series expansion of the potential along the $+z$-axis, which corresponds to $\theta=0$ and $r=z$.

$$\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)P_l(1)$$

or, equivalently,

$$\psi(z)=A_oP_0(1)+A_1P_1(1)z+...+\frac{B_oP_0(1)}{z}+\frac{B_1P_1(1)}{z^2}+...$$

The values of $P_l(1)$ can be determined from the first recursion relationship of 3.29 of Jackson:

$(l+1)P_{l+1}-(2l+1)xP_l+lP_{l-1}=0$

with $x=\cos 0 = 1$, this is

$(l+1)P_{l+1}(1)=(2l+1)P_l(1)-lP_{l-1}(1)$

The first few values can be computed manually

$l=1\qquad P_2(1)=(3P_1(1)-P_0(1))/2=1$

$l=2\qquad P_3(1)=(5P_2(1)-2P_1(1))/3=1$

$l=3\qquad P_4(1)=(7P_2(1)-3P_1(1))/4=1$

Based on the above, we expect that $P_l(1)=1$ for all $l$. (But this is not a proof.) 

For this to match our $z\gt b$ expansion of

$$\Phi^o(z)= \frac{1}{2}\frac{b^2}{z^2} - \frac{\frac{1}{2}\frac{3}{2}}{2}\frac{b^4}{z^4}+ \frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}\frac{b^6}{z^6}+...$$

we need $A_l=0$ for all $l$ and

$B_0=0$ because there is no $1/z$ term in the $z\gt b$ expansion.

$B_1=+\frac{b^2}{2}$ because the $1/z^2$ constants must match.

$B_2=0$ because there is no $1/z^3$ term in the $z\gt b$ expansion.

$\displaystyle B_3=-\frac{\frac{1}{2}\frac{3}{2}}{2}b^4$ 

because the $1/z^4$ constants must match.

$B_4=0$

$$B_5P_5(1)=+\frac{\frac{1}{2}\frac{3}{2}\frac{5}{2}}{3\cdot 2}b^6$$

etc.



We now have values for the $B_l$s:

$B_{l-1}=C_l\qquad l=2, 4, ...$

or, explicitly,

$$B_{l-1}=(-1)^{(l/2+1)} \frac{(l-1) !!}{(l/2)!}\frac{b^l}{2^{l/2}}\qquad l=2,4,...$$

The above steps are what is needed to find the constants for the potential $\Phi^o$ for $z \gt b$. The steps for finding the potential $\Phi^i$ for $z \lt b$ are similar. In this case, the $B_l$ terms are all zero and only every other $A_l$ term is non--zero.

2\. From 1., you will have a potential for $z/b\lt 1$ of the form

$$\psi(r,\theta)=\frac{B_1P_1(\cos\theta)}{r^2}+\frac{B_3P_3(\cos\theta)}{r^4}+...$$

From Gauss's law, the surface charge density just outside of a conductor is $\sigma=\epsilon_o\mathbf{E}\bfcdot\hat{\mathbf{n}}$, where $\hat{\mathbf{n}}$ is the outward normal to the surface. Equivalently,

$\displaystyle\sigma=-\epsilon_o\frac{\partial \psi}{\partial n}$ 

where the partial derivative is evaluated at the the surface.

In this problem, $n=z$ and we need to evaluate the partial derivative at $z=0$. That is, we need to compute

$$\frac{\partial \psi}{\partial z}=\left[\frac{\partial }{\partial z}\frac{B_1P_1(\cos\theta)}{r^2}+\frac{\partial}{\partial z}\frac{B_3P_3(\cos\theta)}{r^4}+...\right]_{z=0}$$

Given that $\cos\theta = z/r$, we can write

$$\frac{\partial \psi}{\partial z}=\left[\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}+\frac{\partial}{\partial z}\frac{B_3P_3(z/r)}{r^4}+...\right]_{z=0}$$

For the first term, we have, using the product rule for derivatives

$$
\begin{align*}
\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2} & =\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)+B_1P_1(z/r)\frac{\partial(1/r^2)}{\partial z}\right]\_{z=0}\\\\
&=\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)\right]\_{z=0}+B_1P_1(0)\frac{\partial(1/r^2)}{\partial z}\Bigg|\_{z=0}
\end{align*}
$$

Given that $P_1(0)=0$, we are left with

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\left[\frac{B_1}{r^2}\frac{\partial }{\partial z}P_1(z/r)\right]_{z=0}$$

At $z=0$, $r=s$ (the radial cylindrical coordinate), so

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^2}\left[\frac{\partial }{\partial z}P_1(z/r)\right]_{z=0}$$

Using the chain rule for derivatives

$\displaystyle \frac{df(g(u))}{du} = \frac{df}{dg}\frac{dg}{du}$ 

with $f=P_1$ and $g=z/r$, the term in square braces can be re-written, giving

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^2}\left[\frac{\partial P_1(g)}{\partial g}\frac{\partial (z/r)}{\partial z}\right]_{z=0}$$

Using

$$\frac{\partial (z/r)}{\partial z}\Big|\_{z=0}=\left[\frac{1}{r}-\frac{z}{r^2}\right]_{z=0}=\frac{1}{s}$$

leaves

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^3}\frac{\partial P_1(g)}{\partial g}\Big|\_{g=0}$$

Given that $\frac{\partial P_1(g)}{\partial g}=1$, we are left with

$$\frac{\partial}{\partial z}\frac{B_1P_1(z/r)}{r^2}=\frac{B_1}{s^3}$$

The remainder of the problem involves steps similar to the above. To obtain a general solution, we need to know $dP_l/dx|_{x=0}$. This can be found using the second equation of 3.29 of Jackson:

$$\frac{dP_{l+1}}{dx}-x\frac{dP_{l+1}}{dx} - (l+1)P_l=0$$

When evaluated at $x=0$, this is

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} =(l+1)P_l(0)$$

Using again the recursion relationship

$(l+1)P_{l+1}-(2l+1)xP_l+lP_{l-1}=0$

with $x=0$, gives

$P_{l+1}(0)=-\frac{l}{l+1}P_{l-1}(0)$

so

$l=1$, $P_2(0)=-\frac{1}{2}P_0(0)=-\frac{1}{2}$

$l=2$, $P_3(0)=-\frac{2}{3}P_1(0)=0$

$l=3$, $P_4(0)=-\frac{3}{4}P_2(0)=\frac{3}{4}\frac{1}{2}$

$l=4$, $P_5(0)=-\frac{4}{5}P_3(0)=0$

$l=5$, $P_6(0)=-\frac{5}{6}P_4(0)=-\frac{5}{6}\frac{3}{4}\frac{1}{2}$

or, in general

$P_l(0)=\frac{(l-1)!!}{l!!}(-1)^{l/2}\qquad l=2,4,...$

From which it follows

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} = 0 \qquad l=1,3,...$$

$$\frac{dP_{l+1}}{dx}\Big|_{x=0} = (l+1)\frac{(l-1)!!}{l!!}(-1)^{l/2}=\frac{(l+1)!!}{l!!}(-1)^{l/2}\qquad l=2,4,...$$

Shifting the index by $-1$ gives

$$\frac{dP_{l}}{dx}\Big|_{x=0} = 0 \qquad l=0,2,...$$

$$\frac{dP_{l}}{dx}\Big|_{x=0} =\frac{l!!}{(l-1)!!}(-1)^{(l-1)/2}\qquad l=1,3,...$$

So the first few non--zero terms are

$$l=1\qquad \frac{dP_{1}}{dx}\Big|_{x=0}=\frac{1!!}{0!!}(-1)^0=1$$

$$l=3\qquad \frac{dP_{3}}{dx}\Big|_{x=0}=\frac{3!!}{2!!}(-1)^1=-\frac{3}{2}$$

$$l=5\qquad \frac{dP_{5}}{dx}\Big|_{x=0}=\frac{5!!}{4!!}(-1)^2=\frac{5\cdot 3\cdot 1}{4\cdot 2}=\frac{15}{8}$$

Check: Table 3.15 gives the first five Legendre polynomials. Manual evaluation of the derivatives gives:

$dP_0(x)/dx=0$

$dP_1(x)/dx\Big|_{x=0}=1$

$dP_2(x)/dx\Big|_{x=0}=0$

$dP_3(x)/dx\Big|_{x=0}=-\frac{3}{2}$

$dP_4(x)/dx\Big|_{x=0}=0$

From [A table](https://en.wikipedia.org/wiki/Legendre_polynomials#Rodrigues'_formula_and_other_explicit_formulas), $P_5={\textstyle {\tfrac {1}{8}}\left(63x^{5}-70x^{3}+15x\right)}$ so

$dP_5(x)/dx\Big|_{x=0}=\frac{15}{8}$

## Sphere held at potential

In class, we started the problem of finding the potential inside and outside of a sphere of radius $b$ that is centered on the origin and is held at potential $V(b,\theta)=V_o\cos^2\theta$.

1. Find $\Phi(r,\theta)$ (unless otherwise stated, this type of statement means for all $r$).

   Most students immediately re--wrote $\cos^2\theta$ as $V_o(P_o/3 + 2P_2/3)$ prior to starting to answer part 1. by using the fact that $P_2=(3\cos^2\theta - 1)/2$ and $P_o=1$. In the general case, it will not always be obvious how to express an arbitrary boundary potential $V(\theta)$ in terms of the Legendre polynomials.

   In 3.2 of Jackson, he notes that an arbitrary function of $\theta$ (he uses $x$, which is also $\cos\theta$) may be written as

   $\displaystyle V(\theta) = \sum_{l=0}^\infty A_lP_l(\cos \theta)$

   To find the coefficients $A_l$, multiply both sides by $P_{l'}(\cos\theta)\sin\theta d\theta$ and then integrate from $0$ to $\pi$. (This is essentially what Griffiths calls "Fourier's trick" except using Legendre polynomials). By orthogonality, one then finds that

   $\displaystyle A_l=\frac{2l+1}{2}\int_0^\pi V(\theta)P_l(\cos\theta) \sin\theta d\theta$

2. Suppose $V(b,\theta)=V_o$ for $\theta=0$ to $\theta=\pi/2$ and $V(b,\theta)=-V_o$ for $\theta=\pi/2$ to $\pi$. Write $V(b,\theta)$ in the form $A_0P_0 + A_1P_1 + A_2P_2$. That is, find a second--order approximation to $V(b,\theta)$ by finding $A_0$, $A_1$, and $A_2$. (If you use a formula from Jackson or elsewhere instead of doing integration to find $A_0, A_1,$ and $A_2$, prove the formula.)

3. Find $\Phi(r,\theta)$ using the boundary value $V(b,\theta)=A_0P_0 + A_1P_1 + A_2P_2$.

4. State at least one way that you can determine if your answer to part 3. makes sense.

5. (Optional) Repeat this problem assuming that instead of being held at a potential, the sphere has a surface charge density of $\sigma(b,\theta)=\sigma_o\cos^2\theta$ or $\sigma(b,\theta)=\sigma_o$ for $\theta=0$ to $\theta=\pi/2$ and $\sigma(b,\theta)=-\sigma_o$ for $\theta=\pi/2$ to $\pi$