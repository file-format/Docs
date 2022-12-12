{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec video de înaltă eficiență",
  "description":"Aflați despre formatul de fișier IDX și despre API-urile care pot crea și deschide fișiere IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Ce este un fișier IDX?

Un fișier IDX este un fișier index de subtitrări care indică lista de informații despre metadate pentru subtitrări din interiorul unui fișier .sub (Subtitrări VobSub). Este creat și utilizat de aplicația software VobSub, care permite utilizatorilor să extragă subtitrări de pe DVD-uri și să le arunce într-un fișier SUB. Fișierele IDX conțin marcaje temporale și decalaje de octeți utilizate pentru a indica fiecare subtitrare. VobSub creează întotdeauna un fișier IDX împreună cu fișierul SUB corespunzător.

## Format de fișier IDX - Mai multe informații

Fișierele IDX sunt generate și salvate ca fișiere text simplu care pot fi deschise în orice editor de text. Un fișier IDX conține informații care sunt citite de playerele media pentru a citi parametri cum ar fi culoarea textului subtitrării de afișat pe ecran, poziția textului subtitrării pe ecran.

### Setări subtitrare IDX

Un fișier IDX tipic stochează aceste informații despre metadate la începutul fișierului. Setările de subtitrare încep cu **#**. Marcajele temporale și referințele la imagini sunt adăugate după toate aceste setări de subtitrare și încep cu **marca temporală:**.

## Exemplu de format de fișier IDX

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

## Cum se utilizează fișierul IDX?

Dacă aveți fișierele Sub și IDX pentru un film, puteți reda aceste subtitrări împreună cu filmul pentru care sunt create. Multe aplicații precum VLC, GOM Player, PotPlayer sau PowerDVD au capacitatea de a încărca aceste fișiere SUB și IDX și de a le reda împreună cu filmul. Aplicațiile software pot încorpora și fișiere de subtitrare SUB și IDX în fișiere [.mkv](/ro/video/mkv/).

## Convertiți IDX în SRT

[SRT](/ro/video/srt/) (format de fișier SubRip) este un fișier simplu de subtitrare salvat în formatul de fișier SubRip. Este mai frecvent utilizat în comparație cu formatul de fișier VobSub. Astfel, dacă doriți să convertiți fișierele SUB/IDX în format de fișier SRT, există instrumente terțe disponibile care pot fi utilizate pentru a realiza acest lucru. Convertorul SUB/IDX în SRT, disponibil pe SubtitleTools.com este un astfel de instrument care preia fișierele SUB și IDX ca intrare și convertește aceste subtitrări VobSub în fișiere SRT.

## Referințe

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

