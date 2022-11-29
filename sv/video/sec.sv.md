---
date: 2022-03-25
keywords: sec, .sec, sec filformat, .sec filformat, .sec extension, sec extension
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig om SEC-filformat och API:er som kan skapa och öppna SEC-filer." 
title: SEC-filformat - Samsung säkerhetsvideofil
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Vad är SEC fil?

En SEC-fil är en videofil som skapas med Samsungs DVR-övervakningssystem. Video spelas in från övervakningskameror och lagras på skiva i SEC-format. Den inspelade SEC-videon kan spelas upp med Samsungs videoprogramvara som kan hantera videoflöden från flera kameror.

## SEC-filformat - Mer information

SEC-filer innehåller h264/AVC-ström inuti med proprietärt filformat. Rubriken på en SEC-fil börjar med modellnumret för SRD-1670D. Information om datum och tid finns i slutet av filen.

### Konvertera SEC-fil till AVI

SEC-filen kan konverteras till standardfilformatet [AVI](/sv/video/avi/) med FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referenser ##

- [Samsung och SEC-filer](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

