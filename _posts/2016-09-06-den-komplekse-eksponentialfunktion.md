---
layout: post
title: Den Komplekse Eksponentialfunktion
date: '2016-09-06 08:00:00 +0200'
author: Anders Wiberg Olsen
categories: basismat
---

# 1. Kort fra sidst:

|     |     |
|:---:|:---:|
| Rektangulære Koordinater | $$ \big (Re(z), Im(z)\big ) $$ |
| Rektangulær Form | $$ z = Re(z)+iIm(z) $$ |
| Polære Koordinater | $$ (\|z\|, arg(z)) $$ |

$$ z = \|z\| \cdot cos \big (arg(z) \big) + i \|z\| \cdot sin \big (arg(z) \big) $$

$$ z = \|z\| \cdot \Big ( cos \big (arg(z) \big) + i \|z\| \cdot sin \big (arg(z) \big) \Big ) $$

# 2. Eulers Formel:

$$ e^{i \alpha} = cos(\alpha)+i\cdot sin(\alpha) $$

$$ \alpha \in \mathbb{R} $$

D.v.s:

Polær form (eksponentiel form):

$$ z = \|z\| \cdot e^{i \cdot arg(z)} $$

## 2.1 Eksempel 1

Vi har tallet

$$ z_{1} = - \sqrt{3} + i $$

$$ \|z_{1}\| = \sqrt{(-\sqrt{3})^{2}+1^{2}} = 2 $$

$$ arg(z_{1}) = arctan \Big (\frac{1}{-\sqrt{3}} \Big ) + \pi = arctan \Big (- \frac{\sqrt{3}}{3} + \pi - \frac {\pi}{6} + \pi = \frac{5 \pi}{6} \Big ) $$

D.v.s. $$ z_{1} $$ har de polære koordinater $$ (2; \frac{5 \pi}{6}) $$, og polær form $$ z = 2 \cdot e^{i \ cdot \frac{5 \pi}{6}} $$

## 2.2 Eksempel 2

$$ z_{2} = 2 - 2\sqrt{3} i $$

$$ \|z_{2}\| = \sqrt{2^2+(-2\sqrt{3})^2} = 4 $$

$$ arg(z_{2}) = arctan \Big (\frac{-2 \sqrt{3}}{1} \Big) = arctan(-\sqrt{3}) = -\frac{\pi}{3} $$

Dvs.

$$ z_{2} + 4 e^{i \cdot \Big (\frac{\pi}{3} \Big)} = 4 e ^{-i \frac{\pi}{3}} $$

Vi tager en formel fra 3g af gymnasiet; vektorregning:

$$ cos(\alpha) = \frac{\vec{a} \cdot \vec{b}}{\| \vec{a}\| \cdot \| \vec{b}\| } $$

Så ved vi at

$$ \| \vec{e_{2} \| = 1} $$

$$ \vec{e_{2}}=\Big (\matrix{cos(\vec{u}) \\ sin(\vec{u})} \Big) $$

Vi finder

$$ cos(\vec{u}-v) = \frac{\Big (\matrix{cos(\vec{u}) \\ sin(\vec{u})} \Big ) \cdot \Big (\matrix{cos(v) \\ sin(v)} \Big ) }{1 \cdot 1} \Leftrightarrow $$

## 2.3 Additionsformlerne for cosinus og sinus:

$$ cos(\vec{u} - v) = cos(\vec{u}) \cdot cos(v) + sin(\vec{u}) \cdot sin(v) $$

$$ cos(\vec{u} + v) = cos(\vec{u}) \cdot cos(v) - sin(\vec{u}) \cdot sin(v) $$

$$ sin(\vec{u} - v) = -cos(\vec{u}) \cdot sin(v) + sin(\vec{u}) \cdot cos(v) $$

$$ sin(\vec{u} + v) = cos(\vec{u}) \cdot sin(v) + sin(\vec{u}) \cdot cos(v) $$

# 3. Multiplikation og division af komplekse tal på polær form

Vi har følgende tal:

$$ z_{1} = r_{1} \cdot e^{i\cdot \alpha_{1}},    r_{1} = \|z_{1}\|, \alpha_{1} = arg(z_{1}) $$

