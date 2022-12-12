---
date: 2020-08-12
keywords: jfif, .jfif, format de fișier jfif, cum se deschide fișierele jfif, extensia .jfif, extensia jfif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Fișier JFIF - Ce este un fișier .jfif?
linktitle: JFIF
description: "Aflați despre formatul de fișier JFIF și despre API-urile care pot crea și deschide fișiere JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Ce este un fișier JFIF?

JFIF (JPEG File Interchange Format (JFIF)) este un fișier în format imagine care utilizează extensia .jfif. JFIF construiește peste JIF (JPEG Interchange Format) reducând complexitatea și rezolvându-i limitările.

## Scurt istoric al JFIF

Dezvoltarea documentelor JFIF a fost condusă de Eric Hamilton și un acord privind prima versiune a fost stabilit la sfârșitul anului 1991. Versiunea 1.02 a fost publicată pe 7 septembrie 1992. RFC 2046 a specificat că formatul JFIF este folosit pentru a transmite imagini JPEG pe internet. JFIF a fost publicat de ECMA în 2009 și a fost standardizat de ITU-T în 2011 ca Recomandarea sa T.871 și de ISO/IEC în 2013 ca ISO/IEC 10918-5

## Format fișier JFIF ##

Un fișier JFIF constă dintr-o secvență de markeri așa cum este definit în partea 1 a standardului JPEG. Fiecare marker constă din doi octeți (FF urmat de un octet care specifică tipul de marker). Markerii pot fi fie autonomi, fie pot indica începutul unui segment de marcator.

JFIF permite ca mai multe componente precum Y, Cb, Cr să aibă rezoluții diferite, dar alinierea lor nu este definită. Spre deosebire de JPEG, JFIF poate oferi informații despre rezoluție și raport de aspect. JFIF definește, de asemenea, modelul de culoare care trebuie utilizat.

### Structura fișierului ##

|Segment|Cod|Descriere|
|---|---|---|
|SOI|FF D8|Începutul imaginii|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segmente de marcare suplimentare|
|SOS|FF DA|Start of Scan|
||date de imagine comprimate||
|EOI|FF D9|Sfârșitul imaginii|

Standardul JFIF definește următoarele segmente:

### Segment marker JFIF APP0 ###

Este un segment obligatoriu care conține parametri de imagine. De asemenea, poate conține o miniatură necomprimată încorporată.

|Câmp|Dimensiune (octeți)|Descriere|
|---|---|---|
|Marcator APP0|2|FF E0|
|Lungime|2|Lungimea segmentului excluzând markerul APP0|
|Identificator|5|JFIF (4A 46 49 46 00) în ASCII terminat cu un octet nul|
|Versiunea JFIF|2|Versiunea JFIF|
|Unități de densitate|1|Unitate pentru următoarele câmpuri de densitate de pixeli</br> 00: Fără unități; raportul de aspect lățime: înălțime este egal cu Ydensity:Xdensity</br> 01 : Pixeli pe inch</br> 02 : Pixeli pe centimetru|
|Xdensity|2|Densitate orizontală a pixelilor mai mare decât zero|
|Ydensity|2|Densitate verticală a pixelilor mai mare decât zero|
|Xthumbnail|1|Numărul orizontal de pixeli al miniaturii RGB încorporate. Poate fi zero|
|Ythumbnail|1|Numărul de pixeli pe verticală a miniaturii RGB încorporate. Poate fi zero|
|Date miniaturi|3 × n|Date miniaturi raster RGB pe 24 de biți necomprimate|

### Segment de marcare APP0 extensie JFIF ###

Aceasta este o secțiune opțională care, dacă este definită, trebuie să urmeze imediat segmentul marker JFIF APP0. Această secțiune este acceptată de JFIF versiunea 1.02 și mai sus și permite încorporarea de miniaturi în trei formate diferite.

|Câmp|Dimensiune (octeți)|Descriere|
|---|---|---|
|Marcator APP0|2|FF E0|
|Lungime|2|Lungimea segmentului excluzând markerul APP0|
|Identificator|5|JFXX (4A 46 58 58 00) în ASCII terminat cu un octet nul|
|Format miniatură|1|Specifică ce format de date este utilizat pentru următoarea miniatură încorporată:</br> 10 : format JPEG</br> 11 : format paletizat de 1 octet per pixel</br> 13 : format RGB de 3 octeți per pixel|
|Date miniaturi|variabilă||

## Conversia JFIF în alte formate de fișiere imagine

JFIF poate fi convertit în formate populare de fișiere imagine, cum ar fi [PNG](/ro/image/png/), [JPG](/ro/image/jpg/) și [PDF](/ro/pdf/).

## Referințe ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

