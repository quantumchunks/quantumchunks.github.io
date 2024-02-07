---
layout: default
title: Qubit
parent: Quantum Computing
has_children: false
nav_order: 1
---

Here you will learn the mathematics of representing quantum information and quantum computing operations. 

# Qubit 
A qubit is represented by a two-dimensional complex vector usually denoted by $$|\psi\rangle$$. 
Historically $$\psi$$ is used as the wavefunction of a quantum particle like an electron or any other object that behaves quantum mechanically. 

## Ket and Bra
The $$|\rangle $$ is called a *ket* introduced by Paul Dirac. It's a way of distinguishing a column vector $$|v\rangle$$ (ket) from its dual row vector $$\langle v|$$ (called *bra*). 
The state of the qubit, $$|\psi\rangle$$, can be explicitly written as a two component column vector  

$$
|\psi\rangle = 
\begin{pmatrix}
c_1 \\  
c_2 
\end{pmatrix}
$$

where $$c_1$$ and $$c_2$$ are complex numbers. 
The qubit can also be represented by its dual row vector  

$$
\langle\psi| = 
\begin{pmatrix}
c_1^* & 
c_2^* 
\end{pmatrix}
$$

These two representations are considered equal.  

## Inner product and normalization 
Now, the elements of the state vector $$c_1$$ and $$c_2$$ cannot be any numbers as they are limited by the *normalization* condition. 
It is a postulate of quantum mechanics that the state of a qubit is normalized which means the magnitude of the state vector is **unity**. 
By definition the magnitude (or norm) of a complex vector $$\|\psi\|$$ is equal to the square root of its inner product with its dual row vector.  

$$
\|\psi\| = \sqrt{\langle \psi | \cdot | \psi \rangle} 
$$

The inner product $$\langle \psi | \cdot | \psi \rangle$$ is often abbreviated as $$\langle \psi | \psi \rangle$$. 
It is worth mentioning that the inner product is always defined between a *bra* and a *ket*. Hence, called bracket.  
We can write the inner product explicitly in terms of $$c_1$$ and $$c_2$$ 

$$
\langle \psi | \psi \rangle = 
\begin{pmatrix}
c_1^* & 
c_2^* 
\end{pmatrix}
\begin{pmatrix}
c_1 \\  
c_2 
\end{pmatrix}
= |c_1|^2 + |c_2|^2. 
$$

Again, the normalization dictates that $$\sqrt{\langle\psi|\psi\rangle}=1$$.  
In other words 

$$
\sqrt{|c_1|^2 + |c_2|^2} = 1.
$$

## Rays 
Let's assume we have a qubit at a specific state $$$$

# Single Qubit Gates
Gates are operations that change the state of qubits. That is what quantum *computing* means. You *compute* by applying gates on your qubits. 


# Multiple Qubits 
The 