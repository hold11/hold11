---
layout: post
title: WK03 - Formal Proof Systems
date: '2016-09-14 10:00:00 +0200'
author: Anders Wiberg Olsen
categories: discrete_math
---

See deduction rules from [WK02](http://localhost:4000/discrete_math/2016/08/31/wk02-limitations-of-propositional-logic.html) (SR1 $$ \rightarrow $$ SR5).

# Resolution and standard mathematical proofs

## 1. Resolution method SR5

$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      P \vee Q\\
      \neg P \vee R
    \end{array}
  }{
    Q \vee R
  }
\end{equation}

 $$

 Not all propositions have a suitable form for SR5.

### 1.2 Proofing

We want to proof:

$$ \begin{equation}
\frac{
    \begin{array}[b]{r}
      A_1\\
      \vdots\\
      A_n
    \end{array}
  }{
    C
  }
\end{equation}
 $$

__Direct Proof__:

$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      A_1\\
      \vdots\\
      A_n
    \end{array}
  }{
    C
  }
\end{equation}

$$

__Indirect Proof__:

$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      A_1\\
      \vdots\\
      A_n\\
      \neg C
    \end{array}
  }{
     0
  }
\end{equation}

$$

$$ \uparrow $$

<center>computer</center>

## 2. Conjunctive Normal Form (CNF)

__literal__: $$ P \vee \neg P $$ - for $$ P $$ a simple proposition

__clause__ : $$ (L_1 \vee \ldots \vee L_n) $$ - with literals $$ L_i $$

__CNF__    : $$ (K_1 \wedge \ldots \wedge K_m) $$ - with clauses $$ K_i $$

CNF is a confunction of disjunction of literals

or

CNF is AND of ORs of literals

### 2.1 Example

#### 2.1.1 CNF:

$$ \neg P \wedge (Q \vee R) $$

$$ P $$

$$ P \wedge Q $$

$$ (P \vee Q) $$

#### 2.1.2 Not in CNF:

$$ \neg (P \vee Q) $$

$$ (P \wedge Q) \vee R $$

$$ \neg \big[(P \Rightarrow Q) \Rightarrow (\neg Q \Rightarrow \neg P) \big] $$

##### Proof for 2.1.2

1. Replace:

$$ P \Rightarrow Q by \neg P \vee Q (1)$$

$$ P \Leftrightarrow Q by (P \Rightarrow Q) \vee (Q \Rightarrow P) $$

- and then apply (1)

2. Use de Morgan's laws ("negations inside"):

$$ \neg (P \vee Q) \rightsquigarrow \neg P \wedge \neg Q $$

$$ \neg (P \wedge Q) \rightsquigarrow \neg P \vee \neg Q $$

and simplify $$ \neg \neg P \rightsquigarrow P $$

3. Use distributive law ("confuntions outside")

$$ P \vee (Q \wedge R) \rightsquigarrow (P \vee Q) \wedge (P \vee R) $$

then

__(a)__:

*Step 1*:

$$ V $$

*Step 2*:

$$ \neg (P \vee Q) = \neg P \wedge \neg Q $$

*Step 3*:

$$ V $$

__(c)__:

$$ \neg \big[(P \Rightarrow Q) \Rightarrow (\neg Q \Rightarrow \neg P) \big] $$

*Step 1*:

$$ \neg \big [(\neg P \vee Q) \Rightarrow (\neg \neg Q \vee \neg P) \big] $$

$$ \neg \big [\neg (\neg P \vee Q) \vee (Q \vee \neg P) \big] $$

*Step 2*:

$$ \neg \neg (\neg P \vee Q) \wedge \neg (Q \vee \neg P) $$

$$ \Leftrightarrow (\neg P \vee Q) \wedge \neg Q \wedge P $$

*Step 3*:

$$ V $$

### 2.3

1. Convert $$ A_i $$ and $$ C $$ (or $$ \neg c $$ for indirect proof) to CNF.

2. Use (SR5) and *identities from table 1.11* to prove $$ C $$

#### 2.3.1 Commonly used identities

(7) $$ P \vee 0 $$ $$ \Leftrightarrow P $$

(9) $$ P \vee \neg P $$ $$ \Leftrightarrow 1 $$

(17) $$ P \vee 1 $$ $$ \Leftrightarrow 1 $$

(en til regel, nåede ikke at se det.)

So, the proof:

The following is the $$ C $$ (look at 1.2.3)

$$ (P \Rightarrow Q) \quad \Rightarrow \quad (\neg Q \Rightarrow \neg P) $$

