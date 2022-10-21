{
  "date" : "2019-10-11",
  "keywords" :[ "mng-Datei", "mng-Dateiformat", "was ist eine mng-Datei", "Datei", "mng-Beispiel", "mng-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG-Dateiformat - Dateiformat für Netzwerkgrafiken mit mehreren Bildern",
  "description":"Erfahren Sie mehr über das MNG-Dateiformat und APIs, die MNG-Dateien erstellen und öffnen können.",
  "linktitle" :"MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine MNG-Datei?

Eine Datei mit der Erweiterung .mng ist ein Dateiformat für Netzwerkgrafiken mit mehreren Bildern, das dem Bildformat [PNG](/de/image/png/) ähnelt, aber animierte Bilder unterstützt. Es wurde entwickelt, um das PNG-Format nicht mit zusätzlichen Animationsfunktionen zu überladen. MNG ähnelt auch [GIF](/de/image/gif/)-Dateien, verwendet jedoch mehr Komprimierung und unterstützt die vollständige Alpha-Funktion. Der inoffizielle MIME-Medientyp für MNG-Dateien ist video/x-mng. MNG-Dateien können in Anwendungen wie ImageMagik und IrfanView geöffnet werden.

## MNG-Dateiformat

Das MNG-Dateiformat ähnelt dem von PNG und verwendet dieselbe Chunk-Struktur wie in den PNG-Spezifikationen definiert. Ein MNG-Decoder muss in der Lage sein, die PNG-Datenströme zu decodieren, ohne irgendwelche speziellen Flags für Decodierungsbefehle zu spezifizieren. MNG gruppiert mehrere Bilder zu einem "Rahmen", wobei einige Bilder als Sprites verwendet werden, um sich von einem Ort zum anderen zu bewegen. Der Mechanismus ermöglicht die Wiederverwendung von Bilddaten, ohne sie erneut zu übertragen. Die [MNG-Spezifikationen](http://www.libpng.org/pub/mng/spec/) können als Referenz für Entwickler herangezogen werden.

### MNG-Signatur

Der MNG-Datenstrom beginnt mit einer 8-Byte-Signatur, die Folgendes enthält:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Dies ähnelt der PNG-Signatur, enthält jedoch MNG anstelle von PNG.

### MNG-Rahmen

Ein MNG-Rahmen besteht aus einem zweidimensionalen Bild kleinerer Bilder. Auf jedes kleine Bild kann unter Verwendung der Zeilen- und Spaltenindexkombination zugegriffen werden. Das Format ist in der Lage, dreidimensionale "Voxel"-Daten zu speichern, die in einer Reihe von zweidimensionalen Ebenen angeordnet sind. Jede Ebene wird durch einen PNG- oder Delta-PNG-Datenstrom dargestellt. Jeder Delta-PNG-Datenstrom definiert ein Bild als die Unterschiede zum Eltern-PNG-Bild. Dies bietet eine viel kompaktere Möglichkeit zur Darstellung nachfolgender Bilder als die Verwendung eines vollständigen PNG-Datenstroms für jedes Bild.

## Verweise ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG-Format v 1.0](http://www.libpng.org/pub/mng/spec/)

