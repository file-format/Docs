{
  "date" : "2019-10-11",
  "keywords" :[ "wmf-Datei", "wmf-Dateiformat", "was ist eine wmf-Datei", "Datei", "wmf-Beispiel", "wmf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafile-Format",
  "description":"Erfahren Sie mehr über das WMF-Dateiformat und APIs, die WMF-Dateien erstellen und öffnen können.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine WMF-Datei?

Dateien mit der Erweiterung WMF stellen Microsoft Windows Metafile (WMF) zum Speichern von Bilddaten im Vektor- und Bitmap-Format dar. Genauer gesagt gehört WMF zur Kategorie der Vektordateiformate der geräteunabhängigen Grafikdateiformate. Windows Graphical Device Interface (GDI) verwendet die in einer WMF-Datei gespeicherten Funktionen, um ein Bild auf dem Bildschirm anzuzeigen. Eine erweiterte Version von WMF, bekannt als Enhanced Meta Files (EMF), wurde später veröffentlicht, die das Format funktionsreicher macht. In der Praxis ähneln WMF SVG.

## Spezifikationen des WMF-Dateiformats ##

Eine WMF-Datei bezog sich zum Zeitpunkt ihres Starts mit Windows 3.0 auf das 16-Bit-Dateiformat. Das Dateiformat besteht aus einer Reihe von Datensätzen variabler Länge, die Befehle zum Zeichnen von Grafiken, Objektdefinitionen und Eigenschaften enthalten. Da WMF-Dateien auf Befehlen basieren, die zum Zeichnen des Bildes an das GDI gerendert werden, wird es auch als digitale Aufzeichnung des Bildes bezeichnet, die wiedergegeben werden kann, um dieses Bild zu reproduzieren. Die vollständigen Dateiformatspezifikationen von WMF sind online verfügbar und sollten für die Entwicklung von Anwendungen zur Arbeit mit WMF-Dateien herangezogen werden. Eine WMF-Datei ist organisiert in:

* WMF-Header-Datensatz
* WMF-Eintrag(e)
* WMF Dateiende-Aufzeichnung

### WMF-Header-Datensatz ###

Der **META_HEADER-Datensatz** enthält Informationen, die die Merkmale der Metadatei definieren, einschließlich:

* Der Typ der Metadatei
* Die Version der Metadatei
* Die Größe der Metadatei
* Die Anzahl der in der Metadatei definierten Objekte
* Die Größe des größten einzelnen Datensatzes in der Metadatei

### Platzierbarer WMF-Header-Datensatz ###

Der **META_PLACEABLE Record** enthält erweiterte Informationen zum Bild, darunter:

* Ein Begrenzungsrechteck
* Größe der logischen Einheit zur Skalierung
* Eine Prüfsumme zur Validierung

### WMF-Eintrag ###

WMF-Datensätze haben ein generisches Format, das im Spezifikationsdokument angegeben ist. Jeder WMF-Datensatz enthält die folgenden Informationen:

* Die Datensatzgröße
* Die Aufnahmefunktion
* Parameter, falls vorhanden, für die Aufnahmefunktion

## Verweise ##

* [[MS-WMF]: Windows Metafile-Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows-Metadatei – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

