{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX — augstas efektivitātes video kodeks",
  "description": "Uzziniet par IDX failu formātu un API, kas var izveidot un atvērt IDX failus.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-lvx"
}
},
  "lastmod": "2022-07-12"
}

## Kas ir IDX fails?

IDX fails ir subtitru indeksa fails, kas norāda uz metadatu informācijas sarakstu subtitriem .sub (VobSub Subtitles) failā. To izveido un izmanto programmatūras lietojumprogramma VobSub, kas lietotājiem ļauj izvilkt subtitrus no DVD un izmest SUB failā. IDX faili satur laikspiedolus un baitu nobīdes, ko izmanto, lai norādītu uz katru apakšvirsrakstu. VobSub vienmēr izveido IDX failu kopā ar atbilstošo SUB failu.

## IDX faila formāts — vairāk informācijas

IDX faili tiek ģenerēti un saglabāti kā vienkārša teksta faili, kurus var atvērt jebkurā teksta redaktorā. IDX fails satur informāciju, ko nolasa multivides atskaņotāji, lai nolasītu tādus parametrus kā ekrānā parādāmā subtitru teksta krāsa, subtitru teksta novietojums ekrānā.

### IDX subtitru iestatījumi

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## IDX faila formāta piemērs

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

## Kā lietot IDX failu?

Ja jums ir filmas sub un IDX faili, varat atskaņot šos subtitrus kopā ar filmu, kurai tie ir izveidoti. Daudzām lietojumprogrammām, piemēram, VLC, GOM Player, PotPlayer vai PowerDVD, ir iespēja ielādēt šos SUB un IDX failus un atskaņot tos kopā ar filmu. Programmatūras lietojumprogrammas var arī iegult SUB un IDX subtitru failus [.mkv](/video/mkv/) failos.

## Konvertējiet IDX uz SRT

[SRT](/video/srt/) (SubRip faila formāts) ir vienkāršs subtitru fails, kas saglabāts SubRip faila formātā. To izmanto biežāk nekā VobSub faila formātu. Tādējādi, ja vēlaties konvertēt SUB/IDX failus SRT faila formātā, ir pieejami trešās puses rīki, ko var izmantot, lai to panāktu. SUB/IDX uz SRT pārveidotājs, kas pieejams vietnē SubtitleTools.com, ir viens no šādiem rīkiem, kas izmanto SUB un IDX failus kā ievadi un pārvērš šos VobSub subtitrus par SRT failiem.

## Atsauces

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

