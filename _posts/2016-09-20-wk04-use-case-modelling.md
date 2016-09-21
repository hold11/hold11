---
layout: post
title: WK04 Use Case Modelling
author: Anders Wiberg Olsen
date: '2016-09-20 13:00:00 +0200'
categories: UML
---

# 1. Kravsspecifikation

Når man laver kravsspecifikationer, er det vigtigt at de såkaldt "_rigtige_" mennesker møder op. Det går fx at CEO dukker op til mødet som den eneste, hvis CEO ikke skal bruge systemet. Også selvom det er ham der betaler for lortet.

Det er vigtigt at krav er:

* Utvetydige
* Præcise
* Tilstrækkelige (nok)
* Ikke for mange (fx EFI med 10.000-15.000 specifikationer)
* Ikke modstridende
* Ikke unødigt begrænsede

## 1.1. Hvem kender kravene?

Hvem kender kravene? Kunden? Nej, ikke altid. __Kunden__ kender kravene. __Brugeren__ kender kravene, så det er vigtigt at netop de er med under udfærdigelse af kravsspecifikationerne. Kunden kan endda have _misforstået_ kravene.

## 1.2. Use case modellering - den korte udgave

* Definer (vælg) _systemet_
  - System boundary
* Identificer _aktørerne_
* Identificer aktørenes _mål_ med systemet
* Identificer _brugsscenarier_
* Generaliser til _use cases_
* Skriv use cases (tekst!)
* Tegn use case diagram.

## 1.3. Systemet

Definer _systemet_. Afgræns det til hvad skal det kunne, og hvad skal det ikke kunne?

# 2. Aktører

En aktør er en person eller andet systemet, som interargerer med systemet. De er eksterne, og er altså dermed ikke en del af systemet. Aktøren er en _rolle_, ikke en bestemt instans (person, objekt).

## 2.1. Identificer aktørerne

Spørg om følgdende:

* Hvem og hvad skal bruge systemet?
* Hvilke roller spiller brugerne?
* Hvem installerer systemet?
* Hvem starter og stopper systemet?
* Hvem vedligeholder systemet?
* Er der andre systemer der bruger dette system?
* Hvem / Hvad leverer og får information fra systemet?
* Er der noget der sker på faste tidspunkter?