$$ z_{2} = r_{2} \cdot e^{i\cdot \alpha_{2}},    r_{2} = \|z_{2}\|, \alpha_{2} = arg(z_{2}) $$

<br/><br/>

$$  z_{1} \cdot z_{2} = r_{1} e^{i\alpha_{1}} \cdot r_{2} e^{i\alpha_{2}} $$

  $$ = r_{1} \cdot r_{2} \cdot \big (cos(\alpha_{1}) + i \cdot sin(\alpha_{1}) \big ) \cdot \big (cos(\alpha_{2}) + i \cdot sin(\alpha_{2}) \big ) $$

  $$ = r_{1} \cdot r_{2} \cdot \big (cos(\alpha_{1} \cdot cos(\alpha_{2}) + i cos(\alpha_{1} \cdot sin(\alpha_{2}) + i sin(\alpha_{1} \cdot sin(\alpha_{2}) + sin(v_{1}) \cdot cos(\alpha_{2}) \big)$$

  $$ = r_{1} \cdot r_{2} \cdot \Big (cos(\alpha_{1} \cdot cos(\alpha_{2}) - sin(\alpha_{1} \cdot sin(\alpha_{2}) + \big(i cos(\alpha_{1} \cdot sin(\alpha_{2}) + sin(v_{1}) \cdot cos(\alpha_{2}) \big) \Big )$$

  $$ = r_{1} \cdot r_{2} \cdot \big (cos(\alpha_{1} + \alpha_{2}) + i \cdot sin(\alpha_{1} + \alpha_{2}) \big ) $$

  $$ = r_{1} \cdot r_{2} \cdot e^{i(\alpha_{1}+\alpha_{2})} $$

# fsædfka

$$ \|\frac{z_{1}}{z_{2}}\| = \|\frac{z_{1}}{z_{2}}\| \cdot \|\frac{z_{2}}{z_{2}\|} = \frac{\|\frac{z_{1}}{z_{2}}\| \cdot \| z_{2}} \| { \|z_{2}\|} $$

$$ = \frac{\|\frac{z_{1}}{z_{2}} \cdot z_{2}\|}{z_{2}} = \frac{\|z_{1}\|}{\|z_{2}\|} $$

$$ arg(\frac{z_{1}}{z_{2}}) = arg(\frac{z_{1}}{z_{2}}) + arg(z_{2}) - arg(z_{2}) $$

$$ arg(\frac{z_{1}}{z_{2}}) -arg(z_{2}) $$

$$ arg(z_{1}) - arg(z_{2}) $$

# Skriv eks fortsat her (billede på tlf)

Resten kommer senere, jeg kan ikke følge med.

# Jeg prøver igen

## Eulers formel:

$$ cos(t) + i \cdot sin(t) = e^{i \cdot t} $$

Vi skifter fortegn på $$ t $$ fordi det åbenbart er smart....

$$ cos(t) - i \cdot sin(t) = e^{- i \cdot t} $$

$$ "+": 2\cdot cos(t) = e^{it} + e^{-it} $$

// i en box:

$$ cos(t)=\frac{e^{it} + e^{-it}}{2} $$

$$ "-": 2\cdot cos(t) = e^{it} - e^{-it} $$

// i en box:

$$ cos(t)=\frac{e^{it} - e^{-it}}{2} $$

//end of box

$$ \int{cos(3t)\cdot sin(8t) dt} = \int{\frac{e^{i3t}+e^{-i3t}}{2} \cdot \frac{e^{i3t}-e^{-i3t}}{2i} dt} $$

$$ \int{\frac{e^{i11t}-e^{-i11t}+e^{i5t}-e^{-i5t}}{2\cdot 2i} dt} $$

$$ = \frac{1}{2} \int{\Big (\frac{e^{i11t}-e^{-i11t}}{2i} + \frac{e^{i5t}-e^{-i5t}}{2i}\Big) dt} $$

$$ = \frac{1}{2} \int{\big(sin(11t) + sin(5t) \big) dt} $$

$$ = \frac{1}{2} \big(-\frac{1}{11}) - \frac{1}{5} \cdot  $$
fuck - sidst på tavle 5
