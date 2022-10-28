{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Datei", "Format", "Öffnen", "Lesen", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD-Konstruktionsdateiformat",
  "description" :"Erfahren Sie mehr über das DGN-Dateiformat und APIs, die DGN-Dateien erstellen und öffnen können.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Was ist eine DGN-Datei?

Eine Datei mit der Erweiterung .dgn (Design) ist eine Zeichnungsdatei, die von CAD-Anwendungen wie MicroStation und Intergraph Interactive Graphics Design System erstellt und unterstützt wird. Es wird zum Erstellen und Speichern von Entwürfen für Bauprojekte wie Autobahnen, Brücken und Gebäude verwendet. Das Format ähnelt dem Dateiformat [DWG](/de/cad/dwg/) von Autodesk und gilt als dessen Konkurrent. DNG-Dateien können entweder im Intergraph Standard File Format oder im V8 DGN gespeichert werden. DGN kann in mehrere andere Formate wie DWG, [BMP](/de/image/bmp/), [JPEG](/de/image/jpeg/), [PDF](/de/pdf/), [GIF](/de/image/ gif/) und andere. Es kann mit Autodesk AutoCAD, Bentley View und Bentley Systems MicroStation sowie anderen Softwareanwendungen wie Corel PaintShop Photo Pro und IMSI TurboCAD Deluxe-Versionen geöffnet werden.

## V8 DGN-Dateiformat

Eine MicroStation V8 DGN-Datei besteht aus einem oder mehreren Modellen. Ein Modell ist ein Behälter für Elemente. Das V8-DGN entfernt alle dateiformatbasierten Beschränkungen, die in früheren Versionen von MicroStation vorhanden waren. Nachfolgend finden Sie eine Liste der Verbesserungen im DGN-Dateiformat.

* Die Begrenzung der Anzahl von Ebenen in einer DGN-Datei wurde entfernt, und jede Ebene wird als Element benannt und gespeichert.
* Die maximale physische Größe der DGN-Datei unterliegt keiner Beschränkung und wird nur durch das Betriebssystem begrenzt (z. B. beträgt die NT-Grenze 4 GB).
* Die maximale Größe eines einzelnen Elements beträgt 128 KB.
* Die maximale Größe einer Zelle ist nicht begrenzt.
* Zellnamen sind auf ca. 500 Zeichen begrenzt.
* Die Anzahl der Referenzen, die an eine DGN-Datei angehängt werden können, ist unbegrenzt.
* Ein Linienzug, eine Form oder eine Punktkurve kann bis zu 5000 Scheitelpunkte haben.
* Die Anzahl der Komponenten in einer komplexen Kette oder komplexen Form ist unbegrenzt.
* Die Anzahl der Grafikgruppen in einer DGN-Datei ist unbegrenzt.
* Der Zaun ist parallel zu der Ansicht, in der er platziert ist.
* Eine einzelne Textzeile kann 65.535 Zeichen enthalten.
* Die maximale Größe eines Textknotens ist unbegrenzt.
* Die Anzahl der Textknoten in einer DGN-Datei ist unbegrenzt.
* Jedes Element hat eine eindeutige 64-Bit-Kennung, die sich während des Lebenszyklus des Elements nicht ändert.
* Jedes Element hat einen Zeitstempel, der den Zeitpunkt der letzten Änderung angibt.

## Verweise

* [DNG – Von Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [MicroStation V8 DGN-Dateiformat] (https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

