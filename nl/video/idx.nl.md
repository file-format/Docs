{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - High Efficiency Video Codec",
  "description":"Meer informatie over IDX-bestandsindelingen en API's die IDX-bestanden kunnen maken en openen.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Wat is een IDX-bestand?

Een IDX-bestand is een ondertitelingsindexbestand dat verwijst naar de lijst met metadata-informatie voor ondertitels in een .sub-bestand (VobSub Subtitles). Het is gemaakt en gebruikt door de VobSub-softwaretoepassing waarmee gebruikers ondertitels van dvd's kunnen extraheren en in een SUB-bestand kunnen dumpen. IDX-bestanden bevatten tijdstempels en byte-offsets die worden gebruikt om naar elke afzonderlijke ondertitel te verwijzen. VobSub maakt altijd een IDX-bestand samen met het bijbehorende SUB-bestand.

## IDX-bestandsindeling - Meer informatie

IDX-bestanden worden gegenereerd en opgeslagen als platte tekstbestanden die in elke teksteditor kunnen worden geopend. Een IDX-bestand bevat informatie die door de mediaspelers wordt gelezen om parameters te lezen, zoals de kleur van de ondertiteltekst die op het scherm moet worden weergegeven, de positie van de ondertiteltekst op het scherm.

### IDX-ondertitelingsinstellingen

Een typisch IDX-bestand slaat deze metadata-informatie op aan het begin van het bestand. Ondertitelinstellingen beginnen met een **#**. Tijdstempels en afbeeldingsreferenties worden toegevoegd na al deze ondertitelinstellingen en beginnen met **timestamp:**.

## Voorbeeld van IDX-bestandsindeling

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

## Hoe IDX-bestand te gebruiken?

Als u de Sub- en IDX-bestanden voor een film hebt, kunt u deze ondertitels afspelen samen met de film waarvoor deze zijn gemaakt. Veel applicaties zoals VLC, GOM Player, PotPlayer of PowerDVD hebben de mogelijkheid om deze SUB- en IDX-bestanden te laden en deze naast de film af te spelen. Softwaretoepassingen kunnen ook SUB- en IDX-ondertitelingsbestanden insluiten in [.mkv](/nl/video/mkv/)-bestanden.

## Converteer IDX naar SRT

De [SRT](/nl/video/srt/) (SubRip-bestandsindeling) is een eenvoudig ondertitelingsbestand dat is opgeslagen in de SubRip-bestandsindeling. Het wordt vaker gebruikt in vergelijking met het VobSub-bestandsformaat. Dus als u SUB/IDX-bestanden naar SRT-bestandsindeling wilt converteren, zijn er tools van derden beschikbaar die kunnen worden gebruikt om dit te bereiken. SUB/IDX naar SRT-converter, beschikbaar op SubtitleTools.com, is zo'n tool die SUB- en IDX-bestanden als invoer gebruikt en deze VobSub-ondertitels naar SRT-bestanden converteert.

## Referenties

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

