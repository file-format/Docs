{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","Datei", "Format", "Dateityp", "Erweiterung","Was ist eine GLB-Datei?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Erfahren Sie mehr über das GLB-Dateiformat und APIs, die GLB-Dateien öffnen und erstellen können.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
"identifier": "3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Was ist eine GLB-Datei?

GLB ist die binäre Dateiformatdarstellung von 3D-Modellen, die im GL-Übertragungsformat ([glTF](/de/3d/gltf/)) gespeichert sind. Informationen zu 3D-Modellen wie Knotenhierarchie, Kameras, Materialien, Animationen und Meshes im Binärformat. Dieses Binärformat speichert das glTF-Asset (JSON, .bin und Bilder) in einem binären Blob. Es vermeidet auch das Problem der Erhöhung der Dateigröße, das im Fall von glTF auftritt. Das GLB-Dateiformat führt zu kompakten Dateigrößen, schnellem Laden, vollständiger 3D-Szenendarstellung und Erweiterbarkeit für die weitere Entwicklung. Das Format verwendet model/gltf-binary als MIME-Typ.

## GLB-Dateiformat – Weitere Informationen

Die von glTF verwendeten Inhaltsbereitstellungsmethoden führen zu einer zusätzlichen Verarbeitung zum Decodieren der Base-64-codierten Binärdaten und erhöhen außerdem die Dateigröße um 33 %. Zu diesen Liefermethoden, die zur Bildung des GLB-Dateiformats beigetragen haben, gehören:

* glTF JSON verweist auf externe Binärdaten (Geometrie, Keyframes, Skins) und Bilder.
* glTF JSON bettet Base64-codierte Binärdaten und Bilder inline unter Verwendung von Daten-URIs ein.

GLB als Containerformat wurde als binäres Dateiformat zur Darstellung von glTF-Assets in einem binären Blob eingeführt, um die durch glTF verursachten Probleme zu vermeiden. Das GLB-Dateiformat [Spezifikationen](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) sollte für jede Reader/Writer-Implementierung desselben für die Anwendungsentwicklung herangezogen werden .

## GLB-Dateistruktur

Das GLB-Dateiformat basiert auf Little Endian und seine Struktur zeigt, dass es Folgendes enthält:

* Eine 12-Byte-Präambel mit dem Titel Header.
* Ein oder mehrere Chunks, die JSON-Inhalte und Binärdaten enthalten.

#### Header

Der Header des GLB-Dateiformats besteht aus drei 4-Byte-Einträgen:

* uint32 magic - magic entspricht 0x46546C67. Es ist eine ASCII-Zeichenfolge glTF und kann verwendet werden, um Daten als binäres glTF zu identifizieren
* uint32-Version – gibt die Version des binären glTF-Containerformats an
* uin32-Länge - die Gesamtlänge des binären glTF, einschließlich Header und aller Chunks in Bytes

#### Brocken

Jeder Chunk in einer GLB-Datei hat die folgende Struktur:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - Länge von chunkData in Bytes
* `chunkType` - gibt den Typ des Chunks an
* `chunkData` - binäre Nutzlast von Chunk

wo die Chunk-Typen sind:

|# |Chunk-Typ|ASCII|Beschreibung|Vorkommen
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturierter JSON-Inhalt|1
|2.|0x004E4942|BIN|Binärpuffer|0 oder 1

Anfang und Ende jedes Chunks müssen an der 4-Byte-Grenze ausgerichtet sein, und zu diesem Zweck sollte Padding verwendet werden.

##### Strukturierter JSON-Inhalt

Dies sollte der allererste Block des binären glTF-Assets sein und ermöglicht es der Implementierung, nach und nach Ressourcen aus nachfolgenden Blöcken abzurufen. Dies bietet auch die Möglichkeit, nur eine ausgewählte Teilmenge von Ressourcen aus einem binären glTF-Asset zu lesen, z. B. die gröbste LOD eines Netzes. Um die Ausrichtungsanforderungen zu erfüllen, muss dieser Chunk mit abschließenden Leerzeichen (0x20) aufgefüllt werden.

##### Binärpuffer #####

Dieser Chunk enthält die binäre Nutzlast für Geometrie, Animationsschlüsselbilder, Skins und Bilder. Es sollte der zweite Block des binären glTF-Assets sein und muss mit nachgestellten Nullen (0x00) aufgefüllt werden, um die Ausrichtungsanforderungen zu erfüllen.

## Verweise ##

* [Spezifikationen des GLB-Dateiformats – Khronos](/de/3d/gltf/)

