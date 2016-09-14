---
layout: post
title: WK02 - Limitations of Propositional Logic
date: '2016-08-31 15:31:00 +0200'
author: Anders Wiberg Olsen
categories: discrete_math
---

1: All men are mortal

2: Aristoteles is a man

3: Therefore Aristoteles is mortal

---

1: For all $$ x: Man(x) \Rightarrow Mortal(x) $$

2: $$ Man(Aristoteles) $$

3: $$ Leftarrow Mortal(Aristoteles) $$

---

$$ \exists x. \neg \exists y. x \neq y \Rightarrow P(x) \wedge P(y) $$

$$ \forall x. \exists y. x \neq 0 \Rightarrow x \cdot y = 1 $$

# Deduction rules

slå det op: SR1, SR2, SR3, SR4 og SR5

SR1:

$$ P \Rightarrow Q $$

$$ P $$

$$ --- $$

$$ Q $$

SR2:

$$ P $$

$$ --- $$

$$ P \vee Q $$

SR3:

$$ P \wedge Q $$

$$ --- $$

$$ P $$

SR4:

$$ P $$

$$ Q $$

$$ --- $$

$$ P \wedge Q $$

SR5:

$$ P \vee Q $$

$$ \neg P \vee R $$

$$ --- $$

$$ Q \vee R $$

---

$$ P \vee Q $$

$$ \neg P \vee R $$

---

We have some numbers. The first is:

<center><b>(1)</b></center>

$$ \frac{(P \vee Q) \Rightarrow R}{(P \Rightarrow R) \wedge (Q \Rightarrow R)}  $$

Second:

<center><b>(2)</b></center>

$$ \neg (P \vee Q) \vee R $$

Third:

<center><b>(3)</b></center>

$$ (\neg P \wedge \neg Q) \vee R $$


Forth:

<center><b>(4)</b></center>

$$ (\neg P \vee R) \vee (\neg Q \vee R) $$

Fifth:

<center><b>(5)</b></center>

$$ (P \Rightarrow R) \wedge (Q \Rightarrow R) $$

---

1. $$ P \Rightarrow (Q \vee R) $$

2. $$ R \vee S $$

3. $$ S => \neg Q $$

$$ --- $$

* $$ P \Rightarrow R $$

$$ [ \Leftrightarrow \neg R \vee R] $$

<br/><br/>

4. $$ \neg P \vee Q \vee R $$

5. $$ \neg S \vee \neg Q $$

6. $$ R \vee \neg Q $$

7. $$ R \vee \neg Q $$

8. $$ R \vee \neg P \vee R $$
