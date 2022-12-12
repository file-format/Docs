---
date: 2022-03-25
keywords: sec, .sec, format pliku sec, format pliku .sec, rozszerzenie .sec, rozszerzenie sec
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się o formacie pliku SEC i interfejsach API, które mogą tworzyć i otwierać pliki SEC."
title: Format pliku SEC — plik wideo Samsung Security
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Czym jest plik SEK?

Plik SEC to plik wideo utworzony za pomocą systemu nadzoru Samsung DVR. Wideo jest przechwytywane z kamer monitorujących i zapisywane na dysku w formacie SEC. Nagrane wideo SEC można odtwarzać za pomocą oprogramowania wideo firmy Samsung, które może zarządzać strumieniem wideo z wielu kamer.

## Format pliku SEC — więcej informacji

Pliki SEC zawierają strumień h264/AVC wewnątrz przy użyciu zastrzeżonego formatu pliku. Nagłówek pliku SEC zaczyna się od numeru modelu SRD-1670D. Informacje o dacie i godzinie są przechowywane na końcu pliku.

### Konwertuj plik SEC na AVI

Plik SEC można przekonwertować na standardowy format pliku [AVI](/pl/video/avi/) za pomocą FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Bibliografia ##

- [Pliki Samsunga i SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

