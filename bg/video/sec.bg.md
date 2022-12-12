---
date: 2022-03-25
keywords: sec, .sec, файлов формат sec, файлов формат .sec, разширение .sec, разширение sec
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Научете за SEC файловия формат и API, които могат да създават и отварят SEC файлове."
title: SEC файлов формат - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Какво е SEC файл?

SEC файлът е видео файл, който е създаден с DVR система за наблюдение на Samsung. Видеото се заснема от камери за наблюдение и се съхранява на диск във формат SEC. Записаният SEC видео може да се възпроизведе с видео софтуера на Samsung, който може да управлява видео подаване от множество камери.

## SEC файлов формат - повече информация

SEC файловете съдържат h264/AVC поток вътре, използвайки собствен файлов формат. Заглавката на SEC файл започва с номера на модела на SRD-1670D. Информацията за датата и часа се съхранява в края на файла.

### Конвертирайте SEC файл в AVI

SEC файлът може да бъде преобразуван в стандартния файлов формат [AVI](/bg/video/avi/) с помощта на FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Препратки ##

- [Файлове на Samsung и SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

