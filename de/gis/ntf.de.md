{
  "date" : "2021-07-28",
  "keywords" :[ "ntf-datei", "ntf-dateiformat", "was ist eine ntf-datei", "datei", "ntf-beispiel", "ntf-dateierweiterung", "erweiterung", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Dateien im nationalen Übertragungsformat",
  "description":"Erfahren Sie mehr über das NTF-Dateiformat und APIs, die NTF-Dateien erstellen und öffnen können.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Was ist eine NTF-Datei?
Die Dateien mit der Erweiterung .ntf werden als Dateien im **National Transfer Format (NTF)** bezeichnet; hauptsächlich von der UK Ordnance Survey (OS) verwendet; speziell für die Übertragung von Geodaten. Es wird von der British Standards Institution verwaltet. Es hat sich zum Standardübertragungsformat für digitale Daten des Ordnance Survey entwickelt. Die britische National Grid-Projektion, eine Art Transverse Mercator, enthält alle georeferenzierten Informationen für NTF-Dateien.

## NTF-Dateiformat
Das NTF-Dateiformat ist Eigentum von Ordnance Survey im Vereinigten Königreich; von der GDB-Bibliothek für den Import unterstützt. Die aktuelle Version des NTF-Dateiformats ist 2.0. Dieses Dateiformat wurde eingeführt, um eine Einschränkung des **PCIDSK**-Vektorsegments zu beheben, das nur ein Attributfeld pro Struktur hat, aber es gibt eine Vielzahl von Attributen, die mit Vektordaten extrahiert werden können. Um das NTF-Dateiformat zu umgehen, besteht es aus zwei Segmenten. Jedes Segment besteht aus denselben Vektoren, jedoch mit unterschiedlichen Attributen. Das erste Segment einer NTF-Vektordatei enthält die Vektoren mit der Feature-Code-Nummer als Attribut. Das zweite Segment enthält die Vektoren mit dem Wert als Attribut.

### Koordinatenbezugssystem
Die GDB-Bibliothek stellt Raster- und Vektordaten mit den entsprechenden TM-Projektionseigenschaften dar:

- Referenzlängengrad: 49.0
- Bezugsbreite: 2,0
- Falscher Ostwert: 400000
- Falscher Hochwert: -100000
- Maßstab: 0,9996012717
- Ellipsoid: Airy 1830 (E009)
Das Aktualisieren oder Schreiben von NTF-Dateien wird nicht unterstützt, und die DTM-Dateien können nicht verlinkt werden.

### Ogrininfo-Beispiel
Das folgende Beispiel verwendet **ogrinfo** in einer NTF-Datei, um Schichtnummern abzurufen:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Verweise

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Mapping – Illustriert von Tyler Mitchell] (https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

