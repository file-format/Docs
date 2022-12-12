{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - високоефективний відеокодек",
  "description":"Дізнайтеся про формат файлу IDX та API, які можуть створювати та відкривати файли IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Що таке файл IDX?

Файл IDX — це файл індексу субтитрів, який вказує на список інформації метаданих для субтитрів у файлі .sub (субтитри VobSub). Він створюється та використовується програмним додатком VobSub, який дозволяє користувачам видобувати субтитри з DVD-дисків і створювати файл SUB. Файли IDX містять мітки часу та зміщення байтів, які використовуються для вказівки на кожен окремий субтитр. VobSub завжди створює файл IDX разом із відповідним файлом SUB.

## Формат файлу IDX - Додаткова інформація

Файли IDX створюються та зберігаються як звичайні текстові файли, які можна відкрити в будь-якому текстовому редакторі. Файл IDX містить інформацію, яку зчитують медіаплеєри для зчитування таких параметрів, як колір тексту субтитрів для відображення на екрані, положення тексту субтитрів на екрані.

### Налаштування субтитрів IDX

Типовий файл IDX зберігає ці метадані на початку файлу. Параметри субтитрів починаються з **#**. Мітки часу та посилання на зображення додаються після всіх цих налаштувань субтитрів і починаються з **timestamp:**.

## Приклад формату файлу IDX

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

## Як використовувати файл IDX?

Якщо у вас є файли Sub та IDX для фільму, ви можете відтворювати ці субтитри разом із фільмом, для якого вони створені. Багато програм, як-от VLC, GOM Player, PotPlayer або PowerDVD, мають можливість завантажувати ці файли SUB та IDX і відтворювати їх разом із фільмом. Програмні програми також можуть вбудовувати файли субтитрів SUB та IDX у файли [.mkv](/uk/video/mkv/).

## Перетворення IDX на SRT

[SRT](/uk/video/srt/) (формат файлу SubRip) — це простий файл субтитрів, збережений у форматі файлу SubRip. Він використовується частіше порівняно з форматом файлу VobSub. Таким чином, якщо ви хочете конвертувати файли SUB/IDX у формат файлу SRT, для цього можна використовувати інструменти сторонніх розробників. Конвертер SUB/IDX у SRT, доступний на SubtitleTools.com, є одним із таких інструментів, який приймає файли SUB та IDX як вхідні дані та перетворює ці субтитри VobSub у файли SRT.

## Список літератури

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

