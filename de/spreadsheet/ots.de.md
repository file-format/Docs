{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "Datei", "Erweiterung", "Dateiformat", "Excel", "Tabellenkalkulation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das OTS-Dateiformat und APIs, die OTS-Dateien erstellen und öffnen können.",
  "title" :"OTS - Dateiformat für OpenDocument-Tabellenkalkulationsvorlagen",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Was ist eine OTS-Datei?

Eine Datei mit der Erweiterung .ots ist eine OpenDocument-Tabellenvorlagendatei, die mit der in Apache OpenOffice enthaltenen Calc-Anwendungssoftware erstellt wird. Die Calc-Anwendungssoftware ähnelt Excel, das in Microsoft Office verfügbar ist. Das OTS-Dateiformat wird verwendet, um Vorlagen zu erstellen, die vordefinierte Einstellungen in Bezug auf Stile, Schriftart, Daten, Tabellenlayout und Formatierung enthalten. OTF-Dateien haben `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Diese Vorlagendateien können als Ausgangspunkt zum Generieren und Speichern tatsächlicher Datendateien verwendet werden, die im [ODS-Dateiformat](/de/spreadsheet/ods/) gespeichert werden. OTS-Dateien können mit Anwendungen wie OpenOffice und LibreOffice verwendet werden.

## OTS-Dateiformat

OTS-Dateien werden im XML-basierten OpenDocument-Dateiformat von OASIS gespeichert, das aus einer Sammlung mehrerer Teildokumente mit einem Paket als [ZIP](/de/compression/zip/)-Archiv besteht. Jedes ZIP-Archiv speichert einen Teil des vollständigen Dokuments und jedes Teildokument speichert einen bestimmten Aspekt des Dokuments. Beispielsweise enthält ein Filialdokument die Stilinformationen und ein anderes Filialdokument den Inhalt des Dokuments. Ein typisches ODF-Dokument hat die folgenden Komponenten:

### OTS-Content.xml

Die Datei content.xml enthält den eigentlichen Inhalt des Dokuments. Dies schließt jedoch keine binären Daten wie Bilder ein.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml des OTS-Dateiformats

Die Datei styles.xml enthält Stilinformationen und wird häufig für Formatierung und Layout verwendet. Zu den Stiltypen gehören:

* Absatzstile
* Seitenstile
* Zeichenstile
* Rahmenstile
* Stile auflisten

### Meta.xml

Die Datei meta.xml enthält Informationen zu den Metadaten der Datei wie Autor, Datum der letzten Änderung usw.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Einstellungen.xml

Die Datei „settings.xml“ enthält Einstellungen auf Dokumentebene wie Zoomfaktor und Cursorposition.

## Verweise ##

* [OpenDocument 1.2-Spezifikation](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument – Von Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

