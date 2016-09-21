---
layout: post
title: Opgave Med Kravsspecifikationer
author: Anders Wiberg Olsen
date: '2016-09-06 15:00:00 +0200'
categories: UML
---

[Use Case]({% post_url 2016-09-20-wk04-use-case-auktionsside %}) for specifikationerne.

# Øvelsestekst

Vi vil gerne have udviklet et web-baseret auktionssystem, hvor det er muligt for kunder at lægge beskrivelse af varer op på auktionsbordet. Kunder kan derefter byde på disse varer. Varer på auktionsbordet er beskrevet med en tekst og der er angivet udløbsdato for auktionen, samt eventuelt en købspris for varen. Når der bydes på varer foregår det som lukket auktion, dvs. byderne kender ikke de andre bud, men kun antallet af bud der er givet. En auktion på en vare slutter enten når en byder vælger at betale købsprisen eller når auktionsperioden for varen udløber. I begge tilfælde skal alle bydere informeres om resultatet af auktionen. Endvidere skal systemet gennemføre en overførelse af penge til kunden fra den der har vundet auktionen. Systemet skal fungere altid og det accepteres ikke at der mistes data ved nedbrud. Det forventes at systemet på sigt skal kunne håndtere mange brugere og det forventes at systemet er intuitivt. På alle systemets sider skal der være plads til reklamer og alle sider skal indeholde vores logo. Kun personer, der har registeret sig som brugere af vores system skal kunne anvende det og det skal være muligt at lukke brugeres konti.

# 1. Functional specifications

* __1-A01__: Brugere skal kunne lægge beskrivelse af varer op på auktionsbordet
* __1-A02__: Kunder skal kunne byde på varer
* __1-A03__: Varer skal have en udløbsdato
* __1-A04__: Varer skal have en eventuel købspris
* __1-A05__: Auktionen skal være lukket (hvert bud skal være anonymt)
* __1-A06__: Brugere skal kende antallet af afgivende bud
* __1-A08__: Resultatet af en afsluttet auktion skal være synligt for byderne
* __1-A09__: Systemet skal gennemføre en overførelse fra kunden der har vundet til kunden der har lagt varen op
* __1-A10__: Ved auktionens afslutning skal alle bydere informeres om resultatet af auktionen.
* __1-A12__: Logo skal være synligt på alle sider
* __1-A13__: Der skal være plads til reklamer på alle sider
* __1-A14__: Kun brugere som er registreret i systemet, skal kunne anvende hjemmesiden
* __1-A15__: Brugere konti skal kunne lukkes

# 2. Usability

* __2-A01__: Systemet skal være intuitivt

# 3. Reliability

* __3-A01__: Ved systemnedbrud må data ikke gå tabt
* __3-A02__: Systemet skal altid fungere

# 4. Performance

* __4-B01__: Systemet skal kunne klare stort pres

# 5. Supportability

* __5-A01__: Systemet skal kunne udvides til at understøtte en voksende mængde brugere
