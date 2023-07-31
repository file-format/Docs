{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extension", "file", "format", "image", "Apple Icon Image", "macOS", "Apple", "Icon" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Apple-Symbolbild",
  "description":"Erfahren Sie mehr über das ICNS-Dateiformat und APIs, die ICNS-Dateien erstellen und öffnen können.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine ICNS-Datei? ##

Ein von macOS-Programmen verwendetes Symbolformat wird als ICNS-Datei bezeichnet. Es erlaubt 1-Bit- und 8-Bit-Alphabänder und speichert ein oder mehrere Bilder, normalerweise aus [PNG](/de/image/png/)-Dokumenten. Das Programmsymbol im macOS-Browser und der Benutzeroberfläche wird mithilfe von ICNS-Dateien angezeigt.

Je nach Standort kann dasselbe Stilsymbol mehrere Einstellungen haben. Das ICNS-Format wurde zahlreichen Änderungen unterzogen und hat sich bis zu dem Punkt entwickelt, an dem es nun als Grundlage für verschiedene kompatible Formate verwendet werden kann. Hier sind einige andere wichtige Punkte, die Sie wissen müssen:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource und Mac OS Icons Resource sind einige der anderen Namen.
* Für Symbolinformationen wird eine Quelle im Ressourcenzweig verwendet.
* In den meisten Fällen enthält eine Datei zahlreiche Bilder. 1612 Pixel im Quadrat und 1024, 512, 256, 128, 48, 32 und 16 Pixel im Quadrat sind unterstützte Bildgrößen.


## ICNS-Dateiformat ##

Das ICNS-Datenformat ist eine Kapsel für ein oder mehrere Bilder, die 1-Bit-Bänder und zahlreiche Bildzustände unterstützt.
Das Betriebssystem kann Symbolbilder an die erforderliche Anzeigegröße anpassen. Die größeren Symbolbilder werden normalerweise als [JPEG](/de/image/jpeg/) 2000- oder [PNG](/de/image/png/)-Dateien gespeichert. Eine Art sowohl komprimierter als auch unkomprimierter ICNS-Dateien ist möglich.

Ein Header und binäre Symboldaten bilden die Struktur einer ICNS-Datei. Der Header enthält 8 Datenbytes, von denen vier das magische Literal und vier die Länge der Datei sind. Typ und Größe jedes Symbolbildes werden im Symboldatenabschnitt gespeichert, dem die binären Bilddaten folgen. Die Bildgröße bestimmt die Größe des Binärabschnitts.

## Technische Spezifikation ##

### Header ###

|Offset|Größe|Objektiv
---|---|---|
|0|4|Magisches Literal, muss "icns" sein (0x69, 0x63, 0x6e, 0x73)
|4|4|Länge der Datei, in Byte, msb zuerst


### Symboldaten ###

|Offset|Größe|Objektiv
---|---|---|
|0|4|Symboltyp
|4|4|Länge der Daten in Bytes (einschließlich Typ und Länge), msb zuerst
|8|Variable|Symboldaten

### Kompression ###

Die Pixeldaten werden zu einem gewissen Grad komprimiert. Die 32-Bit- ("is32", "il32", "ih32", "it32") und ARGB- ("ic04", "ic05") Pixel werden häufig (pro Kanal) ähnlich wie bei PackBits komprimiert.

|Lead Value|Tail Bytes|Ergebnis (unkomprimiert)
---|---|---|
|0 - 127|1 - 128|1 - 128 Bytes
|128 - 255|1 Byte|3 - 130 Kopien

## Bezug ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

