{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - високоефективен видео кодек",
  "description":"Научете за IDX файловия формат и API, които могат да създават и отварят IDX файлове.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Какво е IDX файл?

IDX файлът е файл с индекс на субтитри, който сочи към списъка с информация за метаданни за субтитри в .sub (VobSub субтитри) файл. Създава се и се използва от софтуерното приложение VobSub, което позволява на потребителите да извличат субтитри от DVD и да ги изхвърлят в SUB файл. IDX файловете съдържат времеви отпечатъци и отмествания в байтове, използвани за насочване към всеки отделен субтитър. VobSub винаги създава IDX файл заедно със съответния SUB файл.

## IDX файлов формат - повече информация

IDX файловете се генерират и записват като обикновени текстови файлове, които могат да се отварят във всеки текстов редактор. IDX файлът съдържа информация, която се чете от мултимедийните плейъри за четене на параметри като цвета на текста на субтитрите за показване на екрана, позицията на текста на субтитрите на екрана.

### IDX настройки на субтитрите

Типичен IDX файл съхранява тази информация за метаданни в началото на файла. Настройките на субтитрите започват с **#**. Времеви клейма и препратки към изображения се добавят след всички тези настройки на субтитрите и започват с **timestamp:**.

## Пример за IDX файлов формат

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## Как да използвам IDX файл?

Ако имате Sub и IDX файловете за филм, можете да възпроизвеждате тези субтитри заедно с филма, за който са създадени. Много приложения като VLC, GOM Player, PotPlayer или PowerDVD имат способността да зареждат тези SUB и IDX файлове и да ги възпроизвеждат заедно с филма. Софтуерните приложения могат също да вграждат SUB и IDX файлове със субтитри в [.mkv](/bg/video/mkv/) файлове.

## Преобразувайте IDX в SRT

[SRT](/bg/video/srt/) (файлов формат SubRip) е прост файл със субтитри, записан във файлов формат SubRip. Той се използва по-често в сравнение с файловия формат VobSub. По този начин, ако искате да конвертирате SUB/IDX файлове в SRT файлов формат, има налични инструменти на трети страни, които могат да се използват за постигане на това. SUB/IDX към SRT конвертор, достъпен на SubtitleTools.com, е един такъв инструмент, който приема SUB и IDX файлове като вход и преобразува тези VobSub субтитри в SRT файлове.

## Препратки

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Уики мултимедия](https://wiki.multimedia.cx/index.php?title=VOBsub)

