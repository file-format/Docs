---
date: 2019-10-11
keywords: vob, .vob, format de fișier vob, format de fișier .vob, extensie .vob, extensie vob, format video vob, fișiere dvd vob
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier VOB și despre API-urile care pot crea și deschide fișiere VOB."
title: Format de fișier VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Ce este un fișier VOB? ##

Fișierele VOB sunt stocate de obicei în directorul VIDEO_TS pe un DVD cu extensia .vob. Fișierele VOB conțin date video și audio, precum și alte date, cum ar fi meniuri și subtitrări. VOB se bazează pe formatul de flux de programe MPEG-2, dar are limitări și specificații suplimentare în fluxurile private. Fișierele VOB sunt un subset strict de fluxuri de programe MPEG, astfel încât toate fișierele VOB sunt fluxuri de programe MPEG, dar toate fluxurile de programe MPEG nu sunt compatibile cu VOB.

## Structura DVD-ului video ##

Când un DVD este deschis pe un computer, VIDEO_TS este directorul de nivel superior cu AUDIO_TS. AUDIO_TS este gol și nu este utilizat. În directorul VIDEO_TS, există fișiere VOB, BUP și IFO. Fișierele VOB conțin conținut MPEG. Acestea sunt împărțite în bucăți de 1 GB sau mai puțin, astfel încât acestea să fie compatibile cu toate sistemele de operare. Fișierele IFO conțin informații referitoare la meniuri și structura titlului. Fișierele BUK sunt fișiere de rezervă ale fișierelor IFO cu același nume. Aceste fișiere sunt menite să fie păstrate într-o zonă separată din punct de vedere fizic, astfel încât, în cazul în care fișierul IFO este deteriorat din cauza deteriorării fizice a DVD-ului, fișierul BUK poate furniza aceleași informații.

### Aspect fizic ###

- Toate fișierele de pe disc trebuie să fie învecinate.
- Fișierele aferente ar trebui să fie unul lângă celălalt (VOB, IFO, BUP).
- Fișierele numerotate ar trebui să fie în ordine crescătoare.

## Protecție la copiere ##

Multe DVD-uri video sunt criptate și împiedică copierea datelor de pe DVD. Cheile de autentificare și decriptare sunt necesare pentru a reda fișierele care se află în zona de intrare inaccesibilă a DVD-ului. Aceste chei sunt utilizate de software-ul de decriptare CSS care este prezent în playerul DVD sau playerul software. Fără chei, fișierele video nu pot fi redate, deoarece cheile vor fi solicitate la deschiderea fișierelor.

## Referințe ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Directory Structure](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

