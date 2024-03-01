---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lansaitse SEC-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata SEC-tiedostons.
title: SEC-tiedostomuoto - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Mikä on SEC-tiedosto?

SEC-tiedosto on videotiedosto, joka luodaan Samsungin DVR-valvontajärjestelmällä. Video kaapataan valvontakameroista ja tallennetaan levylle SEC-muodossa. Tallennettua SEC-videota voidaan toistaa Samsungin videoohjelmistolla, joka voi hallita videosyötteitä useista kameroista.

## SEC-tiedostomuoto – lisätietoja

SEC-tiedostot sisältävät h264/AVC-virran omassa tiedostomuodossa. SEC-tiedoston otsikko alkaa SRD-1670D:n mallinumerolla. Päivämäärä- ja aikatiedot ovat tiedoston lopussa.

### Muunna SEC-tiedosto AVI:ksi

SEC-tiedosto voidaan muuntaa normaaliin [AVI](/video/avi/)-tiedostomuotoon FFmpeg:llä.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Viitteet ##

- {{HYPERLINKKI1}}

