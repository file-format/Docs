{
  "date" : "2021-08-09",
  "keywords" :[ "cso-Datei", "cso-Dateiformat", "was ist eine cso-Datei", "Datei", "cso-Beispiel", "cso-Dateierweiterung", "Erweiterung", "format", "iso", "DAX-Komprimierung "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das CSO-Dateiformat und APIs, die CSO-Dateien erstellen und öffnen können.",
  "title" :"CSO - Komprimiertes ISO-Festplatten-Image",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Was ist eine CSO-Datei?

Eine Datei mit der Erweiterung .cso ist eine komprimierte ISO-Image-Datei. Das CSO ist eine Alternative zum DAX-Komprimierungsverfahren; auch bekannt als CISO; war die erste Methode zum Komprimieren der [ISO](/de/compression/iso/)-Dateien und ist normalerweise eine bevorzugte Methode zum Archivieren von PlayStation Portable-Material. Dieses Format verwendet die Deflate-Komprimierung, die bis zu neun Komprimierungsebenen umfassen kann. Zur Erstellung der Bilder wird Software wie Prometheus und YACC verwendet.

## CSO-Dateiformat

Das CSO-Dateiformat war die erste Komprimierungsmethode für ISO, um mehr Speicherplatz zu sparen. Die Erweiterungen wurden von Zeit zu Zeit für eine bessere Komprimierung vorgenommen. Das CSO verwendet die Deflate-Komprimierung mit neun Voreinstellungsstufen, normalerweise kann jede Stufe 2 KiB-Blöcke einzeln verarbeiten. Während die höchsten Komprimierungsstufen die Ladezeiten in Software, die stark vom Disc-Streaming abhängt, verlangsamen und verlängern können, können auch die niedrigeren Stufen eine erhebliche Komprimierung durchführen.

### CSO-Dateistruktur

Das CSO-Dateiformat enthält einen 24-Byte-Header, Datenblöcke und eine Indextabelle. Für Felder größer als ein Byte wird Little-Endian angenommen. Die Architektur-Endianness von PlayStation Portable ist unten angegeben.

#### Header

| Offset (Byte) | Name | Größe (Byte) | Zweck |
----------|----------|--------------|---------|
| 0x0 | Magie | 4 | Immer CISO oder 0x4F534943, wenn es als 32-Bit-Integer gelesen wird. Dieses Feld wird verwendet, um eine CSO-Datei zu identifizieren. Beachten Sie, dass dieses Feld für die anderen Ableitungen von CSO unterschiedlich sein kann, z. B. verwendet ZSO den magischen Code ZISO. |
| 0x4 | Kopfzeilengröße | 4 | Für das ursprüngliche CSO-Dateiformat „v1“ wird dieses Feld ignoriert und muss daher nicht korrekt sein. Das „v2“- und das ZSO-Format erfordern jedoch, dass dieses Feld immer 0x18 (24 Bytes) ist. |
| 0x8 | Unkomprimierte Größe | 8 | Die Größe der ursprünglichen unkomprimierten ISO in Bytes. |
| 0x10 | Blockgröße | 4 | Die Größe jedes Datenblocks in Bytes vor der Komprimierung. Üblicherweise 2048 Bytes, genau wie die Größe jedes ISO 9660-Sektors. |
| 0x14 | Ausführung | 1 | Die Version des verwendeten Dateiformats. Für das „v1“-Format kann der Wert entweder 0 oder 1 sein. Für das „v2“-Format muss dies 2 sein. Außerdem erfordert das ZSO-Format, dass dies 1 ist. |
| 0x15 | Indexausrichtung | 1 | Die Ausrichtung jedes Indexeintrags, angegeben in Bits. |
| 0x16 | Reserviert | 2 | Dieses Feld ist unbenutzt. Im Format "v1" wird dieses Feld ignoriert und kann beliebige Werte enthalten. Im Format "v2" muss dieses Feld null sein. |

#### Indextabelle

Die Indextabelle enthält mehrere 4-Byte-Einträge, die die Position jedes Datenblocks angeben, und einen zusätzlichen, letzten Eintrag, der auf das Ende der Datei zeigt.
Der Inhalt jedes Eintrags ist wie folgt:
| Bit | Länge | Maske | Name | Zweck |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Stelle | Dieses Feld gibt, wenn es um die im Header angegebene Indexausrichtung nach links verschoben wird, die Position an, an der der Datenblock beginnt. |
| 31 | 1 | 0x80000000 | Komprimierungstyp | Das ZSO-Format hat eine ähnliche Semantik, nur dass 0 LZ4 anstelle von Deflate darstellt. Im "v2"-Format. Der Block wird implizit als unkomprimiert betrachtet, wenn die Blockgröße größer oder gleich der im Dateiheader angegebenen Blockgröße ist. |

#### Datenblöcke

Die Datenblöcke umfassen die unkomprimierten oder komprimierten Daten. Die Größe eines Blocks wird berechnet, indem man seine Position erhält und sie dann von der Position des folgenden Blocks subtrahiert. Wenn die Indexausrichtung größer als Null ist, ist es wahrscheinlich, dass die Blockgröße größer ist als die darin enthaltenen Daten.


## Verweise

* N/A

