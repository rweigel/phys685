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
