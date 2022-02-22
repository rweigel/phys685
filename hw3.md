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

1\. One can answer this question by assuming a surface charge of $\sigma_l$ and $\sigma_r$ is induced on the plates at $x=0$ and $x=w$. Then use the formula $\sigma/2\epsilon_o$ for the electric field of the sheets of charge at $x=0$, $x=x'$, and $x=w$ to get the total field $E_l$ and $E_r$.  The two unknowns, $\sigma_l$ and $\sigma_r$, can be found by using the fact that the electric field in either of the conductors is zero - this yields $\sigma' = -(\sigma_l+\sigma_r)$, which is expected because the net charge in the universe is zero. The second equation needed to find $\sigma_l$ and $\sigma_r$ in terms of $\sigma'$ is

$\displaystyle\psi(w)-\psi(0) = 0 = -\int_0^w E\thinspace dx=-\int_0^{x'}E_ldx-\int_{x'}^wE_rdx$

Some students wrote their final answers in terms of $\sigma_l$ and $\sigma_r$. These were not parameters given in the problem statement and so such a solution is incomplete.

Alternatively, one can use the fact that $\nabla^2 \psi(x)=0$ has solutions of the form $\psi=a+bx$, the two boundary conditions and the continuity and jump conditions at $x=x'$.

$\psi_l=A_l+B_lx\qquad\psi_r=A_r+B_rx$

Boundary conditions:

$\psi_l(0)=0\Rightarrow A_l=0$

$\psi_r(w)=0=A_r+B_rw\Rightarrow A_r=-B_rw$

This leaves

$\psi_l=B_lx$ and $\psi_r=B_r(x-w)$

Continuity:

$\psi_l(x')=\psi_r(x')\Rightarrow B_lx'=B_r(x'-w)$

Jump:

The jump condition follows from Gauss's law with a Gaussian cylinder with one end cap to the left of $x'$ and the other to the right. It also follows from integrating $\nabla^2\psi=-\sigma'\delta(x-x')/\epsilon_o$ once with respect to $x$.
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

2\. $\boxed{\psi=\psi_l(x)\Theta(x'-x)+\psi_r(x)\Theta(x-x')}$

Checks: 
* When $x\lt x'$, $\Theta(x'-x)=1$ and $\Theta(x-x')=0$, giving $\psi=\psi_l$.
* When $x\gt x'$, $\Theta(x'-x)=0$ and $\Theta(x-x')=1$, giving $\psi=\psi_lr$.

3\.

$\begin{array}{ll}
\displaystyle\frac{d\psi}{dx} & = \displaystyle\thickspace \psi_l(x)\frac{d}{dx}\Theta(x'-x) + \Theta(x'-x)\frac{d\psi_l(x)}{dx} \\\\
& \displaystyle+\thickspace\psi_r(x)\frac{d}{dx}\Theta(x-x')+\Theta(x-x')\frac{d\psi_r(x)}{dx}
\end{array}
$

If one plots $\psi(x)$, you will see that its derivative has a jump downwards at $x=x'$ of $\sigma'/\epsilon_o$ and so we expect the terms in $d\psi/dx$ with the derivative of the Heavyside step function, which is the delta function, to be zero. So the two terms involving derivatives of $\Theta$ will be addressed first.

The first term can be rewritten using

$\frac{d}{dx}\Theta(x'-x)=-\delta(x'-x)=-\delta(x-x')$

The first equality follows from the identity given in the problem statement: $d\Theta(-x)/dx=-\delta(x)$. The second equality is a standard delta function identity.

The second term is

$\displaystyle\frac{d}{dx}\Theta(x-x')=\delta(x-x')$

The following two equalities follow from the fact that $\delta(x-x')$ is zero except at $x=x'$:

$-\psi_l(x)\delta(x-x')=-\psi_l(x')\delta(x-x')$

$\psi_r(x)\delta(x-x')=\psi_r(x')\delta(x-x')$

As a result of these considerations, the two terms in $d\psi/dx$ involving derivatives of $\Theta$ cancel, leaving

$\displaystyle\frac{d\psi}{dx} = \Theta(x'-x)\frac{d\psi_l(x)}{dx} +\Theta(x-x')\frac{d\psi_r(x)}{dx}$

Straightforward calculation and use of the same identities as above gives

$\displaystyle\frac{d^2\psi}{dx^2}=-\frac{\sigma'}{\epsilon_o}\delta(x-x')$

This matches expectations. For a sheet of charge in the $x=x'$ plane, the volume charge density is

$\rho=\sigma'\delta(x-x')$

and Poisson's equation is $\displaystyle\nabla^2\psi=-\frac{\rho}{\epsilon_o}$

(Recall that the units of $\delta(x)$ are inverse length. This follows from part of the definition of the delta function: $\int\delta(x)dx=1$).

4\. ...

## 1-D Spherical Green Function

Two conducting and grounded spherical shells of radius $b$ and $c$ are centered on the origin, and $c\gt b$.

A nonconducting spherical shell is centered on the origin and has a charge density of $\sigma'$ and radius $r'$, with $b \lt r' \lt c$.

1. Find $\psi_i(r)$, the potential between the inner conducting shell and the charged shell and $\psi_o(r)$, the potential between the charged shell and the outer conducting shell. (Read the subscript $i$ as "inner" and $o$ as "outer".)
2. Find the surface charge densities on the inner and outer conductor.
3. Verify that Gauss's law is satisfied for a Gaussian sphere centered on the origin and with a radius that is between the charged shell and the outer conducting shell.
2. Write the potential $\psi(r)$ for $b\le r\le c$ as a single function using $\psi_i$ and $\psi_o$ and the Heavyside step function $\Theta$.

**Solution**

1\.

$\displaystyle\psi_i=\left(\frac{\sigma'/\epsilon_o}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{b}\right)\left(\frac{1}{r}-\frac{1}{c}\right)$

$\displaystyle\psi_o=\left(\frac{\sigma'/\epsilon_o}{\frac{1}{b}-\frac{1}{c}}\right)\left(\frac{1}{r'}-\frac{1}{c}\right)\left(\frac{1}{r}-\frac{1}{b}\right)$
 
As before, there is symmetry with respect to swapping $r$ and $r'$: $\psi_i(r,r')=\psi_o(r',r)$

2\. From Gauss's law, near the surface of a conductor $\sigma=-\epsilon_o d\psi/dn$. For the inner conductor, $n=r$; for the outer, $n=-r$.


Check: In HW #2.3.2, we found the charge induced when a point charge was at $r'$. We can use that answer and superposition to find the total charge induced if point charges are distributed uniformly on a sphere. This should match the total charge induced found in this problem.

$\displaystyle q'_{r=b}=-\frac{q'b}{c-b}\left(\frac{c}{r_o}-1\right)$

$\displaystyle q'_{r=c}=+\frac{q'c}{c-b}\left(\frac{b}{r_o}-1\right)$

## Jackson Equation 1.42

Before stating Equation 1.42, Jackson (3rd edition) notes that with Equation 1.35 and 1.39, it is simple to obtain a generalization of Equation 1.36.

Show the "simple" steps need to arrive at Equation 1.42.

Be very careful with notation. You'll need to think a bit about the justification and validity of swapping $x$ and $x'$ and/or changing the dummy variable used in integration. When you do either of these, provide a justification so that I know you are not applying the "answer operator".