{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX - High Efficiency Video Codec",
  "description": "Opi IDX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata IDX-tiedostoja.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-fix"
}
},
  "lastmod": "2022-07-12"
}

## Mikä on IDX-tiedosto?

IDX-tiedosto on tekstityshakemistotiedosto, joka osoittaa .sub-tiedoston (VobSub Subtitles) sisällä olevien tekstitysten metatietoluetteloon. Sen luo ja käyttää VobSub-ohjelmistosovellus, jonka avulla käyttäjät voivat poimia tekstityksiä DVD-levyiltä ja upottaa ne SUB-tiedostoon. IDX-tiedostot sisältävät aikaleimoja ja tavupoikkeamia, joita käytetään osoittamaan jokaista tekstitystä. VobSub luo aina IDX-tiedoston yhdessä vastaavan SUB-tiedoston kanssa.

## IDX-tiedostomuoto - lisätietoja

IDX-tiedostot luodaan ja tallennetaan tekstitiedostoina, jotka voidaan avata missä tahansa tekstieditorissa. IDX-tiedosto sisältää tiedot, jotka mediasoittimet lukevat parametrien, kuten näytöllä näytettävän tekstitystekstin värin, tekstitystekstin sijainnin näytöllä, lukemiseksi.

### IDX-tekstitysasetukset

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## Esimerkki IDX-tiedostomuodosta

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

## Kuinka käyttää IDX-tiedostoa?

Jos sinulla on elokuvan Sub- ja IDX-tiedostot, voit toistaa nämä tekstitykset yhdessä elokuvan kanssa, jota varten ne on luotu. Monet sovellukset, kuten VLC, GOM Player, PotPlayer tai PowerDVD, voivat ladata nämä SUB- ja IDX-tiedostot ja toistaa niitä elokuvan rinnalla. Ohjelmistosovellukset voivat myös upottaa SUB- ja IDX-tekstitystiedostoja [.mkv](/video/mkv/)-tiedostoihin.

## Muunna IDX SRT:ksi

[SRT](/video/srt/) (SubRip-tiedostomuoto) on yksinkertainen tekstitystiedosto, joka on tallennettu SubRip-tiedostomuotoon. Sitä käytetään yleisemmin VobSub-tiedostomuotoon verrattuna. Siten, jos haluat muuntaa SUB/IDX-tiedostoja SRT-tiedostomuotoon, on saatavilla kolmannen osapuolen työkaluja, joita voidaan käyttää tämän saavuttamiseen. SubtitleTools.com-sivustolta saatavilla oleva SUB/IDX-SRT-muunnin on yksi tällainen työkalu, joka ottaa SUB- ja IDX-tiedostoja syötteenä ja muuntaa nämä VobSub-tekstitykset SRT-tiedostoiksi.

## Viitteet

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

