---
layout: default
title: "Linear Algebra: Vectors"
parent: Mathematics
has_children: false
---

# Linear Algebra
This is a very short introduction. 
Linear algebra is vast and you can get as much accurate as you want in definitions, proofs, and so on. 
That is not what we want to do here. 
You will learn the basic definitions and operations on vectors and matrices. 
These basics concepts are enough to get started with quantum computing.

## Vector
a vector is an ordered set of numbers.
For example $$\bm{v} = (-1, 0.5, 3)$$ is a vector.[^1] 
It contains three numbers which are also called the _elements_. 
A vector can have any number of elements. 
A vector with only one element is just a scalar (just a number). 

### Column vs Row
There are two ways to list the elements of a vector. In a _row_ 

$$
\bm{v} = 
\begin{pmatrix}
-1 & 0.5 & 3
\end{pmatrix}
$$

or in a _column_ 

$$
\bm{u} = 
\begin{pmatrix}
-1 \\ 0.5 \\ 3
\end{pmatrix}
$$

The row vector $$\bm{v}$$ and the column vector $$\bm{u}$$ are considered to be different.
That is why I used two different letters to represent them. 
There is an operation that relates these two to each other. 
It's called **transpose** and is shown by T in the superscript. 

$$
\bm{v}^T = \bm{u} \\ 
\bm{u}^T = \bm{v} \\  
$$

If you transpose a vector twice, you get the same vector. 

$$
(\bm{v}^T)^T = \bm{v}
$$

### Scalar multiplication 
You can multiply a vector by a scalar (which is just a number). 
For that, you would just need to multiply individual elements of the vector by that same scalar. 

$$
a\bm{u} = 
\begin{pmatrix}
-a \\ 0.5a \\ 3a
\end{pmatrix}
$$




## Footnote
[^1]: A boldface variable $$\bm{v}$$ is usually used to denote a vector. Another way of denoting a vector is to put an arrow on top $$\overrightarrow{v}$$. I'm going to stick to the boldface notation. 


