{
  "date" : "2021-07-30",
  "keywords" :[ "dlg-Datei", "dlg-Dateiformat", "was ist eine dlg-Datei", "Datei", "dlg-Beispiel", "dlg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile-Shape-Index-Format",
  "description":"Erfahren Sie mehr über das DLG-Dateiformat und APIs, die DLG-Dateien erstellen und öffnen können.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Was ist eine DLG-Datei?
Eine Datei mit der Erweiterung .dlg enthält das Digital Line Graph, ein kartografisches Kartenelement, das in digitaler Vektorform angezeigt wird und vom US Geological Survey (USGS) verwaltet wird. Die DLG-Dateien sind in zwei verschiedenen Formaten verfügbar:
1. **Optionales Format**: Ein einfach zu verwendendes Format, das eine logische Datensatzlänge von 80 Byte, das UTM-Bodenkoordinatensystem und Topologieverknüpfungen enthält, die in Linien-, Knoten- und Flächenelementen enthalten sind.
2. **Format des Spatial Data Transfer Standard (SDTS)**: ein Format, das die Übertragung von Geodaten zwischen verschiedenen Computersystemen erleichtert.

## DLG-Dateiformat
Das DLG-Dateiformat wurde für USGS-Karten entwickelt und wird in großem, mittlerem und kleinem Maßstab mit bis zu neun verschiedenen Merkmalskategorien übertragen. Die DLG-Dateien sind in optionalen und Spatial Data Transfer Standard (SDTS)-Formaten erhältlich, die für die Verwendung in Kartierungs- und GIS-Anwendungen topologisch strukturiert sind.
### Spezifikationen des DLG-Dateiformats
Die DLG-Dateien werden in drei verschiedenen Maßstäben verteilt:

1. **Großer Maßstab** - entspricht normalerweise:
- Die USGS 7,5 mal 7,5 Minuten
- Topografische Kartenserien im Maßstab 1:24.000 und 1:25.000
- Maßstab 1:63.360 für Alaska
- Maßstab 1:30.000 für Puerto Rico
 

2. **Zwischenskala** - abgeleitet von der USGS:

- 30- mal 60-Minuten

- Kartenserie im Maßstab 1:100.000
3. **Kleiner Maßstab** – abgeleitet von den USGS-Schnittkarten im Maßstab 1:2.000.000 des Nationalatlas der Vereinigten Staaten
### Datenkategorien
In DLG-Dateien sind neun verschiedene Ebenen- oder Feature-Kategorien verfügbar:
1. Öffentliches Landvermessungssystem (PLSS)
2. Grenzen (BD)
3. Transport (TR)
4. Hydrographie (HY)
5. Hypsographie (HP)
6. Nichtvegetative Merkmale (NV)
7. Vermessungskontrolle und Marker (SM)

8. Künstliche Merkmale (MS)

9. Vegetative Oberflächenbedeckung (SC)

Große DLG-Dateien bieten alle neun Schichten, während mittlere Dateien die fünf Schichten PLSS, BD, TR, HY und HP bieten. Kleine DLGs bieten die fünf Schichten PLSS, BD, TR, HY und MS.

## Verweise

* [Digitales Liniendiagramm - von Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


