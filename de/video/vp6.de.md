{
  "date" : "2021-02-15",
  "keywords" :[ "vp6-Datei", "vp6-Dateiformat", "was ist eine vp6-Datei", "Datei", "vp6-Beispiel", "vp6-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion-Videodatei",
  "description":"Erfahren Sie mehr über das VP6-Dateiformat und APIs, die VP6-Dateien erstellen und öffnen können.",
  "linktitle" :"VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Was ist eine VP6-Datei?

VP6 ist ein Videoformat mit verlustbehafteter Komprimierung, das im Mai 2003 von On2 Technologies eingeführt wurde. Es ist Teil einer Reihe von Video-Codecs, die von TrueMotion entwickelt wurden, einschließlich V3, V4 und V5. Das Format wurde in Kürze im Rundfunkbereich verwendet, beispielsweise mit BBC-Berichten und QuickLink-Software. VP6 wurde im Januar 2005 vom VP7-Codec mit besserer Kompatibilität zur Komprimierung abgelöst.

## VP6-Dateiformat

Vollständige Spezifikationen für V6-Dateien sind nicht öffentlich verfügbar. On2 veröffentlichte die Spezifikationen zunächst, aber bald wurden sie für allgemeine Benutzer nicht verfügbar gemacht. Eine inoffizielle Dokumentation des VP6-Dateiformats ist unter [Multimedia-Wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) verfügbar, die als Referenz für Entwickler herangezogen werden kann.

### Makroblöcke (MB)

Ähnlich wie bei MPEG-2, MPEG-4 Teil 2 und 10 besteht jeder Videoframe einer VP6-Datei aus einem Array von 16x16 Makroblöcken (MB). Jeder MB kann sich in einem der folgenden Modi befinden:

* Intra-MB
* Inter MB, null MV, vorherige Frame-Referenz
* Inter-MB, Differential-MV, vorherige Frame-Referenz
* Inter MB, vier MVs, vorherige Frame-Referenz
* Inter MB, MV 1, vorherige Frame-Referenz
* Inter MB, MV 2, vorherige Frame-Referenz
* Inter MB, null MV, mit Lesezeichen versehene Frame-Referenz
* Inter-MB, differenzieller MV, mit Lesezeichen versehene Frame-Referenz
* Inter MB, MV 1, Frame-Referenz mit Lesezeichen
* Inter MB, MV 2, Frame-Referenz mit Lesezeichen

### Frame-Header

Der Frame-Header eines VP6 ist wie unten gezeigt und folgt dem Big-Endian-Bitpacking.

|Syntax|Anzahl Bits|Typ|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 bedeutet ein Intra-Frame|
|qp |6 |Unsigned |Gültiger Bereich Quantisierungsparameter 0..63|
|Markierung| 1| Konstante| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |entspricht INTRA_FRAME|
|Version |5| Konstante| 6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|version2 |2| Konstante |0=VP60, 3=VP61/62|
|Verschachtelung |1| Boolean |true (1) bedeutet, dass Interlace verwendet wird|
|if (marker==1 oder version2==0) {||||
|Offset |16 |Unsigned| Offset des sekundären Puffers (Bytes relativ zum Anfang des Puffers)|
|}||||
|dim_y |8| Unsigniert| Makroblockhöhe des Videos|
|dim_x |8| Unsigniert| Makroblockbreite des Videos|
|render_y |8 |Unsigned |Höhe des Videos anzeigen|
|render_x |8 |Unsigned |Anzeigebreite des Videos|
|}sonst{||||
|if (marker==1 oder version2==0) {||||
|offset |16 |Unsigned |Offset des sekundären Puffers (Bytes relativ zum Anfang des Puffers)|
|}||||
|}||||

## Verweise

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

