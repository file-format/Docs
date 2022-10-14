---
date: 2022-03-25
keywords: "sec, .sec, sec-Dateiformat, .sec-Dateiformat, .sec-Erweiterung, sec-Erweiterung"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Erfahren Sie mehr über das SEC-Dateiformat und APIs, die SEC-Dateien erstellen und öffnen können."
title: "SEC-Dateiformat - Samsung-Sicherheitsvideodatei"
linktitle: "SEK"
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Was ist eine SEC-Datei?

Eine SEC-Datei ist eine Videodatei, die mit dem Samsung DVR-Überwachungssystem erstellt wird. Videos werden von Überwachungskameras erfasst und im SEC-Format auf Disc gespeichert. Das aufgezeichnete SEC-Video kann mit der Videosoftware von Samsung wiedergegeben werden, die Video-Feeds von mehreren Kameras verwalten kann.

## SEC-Dateiformat – Weitere Informationen

SEC-Dateien enthalten einen h264/AVC-Stream in einem proprietären Dateiformat. Der Header einer SEC-Datei beginnt mit der Modellnummer des SRD-1670D. Die Datums- und Uhrzeitinformationen werden am Ende der Datei gespeichert.

### SEC-Datei in AVI konvertieren

SEC-Dateien können mit FFmpeg in das Standarddateiformat [AVI](/de/video/avi/) konvertiert werden.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Verweise ##

- [Samsung- und SEC-Dateien](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

