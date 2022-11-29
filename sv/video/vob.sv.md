---
date: 2019-10-11
keywords: vob, .vob, vob-filformat, .vob-filformat, .vob-tillägg, vob-tillägg, vob-videoformat, vob dvd-filer
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig mer om VOB-filformat och API:er som kan skapa och öppna VOB-filer." 
title: VOB filformat
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Vad är VOB fil? ##

VOB-filer lagras vanligtvis i VIDEO_TS-katalogen på en DVD med filtillägget .vob. VOB-filer innehåller video- och ljuddata samt andra data som menyer och undertexter. VOB är baserat på MPEG-2 programströmsformat men det har ytterligare begränsningar och specifikationer i privata strömmar. VOB-filer är en strikt delmängd av MPEG-programströmmar så alla VOB-filer är MPEG-programströmmar men alla MPEG-programströmmar är inte VOB-kompatibla.

## Struktur för DVD-video ##

När en DVD öppnas på en dator är VIDEO_TS den översta katalogen med AUDIO_TS. AUDIO_TS är tom och används inte. Inuti VIDEO_TS-katalogen finns VOB-, BUP- och IFO-filer. VOB-filer innehåller MPEG-innehållet. Dessa är uppdelade i 1 GB eller mindre stora bitar så att dessa är kompatibla med alla operativsystem. IFO-filerna innehåller information om menyerna och titelstrukturen. BUK-filerna är säkerhetskopior av IFO-filerna med samma namn. Dessa filer är avsedda att förvaras i ett separat område fysiskt så att om IFO-filen skadas på grund av fysisk skada på DVD:n, kan BUK-filen ge samma information.

### Fysisk layout ###

- Alla filer på disken måste vara angränsande.
- De relaterade filerna ska ligga bredvid varandra (VOB, IFO, BUP).
- De numrerade filerna ska vara i stigande ordning.

## Kopieringsskydd ##

Många video-DVD-skivor är krypterade och förhindrar kopiering av data från DVD-skivan. Autentiserings- och dekrypteringsnycklar behövs för att spela upp filerna som finns i det otillgängliga ingångsområdet på DVD:n. Dessa nycklar används av CSS-dekrypteringsmjukvaran som finns i DVD-spelaren eller mjukvaruspelaren. Utan nycklarna kan videofilerna inte spelas upp eftersom nycklarna kommer att begäras när filerna öppnas.

## Referenser ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

