---
date: 2020-08-12
keywords: jxr, .jxr, format de fișier jxr, cum se deschide fișierele jxr, extensia .jxr, extensia jxr
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier JXR
linktitle: JXR
description: "Aflați despre formatul de fișier JXR și despre API-urile care pot crea și deschide fișiere JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Ce este un fișier JXR? ##

JPEG XR (JPEG extins range) este un format de fișier pentru imagini fotografice cu ton continuu. Este un standard de compresie a imaginilor statice care se bazează pe HD Photo dezvoltat de Microsoft. Acceptă atât compresia cu pierderi, cât și fără pierderi.

## Scurt istoric ##

Windows Media Photo a fost anunțată pentru prima dată de Microsoft la WinHEC 2006. A fost redenumită HD Photo în noiembrie 2006. JPEG XR a fost aprobat ca standard internațional ISO/IEC 29199-2 la 19 iunie 2009. ITU-T și ISO/IEC au publicat o moțiune specificație de format (ITU-T T.833 | ISO/IEC 29199-3), un set de testare de conformitate (ITU-T T.834 | ISO/IEC 29199-4) și software de referință (ITU-T T.835 | ISO /IEC 29199-5) pentru JPEG XR după finalizarea specificației de codificare a imaginii în 2010. Un raport tehnic care descrie arhitectura fluxului de lucru pentru JPEG XR a fost publicat în 2011.

## Design JPEG XR ##

În comparație cu JPEG, JPEG XR oferă mai multe îmbunătățiri, inclusiv:

- **Compresie mai bună**: JPEG XR oferă rapoarte de compresie mai mari.
- **Compresie fără pierderi**: JPEG XR acceptă compresie fără pierderi.
- **Tile Structure**: imaginea JPEG XR poate fi segmentată în regiuni tile unde fiecare regiune poate fi decodificată separat.
- **Mai multă acuratețe a culorii**: JPEG XR include conversia internă în spațiul de culoare YCoCg pentru suportarea imaginilor folosind spațiul de culoare RGB. JPEG XR acceptă, de asemenea, un model de culoare CMYK întreg de 16 biți per componentă (64 de biți per pixel). JPEG XR acceptă formatul de culoare în virgulă mobilă cu exponent partajat RGBE pentru imaginile HDR. JPEG XR acceptă, de asemenea, codificări color în tonuri de gri și multicanal.
- **Hartă de transparență**: JPEG XR acceptă canalul alfa pentru transparență.
- **Modificarea imaginii domeniului comprimat**: Imaginile JPEG XR pot fi convertite la codificare cu pierderi, rezoluție redusă, decupate, răsturnate, rotite, iar structura plăcilor poate fi modificată fără decodarea completă a fișierului.
- **Suport metadate**: fișierul imagine JPEG XR poate conține un profil de culoare ICC pentru o reprezentare coerentă a culorii pe mai multe dispozitive. Formatul acceptă și formatele de metadate Exif și XMP.

## Format container ##

Datele de imagine JPEG XR pot fi stocate în format container asemănător TIFF utilizând un tabel de etichete Image File Directory (IFT). Un fișier JXR conține următoarele în etichete IFD:

- Date de imagine: sunt date de imagine autonome contigue.
- Date opționale ale canalului alfa: dacă acestea sunt prezente, datele imaginii pot fi comprimate separat, permițând suportul aplicațiilor care nu acceptă transparența.
- Metadate
- Metadate XMP opționale
- Metadate Exif opționale

Deoarece se bazează pe formatul TIFF, moștenește toate limitările formatului TIFF, cum ar fi limita de dimensiune a fișierului de 4 GB.

## Referințe ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

