---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Luždirbti apie SEC failo formatą ir API, kurios gali sukurti ir atidaryti SEC failąs.
title: SEC failo formatas – Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Kas yra SEC failas?

SEC failas yra vaizdo failas, sukurtas naudojant Samsung DVR stebėjimo sistemą. Vaizdo įrašas fiksuojamas iš stebėjimo kamerų ir saugomas diske SEC formatu. Įrašytą SEC vaizdo įrašą galima atkurti naudojant Samsung vaizdo įrašų programinę įrangą, kuri gali valdyti vaizdo įrašų tiekimą iš kelių kamerų.

## SEC failo formatas – daugiau informacijos

SEC failuose yra h264 / AVC srautas, naudojant patentuotą failo formatą. SEC failo antraštė prasideda SRD-1670D modelio numeriu. Datos ir laiko informacija yra failo pabaigoje.

### Konvertuoti SEC failą į AVI

SEC failą galima konvertuoti į standartinį [AVI](/video/avi/) failo formatą naudojant FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Nuorodos Nr.

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

