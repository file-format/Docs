{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","Datei", "Format", "Dateityp", "Erweiterung","Was ist eine 3DS-Datei?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das 3DS-Dateiformat und APIs, die 3DS-Dateien öffnen und erstellen können.",
  "title" :"3DS-Dateiformat",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine 3DS-Datei?

Eine Datei mit der Erweiterung .3ds stellt das von Autodesk 3D Studio verwendete Mesh-Dateiformat 3D Studio (DOS) dar. Autodesk 3D Studio ist seit den 1990er Jahren auf dem Markt für 3D-Dateiformate und hat sich nun zu 3D Studio MAX für die Arbeit mit 3D-Modellierung, -Animation und -Rendering entwickelt. Eine 3DS-Datei enthält Daten für die 3D-Darstellung von Szenen und Bildern und ist eines der gängigen Dateiformate für den Import und Export von 3D-Daten. Es berücksichtigt Informationen wie Kamerastandorte, Netzdaten, Beleuchtungsinformationen, Ansichtsfensterkonfigurationen, Glättungsgruppendaten, Bitmap-Referenzen und Attribute, um Scheitelpunkte und Polygone zum Rendern einer Szene zu erstellen.

## 3DS-Dateiformat – Weitere Informationen
An seiner Basis ist 3DS ein binäres Dateiformat und folgt einer vordefinierten Struktur zum Speichern und Abrufen von Daten. Das binäre Dateiformat macht das 3DS-Dateiformat schneller kleiner im Vergleich zu textbasierten Dateiformaten. Daten in einer 3DS-Datei werden in Form von Chunks gespeichert.

### Brocken

Jeder Chunk in einer 3DS-Datei ist ein Datenblock, der eine ID, die Länge des Blocks für die Position des nächsten Blocks und die Daten selbst enthält. Die Chunk-ID ermöglicht Lesern von 3DS-Dateiformaten, die Blöcke zu überspringen, die sie nicht erkennen. Es hilft auch bei der Erweiterbarkeit des Formats. Jeder Chunk speichert Informationen zu Formen, Beleuchtung und Betrachtungsinformationen, die zusammen die Szene rendern. Chunks sind in einer hierarchischen Struktur in einer 3DS-Datei angeordnet und ähneln in ihrer Darstellung einem XML-Dokumentobjektbaum.

**Chunk-ID:** Die ersten beiden Bytes eines Chunks stellen eine Chunk-Kennung dar, mit der der Dateileser entscheiden kann, ob er ihn beim Lesen berücksichtigen oder überspringen möchte.

**Länge des Chunks:** Auf die Chunk-ID folgt eine 4-Byte-Ganzzahl (in Little-Endian), die für die Länge des Chunks steht. Diese Länge beinhaltet auch die Länge der Daten, die Länge ihrer Unterblöcke und den 6-Byte-Header.

**Nutzlast:** Auf die Länge des Chunks folgen die eigentlichen Datenbytes für den Chunk, gefolgt von seinen Sub-Chunks in derselben hierarchischen Struktur, die auf mehrere Ebenen erweitert werden kann.

### Struktur ###

Die hierarchische Struktur eines einfachen Chunks sieht wie folgt aus:

**Ein Brocken**

|Start|Ende|Größe|Name
--- | --- | --- | ---
|0|1|2|Chunk-ID
|2|5|4|Nächster Block

Den Chunks wird eine Hierarchie auferlegt, die durch ihre ID identifiziert wird. Eine 3ds-Datei hat die primäre Chunk-ID 4D4Dh. Dies ist immer der erste Chunk der Datei. Mit im primären Chunk sind die Hauptchunks.

**Hauptstücke**

|id|Beschreibung
--- | ---
|3D3D|Beginn der Objektnetzdaten.
|B000|Beginn der Keyframer-Daten.

Der Next-Chunk-Zeiger nach dem ID-Block zeigt auf den nächsten Main-Chunk.
Direkt nach einem Main Chunk ist ein weiterer Chunk. Dies könnte jede andere Art von Chunk sein, die innerhalb seines Hauptchunks-Umfangs zulässig ist.
Für die Mesh-Beschreibung (3D3D) könnten sie beliebige Vielfache von sein.

**Subchunks von 3D3D - Mesh-Block**


|id|Beschreibung
--- | ---
|1100|unbekannt
|1200|Hintergrundfarbe.
|1201|unbekannt
|1300|unbekannt
|1400|unbekannt
|1420|unbekannt
|1450|unbekannt
|1500|unbekannt
|2100|Umgebungsfarbblock
|2200|Nebel?
|2201|Nebel?
|2210|Nebel?
|2300|unbekannt
|3000|unbekannt
|4000|Objektblock
|7001|unbekannt
|AFFF|unbekannt

**Subchunks von 4000 - Objektbeschreibungsblock**
Das erste Element von Subchunk 4000 ist eine ASCIIZ-Zeichenfolge des Objektnamens.
Denken Sie daran, dass ein Objekt ein Mesh, ein Licht oder eine Kamera sein kann.

|id|Beschreibung
--- | ---
|4010|unbekannt
|4012|Schatten?
|4100|Dreieckiges Polygonobjekt
|4600|Licht
|4700|Kamera

## Verweise

* [Geometriedateiformate – Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS – Von Wikipedia](https://en.wikipedia.org/wiki/.3ds)

