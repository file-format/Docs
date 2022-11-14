{
  "date" : "2021-02-15",
  "keywords" :[ "vp6-bestand", "vp6-bestandsindeling", "wat is een vp6-bestand", "bestand", "vp6-voorbeeld", "vp6-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion-videobestand",
  "description":"Meer informatie over VP6-bestandsindeling en API's die VP6-bestanden kunnen maken en openen.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Wat is een VP6-bestand?

VP6 is een video-indeling met compressie met verlies die in mei 2003 werd geïntroduceerd door On2-technologieën. Het maakt deel uit van een reeks videocodecs die zijn ontwikkeld door TrueMotion, waaronder V3, V4 en V5. Het formaat werd kort gebruikt in de omroepsector, zoals bij BBC-rapporten en QuickLink-software. VP6 werd in januari 2005 opgevolgd door VP7 Codec met betere compressiecompatibiliteit.

## VP6-bestandsindeling

Volledige specificaties voor V6-bestanden zijn niet openbaar beschikbaar. On2 maakte de specificaties aanvankelijk openbaar, maar al snel werden deze niet beschikbaar gemaakt voor algemene gebruikers. Een niet-officiële documentatie van het VP6-bestandsformaat is beschikbaar op [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) waarnaar kan worden verwezen ter referentie van de ontwikkelaar.

### Macroblokken (MB)

Net als bij MPEG-2, MPEG-4 delen 2 en 10, is elk videoframe van een VP6-bestand samengesteld uit een reeks van 16x16 macroblokken (MB). Elke MB kan zich in een van de volgende modi bevinden:

* Intra MB
* Inter MB, null MV, vorige framereferentie
* Inter MB, differentiële MV, vorige framereferentie
* Inter MB, vier MV's, vorige framereferentie
* Inter MB, MV 1, vorige framereferentie
* Inter MB, MV 2, vorige framereferentie
* Inter MB, null MV, framereferentie met bladwijzer
* Inter MB, differentiële MV, framereferentie met bladwijzer
* Inter MB, MV 1, framereferentie met bladwijzer
* Inter MB, MV 2, framereferentie met bladwijzer

### Framekoptekst

De frameheader van een VP6 is zoals hieronder weergegeven en volgt de big-endian bitverpakking.

|Syntaxis|Aantal bits|Type|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 betekent een intra frame|
|qp |6 |Unsigned |Kwantiseringsparameter geldig bereik 0..63|
|markering| 1| Constante| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |is gelijk aan INTRA_FRAME|
|versie |5| Constante| 6=VP60/61, 7=VP60 (elektronische kunst), 8=VP62|
|versie2 |2| Constante |0=VP60, 3=VP61/62|
|interlace |1| Boolean |true (1) betekent dat interlace wordt gebruikt|
|if (marker==1 of version2==0) {||||
|offset |16 |Niet ondertekend| secundaire bufferoffset (bytes ten opzichte van het begin van de buffer)|
|}||||
|dim_y |8| Niet ondertekend| Macroblokhoogte van video|
|dim_x |8| Niet ondertekend| Macroblokbreedte van video|
|render_y |8 |Niet ondertekend |Toon hoogte van video|
|render_x |8 |Niet ondertekend |Weergavebreedte van video|
|}anders{||||
|if (marker==1 of version2==0) {||||
|offset |16 |Unsigned |Secundaire bufferoffset (bytes ten opzichte van het begin van de buffer)|
|}||||
|}||||

## Referenties

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

