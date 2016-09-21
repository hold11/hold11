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

$$ \|\{1, 2 \}\| = \|\{1, 2, 1 \}\| = \|\{x \in \mathbb{N} \| 1 \le x \le 2 \}\| = 2$$

$$ \|\{1, \{1, 2\}, \emptyset \}, \{\{\emptyset \}\} \| = 4 $$

## 3.3 Infinite cardinalities

$$ \|\mathbb{N} = ?\| $$ (countably infinite)

$$ \|\mathbb{R} = ?\| $$ (uncountably infinite)

$$\|\mathbb{N}\| = \aleph $$

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
