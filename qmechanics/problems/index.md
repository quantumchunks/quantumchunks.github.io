---
layout: default
title: Problems
parent: Quantum Mechanics
has_children: false
---

# Normalized wave function stays normalized
How do we know if the wave function stays normalized as it evolves in time? [^1] 

**Solution**  
The answer is in the Schrodinger equation which describes the time evolution of the wave function. 
Imagine a particle with the wave function $$\psi(x, t)$$ in a one-dimensional world with potential energy $$V(x)$$. 
The Schrodinger equation for this particle is 

$$
i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\psi}{\partial x^2} + V\psi. 
$$

Now, let's see what happens if we take the total derivative of the norm of the wave function $$\int\vert\psi\vert^2 dx$$ with respect to time which is equivalent to 

$$
\frac{d}{dt}\int_{-\infty}^{\infty}|\psi|^2 dx = \int_{-\infty}^{\infty}\frac{\partial}{\partial t}|\psi(x, t)|^2 dx.
$$

Since $$\vert\psi\vert^2 = \psi^*\psi$$, we can use the product rule to write the integrand as 

$$
\frac{\partial}{\partial t} |\psi|^2 = \frac{\partial\psi^*}{\partial t}\psi + \psi^* \frac{\partial\psi}{\partial t}.
$$

From the Schrodinger equation and its complex conjugate we know 

$$
i\hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\psi}{\partial x^2} + V\psi,
$$

$$
-i\hbar \frac{\partial \psi^*}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\psi^*}{\partial x^2} + V\psi^*. 
$$

Using this we can rewrite the integrand as

$$
\frac{\partial}{\partial t} |\psi|^2 = \frac{-i\hbar}{2m}\bigg(\frac{\partial^2\psi^*}{\partial x^2}\psi - \psi^*\frac{\partial^2\psi}{\partial x^2}\bigg). 
$$

Let's add and subtract $$(\partial\psi^*/\partial_x)(\partial\psi/\partial_x)$$ so that the right hand side becomes  

$$
\frac{-i\hbar}{2m}\bigg(\frac{\partial^2\psi^*}{\partial x^2}\psi + \frac{\partial\psi^*}{\partial x}\frac{\partial\psi}{\partial x} - \frac{\partial\psi^*}{\partial x}\frac{\partial\psi}{\partial x} - \psi^*\frac{\partial^2\psi}{\partial x^2}\bigg). 
$$

Now it's easy to see that we can factor out a partial derivative with respect to $$x$$ 

$$
\frac{-i\hbar}{2m}\frac{\partial}{\partial x}\bigg(\frac{\partial\psi^*}{\partial x}\psi - \psi^*\frac{\partial\psi}{\partial x}\bigg).
$$

Therefore, the integral is simply evaluated as

$$
\int_{-\infty}^{\infty}\frac{\partial}{\partial t}|\psi|^2 dx = \frac{-i\hbar}{2m}\bigg(\frac{\partial\psi^*}{\partial x}\psi - \psi^*\frac{\partial\psi}{\partial x}\bigg)\bigg|_{-\infty}^{\infty}. 
$$

The wave function $$\psi(x, t)$$ should approach zero in the limit $$x\rightarrow\pm\infty$$ in order to be square integrable and normalizable. As a result, the right hand side amounts to zero.  
Therefore, the time derivative of the norm is zero, 

$$
\frac{d}{dt}\int_{-\infty}^{\infty}|\psi|^2 dx = 0, 
$$

which means that the Schrodinger equation keeps the wave function normalized. 

[^1]: Of course we are assuming that the wave function is not being measured as it evolves. 