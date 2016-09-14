---
layout: post
title: WK01 - Introduction to discrete mathematics.
date: '2016-08-31 15:31:00 +0200'
author: Anders Wiberg Olsen
categories: discrete_math
---

Discrete mathematics is about logicical statements.

For example

**Ex 1:**

  1. If it's windy, my hat flies away
  2. It's windy
  3. Therefore my hat flies away

**Ex 2:**

  1. If the sun shines, then, if it rains, I get wet
  2. If the sun shines, it's summer
  3. It isn't summer
  4. Therefore: if the sun shines, I get wet

Even though it isn't really physically true, it is logically true through discrete mathematics.
<br><br>

## 1. Basic Logic

We have a few logic tables and operators. The most basic is $$ \neg $$ which is *negation*. It compares to programming when using `!` to negate something.

| $$ P $$ | $$ \neg P $$ |
|:-------:|:------------:|
|  True   |    False     |
|  False  |     True     |

As shown, we use a binary answer, so practically we will use 0 and 1 instead of *true* and *false*.

| $$ P $$ | $$ \neg P $$ |
|:-------:|:------------:|
|    0    |      1       |
|    1    |      0       |

### 1.1 Operators

#### 1.1.1 AND

The `and` operator is expressed by $$ \wedge $$ (\wedge in LaTeX). It requires all values to be true. If a value isn't true, then the statement becomes false.

For example:

| $$ P $$ | $$ Q $$ | $$ P \wedge Q $$ |
|:-------:|:-------:|:----------------:|
|    0    |    0    |        0         |
|    0    |    1    |        0         |
|    1    |    0    |        0         |
|    1    |    1    |        1         |

#### 1.1.2 Or (inclusive or)

The `or` operator is express by $$ \vee $$ (\vee in LaTeX). It requires at least one of the values to be true. It can be compared to how children might interpret _'or'_ by adults.
For example if a parent asks a child if it wants chocolate or ice cream, the child may answer with a 'yes', as in the child would like to have both, while the parent exclusively meant either chokolate or ice cream, definitely not both (this is called _xor_, more on that in a bit).

Here is an example on the _inclusive or_ operator:

| $$ P $$ | $$ Q $$ | $$ P \vee Q $$ |
|:-------:|:-------:|:--------------:|
|    0    |    0    |       0        |
|    0    |    1    |       1        |
|    1    |    0    |       1        |
|    1    |    1    |       1        |

#### 1.1.3 Exclusive Or (XOR)

The `exclusive or` (or just xor) is true when either one or another is true (no more than exactly <u>one</u> value). To continue on the last example [1.1.2], the xor operator is the 'adult' who meant either chokolate <ul>or</ul> ice cream, so it limits to only one value.
It is expressed by $$ \oplus $$ (\oplus in LaTeX) and it is same as saying $$ (P \vee Q) \wedge \neg (P \wedge Q)

For example

| $$ P $$ | $$ Q $$ | $$ P \oplus Q $$ |
|:-------:|:-------:|:----------------:|
|    0    |    0    |        0         |
|    0    |    1    |        1         |
|    1    |    0    |        1         |
|    1    |    1    |        0         |

#### 1.1.4 If $$ P $$ then $$ Q (P \Rightarrow Q) $$

Often in mathematics, there are senteces like _"if $$ P $$ then $$ Q $$"_ (which reads: _"$$ P $$ implies $$ Q $$"_). Writing $$ P \Rightarrow Q $$ is the same as writing $$ \neg P \vee Q $$.

There is a nice example to explain what it does. We start by saying that

> When it rains, the street gets wet

Here we have a few values:

* $$ P $$: 'It rains'
* $$ Q $$: 'The street gets wet'

| $$ P $$ | $$ Q $$ | $$ P \Rightarrow Q $$ | Description |
|:-------:|:-------:|:----------------:|:---:|
|    0    |    0    |        1         | Rain, dry street |
|    0    |    1    |        1         | No rain, wet street |
|    1    |    0    |        0         | Rain, dry street |
|    1    |    1    |        1         | Rain, wet street |

The forth row (rain, dry street) contradicts our first sentence as the street can't stay dry while it's raining.

#### 1.1.5 XNOR ($$ P \Leftrightarrow Q $$)

The `XNOR` operator is true when each value in the statement is equal to each other. XNOR is in mathematics read _'if and only if'_. For example when $$ P $$ and $$ Q $$ are both false or both true (not different):

| $$ P $$ | $$ Q $$ | $$ P \Leftrightarrow Q $$ |
|:-------:|:-------:|:----------------:|
|    0    |    0    |        1         |
|    0    |    1    |        0         |
|    1    |    0    |        0         |
|    1    |    1    |        1         |

### 1.2 Tautology

Tautology is a statement that is always true, no matter whether the value is true or false.

1. A statement $$ B $$ is a logical consequence of a statement $$ A $$, if $$ A \Rightarrow B $$ is a tautology.
2. Two statements $$ A $$ and $$ B $$ are logically equal if $$ A \Leftrightarrow B $$ is a tautology.

A basic tautology is $$ [(P \Rightarrow \neg Q) \wedge P] \Rightarrow \neg Q $$. This tautology, as per definition, always returns _true_. These tautologies can be used for verifying if (especially complex) tables are correctly calculated.

For example

| $$ P $$ | $$ \neg Q $$ | $$ Q $$ | $$ P \Rightarrow \neg Q $$ | $$ (P \Rightarrow \neg Q) \wedge P) $$ | $$ [(P \Rightarrow \neg Q) \wedge P] \Rightarrow \neg Q $$ |
|:-------:|:------------:|:-------:|:----:|:---:|:---:|
|    0    |      0       |    1    | 1 | 0 | 1 |
|    0    |      1       |    0    | 1 | 0 | 1 |
|    1    |      0       |    1    | 1 | 1 | 1 |
|    1    |      1       |    0    | 0 | 0 | 1 |
