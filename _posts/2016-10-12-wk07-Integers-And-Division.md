---
layout: post
title: WK07 Integers And Division
author: Anders Wiberg Olsen
date: '2016-10-12 10:00:00 +0200'
categories: discrete_math
---

# 1. Euclid's Algorithm

## 1.1 Key observation

$$ \text{if} \quad b = 0 \quad \text{then} \quad \text{gcd}(a, b) = |a| $$

$$ \text{if} \quad b \neq 0 \quad \text{then} \quad \text{gcd}(a, b) = \text{gcd}(a, b) = |b|, a \mod{|b|} $$

### 1.1.1 Proof

$$ \text{gcd}(a, b) = \text{gcd}(|b|, a \mod {|b|}) $$

$$ a \mod{b} = a - q \cdot |b| \mod{q = \Big\lfloor \frac{a}{b} \Big\rfloor}$$

$$ \exists q. \quad a = q |b| + (a \mod{|b|}) $$

<hr>

$$ \text{let}\ \Big| |b|\ \text{and}\ d \big| a \mod{|b|} $$

$$ \Rightarrow d \Big | (q |b| + |a \mod{b}) $$

$$ \Leftrightarrow d\ |\ a $$

<hr>

$$ \text{let}\ d\ |\ a, d\ |a| $$

$$ \Rightarrow d\ |\ (a-q\ |b|) $$

$$ \Rightarrow d\ |\ (a \mod{|b|}) $$

Those two proofs leads to:

all divisors of $$ a, b =  $$ all divisors of |$$b$$|, $$a$$ mod |$$b$$|
$$ \Rightarrow  $$ gcd equal.

## 1.2 The Algorithm

### 1.2.1 Conceptual Pseudocode

1. $$ a := \text{|}a\text{|}, b:=\text{|}b\text{|} $$

2. $$ \text{while}\ b\neq 0: $$

  2.1. $$ r := a \mod{b} $$

  2.2. $$ a := b $$

  2.3. $$ b := r $$

Fix this later

### 1.2.2 Iterative Formulation

1. $$ r_1 := |a|, r_0 := |b| $$

2. $$ \text{for}\ k=1, \dots : $$

2.1. $$ r_k = r_{k-2} \mod{r_{k-1}} $$

(indended) $$ \text{until}\ r_k = 0 $$

Look at it [here](https://www.campusnet.dtu.dk/cnnet/filesharing/SADownload.aspx?FileId=4305815&FolderId=1016982&ElementId=522059).

## 1.3 Worst case for Euclid's Algorithm

The worst case for the algorithm is when using fibonacci numbers.

i.e. computing $$ \text{gcd}(F_{n+2}, F_{n+1}) $$ requires $$ n $$ steps since $$ F_{n+2}\ \text{mod}\ F_{n+1} = F_n $$

# 2. Linear Diophantine Equations

Consider linear equation in 2 variables over $$ \mathbb{Z} $$:

<div style="border: 1px solid red; padding: 5px;">
  $$ ax + by = c $$
</div>

TODO: make the box smaller ........

The equation has a solution in $$ \mathbb{Z}  $$ if and only if $$ \text{gcd}(a, b) \| c $$.

# 2.1. Towards solutions for linear diophantine Equations

__Problem__: Can now decide whether equation has a solution or not, but how to compute such a solution?

let $$ a, b $$ nonzero integers. Then there exist integers $$ s $$ and $$ t $$ such that

$$ as + bt = \text{gcd}(a, b). $$

Why is that useful? Solutions for $$ ab + by = c $$ exist iff $$ \text{gcd}(a, b) \| c $$.

$$ \Rightarrow \text{Compute} s,t \text{ for}\ as + bt = \text{gcd}(a, b) \text{ and multiply this by } f = c\ /\ \text{gcd}(a, b). $$

$$ \Rightarrow a (fs) + b (ft) = c. $$

$$ fs = x, ft = y $$

# 3. Extending Euclid's Algorithm

We note:

$$ r_1 = a = 1 \cdot a + 0 \cdot b \quad \quad s_{-1},t_{-1}! $$

$$ r_0 = b = 0 \cdot a + 1 \cdot b \quad \quad s_0, t_0! $$

$$ r_1 = r_1-q_1r_0 $$

$$ =  1a + 0b - q_1 (0a + 1b) $$

$$ (1 - q_1 0) \cdot a + (0 - q_1 1) \cdot b \quad \quad s_1,t_1!$$

$$ \vdots \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \vdots $$
