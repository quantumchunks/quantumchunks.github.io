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
The order matters. [^1]  

## Real-imaginary representation
A complex number, $$z = (a, b)$$, can also be represented by 

$$z = a + ib$$ 

where $$a$$ is called the real part, $$ib$$ is called the imaginary part, and $$i$$ is the imaginary unit.  
The **imaginary unit** has a specific definition that is $$i = \sqrt{-1}$$. As you know, negative numbers do not have any real roots. That is why $$i$$ is called imaginary. 
Now the product of a real number $$b$$ and the imaginary unit will be an imaginary number. That is why $$ib$$ is imaginary. 

## Rules of manipulation 
In addition to being an ordered set of two numbers, complex numbers need to follow certain rules of addition, multiplication, and conjugation. 

### Addition
Adding two complex numbers is straightforward. Just add the real parts together and add the imaginary parts together.  

$$
z_1 = a + ib \\
z_2 = c + id \\
z_1 + z_2 = (a + c) + i(b + d) 
$$

### Real multiplication 
To multiply a complex number by a real number $$r$$, you would just multiply each part by $$r$$

$$
rz = ra + irb
$$

### Negation 
The negative of a complex number is obtained by multiplying it by $$-1$$ that is negating the real and imaginary parts individually.

$$
-z = -a - ib
$$

### Subtraction 
Subtracting two complex numbers $$z_1 - z_2$$ is equal to adding the first one to the negative of the second one $$z_1 + (-z_2)$$. 

$$
z_1 - z_2 = (a - c) + i(b - d) 
$$

### Complex Multiplication 
We can actually figure out the rules of multiplying two complex numbers on our own if we use the real-imaginary representation. 
Assume we have two complex numbers $$z_1 = a + ib$$ and $$z_2 = c + id$$. 
Let's multiply these two numbers the same way we do for unknown variables in normal algebra, that is  

$$
z_1 z_2 = (a + ib)(c + id) = ac + iad + ibc + i^2bd
$$

From the definition of imaginary unit $$i = \sqrt{-1}$$ you can see that $$i^2$$ is simply equal to $$-1$$ which is a real number! 
Now let's bundle up the real parts together and the imaginary parts together and come up with a more compact expression for multiplication 

$$
z_1 z_2 = (ac - bd) + i(ad + bc)
$$

### Conjugation 
Conjugation is a fancy name for when you negate the imaginary part of a complex number, that is you multiply the imaginary part by $$-1$$. 
To show that a complex number is conjugated you would add an asterisk on the top right corner of the symbol. 

$$
z = a + ib \rightarrow z^* = a - ib
$$

As a result, if you conjugate a complex number twice you will get the original number 

$$
(z^*)^* = z
$$


## Absolute Value
The absolute value of a complex number $$z$$ tells us how big the complex number is.
It is denoted by $$|z|$$ and is defined as the square root of the multiplication of the complex number with its own conjugate. 

$$
|z| = \sqrt{zz^*}
$$


## Practice Problems 
**1. Division**: Figure out the expression for dividing two complex numbers. 

[Solutions](sol){: .btn target="_blank"}

## Footnote
[^1]: It might be tempting to think of a complex number as a vector and we will do that in later sections. However, they are not any ordinary vectors. For example the rules of multiplication are different for complex numbers from what you have seen with normal vectors in linear algebra. 