So

1. $$ (\neg P \vee Q) \quad \wedge \quad (\neg Q \wedge P) $$

2. $$ \neg P \vee Q $$

3. $$ \neg Q \vee 0 $$

4. <center>$$ P \vee 0 $$</center>
<br/>On number 2 and 3, we'll use SR5 to reduce (since we have both $$ Q $$ and $$ \neg Q $$):<br/>
5. <center>$$ \neg P \vee 0 $$</center>
<br/>On 4 and 5 we have $$ 0 $$ and both $$ P $$ and $$ \neg P $$, so obviously we get:<br/>
6. $$ \underline{\underline{0}} $$

## 3.1 Proof from last week:

### 3.1.1 Direct Proof

$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      P \Rightarrow (Q \vee R)\\
      R \vee S\\
      S \Rightarrow \neg Q
    \end{array}
  }{
    P \Rightarrow R
  }
\end{equation}

$$

### 3.1.2 Indirect Proof

In 3.1.1 $$ P \Rightarrow R $$ is our $$ C $$.

__CNFs__:

1. $$ \neg P \vee Q \vee R $$

2. $$ R \vee S $$

3. $$ \underline{\neg S \vee \neg Q} $$

4. $$ P $$

5. $$ \neg R $$

6. <center>$$ R \vee \neg Q $$ (SR5) on 2+3</center>

7. <center>$$ \neg Q $$ (SR5) on 5+6</center>

8. <center>$$ \neg P \vee R $$ (SR5 on 1+7)</center>

9. <center>$$ R $$ (SR5 on 4+8)</center>

10. <center>$$ 0 $$ (SR5) on 5+9</center>

It should be possible to do this in a different order, to get maybe one step less.

`TODO: Try to get the (SR5) lines on the same line, and stick to the right.`

__CNF of $$ \neg C $$__:

$$ \neg (P \Rightarrow R) $$

$$ \Leftrightarrow \neg (\neg P \vee R) $$

$$ \Leftrightarrow P \wedge \neg R $$

## 4. Basic Proofing Strategies

__Direct Proof__:

_Assume $$ A $$_,

_Deduce $$ B $$_

### 4.1. Direct Proof Example:

__Claim__: $$ V \in \mathbb{N}. \quad n $$ is odd $$ \quad \Rightarrow \quad n^2 $$ is odd.

__Proof__: Assume $$ n $$ is odd. Write $$ n + 2k + 1 $$ for some $$ k \in \mathbb{N}  $$.

Then $$ n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 $$

$$ = 2(2k^2 + 2k) + 1 $$

$$ = 2 k^1 + 1 $$

Therefore $$ n^2 $$ is odd too.

### 4.2 Proof by contraposition

Use

$$
\begin{equation}
    \begin{array}[b]{r}
    A \Rightarrow B\\
    \Updownarrow\\
    \neg B \Rightarrow \neg A
    \end{array}
\end{equation}

$$

Assume $$ \neg B $$, deduce $$ \neg A $$

`TODO: Center statement above, and put it in a box`


### 4.3 Proof by contradiction

Use

$$
\begin{equation}
\frac{
    \begin{array}[b]{r}
      A\\
      \neg B
    \end{array}
  }{
      0
  }
\end{equation}
$$

Assume $$ A $$ and $$ \neg B $$, deduce contradiction.

#### 4.3.1 Example

__CLaim 3__:

$$ \sqrt{2} is irrational $$

$$ \Leftrightarrow \neg \exists p,q \in \mathbb{Z}. \quad [\sqrt{2} = \frac{p}{q} ] $$

Proof: Assume $$ \sqrt{2} $$ is rational.

<center>$$ \Rightarrow \exists p,q \in \mathbb{Z}. \quad \sqrt{2} = \frac{p}{q}  $$, reduced fraction</center>

$$ \Rightarrow 2 = \frac{p^2}{q^2} \Rightarrow 2q^2 = p^2 $$

$$ \Rightarrow p^2 $$ is a even number.

$$ \Rightarrow p $$ is even.

$$ \Rightarrow P=2k $$ for some $$ k $$.

(we see that $$ 2q^2 = p^2 \Leftrightarrow p = 2k $$)

$$ \Rightarrow 2q^2 = (2k)^2 = 4k^2 $$

$$ \Leftrightarrow q^2 = 2k^2 $$

$$ \Rightarrow q^2 $$ is even $$ \Rightarrow  q $$ is even.
