{
  "date": "2021-02-15",
  "keywords": [
"vp6 fails",
"vp6 faila formāts",
"kas ir vp6 fails",
"failu",
"vp6 piemērs",
"vp6 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 — TrueMotion video fails",
  "description": "Uzziniet par VP6 faila formātu un API, kas var izveidot un atvērt VP6 failus.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-lv6"
}
},
  "lastmod": "2021-02-16"
}

## Kas ir VP6 fails?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. Tā ir daļa no TrueMotion izstrādāto video kodeku sērijas, tostarp V3, V4 un V5. Formāts drīz tika izmantots apraides jomā, piemēram, BBC ziņojumos un QuickLink programmatūrā. VP6 nomainīja VP7 Codec 2005. gada janvārī ar labāku saderības saderību.

## VP6 faila formāts

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Makrobloki (MB)

Līdzīgi kā MPEG-2, MPEG-4 2. un 10. daļā, katrs VP6 faila video kadrs sastāv no 16 x 16 makrobloku (MB) masīva. Katrs MB var būt vienā no šiem režīmiem:

 * Intra MB
 * Inter MB, null MV, iepriekšējā kadra atsauce
 * Inter MB, diferenciālis MV, iepriekšējā kadra atsauce
 * Inter MB, četri MV, iepriekšējā kadra atsauce
 * Inter MB, MV 1, iepriekšējā kadra atsauce
 * Inter MB, MV 2, iepriekšējā kadra atsauce
 * Inter MB, null MV, grāmatzīmes kadra atsauce
 * Inter MB, diferenciālis MV, grāmatzīmes kadra atsauce
 * Inter MB, MV 1, grāmatzīmes kadra atsauce
 * Inter MB, MV 2, grāmatzīmes kadra atsauce

### Rāmja galvene

VP6 rāmja galvene ir tāda, kā parādīts tālāk, kas seko lielajam bitu komplektam.

|Sintakse|Bitu skaits|Tips|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 apzīmē iekšējo kadru|
|qp |6 |Neparakstīts |Kvantēšanas parametra derīgais diapazons 0..63|
|marķieris| 1| Pastāvīgs| 0=VP61/62, 1=VP60|
|ja (kadra_režīms == 0) { | 0 | |vienāds ar INTRA_FRAME|
|versija |5| Pastāvīgs| 6=VP60/61, 7=VP60(Elektroniskā māksla), 8=VP62|
|versija2 |2| Konstants |0=VP60, 3=VP61/62|
|interlace |1| Būla vērtība |true (1) nozīmē, ka tiks izmantota pītā|
|ja (marķieris==1 vai versija2==0) {||||
|nobīde |16 |Neparakstīts| sekundārā bufera nobīde (baiti attiecībā pret bufera sākumu)|
|}||||
|dim_y |8| Neparakstīts| Video makrobloka augstums|
|dim_x |8| Neparakstīts| Video makrobloka platums|
|render_y |8 |Neparakstīts |Videoklipa displeja augstums|
|render_x |8 |Neparakstīts |Videoklipa displeja platums|
|}cits{||||
|ja (marķieris==1 vai versija2==0) {||||
|nobīde |16 |Neparakstīts |Sekundārā bufera nobīde (baiti attiecībā pret bufera sākumu)|
|}||||
|}||||

## Atsauces

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


