---
layout: post
title: WK04 Elementary Set Theory
author: Anders Wiberg Olsen
date: '2016-09-21 10:00:00 +0200'
categories: discrete_math
---

# 1. Sets

A __set__ is an __unordered__ collection of objects, called the __elements__ of the set.

We write:

$$ x \in S $$ if $$ x $$ is an element of $$ S $$ (contained in $$ S $$).

$$ x \not\in S $$ otherwise.

## 1.2. Two ways to specify a set

__Enumerative__ (by list): $$ \quad \quad \{1, 2\}, \quad \{2, 1\}, \quad \{1, 2, 1\} $$

__Descriptive__ (by predicate): $$ \quad \{x \in \mathbb{N} \| 1  \le 1 \le 2 \} $$

All 4 examples describe the same set: $$ \{1, 2 \} $$!

## 1.3. More on set specification

__Descriptive specification of sets__

Most general form:

$$ \{x \in M \| P(x) \} $$

with a __universe__ $$ M $$ and a __predicate__ $$ M $$.

<br/><br/>
__The empty set__

We write:

$$ \emptyset \quad \text{or} \quad \{\} $$

<br/><br/>

__Note: Sets can contain sets:__

$$ \{1, \{1, 2\}, \emptyset , \{\{\emptyset \}\}\} $$

$$ \rightarrow $$ Russel's paradox

# 2. Russel's Paradox

Consider: $$ S = \{x \| x \not\in x \} $$

is $$ S \in S $$?

$$ S \in S \Leftrightarrow S \not\in S $$

So technically, $$ S $$ cannot exist.

# 3. Measuring sets

## 3.1. Definition (Set cardinality)

We denote by

$$ |S| $$

the _cardinality_ of a set $$ S $$ (= its number of elements if finite).

## 3.2. In our previous examples:

$$ |\{1, 2 \}| = |\{1, 2, 1 \}| = |\{x \in \mathbb{N} | 1 \le x \le 2 \}| = 2$$

$$ |\{1, \{1, 2\}, \emptyset \}, \{\{\emptyset \}\} | = 4 $$

## 3.3 Infinite cardinalities

$$ | \mathbb{N} = ? | \;\text{(countably infinite)}$$

$$ | \mathbb{R} = ?| \;\text{(uncountably infinite)} $$

$$|\mathbb{N}| = \aleph $$

# 4. Basic relations among sets

## 4.1. Definition

Let $$ A, B $$ be sets. We say

$$ A = B $$ if $$ A $$ and $$ B $$ contain the same elements:  

$$ x \in A \Leftrightarrow x \in B $$

$$ A \subseteq B $$ if $$ A $$ is a __subset__ of $$ B $$:

$$ x \in A \Rightarrow x \in B $$

## 4.2. Properties

$$ A = B \Leftrightarrow (A \subseteq B) \wedge (B \subseteq A) $$

$$ A \subseteq A  \quad \text{for any set} \quad A $$

$$ \emptyset  \subseteq A  \quad \text{for any set} \quad A $$

## 4.3. examples

Say we have two sets:

$$ A = \emptyset , \quad B = \emptyset $$

We can say that

$$ A = B, \quad A \not\in B, \quad A \subseteq B, B \subseteq A $$

<br/><br/>

Let's try some new definitions:

$$ A = \big\{\emptyset , \{1, 1\} \big\}, \quad \big\{\emptyset , \{1\}, 2\big\} $$

Then:

$$ A \neq B, \quad A \not\in B, \quad B \not\in A, \quad A \subseteq B, \quad B \not\subseteq A $$

$$ A \subseteq B $$ if <u>all</u> elements of $$ A $$ is in the subset of $$ B $$.

$$ A \not\subseteq B $$ if <u>only some</u> of the elements of $$ A $$ is in the subset of $$ B $$.

# 5. Power Set

$$ P(a) $$: Set of all subsets $$ A $$

## 5.1. examples

$$ P\big(\{1, 2, 3\} \big) = \big\{\emptyset , \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\} \big\} $$

$$ P(\emptyset ) = \{ \emptyset \} $$

If $$ \|A\| $$ is finite:

$$ |P(A) = 2^{|A|} | $$

# 6. Set Operations

In the following: $$ A, B $$ sets with $$ A, B \subseteq M $$

__Intersection:__

$$ A \cap B = \{x \; |\;  x \in A \; \text{and} \; x \in B \} $$

<img src="http://dtu.wiberg.tech/img/6.1.png" class="center">

__Union:__

$$ A \cup B = \{x \;|\; x \in A \; \text{or}\; x \in B \} $$

<img src="http://dtu.wiberg.tech/img/6.2.png" class="center">

__Difference__:

$$ A \ B = \{x \; |\;  x \in A\;  \text{and}\;  x \not\in B \}  $$

<img src="http://dtu.wiberg.tech/img/6.3.png" class="center">

__Complement__:

$$ \overline{A} = \{x \; |\;  x \in M\;  \text{and}\;  x \not\in A\}  $$

<img src="http://dtu.wiberg.tech/img/6.4.png" class="center">

# 7. The Cartesian Product

Let $$ A, B $$ be sets. We call

$$ A \times B = \{(a,b ) \; | \; a \in A \; \text{and} \; b \in B \} $$

The <u>cartesian product</u> of $$ A $$ and $$ B $$.

Note: The $$ (a, b) $$ are <u>ordered</u> pairs ("tuples").

## 7.0.1. Example 1:

$$ \{1, 2, 3 \} \times \{\pi , \mathrm{e} \} = \big\{(1,\pi), (2,\pi), (3,\pi), (1, \mathrm{e}), (2, \mathrm{e}), (3, \mathrm{e}) \big\}$$

## 7.0.2. Example 2:

`blabla`

## 7.1 Relations

Cartesian products contain <u>all</u> possible combinations. Usualle need only _subsets_:

### 7.1.1. Definition

For sets

$$ A_1, \cdots, A_n, $$

$$ R \subseteq A_1 \times \cdots \times A_n $$

is called a <u>relation</u> between $$ A_1, \cdots, A_n $$

### 7.1.2 Exmaple:

$$ R_s \subseteq \mathbb{N} \times  \{A, \cdots, F\} $$

$$ R_S = \big\{(135007, Martin, A), (132713, Silke, E) \big\} $$


## 7.2 Operations on Relations

Since relations are sets, we have

$$ R_1 \cup R_2 $$

$$ R_1 \cap R_2 $$

$$ R_1 \backslash R_2 $$

$$ \overline{R_1} = (A_1 \times \cdots \times ) \backslash R_1  $$

<hr/>

[Exlporing predicate logic formulas by gamegs](https://www.campusnet.dtu.dk/cnnet/filesharing/SADownload.aspx?FileId=4286786&FolderId=1006751&ElementId=522059).
