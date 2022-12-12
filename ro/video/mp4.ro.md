---
date: 2019-10-11
keywords: MP4, fișier, extensie, format, format video, MPEG-4
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier MP4 și despre API-urile care pot crea și deschide fișiere MP4."
title: Format de fișier MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Ce este un fișier MP4? ##

MP4 (prescurtare pentru MPEG-4 Part 14) este un format de fișier bazat pe ISO/IEC 14496-12:2004, care se bazează pe QuickTime File Format, dar specifică în mod oficial suportul pentru Initial Object Descriptors (IOD) și alte caracteristici MPEG. Este folosit mai ales pentru a stoca videoclipuri și audio, dar poate fi folosit și pentru a stoca subtitrări și imagini statice. Fișierele MP4 sunt stocate cu extensia .mp4. MP4 este un standard internațional de codare audio-vizual. Similar cu majoritatea formatelor de containere moderne, MP4 acceptă streaming prin internet. Datorită compresiei mari utilizate în MP4, fișierele rezultate sunt mai mici ca dimensiune, aproape toată calitatea originală păstrată.

## Scurt istoric ##

Specificația MP4 a fost dezvoltată de Moving Picture Experts Group (MPEG) și s-a bazat pe formatul QuickTime [MOV](/ro/video/mov/) care a fost publicat în 2001. Prima versiune (ISO/IEC 14496-1:2001) a MP4 a fost o revizuire a MPEG-4 Part 1: Systems specification publicată în 1999. Formatul de fișier MP4 a fost generalizat la ISO Base Media File Format ISO/IEC 14496-12:2004 care a definit structura generală pentru fișierele media bazate pe timp. Ca rezultat, este folosit ca bază pentru alte formate de fișiere.

## Structura fișierelor MP4 ##

MP4 este un fișier container extensibil, ceea ce înseamnă că nu definește o structură strictă și permite o structură și o ierarhie personalizată pentru fiecare tip de media. Datele din fișierul MP4 sunt împărțite în două secțiuni, prima conținând datele legate de media și a doua conținând metadate. Datele media conțin audio sau video, iar metadatele indică steaguri pentru acces aleatoriu, marcaje de timp etc.
Structurile din MP4 sunt de obicei denumite atomi sau cutii. Dimensiunea minimă a unui atom este de 8 octeți (primii 4 octeți specifică dimensiunea, iar următorii 4 octeți specifică tipul). Iată o listă a atomilor la nivel de rădăcină conținute în fișierele MP:

- **ftyp**: Conține tipul fișierului, descrierea și structurile de date comune utilizate.
- **pdin**: Conține informații despre încărcarea/descărcarea progresivă a videoclipurilor.
- **moov**: Container pentru toate metadatele filmului.
- **moof**: Container cu fragmente video.
- **mfra**: containerul cu acces aleatoriu la fragmentul video
- **mdat**: Container de date pentru media.
- **stts**: tabel de eșantion la timp.
- **stsc**: tabel de la probă la bucată.
- **stsz**: dimensiunile eșantionului (încadrare)
- **meta**: containerul cu informațiile despre metadate.

Iată o listă de atomi de nivel doi utilizați în MP4:

- **mvhd**: conține informații despre antetul videoclipului cu detalii complete ale videoclipului.
- **trak**: Container cu pista individuală.
- **udta**: containerul cu informații despre utilizator și urmărire.
- **iods**: descriptor de fișier MP4

## Referințe ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

