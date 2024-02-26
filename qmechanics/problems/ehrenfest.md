---
layout: default
title: Ehrenfest's Theorem
parent: Problems
has_children: false
---

# Ehrenfest's Theorem
Ehrenfest's theorem bridges the gap between classical and quantum mechanics. 
It states that in quantum mechanics the **expectation values** obey classical laws. 
For example, the expectation values of position $$\langle x\rangle$$ and momentum $$\langle p\rangle$$ are related as follows 

$$
\langle p\rangle = m\frac{d\langle x\rangle}{dt}. 
$$

Or the Newton's second law still works for the expectation value of momentum $$\langle p\rangle$$ and force $$\langle -\partial_xV\rangle$$ where $$V(x)$$ is the potential energy 

$$
\frac{d\langle p\rangle}{dt} = \langle -\frac{\partial V}{\partial x}\rangle. 
$$

What is meant by an *expectation value*, you might ask. 
Assume a particle that behaves quantum mechanically. It has a wave function $$\psi(x)$$ that spreads over a region in space. 
The expectation value of its position, which is denoted by $$\langle x\rangle$$ is a statistical measure.  

Before I tell you what $$\langle x\rangle$$ means, I want to emphasize what it doesn't. 
It does **NOT** mean the average position if you measure the position of the same particle over and over again.
The reason is that the first time you measure the position of a particle its wave function collapses and the following measurements are not going to be independent. 
What the expectation value actually means is that if you had an **ensemble** of identically prepared particles (same initial wave function) and you measured their positions all at once and you took the average of those values, you'd get a number close to $$\langle x\rangle$$. [^1]

## Proof 
Proving Ehrenfest's theorem is straightforward. It is an opportunity to practice our skills in integration by parts and the product formula for derivatives. 

### First relation 
To _prove_ the first relation we need to take the definition of momentum operator $$p = -i\hbar\partial_x$$ as given otherwise it would be a circular proof. 
Let's start by taking the time derivative of $$\langle x\rangle$$, 

$$
\frac{d\langle x\rangle}{dt} = \int_{-\infty}^{\infty} \frac{\partial}{\partial t} x |\psi|^2 dx = \int_{-\infty}^{\infty} x\bigg(\frac{\partial \psi^*}{\partial t}\psi + \psi^*\frac{\partial \psi}{\partial t}\bigg)dx. 
$$

Using Schrodinger equation and its complex conjugate we can replace the time derivatives with second order spatial derivatives

$$
\frac{d\langle x\rangle}{dt} = -\frac{i\hbar}{2m}\int_{-\infty}^{\infty} x\bigg(\frac{\partial^2 \psi^*}{\partial x^2}\psi - \psi^*\frac{\partial^2 \psi}{\partial x^2}\bigg)dx. 
$$

Adding and removing $$\partial_x\psi^*\partial_x\psi$$ inside parentheses results in 

$$
\frac{d\langle x\rangle}{dt} = -\frac{i\hbar}{2m}\int_{-\infty}^{\infty} x\bigg(\frac{\partial^2 \psi^*}{\partial x^2}\psi + \frac{\partial \psi^*}{\partial x}\frac{\partial \psi}{\partial x} - \frac{\partial \psi^*}{\partial x}\frac{\partial \psi}{\partial x} - \psi^*\frac{\partial^2 \psi}{\partial x^2}\bigg)dx, 
$$

$$
= -\frac{i\hbar}{2m}\int_{-\infty}^{\infty} x\frac{\partial}{\partial x}\bigg(\frac{\partial \psi^*}{\partial x}\psi - \psi^*\frac{\partial \psi}{\partial x}\bigg)dx. 
$$

Integration by parts leads us to 

$$
\frac{d\langle x\rangle}{dt} = -\frac{i\hbar}{2m}\bigg[x\bigg(\frac{\partial \psi^*}{\partial x}\psi - \psi^*\frac{\partial \psi}{\partial x}\bigg)\bigg|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} \bigg(\frac{\partial \psi^*}{\partial x}\psi - \psi^*\frac{\partial \psi}{\partial x}\bigg)dx\bigg]. 
$$

Assuming that the wave function decays at least as fast as $$1/\sqrt{|x|}$$, we can convince ourselves that the boundary term is zero. [^2] 
Let's do another integration by parts, this time on the first term inside the integral above. 
That gives us another boundary term which is zero and another integrand of the form $$\psi^*\partial_x\psi$$. 
Therefore, 

$$
\frac{d\langle x\rangle}{dt} = -\frac{i\hbar}{2m} \int_{-\infty}^{\infty} 2\psi^*\frac{\partial \psi}{\partial x} dx.
$$

