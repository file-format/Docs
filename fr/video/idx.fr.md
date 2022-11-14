{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec vidéo haute efficacité",
  "description":"En savoir plus sur le format de fichier IDX et les API qui peuvent créer et ouvrir des fichiers IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Qu'est-ce qu'un fichier IDX ?

Un fichier IDX est un fichier d'index de sous-titres qui pointe vers la liste des informations de métadonnées pour les sous-titres dans un fichier .sub (VobSub Subtitles). Il est créé et utilisé par l'application logicielle VobSub qui permet aux utilisateurs d'extraire des sous-titres de DVD et de les vider dans un fichier SUB. Les fichiers IDX contiennent des horodatages et des décalages d'octets utilisés pour pointer vers chaque sous-titre. VobSub crée toujours un fichier IDX avec le fichier SUB correspondant.

## Format de fichier IDX - Plus d'informations

Les fichiers IDX sont générés et enregistrés sous forme de fichiers texte brut pouvant être ouverts dans n'importe quel éditeur de texte. Un fichier IDX contient des informations qui sont lues par les lecteurs multimédias pour lire des paramètres tels que la couleur du texte des sous-titres à afficher à l'écran, la position du texte des sous-titres à l'écran.

### Paramètres de sous-titres IDX

Un fichier IDX typique stocke ces informations de métadonnées au début du fichier. Les paramètres de sous-titres commencent par un **#**. Les horodatages et les références d'image sont ajoutés après tous ces paramètres de sous-titres et commencent par **horodatage :**.

## Exemple de format de fichier IDX

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

## Comment utiliser le fichier IDX ?

Si vous avez les fichiers Sub et IDX pour un film, vous pouvez lire ces sous-titres avec le film pour lequel ils ont été créés. De nombreuses applications telles que VLC, GOM Player, PotPlayer ou PowerDVD ont la capacité de charger ces fichiers SUB et IDX et de les lire parallèlement au film. Les applications logicielles peuvent également intégrer des fichiers de sous-titres SUB et IDX dans des fichiers [.mkv](/fr/video/mkv/).

## Convertir IDX en SRT

Le [SRT](/fr/video/srt/) (format de fichier SubRip) est un simple fichier de sous-titre enregistré au format de fichier SubRip. Il est plus couramment utilisé par rapport au format de fichier VobSub. Ainsi, si vous souhaitez convertir des fichiers SUB/IDX au format de fichier SRT, il existe des outils tiers disponibles qui peuvent être utilisés pour y parvenir. Le convertisseur SUB/IDX vers SRT, disponible sur SubtitleTools.com, est l'un de ces outils qui prend les fichiers SUB et IDX en entrée et convertit ces sous-titres VobSub en fichiers SRT.

## Références

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimédia](https://wiki.multimedia.cx/index.php?title=VOBsub)

