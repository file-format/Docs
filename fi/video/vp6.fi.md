{
  "date": "2021-02-15",
  "keywords": [
"vp6 tiedosto",
"vp6 tiedostomuoto",
"mikä on vp6-tiedosto",
"tiedosto",
"vp6 esimerkki",
"vp6 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 - TrueMotion-videotiedosto",
  "description": "Opi VP6-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VP6-tiedostoja.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-fi6"
}
},
  "lastmod": "2021-02-16"
}

## Mikä on VP6-tiedosto?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. Se on osa TrueMotionin kehittämää videokoodekkien sarjaa, mukaan lukien V3, V4 ja V5. Formaattia käytettiin pian lähetyskentillä, kuten BBC:n raporteissa ja QuickLink-ohjelmistossa. VP6:ta seurasi VP7 Codec tammikuussa 2005 paremmalla pakkausyhteensopivuudella.

## VP6 tiedostomuoto

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Makrolohkot (MB)

Samoin kuin MPEG-2, MPEG-4 osat 2 ja 10, jokainen VP6-tiedoston videokehys koostuu 16x16 makrolohkon (MB) joukosta. Jokainen MB voi olla jossakin seuraavista tiloista:

 * Sisäinen MB
 * Inter MB, tyhjä MV, edellinen kehysviite
 * Inter MB, differentiaali MV, edellinen kehysviite
 * Inter MB, neljä MV:tä, edellinen kehysviite
 * Inter MB, MV 1, edellinen kehysviite
 * Inter MB, MV 2, edellinen kehysviite
 * Inter MB, null MV, kirjanmerkillä merkitty kehysviite
 * Inter MB, differentiaali MV, kirjanmerkillä merkitty kehysviite
 * Inter MB, MV 1, kirjanmerkillä merkitty kehysviite
 * Inter MB, MV 2, kirjanmerkillä merkitty kehysviite

### Kehyksen otsikko

VP6:n kehysotsikko on alla olevan kuvan mukainen, mikä seuraa big endian bittipakkausta.

|Syntaksi|Bittien määrä|Tyyppi|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 tarkoittaa sisäistä kehystä|
|qp |6 |Ei-merkitty |Kvantisointiparametrin kelvollinen alue 0..63|
|merkki| 1| Vakio| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |on sama kuin INTRA_FRAME|
|versio |5| Vakio| 6=VP60/61, 7=VP60(Elektroniset taiteet), 8=VP62|
|versio2 |2| Vakio |0=VP60, 3=VP61/62|
|lomitus |1| Boolen |true (1) tarkoittaa, että lomitusta käytetään|
|if (merkki==1 tai versio2==0) {||||
|offset |16 |Allekirjoittamaton| toissijaisen puskurin offset (tavuja suhteessa puskurin alkuun)|
|}||||
|dim_y |8| Allekirjoittamaton| Videon makrolohkon korkeus|
|dim_x |8| Allekirjoittamaton| Videon makrolohkon leveys|
|render_y |8 |Allekirjoittamaton |Videon näyttökorkeus|
|render_x |8 |Allekirjoittamaton |Videon näytön leveys|
|}muu{||||
|if (merkki==1 tai versio2==0) {||||
|offset |16 |Ei allekirjoitettu |Toissijaisen puskurin offset (tavuja suhteessa puskurin alkuun)|
|}||||
|}||||

## Viitteet

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


