{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX - Codec Físeáin Ard-Éifeachtúlachta",
  "description": "Foghlaim faoi fhormáid comhaid IDX agus APIanna ar féidir leo comhaid IDX a chruthú agus a oscailt.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-gax"
}
},
  "lastmod": "2022-07-12"
}

## Cad is comhad IDX ann?

Comhad innéacs na bhfotheideal is ea comhad IDX a dhíríonn ar an liosta faisnéise meiteashonraí d’fhotheidil taobh istigh de chomhad .sub (VobSub Subtitles). Cruthaíonn agus úsáideann feidhmchlár bogearraí VobSub é a ligeann d’úsáideoirí fotheidil a bhaint as DVDanna agus iad a dhumpáil i bhfo-chomhad. Bíonn stampaí ama agus fritháirimh beart a úsáidtear chun gach fotheideal a chur in iúl i gcomhaid IDX. Cruthaíonn VobSub comhad IDX i gcónaí in éineacht leis an bhfochomhad comhfhreagrach.

## Formáid Chomhaid IDX - Tuilleadh Eolais

Déantar comhaid IDX a ghiniúint agus a shábháil mar chomhaid gnáth-théacs is féidir a oscailt in aon eagarthóir téacs. Tá faisnéis i gcomhad IDX a léann na seinnteoirí meán chun paraiméadair a léamh, mar shampla dath an téacs fotheideal atá le taispeáint ar an scáileán, suíomh an téacs fotheideal ar an scáileán.

### Socruithe Fotheideal IDX

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## Sampla Formáid Comhaid IDX

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

## Conas comhad IDX a úsáid?

Má tá na comhaid Fo agus IDX le haghaidh scannáin agat, is féidir leat na fotheidil seo a sheinm siar chomh maith leis an scannán ar cruthaíodh iad. Tá an cumas ag go leor feidhmchlár ar nós VLC, GOM Player, PotPlayer, nó PowerDVD na comhaid SUB agus IDX seo a luchtú, agus iad seo a sheinm taobh leis an scannán. Is féidir le feidhmchláir bogearraí comhaid fotheideal SUB agus IDX a neadú i gcomhaid [.mkv](/video/mkv/) freisin.

## Tiontaigh IDX go SRT

Is comhad fotheideal simplí é an [SRT](/video/srt/) (formáid comhaid SubRip) a shábháiltear i bhformáid comhaid SubRip. Úsáidtear é níos coitianta i gcomparáid le formáid comhaid VobSub. Mar sin, más mian leat comhaid SUB/IDX a thiontú go formáid comhaid SRT, tá uirlisí 3ú páirtí ar fáil ar féidir iad a úsáid chun é seo a bhaint amach. Is uirlis amháin den sórt sin é tiontaire SUB/IDX go SRT, atá ar fáil ar SubtitleTools.com a thógann comhaid SUB agus IDX mar ionchur agus a athraíonn na fotheidil VobSub seo go comhaid SRT.

## Tagairtí

 * [VobSub]( https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

