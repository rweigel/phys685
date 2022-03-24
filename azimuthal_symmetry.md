#azimuthal-symmetry&l=1302&c=1

# Monopole Expansion Using "Standard" Method 

1. Write down the potential $\psi$ as a function of $(x,y,z)$ for a point charge $q$ located at $(x,y,z)=(0,0,z')$ using $kq=1$.

2. Write out the first three terms in the Taylor series expansion of $\psi$ for $z'/r \ll 1$.

3. Show that your result is consistent with equation 3.38 of Jackson 3rd edition:

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|} = \sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)$$

where $r_{<}$ ( $r_{<}$) is the smaller (larger) of $|\mathbf{x}|$ and $|\mathbf{x}'|$ and $\gamma$ is the angle between $\mathbf{x}$ and $\mathbf{x}'$.

4. Show how your result consistent with equation 3.95 of Griffiths 4th edition (by using the delta function to represent the charge density):

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

which was derived assuming that the maximum value of $r'$ for which $\rho\ne 0$ is much less than $r$ and $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$.

'''Optional Problem'''

Repeat the above for a point charge located at $(x,y,z)=(0,y',0)$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|

1.

$$\psi = \frac{1}{|\mathbf{x}-\mathbf{x}'|} =\frac{1}{\sqrt{x^2+y^2+(z-z')^2}}$$

2.

For the case $r\gg z'$, factor out $r$ and re-write in a form that is straightforward to expand as a Taylor series

$$
\begin{align}
\frac{1}{|\mathbf{x}-\mathbf{x}'|} &=\frac{1}{\sqrt{x^2+y^2+(z-z')^2}}\\
&=\frac{1}{\sqrt{x^2+y^2+z^2+z'^2-2zz'}}&&\text{Expand }(z-z')^2\\
&=\frac{1}{|r|\sqrt{1+z'^2/r^2-2zz'/r^2}}&&\text{Using}\thinspacer^2=x^2+y^2+z^2\thinspace\text{and factoring out}\thinspacer\\
&=\frac{1}{r\sqrt{1+z'^2/r^2-2(z'/r)\cos\theta}}&&\text{Using}\thinspacez=r\cos\theta\text{ and }|r|=r\\
& =\frac{1}{r\sqrt{1+\delta}}&&\text{Defining }\delta\equiv z'^2/r^2-2(z'/r)\cos\theta
\end{align}
$$

For $\delta<1$, the binomial function $(1+\delta)^{-1/2}$ can be expanded as a Taylor series, the result of which is

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\delta+\frac{3}{8}\delta^2-\frac{5}{16}\delta^3+...$$

Evaluating terms of order $\delta^2$ and lower using $\delta = z'^2/r^2-2(z'/r)\cos\theta$ gives

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\left(z'^2/r^2-2(z'/r)\cos\theta\right)+\frac{3}{8}\left(z'^2/r^2-2(z'/r)\cos\theta\right)^2+...$$

This can be written in terms of a power series ordered by powers of $z'/r$ giving the result

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\frac{1}{r}\left(1+\frac{z'}{r}\cos\theta+\left(\frac{z'}{r}\right)^2\frac{1}{2}\left(3\cos^2\theta-1\right)-\left(\frac{z'}{r}\right)^3\frac{3}{2}\cos\theta+\frac{3}{8}\left(\frac{z'}{r}\right)^4...\right)$$

The first three terms are identified as $P_0,P_1,$, and $P_2$. The last two terms are parts of $P_4$ and $P_5$ - the full $P_4$ and $P_5$ appear if the $\delta^3$ term is expanded.  Therefore the two expressions are consistent up to $l=2$.

3.

The above equation is to be compared with

$$\sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)=\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)$$

which, given the problem statement and the assumption that $z' < r$, we identify $r_{>}$ as $r$, $r_{<}$ as $z'$. The angle $\gamma$ between $r$ and $r'$ is the same as the spherical polar angle $\theta$ when $r'$ is aligned with the $z$-axis. With this,

