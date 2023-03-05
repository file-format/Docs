{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "Datei", "Erweiterung", "Dateiformat", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine ODS-Datei und APIs sind, die sie erstellen und öffnen können.",
  "title" :"Was ist eine ODS-Datei?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine ODS-Datei?

Dateien mit der Erweiterung .ods stehen für OpenDocument Spreadsheet Document-Format, das vom Benutzer bearbeitet werden kann. Daten werden in der ODF-Datei in Zeilen und Spalten gespeichert. Es ist ein XML-basiertes Format und einer von mehreren Untertypen in der Familie der Open Document Formats (ODF). Das Format wird als Teil der ODF 1.2-Spezifikationen spezifiziert, die von OASIS veröffentlicht und gepflegt werden. Eine Reihe von Anwendungen unter Windows sowie anderen Betriebssystemen können ODS-Dateien zum Bearbeiten und Manipulieren öffnen, darunter Microsoft Excel, NeoOffice und LibreOffice. ODS-Dateien können auch in andere Tabellenkalkulationsformate wie [XLS](/de/spreadsheet/xls/), [XLSX](/de/spreadsheet/xlsx/) und andere von verschiedenen Anwendungen konvertiert werden.

## Kurze Geschichte ##

ODS-Dateiformatspezifikationen basieren auf dem als ODF-Spezifikationen entwickelten Standard. Diese Spezifikationen wurden in der Vergangenheit in Form von drei Versionen entwickelt und von OASIS wie folgt veröffentlicht:

`2005`- Version 1.0 wurde im Mai 2005 veröffentlicht

`2007` - Version 1.1 wurde im Februar 2007 veröffentlicht

`2011` - Version 1.2 wurde im September 2011 veröffentlicht

Beim Übergang von ODF 1.0 zu 1.1 gab es ziemlich kleine Änderungen. Die [ODF 1.2-Version](https://www.oasis-open.org/standards#opendocumentv1.2) ist die neueste Version für ODF-Spezifikationen und sollte von Entwicklern für die Entwicklung von Anwendungen im Zusammenhang mit ODS-Lesen/Schreiben konsultiert werden.

## ODS-Dateiformat ##

Das OpenDocument-Format unterstützt die Dokumentendarstellung als einzelnes XML-Dokument sowie als Sammlung mehrerer Teildokumente innerhalb eines Pakets als [ZIP](/de/compression/zip/)-Archiv. Jede der Dateien aus dem ZIP-Archiv speichert einen Teil des vollständigen Dokuments. Jedes Unterdokument speichert einen bestimmten Aspekt des Dokuments. Beispielsweise enthält ein Filialdokument die Stilinformationen und ein anderes Filialdokument den Inhalt des Dokuments. Ein typisches ODF-Dokument hat die folgenden Komponenten:

* `content.xml` – Dokumentinhalt und automatische Stile, die im Inhalt verwendet werden.
* `styles.xml` – Stile, die im Dokumentinhalt verwendet werden, und automatische Stile, die in den Stilen selbst verwendet werden.
* `meta.xml` – Metainformationen des Dokuments, wie z. B. der Autor oder der Zeitpunkt des letzten Speichervorgangs.
* `settings.xml` – Anwendungsspezifische Einstellungen wie Fenstergröße oder Druckerinformationen.

Außerdem können im Paket viele andere Unterdokumente wie Miniaturansichten, Bilder usw. enthalten sein.

Tabellenkalkulationsdokumentdateien sind die Teilmenge von ODF-Dateien, in denen der Inhalt (Blätter) im Unterdokument content.xml gespeichert ist.

## Verweise ##

* [OpenDocument – Von Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

