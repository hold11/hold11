---
layout: post
title: Kravsspecifikationer
author: Anders Wiberg Olsen
date: '2016-09-06 15:00:00 +0200'
categories: UML
---

Kort detalje: DTU anbefaler at vi bruger pherbs plus.

Når en kunde vil have lavet et stykke program, ved de ofte ikke hvad de præcist vil have, og der kan det være vores job, at foreslå nogle funktioner osv.

# Kom i gang med Kravsspecifikationer

Hvordan kommer man så i gang med at få defineret sine kravsspecifikationer? En måde er at lave et interview. Fx et lukket interview med pre-definerede liste af spørgsmål, eller et åben, hvor man tager det lidt hen ad vejen.

Man kan også lave nogle prototyper. Den kan man bruge til at diskutere med en kunde. Her tupisk en brugergrænseflade, som ikke umiddelbart gør noget, men som viser hvilken type funktionalitet der skal være. Man kan ricikere at man har lavet noget, og når man så viser det for en kunde, så er der pludselig en ting til programmet fx skulle gemme. Der er det rart at man ikke har kodet hele projektet først, så man ikke skal lave lige så meget om.

Kravsspecifikationerne skal dække <u>alle</u> specifikationer i programmet.

Krav kan være delt op i både _funktionelle krav_ og _ikke-funktionelle krav_.

## Funktionelle krav

Funktionelle krav er krav omkring funktionaliteten bag programmet. Det kan fx være at programmet skal kunne dit og dat.

## Ikke-funktionelle krav

De ikke-funktionelle krav kan fx være krav til performance og oppetid osv. Eller at det skal være skrevet i Java version 7, køre linux v2.6.34. Betalingsterminalen skal kunne godkende på mindre end 3 sekunder osv.

## Hvordan skriver man krav?

[ID] The [system] __shall__ [function].

fx _R12_ The application shall do this.

Der findes forskellige type krav:

__A-requirements__ shall always be fulfilled. The word "shall" is used in connection with A-requirements

__B-requirements__ can only be deviated from, when a proper written explanation is given to (and accepted by) the company. The word "shall" is used in connection with B-requirements.

__C-requirements__ are optional. If they are implemented, the implementation shall however follow the guidelines set up in the requirement(s) concerned. The words "may" and "should" are used in connection with B-requirements.

# Validering

Fra slideshow:

* Validation
  * Are we building the right thing?
* Verification
  * Are we building the right thing?

Så det handler om at verificere og validere at alting er som det skal være.

# Referencer

* [http://upedu.org](http://upedu.org)