Rearranging the variables we arrive at 

$$
m\frac{d\langle x\rangle}{dt} = \int_{-\infty}^{\infty} \psi^*\bigg(-i\hbar\frac{\partial}{\partial x}\bigg)\psi dx = \langle p\rangle.
$$

### Second relation 
To prove the second relation, we start with the time derivative of momentum

$$
\frac{d\langle p\rangle}{dt} = -i\hbar \int_{-\infty}^{\infty} \frac{\partial}{\partial t} \bigg(\psi^*\frac{\partial \psi}{\partial x}\bigg) dx.
$$

Apply the product formula 

$$
\frac{d\langle p\rangle}{dt} = -i\hbar \int_{-\infty}^{\infty} \bigg(\frac{\partial \psi^*}{\partial t}\frac{\partial \psi}{\partial x} + \psi^*\frac{\partial^2 \psi}{\partial t\partial x}\bigg) dx. 
$$

Use [Schrodinger equation](normalized) to replace the time derivatives with spatial derivatives and the potential energy 

$$
\frac{d\langle p\rangle}{dt} = \int_{-\infty}^{\infty} \bigg[\bigg(-\frac{\hbar^2}{2m}\frac{\partial^2 \psi^*}{\partial x^2} + V\psi^*\bigg)\frac{\partial \psi}{\partial x} + \psi^*\frac{\partial}{\partial x}\bigg(\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial x^2} - V\psi\bigg)\bigg] dx, 
$$

$$
\frac{d\langle p\rangle}{dt} = \int_{-\infty}^{\infty} \bigg[-\frac{\hbar^2}{2m}\bigg(\frac{\partial^2 \psi^*}{\partial x^2}\frac{\partial \psi}{\partial x} - \psi^*\frac{\partial^3 \psi}{\partial x^3}\bigg) + \bigg(V\psi^* \frac{\partial \psi}{\partial x} - \psi^*\frac{\partial (V\psi)}{\partial x} \bigg) \bigg] dx, 
$$

Note that $$\psi^*\partial_x(V\psi) = \psi^*(\partial_xV)\psi + \psi^*V\partial_x\psi$$. Therefore, the second term in the integrand reduces to $$\psi^*(\partial_xV)\psi$$. 
Moreover, using integration by parts we can replace the $$\psi^*\partial^3_x\psi$$ term with 

$$
\int_{-\infty}^{\infty} \psi^*\frac{\partial^3 \psi}{\partial x^3} dx = \psi^*\frac{\partial^2 \psi}{\partial x^2}\bigg|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} \frac{\partial \psi^*}{\partial x}\frac{\partial^2 \psi}{\partial x^2} dx.
$$

The boundary term is zero as the wave function and its derivatives approach zero at infinity. Therefore, 

$$
\frac{d\langle p\rangle}{dt} = \int_{-\infty}^{\infty} \bigg[-\frac{\hbar^2}{2m}\bigg(\frac{\partial^2 \psi^*}{\partial x^2}\frac{\partial \psi}{\partial x} + \frac{\partial \psi^*}{\partial x}\frac{\partial^2 \psi}{\partial x^2}\bigg) - \psi^* \frac{\partial V}{\partial x}\psi \bigg] dx, 
$$

$$
\frac{d\langle p\rangle}{dt} = \int_{-\infty}^{\infty} \bigg[-\frac{\hbar^2}{2m}\frac{\partial}{\partial_x}\bigg(\frac{\partial \psi^*}{\partial x}\frac{\partial \psi}{\partial x}\bigg) - \psi^* \frac{\partial V}{\partial x}\psi \bigg] dx.
$$

The first term of the integrand becomes a boundary term after integration 

$$
\int_{-\infty}^{\infty} \frac{\partial}{\partial_x}\bigg(\frac{\partial \psi^*}{\partial x}\frac{\partial \psi}{\partial x}\bigg)dx = \frac{\partial \psi^*}{\partial x}\frac{\partial \psi}{\partial x} \bigg|_{-\infty}^{\infty}=0
$$

which amounts to zero as the wave function approaches zero at infinity. 
Finally we are left with

$$
\frac{d\langle p\rangle}{dt} = \int_{-\infty}^{\infty} \psi^* \bigg(-\frac{\partial V}{\partial x}\bigg)\psi dx = \langle -\frac{\partial V}{\partial x}\rangle.
$$

## Footnote 
[^1]: The ensemble average is not always exactly the same as the expectation value but it approaches the expectation value as your sample size gets larger and larger. 
[^2]: This assumption breaks down in the case of a plane wave.
