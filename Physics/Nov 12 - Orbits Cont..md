$$
\newcommand{\prt}[2]{\frac{\partial{#1}}{\partial{#2}}}
\newcommand{\vdot}[1]{\dot{\vec{#1}}}
\newcommand{\p}[1]{\left(#1\right)}
\newcommand{\ddt}[1]{\frac{d #1}{dt}}
\newcommand{\ddtp}[1]{\frac{d}{dt}\left(#1\right)}
\newcommand{\mag}[1]{\left | #1 \right |}
\newcommand{\def}{\equiv}
$$
When we throw something with enough velocity, it is possible to analyze that the object says in a perfect circular orbit. So, what we want to do is to move from:
$$U\to U_{eff}$$
If this orbit was **unstable**, it'll crash into the object or oscillate up and down along the particular circular path. The way we are tackling this problem is looking at the one-body Lagrangian:
$$L=\frac{1}2\dot \mu \dot r ^2 + \frac{1}2 \mu r^2\dot \phi^2 - U(r)$$
***
Now we say that: $\mag{\vec L}\equiv \ell$ 
Thus, we have that : $\vec L = \vec r \times \vec p$.
Taking the derivative gives us that:
$$\begin{align*}
\ddt{\vec L}&=\frac{1}mm\ddt{\vec r}\times \vec p + \vec r \times \ddt{\vec p}\\
&= \vec r \times \ddt{\vec p}\end{align*}
$$
Note that $m\ddt{\vec r}= \vec p$, thus $\vec p \times \vec p= 0$.
Now, we know that $\ddt{\vec p} = \vec F_{\text{net}}$

Prabal claims that the torque $\p{\vec r \times \ddt{\vec p}}=0$, and that's because we can't have any movement into the $z$ axis for this problem. 
***
Let's return to our Lagrangian:
$$L=\frac{1}2\dot \mu \dot r ^2 + \frac{1}2 \mu r^2\dot \phi^2 - U(r)$$
We know here that because we have no dependence on $\phi$, that via. the Euler Lagrange:
$$\ddtp{\prt{L}{\dot \phi}}=0$$
Now we define $\prt{L}{\dot \phi}\def \ell$. Thus we nkow:
$$\begin{align*}
\prt{L}{\dot \phi}&=r^2\mu \dot \phi\\
&=r\cdot \mu r \dot\phi
\end{align*}$$
And we know that $r\def \mag{\vec r}$ and $\mu r \dot \phi \def \mag{\vec p_\phi}$. So, we can write:
$$r\cdot \mu r \dot \phi = \mag{\vec r} \mag{\vec {p_\phi}}\sin(90˚)$$
***
So now we have this $\ell$, this conserved quantity $\ell \equiv r\cdot \mu r \dot\phi$, and we can write:
$$\dot \phi \def \frac{\ell}{\mu r^2}$$
Solving our Euler-Lagrangian for $r$:
$$\ddtp{\prt{L}{\dot r}}=\prt{L}r$$
Gives us that:
$$\begin{align*}
\mu \ddot r &= \mu r \dot \phi ^2 - \prt{U}r \def -\prt{U_{eff}}{r}\\
&= \frac{\ell^2}{r^3}-\prt{U}r\\
&=-\prt{}r\p{\frac{\ell^2}{2\mu r^2}+U(r)}
\end{align*}$$
Where we have that $\p{\frac{\ell}{2\mu r^2}+U(r)}=U_{eff}$.
***
Now our goal is to solve two example problems!
1. Find $r_0$ using $U_{eff}$
	We know that:
	$\to \frac{dU_{eff}}{dr}=0\implies r_0 = ?$
	$\to\frac{d^2U_{eff}}{dr^2}$
	So, let's solve this!
	$$\begin{align*}
	0&=\frac{d}{dr}U_{eff}=\frac{d}{dr}\p{\frac{\ell^2}{2\mu r^2}-\frac{\alpha}r}\\
	&=-\frac{\ell^2}{4\mu r^3}+\frac{\alpha}{r^2}=0\\
	&\Rightarrow\frac{\ell^2}{\mu}=\alpha r
	\end{align*}$$
	Thus, we get that:
	$$\boxed{r_0=\frac{\ell^2}{\mu\alpha}}$$
2. Determine $\omega_r$ for small oscillations