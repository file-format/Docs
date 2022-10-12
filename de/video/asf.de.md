{
  "date" : "2021-02-15",
  "keywords" :[ "asf-Datei", "asf-Dateiformat", "was ist eine asf-Datei", "Datei", "asf-Beispiel", "asf-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Erweitertes Systemdateiformat",
  "description":"Erfahren Sie mehr über das ASF-Dateiformat und APIs, die ASF-Dateien erstellen und öffnen können.",
  "linktitle" :"ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Was ist eine ASF-Datei?

Eine Datei mit der Erweiterung .asf ist ein Multimedia-Dateiformat zum Speichern und Wiedergeben digitaler Medienströme über das Netzwerk. Es ist ein Container-Dateiformat, das sowohl Video- als auch Audioinhalte für das Online-Streaming enthalten kann. Sie werden selten ASF-Dateien finden und eher auf die Dateien Windows Media Audio ([WMA](/de/audio/wma/)) und Windows Media Video ([WMV](/de/video/wmv/)) stoßen, die beide ASF-Dateien spezifizieren mit Inhalten, die mit entsprechenden Codecs codiert sind. Windows Media-Dateien können mit dem Windows Media Format SDK erstellt und gelesen werden.

## ASF-Dateiformat

Eine ASF-Datei kann mehrere unabhängige oder abhängige Streams umfassen. Dies kann mehrere Audiostreams für Mehrkanal-Audio oder Videostreams mit mehreren Bitraten umfassen. Durch die mehreren Bitraten eignen sich die Streams für die Übertragung über verschiedene Bandbreiten. Darüber hinaus können die Streams in einer ASF-Datei im komprimierten oder unkomprimierten Format vorliegen. Die beste Komprimierung wird mit den Codecs der Microsoft Windows Media Audio- und Video 9-Reihe erreicht. Vollständige Spezifikationen des ASF-Dateiformats sind auf der [Microsoft-Website] (https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) verfügbar.

### ASF-Dateistruktur der obersten Ebene

ASF-Dateien enthalten logischerweise drei Arten von Objekten der obersten Ebene:

* `Header Object` - obligatorisch und muss am Anfang jeder ASF-Datei platziert werden
* „Datenobjekt“ – obligatorisch und muss dem Header-Objekt folgen
* „Index-Objekt(e)“ – optional, aber nützlich, um zeitbasierten Direktzugriff auf ASF-Dateien bereitzustellen

Das folgende Bild zeigt die Dateistruktur der obersten Ebene von ASF-Dateien.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF-Header-Objekt der obersten Ebene

Das Header-Objekt stellt eine bekannte Bytefolge am Anfang der ASF-Dateien bereit und kann optional Metadaten wie bibliografische Informationen enthalten. Es enthält alle Informationen, die erforderlich sind, um die Informationen innerhalb des Datenobjekts richtig zu interpretieren. Das Header-Objekt kann mehrere Standardobjekte enthalten, einschließlich, aber nicht beschränkt auf:

* Dateieigenschaftenobjekt - Enthält globale Dateiattribute.
* Stream-Eigenschaftenobjekt – Definiert einen digitalen Medienstream und seine Eigenschaften.
* Header-Erweiterungsobjekt - Ermöglicht das Hinzufügen zusätzlicher Funktionen zu einer ASF-Datei unter Beibehaltung der Abwärtskompatibilität.
* Inhaltsbeschreibungsobjekt - Enthält bibliografische Informationen.
* Skriptbefehlsobjekt - Enthält Befehle, die auf der Wiedergabezeitachse ausgeführt werden können.
* Markierungsobjekt - Bietet benannte Sprungpunkte innerhalb einer Datei.

Das Header-Objekt wird durch die folgende Struktur dargestellt:

|Feldname |Feldtyp |Größe (Bits)|
---|---|---|
|Objekt-ID| GUID| 128|
|Objektgröße| QWORT| 64|
|Anzahl Header-Objekte| DWORT| 32|
|Reserviert1| BYTE| 8|
|Reserviert2| BYTE| 8|

#### ASF-Datenobjekt der obersten Ebene

Alle digitalen Mediendaten einer ASF-Datei sind im Datenobjekt enthalten und werden in Form von ASF-Datenpaketen gespeichert. Jedes Datenpaket hat eine feste Länge und enthält Daten für einen oder mehrere digitale Medienströme.

#### ASF-Indexobjekte der obersten Ebene

ASF-Indexobjekte der obersten Ebene haben die folgenden zwei Typen:

* `Simple Index Object` - Enthält einen zeitbasierten Index der Videodaten in einer ASF-Datei. Das Zeitintervall zwischen Indexeinträgen ist konstant und wird im Simple Index Object gespeichert.
* „Indexobjekt“ – Bezieht sich auf das Indexobjekt, das Medienobjekt-Indexobjekt und das Timecode-Indexobjekt, deren Formate ähnlich sind. Wie das einfache Indexobjekt indiziert das Indexobjekt nach Zeit mit einem festen Zeitintervall, ist aber nicht auf Videostreams beschränkt.

## Verweise

* [ASF-Dateiformat – Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime-Dateiformat – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

