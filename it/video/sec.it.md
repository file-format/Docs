---
date: 2022-03-25
keywords: sec, .sec, formato file sec, formato file .sec, estensione .sec, estensione sec
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Scopri il formato di file SEC e le API che possono creare e aprire file SEC."
title: Formato file SEC - File video di sicurezza Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Che cos'è un file SEC?

Un file SEC è un file video creato con il sistema di sorveglianza DVR Samsung. Il video viene catturato dalle telecamere di sorveglianza e archiviato su disco in formato SEC. Il video SEC registrato può essere riprodotto con il software video Samsung in grado di gestire il feed video da più fotocamere.

## Formato file SEC - Ulteriori informazioni

I file SEC contengono il flusso h264/AVC all'interno utilizzando un formato di file proprietario. L'intestazione di un file SEC inizia con il numero di modello dell'SRD-1670D. Le informazioni sulla data e l'ora sono conservate alla fine del file.

### Converti file SEC in AVI

Il file SEC può essere convertito nel formato file standard [AVI](/it/video/avi/) utilizzando FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Riferimenti ##

- [File Samsung e SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

