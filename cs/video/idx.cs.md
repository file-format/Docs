{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX – vysoce účinný video kodek",
  "description":"Další informace o formátu souborů IDX a rozhraních API, která mohou vytvářet a otevírat soubory IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Co je soubor IDX?

Soubor IDX je soubor indexu titulků, který ukazuje na seznam informací metadat pro titulky v souboru .sub (VobSub Subtitles). Je vytvořen a používán softwarovou aplikací VobSub, která uživatelům umožňuje extrahovat titulky z DVD a uložit je do SUB souboru. Soubory IDX obsahují časová razítka a bajtové offsety používané k ukázání na každý jednotlivý titulek. VobSub vždy vytvoří soubor IDX spolu s odpovídajícím souborem SUB.

## Formát souboru IDX – Další informace

Soubory IDX se generují a ukládají jako soubory ve formátu prostého textu, které lze otevřít v libovolném textovém editoru. Soubor IDX obsahuje informace, které jsou čteny přehrávači médií za účelem čtení parametrů, jako je barva textu titulků pro zobrazení na obrazovce, poloha textu titulků na obrazovce.

### Nastavení titulků IDX

Typický soubor IDX ukládá tyto informace o metadatech na začátek souboru. Nastavení titulků začíná znakem **#**. Časová razítka a odkazy na obrázky jsou přidány po všech těchto nastaveních titulků a začínají **časovým razítkem:**.

## Příklad formátu souboru IDX

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

## Jak používat soubor IDX?

Pokud máte pro film soubory Sub a IDX, můžete tyto titulky přehrát spolu s filmem, pro který byly vytvořeny. Mnoho aplikací, jako je VLC, GOM Player, PotPlayer nebo PowerDVD, má schopnost načíst tyto soubory SUB a IDX a přehrát je spolu s filmem. Softwarové aplikace mohou také vkládat soubory titulků SUB a IDX do souborů [.mkv](/cs/video/mkv/).

## Převést IDX na SRT

[SRT](/cs/video/srt/) (formát souboru SubRip) je jednoduchý soubor titulků uložený ve formátu souboru SubRip. Ve srovnání s formátem souboru VobSub se používá častěji. Pokud tedy chcete převést soubory SUB/IDX do formátu souboru SRT, jsou k dispozici nástroje třetích stran, které lze použít k dosažení tohoto cíle. Převaděč SUB/IDX na SRT, dostupný na SubtitleTools.com, je jedním z takových nástrojů, který přijímá soubory SUB a IDX jako vstup a převádí tyto titulky VobSub na soubory SRT.

## Reference

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub – Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

