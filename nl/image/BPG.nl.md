---
date: 2020-08-12
keywords: bpg, .bpg, bpg-bestandsindeling, hoe bpg-bestanden te openen, .bpg-extensie, bPG-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG-bestandsindeling
linktitle: BPG
description: "Meer informatie over BPG-bestandsindeling en API's die BPG-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Wat is een BPG-bestand? ##

BPG (Better Portable Graphics) is een bestandsindeling die in 2014 door Fabrice Bellard is gemaakt voor digitale afbeeldingen. Hij stelde BPG voor als vervanging voor JPEG omdat BPG meer compressie of grootte-efficiënt was. BPG gebruikt de intra-frame-codering van de HEVC-standaard (High-Efficiency Video Coding) voor videocompressie.

BPG is ontworpen als een draagbaar geheugenefficiënt formaat om te werken op handheld- en IoT-apparaten. Momenteel ondersteunen webbrowsers het BPG-formaat niet, maar websites kunnen nog steeds BPG-afbeeldingen leveren met behulp van een JavaScript-bibliotheek die is geschreven door Bellard. BPG gebruikt het HEVC Main 4:4:4 16 Still Picture-profiel tot 14 bits per sample.

## Specificaties ##

Het BPG-containerformaat is een generiek beeldformaat in plaats van de onbewerkte bitstream die in HEVC wordt gebruikt. BPG ondersteunt 4:4:4, 4:2:2 en 4:2:0 kleurformaten. Alfakanaal wordt ook ondersteund met een apart gecodeerd extra kanaal of het vierde kanaal van CMYK-beeld. BPG biedt metadata-ondersteuning voor Exif, ICC-profielen en XMP. BPG ondersteunt YCbCr (ITU-R BT.601, BT.709 en BT.2020 (niet-constante luminantie)), YCgCo, RGB, CMYK en grijswaardenkleurruimte. BGP ondersteunt ook animatie en lossy en lossless HEVC-gegevenscompressie.

## Referenties ##

- [Betere draagbare afbeeldingen - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

