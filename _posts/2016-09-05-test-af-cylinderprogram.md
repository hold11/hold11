---
layout: post
author: 'Anders, Troels og Iman'
title: Test af Cylinderprogram
date: '2016-08-30 08:00:00 +0200'
categories: versionsstyring
---

Vi vil her dokumentere test af cylinderprogram. Programmet kan findes [her](https://github.com/hold11/Uge2_Opgaver/releases/tag/1.0).

# 1 Positiv Test

Vi stater med positiv test af programmet for at se om vi får det rigtige resultat ud.

```
Indtast højde af cylinder
$ 7
Indtast radius af cylinder
$ 3
Rumfanget af cylinder: 198
```

Det ses her at resultatet af positivtesten er positiv.

# 2 Negativ Test

## 2.1 Vi tester exception handling

### 2.1.1 Bogstav

Vi prøver først at sætte et bogstav, _z_, ind:

```
Indtast højde af cylinder
$ z
Exception in thread "main" java.util.InputMismatchException
           at java.util.Scanner.throwFor(Scanner.java:864)
           at java.util.Scanner.next(Scanner.java:1485)
           at java.util.Scanner.nextDouble(Scanner.java:2413)
           at Cylinderberegner.main(Cylinderberegner.java:20)
```

Vi ser altså at programmet ikke kan håndtere bogstaver.

### 2.1.2 Matematiske operationer

Vi tester nu med matematiske operationer, fx $$ 3+2 $$:

```
Indtast højde af cylinder
$ 3+2
Exception in thread "main" java.util.InputMismatchException
           at java.util.Scanner.throwFor(Scanner.java:864)
           at java.util.Scanner.next(Scanner.java:1485)
           at java.util.Scanner.nextDouble(Scanner.java:2413)
           at Cylinderberegner.main(Cylinderberegner.java:20)
```

Så det kan den heller ikke klare.

### 2.1.3 Mellemrum

Vi tester nu om programmet kan håndtere mellemrum før og efter vores inputs

```
Indtast højde af cylinder
$       7
Indtast radius af cylinder
$ 5
Rumfanget af cylinder: 550
```

Og mellemrum mellem tal:

```
Indtast højde af cylinder
$ 6
Indtast radius af cylinder
$ 2   8
Rumfanget af cylinder: 75
```

Det virker, men den ekskluderer alt efter mellemrum.

## 2.2 Test af overflow

Vi tester med det højeste _double_ kan klare, og sætter et 0 bag på:

```
Indtast højde af cylinder
$ 1.7976931348623157E3080
Indtast radius af cylinder
$ 1.7976931348623157E3080
Rumfanget af cylinder: 9223372036854775807
```

Vi prøver så igen, bare med nogle flere 0'er

```
Indtast højde af cylinder
$ 1.7976931348623157E308000
Indtast radius af cylinder
$ 1.7976931348623157E308000
Rumfanget af cylinder: 9223372036854775807
```

Vi ser her, at vi får det samme resultat i begge tilfælde. Dvs. at overflow bliver blokeret, og vi får blot outputtet det højeste tal den kan klare (de 2 resultater er ens).

# 3 Konklusion

Der er visse faldgrupper. Programmet viste sig at være ustabilt når man gav den et input, som den ikke forventede (bogstaver, matematiske operationer).

Vi så under negativtesten at der ikke var nogen exception handling.

Til gengæld bestod programmet i vores positivtest, og vi fik et svar som forventet.
