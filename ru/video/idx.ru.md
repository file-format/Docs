{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX — высокоэффективный видеокодек",
  "description":"Узнайте о формате файлов IDX и API, которые могут создавать и открывать файлы IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## .IDX вариант №

Файл IDX представляет собой индексный файл субтитров, который указывает на список метаданных для субтитров внутри файла .sub (VobSub Subtitles). Он создается и используется программным приложением VobSub, которое позволяет пользователям извлекать субтитры с DVD-дисков и выгружать их в файл SUB. Файлы IDX содержат метки времени и смещения байтов, используемые для указания на каждый отдельный субтитр. VobSub всегда создает файл IDX вместе с соответствующим файлом SUB.

## Формат файла IDX — дополнительная информация

Файлы IDX создаются и сохраняются в виде простых текстовых файлов, которые можно открыть в любом текстовом редакторе. Файл IDX содержит информацию, которая считывается медиаплеерами для чтения таких параметров, как цвет текста субтитров для отображения на экране, положение текста субтитров на экране.

### Настройки субтитров IDX

Типичный файл IDX хранит эту информацию метаданных в начале файла. Настройки субтитров начинаются с **#**. Временные метки и ссылки на изображения добавляются после всех этих настроек субтитров и начинаются с **timestamp:**.

## Пример формата файла IDX

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

## Как использовать файл IDX?

Если у вас есть файлы Sub и IDX для фильма, вы можете воспроизводить эти субтитры вместе с фильмом, для которого они созданы. Многие приложения, такие как VLC, GOM Player, PotPlayer или PowerDVD, имеют возможность загружать эти файлы SUB и IDX и воспроизводить их вместе с фильмом. Программные приложения также могут встраивать файлы субтитров SUB и IDX в файлы [.mkv](/ru/video/mkv/).

## Конвертировать IDX в SRT

[SRT](/ru/video/srt/) (формат файла SubRip) — это простой файл субтитров, сохраненный в формате файла SubRip. Он чаще используется по сравнению с форматом файла VobSub. Таким образом, если вы хотите преобразовать файлы SUB/IDX в формат файлов SRT, для этого можно использовать сторонние инструменты. Конвертер SUB/IDX в SRT, доступный на SubtitleTools.com, является одним из таких инструментов, который принимает файлы SUB и IDX в качестве входных данных и преобразует эти субтитры VobSub в файлы SRT.

## использованная литература

* [VobSub] (https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

