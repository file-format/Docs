{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Hocheffizienter Videocodec",
  "description":"Erfahren Sie mehr über das IDX-Dateiformat und APIs, die IDX-Dateien erstellen und öffnen können.",
  "linktitle" :"IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Was ist eine IDX-Datei?

Eine IDX-Datei ist eine Untertitel-Indexdatei, die auf die Liste der Metadateninformationen für Untertitel in einer .sub-Datei (VobSub Subtitles) verweist. Es wird von der VobSub-Softwareanwendung erstellt und verwendet, mit der Benutzer Untertitel von DVDs extrahieren und in einer SUB-Datei ablegen können. IDX-Dateien enthalten Zeitstempel und Byte-Offsets, die verwendet werden, um auf jeden einzelnen Untertitel zu verweisen. VobSub erstellt immer eine IDX-Datei zusammen mit der entsprechenden SUB-Datei.

## IDX-Dateiformat – Weitere Informationen

IDX-Dateien werden als reine Textdateien generiert und gespeichert, die in jedem Texteditor geöffnet werden können. Eine IDX-Datei enthält Informationen, die von den Mediaplayern gelesen werden, um Parameter wie die Farbe des auf dem Bildschirm anzuzeigenden Untertiteltexts und die Position des Untertiteltexts auf dem Bildschirm zu lesen.

### IDX-Untertiteleinstellungen

Eine typische IDX-Datei speichert diese Metadateninformationen am Anfang der Datei. Untertiteleinstellungen beginnen mit einem **#**. Zeitstempel und Bildreferenzen werden nach all diesen Untertiteleinstellungen hinzugefügt und beginnen mit **timestamp:**.

## Beispiel für das IDX-Dateiformat

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

## Wie verwende ich die IDX-Datei?

Wenn Sie die Sub- und IDX-Dateien für einen Film haben, können Sie diese Untertitel zusammen mit dem Film wiedergeben, für den sie erstellt wurden. Viele Anwendungen wie VLC, GOM Player, PotPlayer oder PowerDVD können diese SUB- und IDX-Dateien laden und neben dem Film abspielen. Softwareanwendungen können auch SUB- und IDX-Untertiteldateien in [.mkv](/de/video/mkv/)-Dateien einbetten.

## Konvertieren Sie IDX in SRT

[SRT](/de/video/srt/) (SubRip-Dateiformat) ist eine einfache Untertiteldatei, die im SubRip-Dateiformat gespeichert wird. Es wird im Vergleich zum VobSub-Dateiformat häufiger verwendet. Wenn Sie also SUB/IDX-Dateien in das SRT-Dateiformat konvertieren möchten, stehen Tools von Drittanbietern zur Verfügung, mit denen Sie dies erreichen können. Der SUB/IDX-zu-SRT-Konverter, der auf SubtitleTools.com verfügbar ist, ist ein solches Tool, das SUB- und IDX-Dateien als Eingabe verwendet und diese VobSub-Untertitel in SRT-Dateien konvertiert.

## Verweise

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

