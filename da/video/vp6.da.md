{
  "date": "2021-02-15",
  "keywords": [
"vp6 fil",
"vp6 filformat",
"hvad er en vp6 fil",
"fil",
"vp6 eksempel",
"vp6 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 - TrueMotion videofil",
  "description": "Lær om VP6-filformat og API'er, der kan oprette og åbne VP6-filer.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-da6"
}
},
  "lastmod": "2021-02-16"
}

## Hvad er en VP6 fil?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. Det er en del af en serie af video-codecs udviklet af TrueMotion, herunder V3, V4 og V5. Formatet blev brugt kort tid inden for udsendelsesområdet, såsom med BBC-rapporter og QuickLink-software. VP6 blev efterfulgt af VP7 Codec i januar 2005 med bedre kompressionskompatibilitet.

## VP6 filformat

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Makroblokke (MB)

I lighed med MPEG-2, MPEG-4 del 2 og 10 er hver videoramme i en VP6-fil sammensat af et array af 16x16 makroblokke (MB). Hver MB kan være i en af følgende tilstande:

 * Intra MB
 * Inter MB, null MV, tidligere rammereference
 * Inter MB, differential MV, tidligere rammereference
 * Inter MB, fire MV'er, tidligere rammereference
 * Inter MB, MV 1, tidligere rammereference
 * Inter MB, MV 2, tidligere rammereference
 * Inter MB, null MV, bogmærket rammereference
 * Inter MB, differential MV, bogmærket rammereference
 * Inter MB, MV 1, bogmærket rammereference
 * Inter MB, MV 2, bogmærket rammereference

### Rammehoved

Rammehovedet på en VP6 er som vist nedenfor, der følger big-endian bitpakningen.

|Syntaks|Antal bits|Type|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 betyder en intraramme|
|qp |6 |Usigned |Gyldigt område for kvantiseringsparameter 0..63|
|markør| 1| Konstant| 0=VP61/62, 1=VP60|
|hvis (ramme_tilstand == 0) { | 0 | |lig med INTRA_FRAME|
|version |5| Konstant| 6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|version2 |2| Konstant |0=VP60, 3=VP61/62|
|interlace |1| Boolean |true (1) betyder interlace vil blive brugt|
|if (markør==1 eller version2==0) {||||
|offset |16 |Usigned| sekundær buffer offset (bytes relateret til starten af buffer)|
|}||||
|dim_y |8| Usigneret| Makroblokhøjde af video|
|dim_x |8| Usigneret| Makroblokbredde af video|
|render_y |8 |Usigned |Vis højde på video|
|render_x |8 |Usigned |Visningsbredde på video|
|}else{||||
|if (markør==1 eller version2==0) {||||
|offset |16 |Usigned |Sekundær bufferoffset (bytes relateret til starten af buffer)|
|}||||
|}||||

## Referencer

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


