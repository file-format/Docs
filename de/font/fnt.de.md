{
  "date" : "2020-08-20",
  "keywords" :[ "fnt-Datei", "fnt-Dateiformat", "was ist eine fnt-Datei", "Datei", "fnt-Beispiel", "fnt-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows-Schriftartdatei",
  "description":"Erfahren Sie mehr über das FNT-Dateiformat und APIs, die FNT-Dateien erstellen und öffnen können.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Was ist eine FNT-Datei?

Eine Datei mit der Erweiterung .fnt ist eine Schriftartdatei, die generische Schriftartinformationen auf Windows-Betriebssystemen speichert. FNT-Dateien wurden größtenteils durch die Dateiformate TrueType (.TTF) und OpenType (.OTF) ersetzt und sind ab sofort ein veraltetes Dateiformat für Schriftarten. Diese Dateien können eine einzelne Rater- oder Vektorschriftart speichern. Alle Gerätetreiber unterstützen die Windows 2.x-Schriftarten. Allerdings nicht alle Gerätetreiber
unterstützen die Windows 3.0-Version.

## FNT-Dateiformat

FNT-Dateien können eine einzelne Raster- oder Vektorschriftart speichern. Die Vektorformate werden von GDI häufiger verwendet als das Raster, bei dem die Glyphe jeder Charta mithilfe einer kleinen Bitmap definiert wird. Der offensichtliche Grund für die Ersetzung von .fnt durch .ttf und .otf ist das Rasterformat.

### Schriftartdatei-Header
Der Anfang von Raster- und Vektorfontdateien ist gleich, gefolgt von unterschiedlichen Informationen für jeden Dateityp. Der Font-File-Header Includes für Windows 3.0 enthält die folgenden sechs neuen Felder, die auf Null gesetzt werden, um die Kompatibilität mit zukünftigen Windows-Versionen zu gewährleisten.

* dFlags
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserviert1

Ausführliche Informationen zu den Headern für Windows 3.0 und 2.0 finden Sie im [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Verweise
* [Schriftdateiformat](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [So installieren oder entfernen Sie eine Schriftart in Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

