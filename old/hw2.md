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

**1\.** Let the unprimed system have a conducting plate in $z=0$ plane held at $\Phi=0$ and a conducting plate in the $z=d$ plane held at at $\Phi=V_o$.

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

**2\.** The procedure here is nearly identical to part 1. The potential between the sphere in the unprimed system when the potential at $r=b$ is $V_o$ and the potential at $r=c$ is zero is

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

    (this is equation 1.32 of Jackson)
2. Show that

   $$\int_{\mathcal{V}} f\thinspace\mathbf{\nabla}\bfcdot \mathbf{A}\thinspace d^3x = -\int_{\mathcal{V}}\mathbf{A}\bfcdot(\mathbf{\nabla}f)\thinspace d^3x+\oint_{\mathcal{S}} f\mathbf{A}\bfcdot\hat{\mathbf{n}}\thinspace da$$

  where $\mathcal{V}$ is the volume enclosed by the surface $\mathcal{S}$, $\hat{\mathbf{n}}$ is the normal to a differential area element $da$ on $\mathcal{S}$, and $d^3x$ is a differential volume element. (This is needed in the following problem.)

3. Verify the result in 2. by using an $f$, $\mathbf{A}$ and $\mathcal{V}$ of your choosing.

**Solution**

**1\.** This can be shown by writing $\boldsymbol{\nabla}$ and $\mathbf{A}$ in cartesian coordinates.

**2\.** The divergence theorem

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
