---
layout: post
title: Opgave Med Kravsspecifikationer
author: Anders Wiberg Olsen
date: '2016-09-06 15:00:00 +0200'
categories: UML
---

# Øvelsestekst

Vi vil gerne have udviklet et web-baseret auktionssystem, hvor det er muligt for kunder at lægge beskrivelse af varer op på auktionsbordet. Kunder kan derefter byde på disse varer. Varer på auktionsbordet er beskrevet med en tekst og der er angivet udløbsdato for auktionen, samt eventuelt en købspris for varen. Når der bydes på varer foregår det som lukket auktion, dvs. byderne kender ikke de andre bud, men kun antallet af bud der er givet. En auktion på en vare slutter enten når en byder vælger at betale købsprisen eller når auktionsperioden for varen udløber. I begge tilfælde skal alle bydere informeres om resultatet af auktionen. Endvidere skal systemet gennemføre en overførelse af penge til kunden fra den der har vundet auktionen. Systemet skal fungere altid og det accepteres ikke at der mistes data ved nedbrud. Det forventes at systemet på sigt skal kunne håndtere mange brugere og det forventes at systemet er intuitivt. På alle systemets sider skal der være plads til reklamer og alle sider skal indeholde vores logo. Kun personer, der har registeret sig som brugere af vores system skal kunne anvende det og det skal være muligt at lukke brugeres konti.

# 1. Functional specifications

* 1-A01: Brugere skal kunne lægge beskrivelse af varer op på auktionsbordet
* 1-A02: Kunder skal kunne byde på varer
* 1-A03: Varer skal have en udløbsdato
* 1-A04: Varer skal have en eventuel købspris
* 1-A05: Auktionen skal være lukket (hvert bud skal være anonymt)
* 1-A06: Brugere skal kende antallet af afgivende bud
1-A07: Auktionen afslutter når sluttidspunktet er nået eller når køber vælger at betale varens  købspris.
* 1-A08: Resultatet af en afsluttet auktion skal være synligt for byderne
* 1-A09: Systemet skal gennemføre en overførelse fra kunden der har vundet til kunden der har lagt varen op
* 1-A10: Ved auktionens afslutning skal alle bydere informeres om resultatet af auktionen.
* 1-A12: Logo skal være synligt på alle sider
* 1-A13: Der skal være plads til reklamer på alle sider
* 1-A14: Kun brugere som er registreret i systemet, skal kunne anvende hjemmesiden
* 1-A15: Brugere konti skal kunne lukkes

# 2. Usability

* 2-A01: Systemet skal være intuitivt

# 3. Reliability

* 3-A01: Ved systemnedbrud må data ikke gå tabt
* 3-A02: Systemet skal altid fungere

# 4. Performance

* 4-B01: Systemet skal kunne klare stort pres

# 5. Supportability

* 5-A01: Systemet skal kunne udvides til at understøtte en voksende mængde brugere
