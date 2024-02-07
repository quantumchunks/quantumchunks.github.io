---
layout: default
title: Complex Numbers Solution
parent: Mathematics
has_children: false
nav_exclude: true
---

# Solutions to Complex Numbers

**1. Division**: Figure out the expression for dividing two complex numbers.  

Assume two complex numbers $$z_1 = a + ib$$ and $$z_2 = c + id$$.  
We want to figure out how to divide $$z_1$$ by $$z_2$$. 
First, we multiply both with $$z_2^*$$. 
That won't change the ratio

$$
\frac{z_1}{z_2} = \frac{z_1z_2^*}{z_2z_2^*}. 
$$

Notice that the denominator is just a real number $$z_2z_2^* = |z_2|^2 = c^2 + d^2$$. 
So dividing by $$|z_2|^2$$ is just like a scalar multiplication by $$1/|z_2|^2$$. 
Therefore, we just need to calculate $$z_1z_2^*$$. 

$$
z_1z_2^* = (ac + bd) + i(-ad + bc)
$$

Finally, rescaling this by $$1/(c^2 + d^2)$$ leads us to the final expression for division 

$$
\frac{z_1}{z_2} = \frac{1}{c^2 + d^2} [(ac + bd) + i(-ad + bc)]
$$

