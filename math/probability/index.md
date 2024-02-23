---
layout: default
title: Probability Theory
parent: Mathematics
has_children: false
---

# Probability Theory
Quantum theory has a probabilistic interpretation. 
There is an inherent uncertainty in determining physical quantities in quantum mechanics. 
For example, you can't determine the position and velocity of an electron simultaneously. 
It's just a direct consequence of the math that is used in quantum mechanics. 
Same is true for qubits which are quantum mechanical objects. 
You can't determine the exact state of any arbitrary qubit.
But, you _can_ describe the state of a qubit probabilistically and measure the qubit and get a value as a result. 
However, this does not guarantee that if you prepare the same qubit and measure it again, the result would be the same. 
The point I'm trying to make is that probability theory is necessary in understanding how a quantum object behaves or a quantum computer operates.  

Here, you will learn the basics of probability theory. 

// talk about probabilistic events and random experiments and outcomes 

## Sample space 
The sample space contains all the possible **outcomes** of a random experiment (such as tossing coins, rolling dice, or measuring qubits). 
Mathematically it is defined as a **set** and is usually denoted by $$S$$. 
For example, the sample space of an experiment involving a single coin toss is a set with two members heads and tails 

$$
S = \{H, T\}.
$$

Rolling a 6-sided die has the following sample space 

$$
S = \{1, 2, 3, 4, 5, 6\}.
$$

**Measuring a qubit** is not exactly similar to a coin toss, though its sample space has two members as well 

$$
S = \{\uparrow, \downarrow\}.
$$ 

The up and down arrows signify the possible values for measuring the spin of an electron (spin-up and spin-dowwn). An electron's spin is equivalent to a qubit. [^1]

## Probability 
Each outcome $$s$$ has a probability of occurrence $$P(s)$$ that is a positive number less than or equal to 1 ($$0< P(s) \le 1$$). 
Common sense guides us to establish an axiom that the probabilities of all outcomes add up to 1. 
Mathematically, the axiom is written as [^2]

$$
\sum_{s \in S} P(s) = 1. 
$$

### No prior assumption 
In the absence of any prior assumptions, all the outcomes of an experiment are considered to have **equal probabilities**. 
For example in a die roll each side has a probability of 1/6, that is  

$$
P(1) = P(2) = P(3) = P(4) = P(5) = P(6) = \frac{1}{6}.
$$

Or in the case of two coin tosses with the sample space $$S = \{HH, HT, TH, TT\}$$ each outcome has a probability of 1/4 that is 

$$
P(HH) = P(HT) = P(TH) = P(TT) = \frac{1}{4}.
$$

## Event 
An event $$E$$ is a _subset_ of the sample sample space $$E \subset S$$. 
The probability of an event is the sum of probabilities of its outcomes, that is 

$$
P(E) = \sum_{s \in E} P(s) \le 1.
$$

For example, in tossing two coins, the event for the first coin being tails is $$E = \{TH, TT\}$$ and the probability of this event is $$P(E) = P(TH) + P(TT) = 1/2$$. 
Similarly if we measure the spin of two electrons (or measure the state of two qubits) the sample space would be $$S = \{\uparrow\uparrow, \uparrow\downarrow, \downarrow\uparrow, \downarrow\downarrow\}$$ and the event of first electron having an up spin would be $$E = \{\uparrow\uparrow, \uparrow\downarrow\}$$ with a probability of $$P(E) = 1/2$$. 

## 

## Footnote 
[^1]: Qubits in general have more than two states but they are engineered in a way that they almost always operate within the two states that have the lowest energy. Under this condition, they are equivalent to the spin of an electron. 
[^2]: If you are not familiar with the symbols I have used, here are the definitions. $$\in$$: in / a member of, $$\sum$$: sum of the following items. 

