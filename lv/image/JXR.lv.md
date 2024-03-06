---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR faila veidlapaat
linktitle: JXR
description: Lnopelniet par JXR faila formātu un API, kas var izveidot un atvērt JXR failus.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Kas ir JXR fails? ##

JPEG XR (JPEG paplašinātais diapazons) ir failu formāts nepārtrauktu toņu fotogrāfiju attēliem. Tas ir nekustīgu attēlu saspiešanas standarts, kura pamatā ir Microsoft izstrādātais HD fotoattēls. Tā atbalsta gan zudumu, gan bezzudumu saspiešanu.

## Īsa vēsture ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. 2006. gada novembrī tas tika pārdēvēts par HD Photo. JPEG XR tika apstiprināts kā starptautiskais standarts ISO/IEC 29199-2 2009. gada 19. jūnijā. ITU-T un ISO/IEC publicēja kustības formāta specifikāciju (ITU-T T.833 | ISO/ IEC 29199-3), atbilstības pārbaudes komplekts (ITU-T T.834 | ISO/IEC 29199-4) un atsauces programmatūra (ITU-T T.835 | ISO/IEC 29199-5) JPEG XR pēc pabeigšanas. attēla kodēšanas specifikācijas 2010. gadā. Tehniskais ziņojums, kurā aprakstīta JPEG XR darbplūsmas arhitektūra, tika publicēts 2011. gadā.

## JPEG XR dizains ##

Salīdzinot ar JPEG, JPEG XR piedāvā vairākus uzlabojumus, tostarp:

- **Labāka saspiešana**: JPEG XR piedāvā lielāku saspiešanas pakāpi.
- **Bezzudumu saspiešana**: JPEG XR atbalsta bezzudumu saspiešanu.
- **Flīžu struktūra**: JPEG XR attēlu var segmentēt flīžu reģionos, kur katru reģionu var atšifrēt atsevišķi.
- **Lielāka krāsu precizitāte**: JPEG XR ietver iekšēju pārveidošanu YCoCg krāsu telpā, lai atbalstītu attēlus, izmantojot RGB krāsu telpu. JPEG XR atbalsta arī 16 bitu uz komponentu (64 biti uz pikseļu) veselu CMYK krāsu modeli. JPEG XR atbalsta RGBE dalītā eksponenta peldošā punkta krāsu formātu HDR attēliem. JPEG XR atbalsta arī pelēktoņu un daudzkanālu krāsu kodējumus.
- **Caurspīdības karte**: JPEG XR atbalsta alfa kanālu caurspīdīgumam.
- **Saspiestā domēna attēla modifikācijas**: JPEG XR attēlus var pārveidot par kodējumu ar zaudējumiem, samazināt izšķirtspēju, apgriezt, apgriezt, pagriezt, un visu var mainīt elementu struktūru bez pilnīgas faila dekodēšanas.
- **Metadatu atbalsts**: JPEG XR attēla failā var būt ietverts ICC krāsu profils, lai nodrošinātu konsekventu krāsu attēlojumu vairākās ierīcēs. Formāts atbalsta arī Exif un XMP metadatu formātus.

## Konteinera formāts ##

JPEG XR attēla datus var saglabāt TIFF līdzīgā konteinera formātā, izmantojot attēlu failu direktorija (IFT) tagu tabulu. JXR fails IFD tagos satur:

- Attēla dati: tie ir blakus esoši atsevišķi attēla dati.
- Izvēles alfa kanāla dati: ja tādi ir, attēla datus var saspiest atsevišķi, ļaujot atbalstīt lietojumprogrammas, kas neatbalsta caurspīdīgumu.
- Metadati
- Izvēles XMP metadati
- Izvēles Exif metadati

Tā kā tas ir balstīts uz TIFF formātu, tas pārmanto visus TIFF formāta ierobežojumus, piemēram, 4 GB faila lieluma ierobežojumu.

## Atsauces Nr.

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

