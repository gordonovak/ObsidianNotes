$$
\newcommand{\prt}[2]{\frac{\partial{#1}}{\partial{#2}}}
\newcommand{\vdot}[1]{\dot{\vec{#1}}}
\newcommand{\p}[1]{\left(#1\right)}
\newcommand{\ddt}[1]{\frac{d}{dt}\left(#1\right)}
$$
We have a puzzle where we have a mass rotating around an object (due to gravity). 
It has potential:
$$U=-\frac{\alpha}r, \;\alpha \equiv Gm_1m_2$$
However, if we look at the potential well, this doesn't really work, because we should see the potential well just fall all the way down. 

Thus, we consider the Lagrangian of the system:
$$\tilde L=\frac{1}2m_1\dot{\vec r_1}\cdot\dot{\vec r_1}+\frac{1}2m_2\dot{\vec r_2}\cdot\dot{\vec r_2}-U(r)$$
We can rewrite our Lagrangian as:
$$=\frac{1}2\mathrm M\dot{\vec R}\cdot\dot{\vec R}+\frac{1}2\mu\dot{\vec r}\cdot\dot{\vec r}-U(r)$$
(This is just algebraic manipulation)
Essentially with $\mathrm M = m_1+m_2$. 
Then, we label the second part of the equation to be:
$$L=\frac{1}2\mu\dot{\vec r}\cdot\dot{\vec r}-U(r)$$
Why are we doing this?

This allows us to separate our system such that: $\mathrm M$ is our center of mass, which is not dependent on $U(r)$ and then we get an effective potential energy $U_{eff}$ with the second part of the equation (which we labeled $L$). 

How do we find $\mu$? Easy. Prabal just says: 
$$\frac{1}\mu = \frac{1}{m_1}+\frac{1}{m_2}$$
However, if our $m_1$ is really really big, (like the earth with a pen), this equation just becomes:
$$\frac{1}\mu = \frac{1}{m_2}\implies \mu = m_2$$
($\mu$ is a reduced mass) Note that in this scenario that:
$$\vec R \equiv \frac{m_1\vec {r_1}+m_2\vec{r_2}}{m_1+m_2}$$
$$F=\frac{mv^2}r\implies ma=\frac{mv^2}r\implies r=\frac{\dot x^2}{\ddot x}$$Then, we can combine this with our gravity equation to get:
$$-\frac{mv^2}r\hat r = -\frac{\alpha}r^2\hat r \implies r = \frac{\alpha}{mv^2}$$
So now that we have redefined our Lagrangian, let's try and solve this problem with Lagrangian mechanics rather than with our Analytical tools. Consider:
$$L=\frac{1}2\mu\dot{\vec r} \cdot \dot{\vec r}-U(r)$$
$$\dot{\vec r}=\dot r \hat r + r \dot \phi \hat\phi$$
$$L=\frac{1}2\mu\dot r ^2+\frac{1}2 \mu r^2\dot \phi ^2 - U(r), \quad U(r)\equiv \alpha/r$$
First, we write the Lagrangian for $\phi$. 
$$\frac{d}{dt}\left(\frac{\partial L}{\partial \dot\phi} \right)= \frac{\partial L}{\partial \phi}=0\implies \prt{L}{\dot\phi}=\mu r^2\dot \phi \equiv \ell$$
$$\ddt{\prt{L}{\dot r}}=\prt{L}r$$
$$\ddt{\mu\dot r}=-\prt{}{r}\p{-\frac{1}2\mu r^2\dot\phi ^2 + U(r)}$$
$$=-\prt{}{r}\p{-\frac{1}2\mu r^2\p{\frac{\ell}{\mu r^2}}^2+U(r)}$$
Thus we get that:
$$\mu\ddot r = -\prt{}r\p{-\frac{\ell^2}{\mu r^2}+U(r)}$$
Now we have found our effective potential energy:
$$U_{eff}=-\frac{\ell^2}{\mu r ^2} + U(r)$$
