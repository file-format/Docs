---
date: 2020-08-12
keywords: bpg, .bpg, format pliku bpg, jak otwierać pliki bpg, rozszerzenie .bpg, rozszerzenie bpg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku BPG
linktitle: BPG
description: "Dowiedz się o formacie pliku BPG i interfejsach API, które mogą tworzyć i otwierać pliki BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Czym jest plik BPG? ##

BPG (Better Portable Graphics) to format pliku stworzony przez Fabrice'a Bellarda w 2014 roku dla obrazów cyfrowych. Zaproponował BPG jako zamiennik JPEG, ponieważ BPG był bardziej wydajny pod względem kompresji lub rozmiaru. BPG wykorzystuje kodowanie wewnątrzklatkowe standardu kompresji wideo HEVC (High-Efficiency Video Coding).

BPG został zaprojektowany jako przenośny, wydajny format pamięci do pracy na urządzeniach przenośnych i IoT. Obecnie przeglądarki internetowe nie obsługują formatu BPG, ale strony internetowe nadal mogą dostarczać obrazy BPG przy użyciu biblioteki JavaScript napisanej przez firmę Bellard. BPG wykorzystuje profil HEVC Main 4:4:4 16 Still Picture do 14 bitów na próbkę.

## Specyfikacje ##

Format kontenera BPG jest ogólnym formatem obrazu, a nie surowym strumieniem bitów używanym w HEVC. BPG obsługuje formaty kolorów 4:4:4, 4:2:2 i 4:2:0. Kanał alfa jest również obsługiwany za pomocą oddzielnie kodowanego dodatkowego kanału lub czwartego kanału obrazu CMYK. BPG zapewnia obsługę metadanych dla profili Exif, ICC i XMP. BPG obsługuje YCbCr (ITU-R BT.601, BT.709 i BT.2020 (niestała luminancja)), YCgCo, RGB, CMYK i skalę szarości. BGP obsługuje również animację oraz stratną i bezstratną kompresję danych HEVC.

## Bibliografia ##

- [Lepsza przenośna grafika - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

