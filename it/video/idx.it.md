{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec video ad alta efficienza",
  "description":"Scopri il formato di file IDX e le API che possono creare e aprire file IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Che cos'è un file IDX?

Un file IDX è un file di indice dei sottotitoli che punta all'elenco delle informazioni sui metadati per i sottotitoli all'interno di un file .sub (VobSub Subtitles). Viene creato e utilizzato dall'applicazione software VobSub che consente agli utenti di estrarre i sottotitoli dai DVD e di scaricarli in un file SUB. I file IDX contengono timestamp e offset di byte utilizzati per puntare a ogni singolo sottotitolo. VobSub crea sempre un file IDX insieme al file SUB corrispondente.

## Formato file IDX - Ulteriori informazioni

I file IDX vengono generati e salvati come file di testo semplice che possono essere aperti in qualsiasi editor di testo. Un file IDX contiene informazioni che vengono lette dai lettori multimediali per leggere parametri come il colore del testo dei sottotitoli da visualizzare sullo schermo, la posizione del testo dei sottotitoli sullo schermo.

### Impostazioni dei sottotitoli IDX

Un tipico file IDX memorizza queste informazioni sui metadati all'inizio del file. Le impostazioni dei sottotitoli iniziano con un **#**. I timestamp e i riferimenti alle immagini vengono aggiunti dopo tutte queste impostazioni dei sottotitoli e iniziano con **timestamp:**.

## Esempio di formato file IDX

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

## Come utilizzare il file IDX?

Se hai i file Sub e IDX per un film, puoi riprodurre questi sottotitoli insieme al film per il quale sono stati creati. Molte applicazioni come VLC, GOM Player, PotPlayer o PowerDVD hanno la capacità di caricare questi file SUB e IDX e riprodurli insieme al film. Le applicazioni software possono anche incorporare file di sottotitoli SUB e IDX in file [.mkv](/it/video/mkv/).

## Converti IDX in SRT

[SRT](/it/video/srt/) (formato file SubRip) è un semplice file di sottotitoli salvato nel formato file SubRip. È più comunemente usato rispetto al formato di file VobSub. Pertanto, se desideri convertire file SUB/IDX in formato file SRT, sono disponibili strumenti di terze parti che possono essere utilizzati per ottenere ciò. Il convertitore da SUB/IDX a SRT, disponibile su SubtitleTools.com, è uno di questi strumenti che accetta file SUB e IDX come input e converte questi sottotitoli VobSub in file SRT.

## Riferimenti

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

