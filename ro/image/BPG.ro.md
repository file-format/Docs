---
date: 2020-08-12
keywords: bpg, .bpg, format de fișier bpg, cum se deschide fișierele bpg, extensia .bpg, extensia bpg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier BPG
linktitle: BPG
description: "Aflați despre formatul de fișier BPG și despre API-urile care pot crea și deschide fișiere BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Ce este un fișier BPG? ##

BPG (Better Portable Graphics) este un format de fișier creat de Fabrice Bellard în 2014 pentru imagini digitale. El a propus BPG ca înlocuitor pentru JPEG, deoarece BPG era mai eficient în compresie sau dimensiune. BPG utilizează codificarea intra-cadru a standardului de compresie video HEVC (High-Efficiency Video Coding).

BPG este conceput ca un format portabil eficient din punct de vedere al memoriei pentru a funcționa pe dispozitive portabile și IoT. În prezent, browserele web nu acceptă formatul BPG, dar site-urile web pot livra în continuare imagini BPG utilizând o bibliotecă JavaScript scrisă de Bellard. BPG folosește profilul principal al HEVC 4:4:4 16 Still Picture de până la 14 biți per probă.

## Specificații ##

Formatul container BPG este un format de imagine generic, mai degrabă decât fluxul de biți brut utilizat în HEVC. BPG acceptă formatele de culoare 4:4:4, 4:2:2 și 4:2:0. Canalul alfa este, de asemenea, acceptat cu un canal suplimentar codificat separat sau cu al patrulea canal al imaginii CMYK. BPG oferă suport pentru metadate pentru Exif, profiluri ICC și XMP. BPG acceptă YCbCr (ITU-R BT.601, BT.709 și BT.2020 (luminanță non-constant)), YCgCo, RGB, CMYK și spațiu de culoare în tonuri de gri. BGP acceptă, de asemenea, animație și comprimarea datelor HEVC cu pierderi și fără pierderi.

## Referințe ##

- [Better Portable Graphics - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

