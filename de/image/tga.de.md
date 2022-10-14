{
  "date" : "2019-10-11",
  "keywords" :[ "tga-Datei", "tga-Dateiformat", "was ist eine tga-Datei", "Datei", "tga-Beispiel", "tga-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA-Dateiformat - Eine TARGA-Grafikbilddatei",
  "description":"Erfahren Sie mehr über das TGA-Dateiformat und APIs, die TGA-Dateien erstellen und öffnen können.",
  "linktitle" :"TG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine TGA-Datei?

Eine Datei mit der Erweiterung .tga ist ein Rastergrafikformat und wurde von Truevision Inc. erstellt. Sie wurde für die TARGA-Karten (Truevision Advanced Raster Adapter) entwickelt und bot Highcolor/Truecolor-Anzeigeunterstützung für IBM-kompatible PCs. Es unterstützt 8, 16, 24 und 32 Bit pro Pixel und 8-Bit-Alphakanal. Es unterstützt auch die verlustfreie RLE-Komprimierung, die angewendet werden kann, um die Bildgröße zu reduzieren. Digitale Fotos und Texturen verwenden das TGA-Bildformat.

## Kurze Geschichte

Die Bildung des TGA-Dateiformats entstand 1984 durch AT&T EPICenter (später extrahiert und als unabhängige Einheit namens Truevision gegründet), das an der Vermarktung neuer Technologien arbeitete, die von AT&T für Farbbildpuffer entwickelt wurden. EPICenter arbeitete bereits an seinen ersten beiden Karten, dem VDA (Video Display Adapter) und ICB (Image Capture Board), für die die Arbeit an zwei Dateitypen, .vda und .icb, bereits im Gange war. Diese Dateiformate wurden kodifiziert und das weniger breite spezifische Dateiformat TGA wurde eingeführt. TGA war eine Erweiterung dessen, was bereits verwendet wurde, und lieferte Informationen wie Breite, Höhe, Pixeltiefe, zugehörige Farbkarte und Bildursprung.

Die 1989 veröffentlichte Version 2.0 von TGA enthielt mehrere erweiterte Funktionen wie:

* Miniaturansichten
* Alphakanal
* Gammawert
* Textliche Metadaten

Zu den Hauptmitarbeitern der Version 2.0 von TGA gehören Shawn Steiner, Kevin Fiedly und David Spoelstra von Truevision.

## TGA TARGA-Dateiformatspezifikationen

Eine TGA-Datei besteht aus 2 Hauptteilen:

* Header
* Informationen zu Farbpixeln

Alle Werte in einer TGA-Datei sind gemäß den Formatspezifikationen in Littl-Endian.

### TGA-Header

Ein TGA-Dateiheader besteht aus den folgenden 5 Feldern.

|Feld-Nr.|Länge |Feldname |Beschreibung|
---|---|---|---|
|1| 1 Byte |ID-Länge| Länge des Bild-ID-Feldes (0-255)|
|2| 1 Byte |Farbabbildungstyp| Ob eine Farbkarte enthalten ist (0 – zeigt an, dass keine Farbkartendaten in diesem Bild enthalten sind. 1 – zeigt an, dass eine Farbkarte in diesem Bild enthalten ist.)|
|3| 1 Byte |Bildtyp| Komprimierungs- und Farbtypen (0 – Keine Bilddaten enthalten. 1 – Unkomprimiert, Bild mit Farbzuordnung, 2 – Unkomprimiert, Echtfarbenbild, 9 – Lauflängenkodiert, Farbzuordnungsbild, 11 – Lauflängenkodiert, Schwarzweißbild )|
|4| 5 Bytes |Farbabbildungsspezifikation| Beschreibt die Farbkarte|
|5| 10 Byte |Bildspezifikation| Bildabmessungen und -format|

### Bild- und Farbkartendaten

|Feld-Nr. |Länge |Feld |Beschreibung|
---|---|---|---|
|6 |Vom Bild-ID-Längenfeld| Bild-ID| Optionales Feld mit identifizierenden Informationen|
|7 |Vom Farbkarten-Spezifikationsfeld| Farbkartendaten| Nachschlagetabelle mit Farbkartendaten|
|8 |Vom Bildspezifikationsfeld| Bilddaten| Gespeichert gemäß dem Bilddeskriptor|

### Entwicklerbereich (optional)

Die TGA-Version 2.0 bietet Unterstützung für zusätzliche Erweiterungen/Extras, für die viele Entwickler weitere Informationen speichern wollten. Die Information ist optional, sodass sie ignoriert wird, wenn ein TGA-Decoder sie nicht interpretieren kann.

### Erweiterungsbereich (optional)

|Feld-Nr.| Länge| Feld |Beschreibung|
---|---|---|---|
|10| 2 Bytes |Erweiterungsgröße |Größe des Erweiterungsbereichs in Bytes, immer 495|
|11| 41 Byte| Name des Autors |Name des Autors. Wenn nicht verwendet, sollten Bytes auf NULL (\0) oder Leerzeichen| gesetzt werden
|12| 324 Byte| Kommentar des Autors| Ein Kommentar, organisiert in vier Zeilen mit jeweils 80 Zeichen plus NULL|
|13| 12 Bytes| Datums-/Zeitstempel |Datum und Uhrzeit der Erstellung des Bildes|
|14| 41 Byte| Job-ID||
|15| 6 Bytes| Arbeitszeit| Stunden, Minuten und Sekunden, die für die Erstellung der Datei aufgewendet werden (für die Abrechnung usw.)|
|16| 41 Byte| Software-ID |Die Anwendung, die die Datei erstellt hat.|
|17| 3 Bytes| Softwareversion||
|18| 4 Bytes| Schlüsselfarbe||
|19| 4 Bytes| Pixel-Seitenverhältnis||
|20| 4 Bytes| Gammawert||
|21| 4 Bytes| Farbkorrektur-Offset |Anzahl Bytes vom Anfang der Datei bis zur Farbkorrekturtabelle, falls vorhanden|
|22| 4 Bytes| Briefmarke | Anzahl der Bytes vom Anfang der Datei bis zum Briefmarkenbild, falls vorhanden|
|23| 4 Bytes| Abtastzeilenversatz| Anzahl der Bytes vom Anfang der Datei bis zur Abtastzeilentabelle, falls vorhanden|
|24| 1 byte| Attributtyp| Gibt den Alphakanal| an

### Dateifuß (optional)

Die letzten 26 Bytes der Datei stellen die Fußzeile dar, was, falls vorhanden, bedeutet, dass es sich wahrscheinlich um eine TGA-Datei der Version 2 handelt.

|Feld Nr.| Länge| Feld| Beschreibung|
---|---|---|---|
|28| 4 Bytes| Erweiterungsoffset| Offset in Bytes vom Anfang der Datei|
|29| 4 Bytes| Offset des Entwicklerbereichs| Offset in Bytes vom Anfang der Datei|
|30| 16 Bytes| Unterschrift| Enthält „TRUEVISION-XFILE“|
|31| 1 byte| | Enthält "."|
|32| 1 byte| | Enthält NULL|


## Verweise

* [TGA 2.0-Dateiformatspezifikationen](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA von Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

