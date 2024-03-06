---
date: 2019-10-11
keywords: vob, .vob, vob file format, .vob file format, .vob extension, vob extension, vob video format, vob dvd files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par VOB faila formātu un API, kas var izveidot un atvērt VOB failus.
title: VOB faila veidlapaat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Kas ir VOB fails? ##

VOB faili parasti tiek glabāti DVD diska direktorijā VIDEO_TS ar paplašinājumu .vob. VOB faili satur video un audio datus, kā arī citus datus, piemēram, izvēlnes un subtitrus. VOB pamatā ir MPEG-2 programmas straumes formāts, taču tam ir papildu ierobežojumi un specifikācijas privātajām straumēm. VOB faili ir stingra MPEG programmu straumju apakškopa, tāpēc visi VOB faili ir MPEG programmu straumes, bet visas MPEG programmu straumes nav saderīgas ar VOB.

## DVD video struktūra ##

Kad DVD tiek atvērts datorā, VIDEO_TS ir augstākā līmeņa direktorijs ar AUDIO_TS. AUDIO_TS ir tukšs un netiek izmantots. VIDEO_TS direktorijā ir VOB, BUP un IFO faili. VOB faili satur MPEG saturu. Tie ir sadalīti 1 GB vai mazākos gabalos, lai tie būtu saderīgi ar visām operētājsistēmām. IFO faili satur informāciju par izvēlnēm un nosaukumu struktūru. BUK faili ir IFO failu dublējuma faili ar tādu pašu nosaukumu. Šie faili ir paredzēti fiziski glabāšanai atsevišķā apgabalā, lai gadījumā, ja IFO fails ir bojāts DVD fizisku bojājumu dēļ, BUK fails var sniegt to pašu informāciju.

### Fiziskais izkārtojums ###

- Visiem diskā esošajiem failiem jābūt blakus.
- The related files should be next to each other(VOB, IFO, BUP).
- Numurētajiem failiem jābūt augošā secībā.

## Aizsardzība pret kopēšanu ##

Daudzi video DVD ir šifrēti un neļauj kopēt datus no DVD. Autentifikācijas un atšifrēšanas atslēgas ir nepieciešamas, lai atskaņotu failus, kas atrodas DVD nepieejamā ievades zonā. Šīs atslēgas izmanto CSS atšifrēšanas programmatūra, kas atrodas DVD atskaņotājā vai programmatūras atskaņotājā. Bez taustiņiem video failus nevar atskaņot, jo taustiņi tiks pieprasīti, kad faili tiks atvērti.

## Atsauces Nr.

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

