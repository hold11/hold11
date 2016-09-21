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

## 1.e: $$ (A \cup B) \backslash C $$

Jeg starter med parentesen:

$$ A \cup B = \{1, 2, 3, 4, 5, 8 \} $$

$$ A \backslash B $$ betyder mængden af de elementer i $$ A $$, som <u>ikke</u> er i $$ B $$. Dvs.:

$$ (A \cup B) \backslash C = \{4, 8 \} $$

## 1.f: $$ A \cup (B \backslash C) $$

Jeg starter med parentesen:

$$ B \backslash C = \{4, 8 \} $$

Dvs.:

$$ A \cup (B \backslash C) = \{1, 2, 3, 4, 5, 8\} $$

<hr/>

# Opgave 2

Bevis at

$$ A \backslash(B \cup C) = (A \backslash B) \cap (A \backslash C). $$

`Opgave kommer når jeg lige har fattet det. Lige et øjeblik.`

<hr />

# Opgave 3

Lad $$ A \ne \emptyset $$ og $$ A \cup B = A \cup C $$

## 3.a:

_Kan man heraf slutte, at $$ B = C $$?_

Nej, fordi $$ \cup $$ angiver, at det en værdi kun skal være i <u>en</u> af værdierne.

## 3.b:

_Hvis der <b>samtidig</b> gælder, at $$ A \cap B = A \cap C $$, kan man så slutte, at $$ B = C $$?_

Det kan man til gengæld godt; siden $$ \cap $$ betyder, at værdierne skal være i <u>både</u> den ene og den anden.

<hr />

# Opgave 4

Lad $$ A, C $$ og $$ C $$ være delmængde af en mængde $$ M $$. Undersøg om der gælder:

$$ A \cup (B \backslash C) = (A \cup B) \backslash (A \cup C). $$

```Kommer senere```

<hr/>

# Opgave 5

Lad $$ \|A\| $$ betegne antallet af elementer i en mængde $$ A $$. Vis at

$$ \|A \cup B\| = \|A\| + \|B\| - \|A \cap B\|. $$

```Kommer senere```
