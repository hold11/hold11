---
layout: post
title: WK10 Sequenses
author: Anders Wiberg Olsen
date: '2016-11-09 10:00:00 +0200'
categories: discrete_math
---

$$ \sum_{n=0}^{\infty}{a_n x^n} = a_0 x^0 + a_1 x^1 + \dots + a_\infty x^\infty $$

# 1. Generating functions, some examples

$$ \langle a_n \rangle = a_0, a_1, \dots, a_n \Leftrightarrow A(x) = \sum_{n=0}^{\infty}{a_n x^n} $$

## 1.2 Finite sequences (zero extended)

$$ \langle a_n \rangle = 1, 1, 1, 0, 0, \dots $$

$$ A(x) = 1x^0 + 1x^1 + 1x^2 + 0x^3 + 0x^4 + \dots = 1 + x + x^2 $$

## 1.3 Infinite sequences

$$ \langle b_n \rangle = 1, 1, 1, 1, \dots $$

$$ B(x) = 1x^0 + 1x^1 + 1x^2 + 1x^3 + \dots + \sum_{n=0}^{\infty}{x^n} $$

---

$$ \langle c_n \rangle = 0, 1, 1, 1, \dots $$

$$ C(x) = 0x^0 + 1x^1 + 1x^2 + 1x^3 + \dots = \sum_{n=1}^{\infty}{x^{n+1}} $$

# 2. Manipulation fo generating functions

## 2.1 Extraction of constants

$$ \sum_{n=0}^{\infty}{ca_n x^n} = c \sum_{n=0}^{\infty}{a_n x^n}, \quad c \in \mathbb{R} $$

## 2.2 Addition of power series

$$ \sum_{n=0}^{\infty}{a_n x^n} + \sum_{n=0}^{\infty}{b_n x^n} = \sum_{n=0}^{\infty}{(a_n + b_n) x^n}$$

## 2.3 Examples:

$$ \langle T_n \rangle = 2, 3, 5, 9, \dots $$

$$ = \langle d_n + b_n \rangle $$

$$ T(x) = D(x) + B(x)= \sum_{n=0}^{\infty}{2^n x^n} + \sum_{n=0}^{\infty}{x^n} $$

$$ = \sum_{n=0}^{\infty}{(2^n + n) x^n} = t_n $$

# 3. Manipulation of generating functions (cont'd)

## 3.1 Multiplication of power series

$$ \left ( \sum_{n=0}^{\infty}{a_n x^n} \right) \cdot \left (\sum_{n=0}^{\infty}{b_n x^n} \right) = \sum_{n=0}^{\infty}{ \left (\sum_{j=0}^{n}{a_j b_{n-j}} \right) x^n } $$

## 3.2 Index shift

$$ \sum_{n=n_0}^{\infty}{a_n x^{n+k}} = \sum_{n=n_0 + k}^{\infty}{a_{n-k} x^n} $$

## 3.3 Understanding Multiplication

| $$ x^0 $$ | $$ x^1 $$ | $$ x^2 $$ | $$ x^3 $$ | $$ \dots $$ |
|:----:|:-----:|:-----:|:------:|
| $$ a_0 b_0 $$ | $$ a_0 b_1 $$ | $$ a_0 b_2 $$ | $$ a_0 b_3 $$ |  |
|   | $$ a_1 b_0 $$ | $$ a_1 b_1 $$ | $$ a_1 b_1 $$ |   |
|   |   | $$ a_2 b_0 $$ | $$ a_3 b_0 $$ |   |
|   |   |   | a_3 b_0 |   |
| $$ \sum_{j=0}^{0}{a_j b_{0-j}} $$ | $$ \sum_{j=0}^{1}{a_j b_{1-j}} $$ | $$ \sum_{j=0}^{2}{a_j b_{2-j}} $$ | $$ \sum_{j=0}^{3}{a_j b_{3-j}} $$ | $$ \dots $$ |

## 3.4 example

Suppose we have 200 ones: have to write: $$ 1 + x + \dots + x^199 $$?

Start with $$ \langle b_n \rangle = 1, 1, 1, \dots $$

Consider:

$$ B(x) = \sum_{n=0}^{\infty}{x^n} = 1 + x + x^2 + \dots $$

Define:

$$ G(x) = 1 - x \quad (\text{so } \langle g_n \rangle = 1, -1, 0, 0, \dots) $$

Then:

$$ B(x) G(x) = \sum_{n=0}^{\infty}{ \left (\sum_{j=0}^{n}{b_j g_{n-j}} \right) x^n } = \sum_{n=0}^{\infty}{ \left (\sum_{j=0}^{n}{g_{n-j}} \right) x^n }, $$

$$ = 1x^0 + (-1 + 1)x^1 + (0 - 1 + 1)x^2 + \dots $$

$$ = 1 $$

Therefore:

$$ \sum_{n=0}^{\infty}{x^n} = \frac{1}{G(x)} = \frac{1}{1-x}  $$

# 3.5

<center>
<img src="/img/wk10-3.5.png" />
</center>
