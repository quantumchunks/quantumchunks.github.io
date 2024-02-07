---
layout: default
title: Complex Numbers
parent: Mathematics
has_children: false
---

# Complex Numbers 

This is a brief introduction to complex numbers and some essential concepts that are used in quantum mechanics and quantum computing. 
Historically, complex numbers were used in quantum mechanics to represent the wavefunction of a quantum object like electrons. 
In quantum computing, complex numbers are used to specify the states of qubits. 
You usually need more than one complex number to specify all the state of a quantum object or a quantum computer. 

## What is a complex number 
A complex number is a special ordered set of two real numbers. 
It is usually represented by $$c$$ or $$z$$. 
For example $$c = (1, -2)$$ is a complex number and is different from $$c' = (-2, 1)$$ which is another complex number. 
The order matters.  

## Real-imaginary representation
A complex number, $$z = (a, b)$$, can also be represented by 

$$z = a + ib$$ 

where $$a$$ is called the real part, $$ib$$ is called the imaginary part, and $$i$$ is the imaginary unit.  
The imaginary unit has a specific definition that is $$i = \sqrt{-1}$$. As you know, negative numbers do not have any real roots. That is why $$i$$ is called imaginary. 
Now the product of a real number $$b$$ and the imaginary unit will be an imaginary number. That is why $$ib$$ is imaginary. 

## Rules of manipulation 
In addition to being an ordered set of two numbers, complex numbers need to follow certain rules of addition, multiplication, and conjugation. 

### Addition
Adding two complex numbers is straightforward. You just add the real parts together and add the imaginary parts together.  

$$
z_1 = a + ib \\
z_2 = c + id \\
z_1 + z_2 = (a + c) + i(b + d) 
$$

### Negation 
The negative of a complex number is obtained by negating the real and imaginary parts individually.

$$
-z = -a - ib
$$

### Subtraction 
Subtracting two complex numbers $$z_1 - z_2$$ is equal to adding the first one to the negative of the second one $$z_1 + (-z_2)$$. 

$$
z_1 - z_2 = (a - c) + i(b - d) 
$$

### Multiplication 

