{
  "date": "2021-02-15",
  "keywords": [
"vp6 failas",
"vp6 failo formatas",
"kas yra vp6 failas",
"failą",
"vp6 pavyzdys",
"vp6 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 – „TrueMotion“ vaizdo failas",
  "description": "Sužinokite apie VP6 failo formatą ir API, kurios gali kurti ir atidaryti VP6 failus.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-lt6"
}
},
  "lastmod": "2021-02-16"
}

## Kas yra VP6 failas?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. Tai yra TrueMotion sukurtų vaizdo kodekų serijos dalis, įskaitant V3, V4 ir V5. Šis formatas netrukus buvo naudojamas transliavimo srityje, pavyzdžiui, su BBC pranešimais ir QuickLink programine įranga. 2005 m. sausio mėn. VP6 pakeitė VP7 kodekas su geresniu glaudinimo suderinamumu.

## VP6 failo formatas

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Makroblokai (MB)

Panašiai kaip MPEG-2, MPEG-4 2 ir 10 dalyse, kiekvienas VP6 failo vaizdo kadras yra sudarytas iš 16 x 16 makroblokų (MB) masyvo. Kiekvienas MB gali būti vienu iš šių režimų:

 * Vidinis MB
 * Inter MB, null MV, ankstesnė kadro nuoroda
 * Inter MB, diferencialas MV, ankstesnė kadro nuoroda
 * Inter MB, keturi MV, ankstesnė kadro nuoroda
 * Inter MB, MV 1, ankstesnė kadro nuoroda
 * Inter MB, MV 2, ankstesnė kadro nuoroda
 * Inter MB, null MV, pažymėta kadro nuoroda
 * Inter MB, diferencialas MV, pažymėta rėmelio nuoroda
 * Inter MB, MV 1, pažymėta kadro nuoroda
 * Inter MB, MV 2, pažymėta kadro nuoroda

### Rėmelio antraštė

VP6 rėmelio antraštė yra tokia, kaip parodyta toliau, o tai atitinka didžiųjų bitų paketą.

|Sintaksė|Bitų skaičius|Tipas|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 reiškia vidinį kadrą|
|qp |6 |Nepasirašytas |Kvantifikavimo parametro galiojantis diapazonas 0..63|
|žymeklis| 1| Pastovus| 0=VP61/62, 1=VP60|
|jei (kadro_režimas == 0) { | 0 | |lygu INTRA_FRAME|
|versija |5| Pastovus| 6=VP60/61, 7=VP60(elektroniniai menai), 8=VP62|
|2 versija |2| Pastovi |0=VP60, 3=VP61/62|
|susipynimas |1| Būlio reikšmė |tiesa (1) reiškia, kad bus naudojamas persipynimas|
|jei (žymeklis==1 arba versija2==0) {||||
|kompensacija |16 |Nepasirašyta| antrinio buferio poslinkis (baitai, palyginti su buferio pradžia)|
|}||||
|dim_y |8| Nepasirašytas| Vaizdo įrašo makrobloko aukštis|
|dim_x |8| Nepasirašytas| Vaizdo įrašo makrobloko plotis|
|render_y |8 |Nepasirašytas |Vaizdo įrašo rodymo aukštis|
|render_x |8 |Nepasirašytas |Vaizdo įrašo rodymo plotis|
|}kita{||||
|jei (žymeklis==1 arba versija2==0) {||||
|Poslinkis |16 |Nepasirašytas |Antrinis buferio poslinkis (baitai buferio pradžios atžvilgiu)|
|}||||
|}||||

## Nuorodos

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