$$\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)=\frac{1}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^l P_l(\cos \theta)$$

Therefore the two expressions are consistent up to $l=2$.

The steps above can be repeated by factoring out $z'$ and using $\delta \equiv r^2/z'^2-2(r/z')\cos\theta$ for the case $z'\gg r$.

4.

Note that there is a complication introduced by choosing the location of the charge to be $z'$ when using Griffiths equation 3.95. (If I had stated that the charge was located at $z_o$ instead of $z'$, we would not have this problem.) In the integral

$$\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

the dummy index is also primed. In this problem, the location of the charge is $\mathbf{r}'=(0,0,z')$, so the charge density can be written as

$$\rho(\mathbf{r})=q\delta(x)\delta(y)\delta(z-z')$$

Plugging this into the expression for the delta function would give

$$\rho({\mathbf{r}'})=q\delta(x')\delta(y')\delta(z'-z')=q\delta(x')\delta(y')\delta(0)$$

This does not make sense because the charge density should be zero everywhere except for at the point $(0,0,z')$.

To circumvent this issue, choose the dummy integration index to be double primed (or use $z_o$ as the location of the charge instead of $z'$). If the dummy index is double-primed, then

<nowiki>
$$\rho({\mathbf{r}^{\prime\prime}})=q\delta(x^{\prime\prime})\delta(y^{\prime\prime})\delta(z^{\prime\prime}-z')$$

which corresponds to the charge density of a point charge at a fixed location $z'$. Then

$$\rho({\mathbf{r}''})=q\delta(x'')\delta(y'')\delta(z''-z')$$

which corresponds to the charge density of a point charge at a fixed location $z'$. Then

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r'')^nP_n(\cos\alpha)\rho(\mathbf{r}'')d\tau''$$

Using $\alpha=\theta$ and factoring out (\q$ and $P_l(\cos(\theta))$ and using $kq=1$ gives

$$\psi(\mathbf{r})=\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}P_n(\cos\theta)\int\int\int(x''^2+y''^2+z''^2)^{n/2}\rho(\mathbf{r}'')dx''dy''dz''$$

The integral evaluates to

$$
\begin{align}
& \int\int\int(x'^2+y'^2+z'^2)^{n/2} q\delta(x'')\delta(y'')\delta(z''-z') dx''dy''dz''=\\
& \int\int(y''^2+z''^2)^{n/2} q\delta(y'')\delta(z''-z') dy'dz' = \\
& \int(z''^2)^n q\delta(z''-z') dz''=\\
& z'^{n}
\end{align}
$$
</nowiki>

The final result is

$$\psi = \frac{1}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^l P_l(\cos \theta)$$

which is the same as found earlier.

'''Optional'''

For the case the charge at $(0,y',0)$, one needs to note that $y=r\sin\theta\sin\phi=r\cos\gamma$ and follow the same steps, for $y'\ll r$ factor out $r$ and for $y'\gg r$ factor out $y'$. For the case $r\gg y'$, the expansion should yield

$$\frac{1}{|\mathbf{x}-\mathbf{x}'|}=\frac{1}{r}\left(1+\frac{y'}{r}\cos\gamma+\left(\frac{y'}{r}\right)^2\frac{1}{2}\left(3\cos^2\gamma-1\right)-\left(\frac{y'}{r}\right)^3\frac{3}{2}\cos\gamma+\frac{3}{8}\left(\frac{y'}{r}\right)^4...\right)$$

and one makes the identification that $r_{>}$ is $r$, $r_{<}$ is $y'$ and concludes that this is consistent with Jackson's equation 3.38.

----

Having done the derivation for charges at specific points, one can then follow the same steps to find the result for an arbitrary location in space $r'$ for the charge.

$$
\begin{align}
\frac{1}{|\mathbf{x}-\mathbf{x}'|} &=\frac{1}{\sqrt{(x-x')^2+(y-y')^2+(z-z')^2}}\\
&=\frac{1}{\sqrt{x^2+y^2+z^2+x'^2+y'^2+z'^2-2xx'-2yy'-2zz'}}\\
&=\frac{1}{r\sqrt{1+r'^2/r^2-2(xx'+yy'+zz')/r^2}}\\
&=\frac{1}{r\sqrt{1+r'^2/r^2-2(r'/r)\cos\gamma}}\\
\end{align}
$$

$$r^2=x^2+y^2+z^2$$

$$r'^2=x'^2+y'^2+z'^2$$

$$\cos\gamma=\frac{\mathbf{r}\cdot\mathbf{r'}}{rr'}=\frac{xx'+yy'+zz'}{rr'}$$

$$\delta = r'^2/r^2-2(r'/r)\cos\gamma$$

For $r \gg r'$,

$$\frac{1}{\sqrt{1+\delta}}=1-\frac{1}{2}\delta+\frac{3}{8}\delta^2-\frac{5}{16}\delta^3+...$$

$$\frac{1}{r\sqrt{1+r'^2/r^2-2(r'/r)\cos\gamma}}=\frac{1}{r}\left(1+\frac{r'}{r}\cos\gamma+\left(\frac{r'}{r}\right)^2\frac{1}{2}\left(3\cos^2\gamma-1\right)+\left(\frac{r'}{r}\right)^3\frac{1}{2}\left(5\cos^3\gamma-3\cos\gamma\right)+...\right)$$

$$\frac{1}{r}\sum_{l=0}^\infty \left(\frac{r'}{r}\right)^l P_l(\cos \gamma)$$

This process can be repeated using $r' \gg r$ giving

$$\frac{1}{r'}\sum_{l=0}^\infty \left(\frac{r}{r'}\right)^l P_l(\cos \gamma)$$

The equations for $r \gg r'$ and $r'\gg r$ can be combined into one equation

$$\sum_{l=0}^\infty \frac{r^l_{<}}{r^{l+1}_{>}}P_l(\cos \gamma)=\frac{1}{r_{>}}\sum_{l=0}^\infty \frac{r^l_{<}}{r^l_{>}}P_l(\cos \gamma)$$

using the convention that $r_{>}$ is the larger of $r$ & $r'$ and $r_{<}$ is the smaller of $r$ and $r'$.
|}

# Monopole Expansion Using the Azimuthal Symmetry Trick 

In section 3.3 of Jackson 3rd edition, he notes that for a problem with azimuthal symmetry, the general solution to Laplace's equation in spherical coordinates is

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

The coefficients $A_l$ and $B_l$ in the expansion can be found using a trick, provided that $\psi(z)$ is known as a power series for a charge distribution that is independent of the spherical angle $\phi$ (so $\psi$ has azimuthal symmetry). Using this trick, he finds $\psi(r,\theta)$ for a point charge at $\mathbf{x}'$ by noting that $\psi(z)$ for a charge located on the $z-$axis is easily converted to a power series using a Taylor series expansion. (He uses the same trick to find  $\psi(r,\theta)$ for a ring of charge in the $x-y$ plane and centered on the $z-$axis.)

1. In a few sentences, explain the justification for why the trick works.

2. Use the trick to find the coefficients $A_l$ and $B_l$ for a charge: $q$ at $z'= d$ using $kq=1$. (That is, repeat Jackson's derivation, but fill in the missing steps and write it in a way that makes sense to you.)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
1.

The justification is that due to the uniqueness of solutions to Laplace's equation, there must exist a single solution (single set of coefficients $A_l$ and $B_l$) for all space in the general solution so the coefficients $a_l$ and $b_l$ in an expansion of the potential in the form of $\psi(z)=\sum_{l=0}^{\infty} a_lz^l + b_l/z^{l+1}$ that applies to the $z-$axis must be the same as $A_l$ and $B_l$. 

Suppose for a given charge configuration, one can find a solution for the potential on the $z$-axis as a power-series 

$$\psi(z)=\sum_{l=0}^{\infty} \left(a_lz^l + \frac{b_l}{z^{l+1}}\right)$$

and the charge configuration has azimuthal symmetry. The general solution to Laplace's equation for a potential that does not depend on $\phi$ is $\nabla^2\psi(r,\theta)=0$ is

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

Setting $r=z$, $\theta=0$, and noting that $P_l(1)=0$, this equation becomes

$$\psi(r=z,\theta=0)=\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)$$

The equations for $\psi(z)$ in terms of $a_l$ & $b_l$ and $A_l$ & $B_l$ both satisfy Laplace's equation. If solutions to Laplace's equations are unique, then $A_l=a_l$ and $B_l=b_l$.
|}

# Dipole Expansion 

Point charges $q=\pm 1$ are located at $(x,y,z)=(0,0,\pm z')$ and $kq=1$.

Find the potential in three ways

1. Using the azimuthal symmetry trick
1. Using equation 3.38 of Jackson 3rd edition (quoted in a previous problem)
1. Using equation 3.95 of Griffiths 4th edition (quoted in a previous problem)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Solution
|-
|
1.

First, consider the $z>0$ case, so $|z|=z$.

Using $q/4\pi\epsilon_o=1$

$$\psi(z)=\frac{1}{\sqrt{(z-z')^2}}-\frac{1}{\sqrt{(z+z')^2}}=\frac{1}{|z-z'|}-\frac{1}{|z+z'|}$$

For $z'\lt z$,

$$
\begin{align}
\frac{1}{|z-z'|}=\frac{1}{|z|}\frac{1}{(1-z'/z)}&=\frac{1}{z}\left(1 + \frac{z'}{z} + \left(\frac{z'}{z}\right)^2 + \left(\frac{z'}{z}\right)^3 + \left(\frac{z'}{z}\right)^4 + ... \right)\\
\frac{1}{|z+z'|}=\frac{1}{|z|}\frac{1}{(1+z'/z)}&=\frac{1}{z}\left(1 - \frac{z'}{z} + \left(\frac{z'}{z}\right)^2 - \left(\frac{z'}{z}\right)^3 + \left(\frac{z'}{z}\right)^4 + ... \right)\\
\end{align}
$$

Combining these two equations gives

$$\psi(z)=\frac{1}{|z-z'|}-\frac{1}{|z+z|}=\frac{2z'}{z^2}+\frac{2z'^3}{z^4}+\frac{2z'^5}{z^6}+...$$

This is to be compared to the general solution to Laplace's equation 

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

for $\theta=0$. Using this, $r=z$, and $P_l(\cos 0)=P_l(1)=1$,

$$\psi(z)=\sum_{l=0}^{\infty}\left(A_lz^l + B_lz^{-l-1}\right)=A_o+A_1z+A_2z^2+...+\frac{B_o}{z}+\frac{B_1}{z^2}+\frac{B_2}{z^3}+\frac{B_3}{z^4}+...$$

If the two $\psi(z)$ potential equations are to match, $A_l=0$ for all $l$ and $B_1=2z'$, $B_3=2z'^3$, $B_5=2z'^5$, $...$ for $l=1,3,5,...$, and $B_l=0$ otherwise. 

$$
\begin{align}
\psi(\mathbf{x}) & = \frac{2z'}{r^2}P_1(\cos\theta)+\frac{2z'^3}{r^4}P_3(\cos\theta)+\frac{2z'^5}{r^6}P_5(\cos\theta)+...\\
& = \frac{2}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)
\end{align}
$$

When $z<z'$, a power series form of the potential can be found by repeating the above steps with $z$ and $z'$ interchanged. The result is then this last equation with $r$ and $z'$ swapped:

$$\psi(\mathbf{x})=\frac{2}{z'}\sum_{l=0}^\infty \left(\frac{r}{z'}\right)^{2l+1}P_l(\cos\theta)$$

Note that the above was done under the assumption that $z>0$. If $z < 0$, we would need to make two changes: (1) $|z|=-z$ and (2) $\theta=\pi$. The results are the same. However, this calculation actually does not need to be done or considered because we have already found a general solution.

2.

This could also have been shown using equation 3.38 of Jackson (shown here for $r>r'$)

$$\frac{1}{|\mathbf{x}-\mathbf{x_+}|}=\sum_{l=0}^\infty \frac{r^l_{+}}{r^{l+1}} P_l(\cos \gamma_+)$$

$$\frac{1}{|\mathbf{x}-\mathbf{x_-}|}=\sum_{l=0}^\infty \frac{r^l_{-}}{r^{l+1}} P_l(\cos \gamma_-)$$

Where  $r_{+}=r_{-}=z'$, $\gamma_+$ is the angle from the $+q$ charge at $\mathbf{x}_+ = z'\hat{\mathbf{z}}$ to $\mathbf{x}$ and $\gamma_-$ is the angle from the $-q$ charge at $\mathbf{x}_- = -z'\hat{\mathbf{z}}$ to $\mathbf{x}$.

Using, $\gamma_+ = \theta$, $\gamma_++\gamma_-=\pi \Rightarrow \gamma_-=\pi-\theta$, and $P_l(x)=-P_l(-x)$ for $l=1,3,...$ and $P_l(x) = P_l(-x)$ otherwise:

$$\begin{eqnarray}
\frac{1}{|\mathbf{x}-\mathbf{x_+}'|}-\frac{1}{|\mathbf{x}-\mathbf{x_-}'|} & = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} P_l(\cos \theta)-\sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} P_l(\cos (\pi-\theta))\\
& = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} \Big[P_l(\cos \theta) - P_l(\cos (\pi-\theta))\Big]\\
& = & \sum_{l=0}^\infty \frac{z^{'l}}{r^{l+1}} \Big[P_l(\cos \theta) - P_l(-\cos \theta)\Big]\\
& = & \sum_{l=1,3,...}^\infty \frac{z^{'l}}{r^{l+1}} 2P_l(\cos \theta)\\
& = & \sum_{l=0}^\infty \frac{z^{'2l+1}}{r^{2l+2}} 2P_l(\cos \theta)\\
& = & \frac{2}{r}\sum_{l=0}^\infty \left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)
\end{eqnarray}$$

For $r < z'$, all of the above steps apply and the result is the above equation with $r$ and $z'$ swapped.

3. 

In this case, the charge density in primed coordinates is (using $d\equiv z'$ to avoid issue noted in problem 1)

$$\rho({\mathbf{r}}')=q\delta(x')\delta(y')\delta(z'-d)-q\delta(x')\delta(y')\delta(z'+d)$$

or

$$\rho({\mathbf{r}}')=\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta')-\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)$$

The following charge density could also be used

$$\rho({\mathbf{r}}')=\frac{q}{r'^2\sin\theta'}\delta(r'-d)\delta(\theta')\delta(\phi')-\frac{q}{r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)\delta(\phi')$$

(In fact, we could use $\delta(\phi'-\delta)$, where $\delta$ is arbitrary.)

As noted in class, one should check that this charge density gives $\int \rho(\mathbf{r}')r'^2\sin\theta'dr'd\theta'd\phi'=q-q$. Also note that the second term has $\delta(r'-d)$ and not $\delta(r'+d)$, which is a common error; $r'$ must be greater than zero, so $\delta(r'+d)$ corresponds to a charge at $r'=-d$.

In general, $\alpha$ depends on the primed coordinates

$$\cos \alpha = \frac{\mathbf{r}\cdot \mathbf{r}'}{r\thinspacer'}=\sin\theta\sin\theta'\cos\phi\cos\phi' + \sin\theta\sin\theta'\sin\phi\sin\phi'+\cos\theta\cos\theta'$$

which can also be written as

$$\cos \alpha = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$$

We need to evaluate

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

In spherical coordinates, $d\tau'=r'^2\sin\theta'dr'd\theta'd\phi'$. The integral to evaluate is 

$$\int(r')^nP_n(\cos\alpha)\left[\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta')-\frac{q}{2\pi r'^2\sin\theta'}\delta(r'-d)\delta(\theta'-\pi)\right]r'^2\sin\theta'dr'd\theta'd\phi'$$

After cancellation

$$\frac{q}{2\pi}\int(r')^nP_n(\cos\alpha)\left[\delta(r'-d)\delta(\theta')-\delta(r'-d)\delta(\theta'-\pi)\right]dr'd\theta'd\phi'$$

Integration over $r'$ gives

$$\frac{q}{2\p\thinspace d^{\thinspacen}\int P_n(\cos\alpha)\left[\delta(\theta')-\delta(\theta'-\pi)\right]d\theta'd\phi'$$

Recalling that

$$\cos \alpha = \sin\theta\sin\theta'\cos(\phi-\phi') +\cos\theta\cos\theta'$$

and using

$$P_l(\cos\alpha)\delta(\theta') = P_l(\sin(\theta)\sin 0\cos(\phi-\phi')+\cos\theta\cos 0)=P_l(\cos\theta)$$

$$P_l(\cos\alpha)\delta(\theta-\pi) = P_l(\sin(\theta)\sin 0\cos(\phi-\phi')+\cos\theta\cos \pi)=P_l(-\cos \theta)$$

allows the integration over $\theta$ to be evaluated as

$$\frac{q}{2\p\thinspace d^{\thinspacen}\int P_n(\cos\alpha)\left[\delta(\theta')-\delta(\theta'-\pi)\right]d\theta'=\frac{q}{2\pi}d^{\thinspacen}[P_n(\cos\theta)-P_n(-\cos\theta)]\int d\phi'$$

Integration over $\phi'$ leaves

$\thinspace d^{\thinspacen}[P_n(\cos\theta)-P_n(-\cos\theta)]$$

Thus, 

$$\psi(\mathbf{r})=\frac{1}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{1}{r^{n+1}}\int(r')^nP_n(\cos\alpha)\rho(\mathbf{r}')d\tau'$$

simplifies to

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{n=0}^{\infty}\frac{d^{\thinspacen}}{r^{n+1}}[P_n(\cos\theta)-P_n(-\cos\theta)]$$

for $\pm q$ at $z=\pm d$

The $n=0, 2, ...$ Legendre polynomials are even functions, so $P_n(x)=P_n(-x)$. The $n=1, 3, ...$ Legendre polynomials are odd functions, os $P_n(x)=-P_n(-x)$. As a result, 

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{n=1,3,...}^{\infty}\frac{d^{\thinspacen}}{r^{n+1}}[2P_n(\cos\theta)]$$

or, using $n=2l+1$ and switching replacing $d$ with $z'$

$$\psi(\mathbf{r})=\frac{q}{4\pi\epsilon_0}\sum_{l=0}^{\infty}\frac{z'^{2l+1}}{r^{2l+2}}[2P_l(\cos\theta)]=\frac{q}{4\pi\epsilon_0}\frac{2}{r}\sum_{l=0}^{\infty}\left(\frac{z'}{r}\right)^{2l+1}P_l(\cos\theta)$$

which matches the earlier results. This process can be repeated for $r\lt z'$ and the result is the above equation with $r$ and $z'$ swapped.
|}

# Line of Charge 

Due on April 22nd before class starts.

A line of charge with a charge density of $\lambda$ is on the $z$-axis and extends from $z=-1$ to $z=1$. 

1. For $r\gt 1$, find the coefficients $A_l$ and $B_l$ for the potential expressed in the form

$$\psi(r,\theta)=\sum_{l=0}^{\infty}\left(A_lr^l + B_lr^{-l-1}\right)P_l(\cos\theta)$$

where $r$ and $\theta$ are the radial and polar angles in spherical coordinates.

2. For $(y,z)=(1,1)$, <span style="background-color:yellow">Correction: $(s,z)=(1,1)$</span> compute the ratio of the exact potential with the potential found from the above equation using only the $l=0, 1$, and $2$ terms.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
First, we expect the leading order term to be $2k\lambda L/r$, which is the potential for a charge $2L\lambda$ at the origin, where $L=1$.

1.

In the following, the azimuthal symmetry trick is used.

$$\psi(z) = k\int_{-1}^1\frac{\lambda dz'}{|z-z'|}$$

For $z\gt 1$, $|z-z'| = z-z'$. Using this and $u=z-z'$ gives

$$\psi(z) = k\lambda \int_{z-1}^{z+1}\frac{du}{u}=k\lambda[\ln(z+1)-\ln(z-1)]=k\lambda[\ln(1+1/z)-\ln(1-1/z)]$$

Using the expansion for $\delta \lt 1$

$$\ln(1+\delta)=\delta + \frac{\delta^2}{2} + \frac{\delta^3}{3} + ...$$

so for $z\gt 1$,

$$\psi(z) = k\lambda\left(2\frac{1}{z}+\frac{2}{3}\frac{1}{z^3} + \frac{2}{5}\frac{1}{z^5} + ...\right)$$

And from the azimuthal symmetry trick logic it follows that $B_0=2k\lambda$, $B_2=2k\lambda/3$, $B_4=2k\lambda/5$, $...$ or

$$
B_n=
\begin{cases}
\frac{2k\lambda}{l+1} & \text{for }l = 0, 2, ...\\
0 & \text{otherwise}
\end{cases}
$$

so

$$\psi(r,\theta) = \sum_{l=0}^{\infty}\frac{2k\lambda}{2l+1}\frac{1}{r^{2l+1}}P_l(\cos\theta)$$

$(s,z)=(1,1) \Rightarrow (r,\theta) = (\sqrt{2},\pi/4)$.

Using $P_2(x)=(3x^2-1)/2$,

$$P_2(\cos(\pi/4))=P_2(1/\sqrt{2})=\frac{1}{2}(3/2-1)=\frac{1}{4}$$

and so

$$
\begin{align}
\psi(1,1) & \approx k\lambda\left(\frac{2}{\sqrt{2}} + \frac{2}{3}\frac{1}{\sqrt{2}^3}P_2(1/\sqrt{2})\right) \\
& = k\lambda\sqrt{2}\left(1 + \frac{1}{24}\right)\\
& = 1.4371k\lambda
\end{align}
$$

2.

$$\psi(s,z) = k\int_{-1}^1\frac{\lambda dz'}{\sqrt{(z-z')^2 + s^2}}$$

This integral can be looked up or solved using trigonometric substitutions. The result is

$$\psi(s,z) = k\lambda\ln\left[\frac{1+z+\sqrt{(1+z)^2 + s^2}}{z-1+\sqrt{(z-1)^2 + s^2}}\right]$$

$$\psi(1,1) \approx 1.4436k\lambda$$

$$\frac{\psi_{approx}}{\psi_{exact}}\simeq 1.02$$

The following is a Python script that can be used to explore the accuracy using NumPy's Legendre polynomial functions.

```Python
import numpy as np

z = 1
s = 1

N = (1+z)+ np.sqrt((1+z)**2 + s**2)
D = -(1-z) + np.sqrt((1-z)**2 + s**2)
psi_e = np.log(N/D)

r = np.sqrt(s**2 + z**2)
x = z/np.sqrt(s**2 + z**2)
psi_a = 2/r + ((2/3)/np.power(r,3))*(1/2)*(3*x**2-1)

print('Exact: {0:.4f}; Approximate: {1:.4f}; Approximate/Exact: {2:.4f}'
      .format(psi_e, psi_a, psi_a/psi_e))

1. Compute solution out to l = 10
c = np.zeros(10)
for k in range(1,10,2):
    c[k-1] = (2/k)/np.power(r,k)
    
l = np.polynomial.legendre.legval(x,c)
print(l)
```
