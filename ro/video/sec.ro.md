---
date: 2022-03-25
keywords: sec, .sec, format de fișier sec, format de fișier .sec, extensie .sec, extensie sec
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Aflați despre formatul de fișier SEC și despre API-urile care pot crea și deschide fișiere SEC."
title: Format fișier SEC - Fișier video de securitate Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Ce este un fișier SEC?

Un fișier SEC este un fișier video care este creat cu sistemul de supraveghere Samsung DVR. Videoclipul este captat de la camerele de supraveghere și stocat pe disc în format SEC. Videoclipul SEC înregistrat poate fi redat cu software-ul video Samsung care poate gestiona fluxul video de la mai multe camere.

## Format de fișier SEC - Mai multe informații

Fișierele SEC conțin flux h264/AVC în interior folosind formatul de fișier proprietar. Antetul unui fișier SEC începe cu numărul de model al SRD-1670D. Informațiile privind data și ora sunt păstrate la sfârșitul fișierului.

### Convertiți fișierul SEC în AVI

Fișierul SEC poate fi convertit în formatul standard de fișier [AVI](/ro/video/avi/) folosind FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referințe ##

- [Fișiere Samsung și SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

