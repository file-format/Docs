{
  "date" : "2021-07-29",
  "keywords" :[ "shx-Datei", "shx-Dateiformat", "was ist eine shx-Datei", "Datei", "shx-Beispiel", "shx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile-Shape-Index-Format",
  "description":"Erfahren Sie mehr über das SHX-Dateiformat und APIs, die SHX-Dateien erstellen und öffnen können.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Was ist eine SHX-Datei?
Die SHX-Datei gehört zum Shape-Index-Format, das ein Positionsindex der Feature-Geometrie ist, um eine schnelle Vorwärts- und Rückwärtssuche zu ermöglichen. Die SHX ist eine Offset-Datei mit direktem Zugriff. Diese Datei enthält keine Daten, nur eine doppelte Kopie der ersten hundert Bytes, der Datensatznummer und des Offsets zum Startbyte dieses Datensatzes in der shp. Bitte beachten Sie, dass die Datei mit der Erweiterung .shx die [SHP](/de/gis/shp) und [DBF](/de/database/dbf) nicht verknüpft.

## SHX-Dateiformat
Das SHX-Format enthält einen Positionsindex der Feature-Geometrie und einen 100-Byte-Header ähnlich der SHP-Datei, gefolgt von einer beliebigen Anzahl von 8-Byte-Datensätzen mit fester Länge, die die folgenden zwei Felder enthalten:
| Bytes | Geben Sie | ein Endianität | Verwendung |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | groß | Datensatz-Offset (in 16-Bit-Worten) |
| 4–7 | int32 | groß | Datensatzlänge (in 16-Bit-Worten) |

Dieser Index ermöglicht es, im Shapefile rückwärts zu suchen, indem man zuerst rückwärts im Shape-Index sucht und dann den Datensatz-Offset liest. Dieser Offset kann verwendet werden, um nach der richtigen Position in der SHP-Datei zu suchen. Sie können auch vorwärts suchen; eine beliebige Anzahl von Datensätzen mit der gleichen Methode. Es ist zwar möglich, einen vollständigen Index zusammen mit einer SHP-Datei zu generieren, aber es kann die Wahrscheinlichkeit erhöhen, dass die SHP-Datei schnell beschädigt wird.


## Verweise

* [Shapefile - von Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


