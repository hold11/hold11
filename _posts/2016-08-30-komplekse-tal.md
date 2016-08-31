---
layout: post
title: Komplekse Tal
date: '2016-08-30 08:00:00 +0200'
categories: basismat
---

## 1.1 Introduktion

Vi har forskellige talrækker. De mest brugte er:

* Naturlige tal: $$ \mathbb{N} = \{1, 2, 3, ..., \infty \} $$
* Reelle tal: $$ \mathbb{R} = \{-\infty , ..., -2, -1, 0, 1, 2, ..., \infty \} $$
* Hele tal: $$ \mathbb{Q} $$, som også inkluderer tal som fx $$ \sqrt{2} $$, $$ \pi $$, $$ e $$

Og så har vi de komplekse tal, $$ \mathbb{C} $$, som er alle tal, som ligger i en plan.

Imaginære tal er opstilt således:

$$ a+bi $$

Forestil en graf med reelle tal hen ad $$ x $$-aksen. $$ y $$-aksen kaldes for den imaginære akse. $$ a $$ er hen ad $$ x $$-aksen og $$ bi $$ er op ad $$ y $$-aksen.

## 1.2 Regning med komplekse tal

Hvis vi har 2 komplekse tal, fx $$ z_1 = 2 + 3i $$ og $$ z_2 = 5 + i $$, så kan vi bl.a. lave:

* Addition: $$ z_1 + z_2 = 2 + 3i + 5 + i = 7 + 4i $$
* Subtraktion: $$ z_1 - z_2 = 2 + 3i - (5 + i) = -3 + 2i $$
* Multiplikation: $$ i^2 = -1 $$, dvs. at $$ z_1 \cdot z_2 = (2 + 3i) \cdot (5 + i) = 10 + 2i + 15i + 3i^2 = 7 + 17i $$
* Division: $$ \frac{z_1}{z_2} = \frac{2 + 3i}{5 + i} = \frac{(2+3i)(5-i)}{(5+i)(5-i)} = \frac{10 - 2i + 15i - 3i^2}{25 -5i + 5i - i^2} = \frac{13 + 13i}{26} = \frac{1}{2} + \frac{1}{2}i $$

Tricket her er altså at forlænge brøken med nævnerens kompleks konfugerede (altså nævneren $$ a + ib $$ omskrives til $$ a - ib $$ -- i dette eksempel forlænges brøken med $$ 5-i $$). Derved får vi altså nemlig et reelt tal i tælleren (fordi de imaginære tal går ud med hinanden i nævneren).

## 1.3 Polære koordinater

De polære koordinater siger noget om hvor langt det imaginære tal er, og hvilken vinkel det har.

Modulus = absolut værdi (_abs_ i Maple).

$$ \|z\| $$ - modulus (eller numerisk værdi, eller absolut værdi af $$ z $$)(_"længden af $$ z $$"_).

$$ arg(z) $$ er argumentet for $$ z $$ (_"vinklen for $$ z $$"_). Det angives oftest i $$ ]-\pi ; \pi ] $$ (hovedargumentet).

### 1.3.1 Polære koordinater $$ \rightarrow $$ rektangulære koordinater

$$ Re(z) = \|z\| \cdot cos(arg(z)),  Im(z) = \|z\| \cdot sin(arg(z)) $$

($$ Re $$ er $$ x $$-aksen og $$ Im $$ er $$ y $$-aksen)

### 1.3.2 Rektangulære koordinater $$ \rightarrow $$ polære koordinater

$$ \|z\| = \sqrt{a^2+b^2}, (z=a+ib) $$

$$ tan(arg(z)) = \frac{b}{a} $$

$$ a $$ må dog selvfølgelig ikke være lig $$ 0 $$.

For at finde argumentet, skal vi fjerne $$ tan $$ ved hjælp af $$ arctan $$ (også kendt som $$ tan^{-1} $$)

Dvs.

$$
\begin{cases}
arctan(\frac{b}{a}), \text{a > 0}\\
arctan(\frac{b}{a}+\pi , \text{a < 0}, \text{b} \geq 0)\\
arctan(\frac{b}{a}-\pi , \text{a < 0,}\text{b < 0})\\
\frac{\pi}{2}, a = 0, b > 0\\
-\frac{\pi}{2}, a = 0, a < 0\\
\end{cases}
$$

#### 1.3.2.1 eksempel

Polære koordinater for $$ z_1 = 2 + 3i $$

$$ \|z\| = \sqrt{2^2+3^2i} = \sqrt{i3} $$

$$ arg(z_1) = arctan\Big(\frac{3}{2}\Big) $$
