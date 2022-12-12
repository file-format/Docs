{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - High Efficiency Video Codec",
  "description":"További információ az IDX fájlformátumról és az IDX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Mi az IDX fájl?

Az IDX-fájl egy feliratindexfájl, amely a .sub (VobSub Subtitles) fájlban található feliratok metaadat-információira mutat. A VobSub szoftveralkalmazás hozza létre és használja, amely lehetővé teszi a felhasználók számára, hogy feliratokat bontsanak ki a DVD-kről, és egy SUB fájlba írják be. Az IDX fájlok időbélyegeket és bájteltolásokat tartalmaznak, amelyek minden egyes feliratra mutatnak. A VobSub mindig létrehoz egy IDX-fájlt a megfelelő SUB-fájllal együtt.

## IDX fájlformátum - További információ

Az IDX fájlok egyszerű szöveges fájlokként jönnek létre és menthetők, amelyek bármely szövegszerkesztőben megnyithatók. Az IDX fájl olyan információkat tartalmaz, amelyeket a médialejátszók olvasnak be olyan paraméterek olvasásához, mint a képernyőn megjelenítendő feliratszöveg színe, a felirat szövegének helyzete a képernyőn.

### IDX feliratbeállítások

Egy tipikus IDX-fájl ezeket a metaadat-információkat a fájl elején tárolja. A feliratbeállítások **#**-al kezdődnek. Az időbélyegek és a képhivatkozások az összes feliratbeállítás után hozzáadódnak, és az **időbélyeg:** karakterlánccal kezdődnek.

## IDX fájlformátum példa

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

## Hogyan kell használni az IDX fájlt?

Ha egy filmhez rendelkezik Sub- és IDX fájlokkal, akkor lejátszhatja ezeket a feliratokat azzal a filmmel együtt, amelyhez azokat létrehozta. Számos alkalmazás, például a VLC, a GOM Player, a PotPlayer vagy a PowerDVD képes betölteni ezeket a SUB és IDX fájlokat, és lejátszani a filmmel együtt. A szoftveralkalmazások SUB és IDX feliratfájlokat is beágyazhatnak [.mkv](/hu/video/mkv/) fájlokba.

## Az IDX konvertálása SRT-vé

Az [SRT](/hu/video/srt/) (SubRip fájlformátum) egy egyszerű, SubRip fájlformátumban mentett feliratfájl. A VobSub fájlformátumhoz képest gyakrabban használják. Így ha a SUB/IDX fájlokat SRT fájlformátumba szeretné konvertálni, rendelkezésre állnak harmadik féltől származó eszközök, amelyek ezt elérhetik. A SubtitleTools.com webhelyen elérhető SUB/IDX-SRT konverter az egyik ilyen eszköz, amely SUB- és IDX-fájlokat vesz be bemenetként, és ezeket a VobSub-feliratokat SRT-fájlokká alakítja.

## Hivatkozások

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

