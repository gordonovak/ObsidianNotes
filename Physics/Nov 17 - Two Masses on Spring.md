$$\newcommand{\bmat}[1]{\begin{pmatrix}#1\end{pmatrix}}
\newcommand{\dvec}[1]{\overleftrightarrow{#1}}
\newcommand{\prt}[2]{\frac{\partial{#1}}{\partial{#2}}}$$

Consider that we have two masses on a spring, $m_1$ and $m_2$ defined by the potential energy between them as:
$$U(r)=\frac{1}2kr^2$$
The only constraint is that our angular momentum is zero:
$$\ell=0$$
Now, we would usually get the Lagrangian:
$$L=\frac{1}2m_1\dot r^2 + \frac{1}2m_2\dot r^2 - \frac{1}2kr^2$$
However, we should use the mass-reduced mass formulation with:
$$\tilde L_0 = \frac{1}2M\dot R^2+\frac{1}2\mu\dot r^2-\frac{1}2kr^2$$
Here, we have that $M\ddot R =0$, because our center of mass is not accelerating. Thus, we have the following implications:
$$\begin{align*}
M\ddot R = 0&\implies \boxed{\omega = 0}\\
\mu\ddot r = -kr&\implies \boxed{\omega = \sqrt{\frac{k}\mu}}
\end{align*}$$
The boxed equations are called the **Normal Mode Frequencies**
Now, if we look at these equations, it really looks like a single-body problem. However, in more complex objects, we need to consider resonances and multiple objects. 

***
Now, Prabal wants us to know the basics. What does this mean? I have no idea, so he's gonna explain it. 

We'll use the same Lagrangian as before:
$$\boxed{\boxed{\tilde L_0=\frac{1}2m_1\dot x_1^2 + \frac{1}2m_2\dot x_2^2 - \frac{1}2k(x_1-x_2)^2}}$$
Solving our lagrangians gives us the representative equations:
$$\begin{align*}
m_1\ddot x_1&=-k(x_1-x_2)\\
m_2\ddot x_2&=k(x_1-x_2)
\end{align*}$$
If we formulate with linear algebra, we get that:
$$\bmat{m_1 & 0 \\ 0 & m_2}\bmat{\ddot x_1 \\ \ddot x_2}=-\bmat{k & -k \\ -k & k}\bmat{x_1\\ x_2}$$
$$\dvec M \ddot{\vec x} = -\dvec{K}\vec x, \text{ where } \vec x \equiv \bmat{x_1 \\ x_2}$$
Prabal asks, "Are we comfortable with this statement?" (We are making an anzatz to solve the differential equation):
$$\vec x= \vec b e^{i\omega t}$$
$$\ddot{\vec x} = -\omega^2\vec x$$
Now, in the multi-particle system, the system behaves as one mode, so that the $\omega$ is the same for all particles. Although multiple frequencies can propagate through a wave, we can break it down with a Fourier transform into modes, and we can break it down into $\omega$. 

Let's return to the problem. With our anzatz in place, plugging it in gives:
$$\begin{align*}
-\dvec M \omega^2\vec x &= -\dvec K \vec x\\
\dvec{K}\vec x &= \dvec M \omega^2\vec x\\
\dvec{M}^{-1}\dvec K \vec x &= \omega^2 \vec x
\end{align*}$$
Then, we turn that final equation into:
$$\hat H|\psi\rangle = \hbar \omega | \psi\rangle$$
Bugs club!

If we remember quantum mechanics, we see that:
$$i\hbar \prt{}t \psi(t, x)=\cdots$$
Given that:
$$\dvec M ^{-1}= \bmat{\frac{1}{m_1}&0\\0 & \frac{1}{m_2}}$$
We can solve that:
$$\dvec M ^{-1}\dvec K = \bmat{\frac{k}{m_1}&-\frac{k}{m_1}\\ -\frac{k}{m_2}&\frac{k}{m_2}}=\bmat{c & -c \\ -d & d}$$
Now plugging in our $\vec b$ gives that:
$$\bmat{c & -c \\ -d & d}\bmat{b_1 \\b_2}=\omega^2\bmat{b_1\\b_2}$$
Solving our eigenvalue equation gives that (given $\omega\equiv \lambda$)
$$(c-\lambda)(d-\lambda)-cd=0$$
$$\lambda[-(c+d)+\lambda]=0$$
$$\lambda = 0,\; c+d$$
Consider the scenario when $\omega^2 = 0$. We get that:
$$\bmat{c & -c \\ -d & d}\bmat{b_1 & b_2}=\vec0$$
$$\bmat{cb_1-cb_2 \\ -db_1+db_2}=\vec 0$$

Thus, we get that $b_1=b_2$. Thus, because we defined:
$$\vec x= \vec b^{i\omega t}=\frac{1}{\sqrt 2}\bmat{1 \\ 1}b_1e^{0}$$
We call the quantity $$\frac{1}{\sqrt 2}\bmat{1 \\ 1}\equiv e_1$$
Solving the other equation when $\lambda \ne 0$, we get that:
$$\omega ^2 = \frac{k}{m_1}+\frac{k}{m_2}=\left(\frac{1}{m_1}+\frac{1}{m_2}\right)k=\frac{k}\mu$$
Now we have to write down the eigenvalue equation as we did before, and then we follow the procedure:
$$\begin{aligned}
\bmat{ \frac{k}{m_1}(b_1 - b_2) \\-\frac{k}{m_2}(b_1 - b_2) }
&=
\bmat{ \frac{k}{\mu} b_1 \\ \frac{k}{\mu} b_2 }
\end{aligned}
$$
Solving this equation gives that:
$$\frac{b_1}{b_2}=-\frac{m_2}{m_1}$$
Now if we remember from 130, we must enforce the condition that the center of mass must stay at rest:
$$\frac{m_1x_1+m_2x_2}{m_1+m_2}=0\implies -\frac{m_2}{m_1}$$
Wow, how crazy. If we want to write the $e_2$ associated with this mode, we normalize it (with $\sqrt{m_1^2+m_2^2}$ and get that:
$$e_1=\frac{1}{\sqrt{m_1^2+m_2^2}}\bmat{-m_2 \\ m_1}$$
We know this because from our equation $b_1=-\frac{m_2}{m_1}b_2$. 
(In the case where $m_1=m_2$, we get that :
$$e_2=\frac{1}{\sqrt 2}\bmat{-1 \\ 1}$$
