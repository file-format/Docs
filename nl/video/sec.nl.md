---
date: 2022-03-25
keywords: sec, .sec, sec bestandsformaat, .sec bestandsformaat, .sec extensie, sec extensie
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Meer informatie over SEC-bestandsindelingen en API's die SEC-bestanden kunnen maken en openen."
title: SEC-bestandsindeling - Samsung-beveiligingsvideobestand
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Wat is een SEC-bestand?

Een SEC-bestand is een videobestand dat is gemaakt met het Samsung DVR-bewakingssysteem. Video wordt vastgelegd van bewakingscamera's en opgeslagen op schijf in SEC-formaat. De opgenomen SEC-video kan worden afgespeeld met Samsung's videosoftware die de videofeed van meerdere camera's kan beheren.

## SEC-bestandsindeling - Meer informatie

SEC-bestanden bevatten een h264/AVC-stream in het eigen bestandsformaat. De header van een SEC-bestand begint met het modelnummer van de SRD-1670D. De datum- en tijdinformatie wordt aan het einde van het bestand bewaard.

### Converteer SEC-bestand naar AVI

SEC-bestand kan worden geconverteerd naar het standaard [AVI](/nl/video/avi/)-bestandsformaat met behulp van FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referenties ##

- [Samsung- en SEC-bestanden](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

