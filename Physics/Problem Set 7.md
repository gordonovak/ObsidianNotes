$$
\newcommand{\prt}[2]{\frac{\partial{#1}}{\partial{#2}}}
\newcommand{\vdot}[1]{\dot{\vec{#1}}}
\newcommand{\p}[1]{\left(#1\right)}
\newcommand{\ddt}[1]{\frac{d #1}{dt}}
\newcommand{\ddtp}[1]{\frac{d}{dt}\left(#1\right)}
\newcommand{\mag}[1]{\left | #1 \right |}
\newcommand{\def}{\equiv}
$$
### Problem 34
*Pendulum*. We're going to start by considering a pendulum given by the Lagrangian:
$$L=\frac{1}2m\ell^2\dot\theta^2+mg\ell\cos\theta$$
###### A: Find the conjugate momentum associated with $\theta$
First, we note the conjugate momentum formula:
$$p=\prt{L}{\dot \theta}$$
Thus, we just evaluate the Lagrangian with respect to $\dot \theta$:
$$\prt{}{\dot \theta}\p{\frac{1}2m\ell^2\dot\theta^2+mg\ell\cos\theta}=m\ell^2\dot\theta$$
###### B: Find the Hamiltonian
First, we have our Hamiltonian formula:
$$H=p\dot q- L$$
Thus, our Hamiltonian must be:
$$H=p\dot \theta - \frac{1}2m\ell^2\dot\theta^2-mg\ell\cos\theta$$
We can double check our work with the fact that $\dot p=\prt{H}{\dot q}$:
$$\begin{align*}
\prt{}{\dot\theta}(H)&=\prt{}{\dot\theta}(m\ell\dot\theta\dot \theta-\frac{1}{2}m\ell^2\dot\theta^2-mg\ell\cos\theta)\\
&=2m\ell^2\dot\theta-m\ell^2\dot\theta\\
&=m\ell^2\dot\theta\\
&=p
\end{align*}$$
And also with $\dot\theta=\prt{H}{p}$
$$\begin{align*}
\prt{H}{\dot\theta}&=\prt{}{\dot\theta}\p{\frac{p^2}{m\ell^2}-\frac{1}{2}\frac{p^2}{m\ell^2}}\\ 
&=\frac{2p}{m\ell^2}-\frac{p}{m\ell^2}\\
&= \frac{p}{m\ell^2}\\
&=\dot\theta
\end{align*}$$
###### C: Use Hamilton's equations to show that $\ddt{H}=0$
Ok, so we just take the derivative with respect to time:
$$\ddt{}\p{m\ell\dot\theta^2-\frac{1}2m\ell^2\dot\theta^2-mg\ell\cos\theta}$$
$$2m\ell^2\dot\theta\ddot\theta-m\ell^2\dot\theta\ddot\theta+mg\ell\sin\theta\dot\theta$$
$$p\dot\theta\ddot\theta+pg\sin\theta\frac{1}\ell\dot\theta$$
Now, we know that via the euler-lagrange,
$$\ddt{}(\prt{L}{\dot\theta})-\prt{L}{\theta}=m\ell^2\ddot\theta+mg\ell\sin\theta=0$$
So that means the internal part of our equation:
$$\dot\theta(p\ddot\theta+mg\ell\sin\theta)\implies0$$
##### D: Use Hamilton's equations to write down equation of motion for $\theta$
Now, consider that:
$$\dot\theta=\prt{H}{p}=\frac{p}{m\ell^2}$$
Now we have that:
$$\ddot\theta = \frac{\dot p}{m\ell^2}=\frac{-mg\ell\sin\theta}{m\ell^2}$$
$$\ddot\theta=-\frac{g}{\ell}\sin\theta$$

### Problem 35
*Mass on a vertical spring*. Consider a vertically aligned mass on a spring for which the Lagrangian is:
$$L=\frac{1}2m\dot y^2-\frac{1}2k(y-y_0)^2-mgy$$
##### A: What is the conjugate momentum?
$$\newcommand{\dth}{\dot\theta}
\newcommand{\ddth}{\dot\dot\theta}
$$
Conjugate momentum is defined as:
$$\prt{H}{\dot y}=p$$
So we get:
$$p=m\dot y$$
##### B: Find the hamiltonian.
$$H=p\dot y - L$$
$$H(y,\dot y) = p\dot y - \frac{1}2my^2-\frac{1}2k(y-y_0)^2-mgy$$
##### C: Apply the Hamilton's equations of motion and show that the correct equation of motion is reproduced
Now note that:
$$\dot p = -k(y-y_0)-mg$$
$$\dot y = \frac{p}m$$
$$\ddot y = \frac{\dot p}m$$
So we get that:
$$\ddot y = \frac{-k(y-y_0)-mg}{m}$$
When $y_0=0$ we get:
$$\ddot y = -\frac{k}my-g$$
### Problem 36
#### Hamiltonian of a relativistic particle
##### A: Use the relativistic Lagrangian, L = $-\gamma^{-1}mc^2$ of a free particle to construct its Hamiltonian. 
$$\newcommand{\gam}{\sqrt{1-\frac{\dot x^2}{c^2}}}$$
$$L=-mc^2\gam $$
We know that the Hamiltonian is given by:
$$H=p\dot x - L$$
So then we find $p$: $p=\prt{L}{\dot x}$.
We get that our partial is:
$$\prt{L}{\dot x}=p=\gamma m\dot x$$
Now our hamiltonian:
$$H(\dot x)=\gamma m\dot x^2+mc^2\gam$$
$$H(\dot x)=mc^2(\gamma\frac{\dot x^2}{c^2}+ \gamma^{-1})$$

$$H(\dot x)=mc^2(\frac{\gamma^2\frac{\dot x^2}{c^2}+ 1}{\gamma})$$
This is not fun to solve:
$$H(\dot x)=mc^2(\frac{\frac{\frac{\dot x^2}{c^2}}{1-\frac{\dot x^2}{c^2}}+ 1}{\gamma})$$
$$H(\dot x)=mc^2(\frac{\frac{\frac{\dot x^2}{c^2}(1+\frac{x^2}{c^2})}{1+\frac{\dot x^4}{c^4}}+ 1}{\gamma})$$
$$H(\dot x)=mc^2(\frac{{\gamma^2-1}+ 1}{\gamma})$$
$$H(\dot x)=mc^2\gamma$$
##### B: Show the hamiltonian reduces to non-relativistic particle
When $v <<c$, we then see that $\gamma$ goes to 1, so we get that:
$$H(\dot x)=mc^2$$
### Problem 37
#### Hamiltonian of the bead
$$L=\frac{1}2mR^2\dot\theta^2+\frac{1}2m(R\sin\theta)^2\Omega^2+mgR\cos\theta$$
##### A: Conjugate momentum
$$p=\prt{L}{\dot \theta}=mR^2\dot\theta$$
##### B: The hamiltonian is defined as:
$$H=p\dot\theta - L$$
What should the Hamiltonian be a function of?
It should be dependent on $\dot \theta$ and $\theta$. 
##### C: Find the Hamiltonian of the system and show that it is conserved. 
We have that:
$$H = p\dot\theta -\frac{1}2mR^2\dot\theta^2-\frac{1}2m(R\sin\theta)^2\Omega^2-mgR\cos\theta$$
Now we find derivative with respect to time. 
$$\ddt{H}=\dot p \dot \theta + p\ddot \theta-\frac{1}2mR^2\dot\theta\theta-\frac{1}2m(R^2\sin\theta)\cos\theta\Omega^2\dot\theta+mgR\sin\theta\dot\theta$$
Then, we can perform substitutions for:
$$\dot p = \prt{H}{\theta}=m(R^2\sin\theta\cos\theta\Omega^2)-mgR\sin\theta$$
And substituting in we get that:
$$\ddt{H}=0+0-0+p\ddot\theta-mR^2\ddot\theta\dot\theta=0$$
##### D: Find the energy of the system
We just do the Lagrangian but we do energy + potential:
$$E=\frac{1}2mR^2\dot\theta^2+\frac{1}2m(R\sin\theta)^2\Omega^2+mgR\cos\theta$$
##### Discuss (with proof) whether the energy of the system is conserved
We take the derivative with respect to the time of energy and hope that everything works out:
$$\ddt{E}=mR^2\dot\theta\ddot\theta+mR^2\sin\theta\cos\theta\Omega^2\dot\theta-mgR\sin\theta\dot\theta$$
If we recall from our hamiltonian:
$$p=mR\dot\theta$$
And that
$$\dot p = \prt{H}{\theta}=m(R^2\sin\theta\cos\theta\Omega^2)+mgR\sin\theta$$
Thus, we get that with substituting in:
$$\ddt{E}=p\ddot \theta+0-0-p\ddot\theta + m(R^2\sin\theta\cos\theta\Omega^2)$$
Here, our terms don't cancel properly, and we're left with the $\Omega^2$ term. Thus, Energy is not conserved?