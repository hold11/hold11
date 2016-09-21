---
layout: post
title: WK04 Dmath-Opgaver Fællesmængde
author: Anders Wiberg Olsen
date: '2016-09-21 08:00:00 +0200'
categories: discrete_math
---

# Opgave 1

Lad $$ M = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10 \}, A = \{1, 2, 3, 4, 5 \}, B = \{1, 2, 4, 8 \}, C = \{1, 2, 3, 5, 7 \}, D = \{2, 4 ,6 ,8 \} $$. Bestem:

## 1.a: $$ (A \cup B) \cap C $$

Lad os tage dem hver for sig. Start med parentesen. $$ \cup $$ betyder mængden af elementer som er i mindst én af mængderne $$ A $$ og $$ B $$. Dvs.:

$$ A \cup B = \{1, 2, 3, 4, 5, 8 \} $$

Symbolet $$ \cap $$ betyder mænden af elementer der er i både $$ A $$ og $$ B $$. Dvs.:

$$ (A \cup B) \cap C = \{1, 2 \} $$

## 1.b: $$ A \cap (B \cup C) $$

Jeg starter med parentesen igen:

$$ B \cup C  = \{1, 2 \} $$

Og det hele:

$$ A \cap (B \cup C) = \{1, 2 \} $$

## 1.c: $$ \overline{C} \cap \overline{D} $$

$$ \overline{A} $$ betyder mængden af elementer der i $$ M $$ der <u>ikke</u> er med i mængden $$ A $$.

Jeg starter med at regne dem ud først:

$$ \overline{C} = \{4, 6, 7, 8, 9, 10 \}  $$

$$ \overline{D} = \{1, 3, 5, 7, 9, 10 \} $$

Dvs.:

$$ \overline{C} \cap \overline{D} = \{7, 9, 10 \} $$

## 1.d: $$ \overline{C \cap D}  $$

Jeg starter med at regne $$ C \cap D $$:

$$ C \cap D = \{2 \} $$

Så dvs:

$$ \overline{C \cap D} = \{1, 3, 4, 5, 6, 7, 8, 9, 10 \}  $$
