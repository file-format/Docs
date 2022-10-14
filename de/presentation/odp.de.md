{
  "date" : "2019-10-11",
  "keywords" :[ "ODP-Datei", "ODP-Dateiformat", "Was ist eine ODP-Datei", "Datei", "ODP-Beispiel", "ODP-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice-Präsentationsdateiformat",
  "description":"Erfahren Sie mehr über das ODP-Dateiformat und APIs, die ODP-Dateien erstellen und öffnen können.",
  "linktitle" :"ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine ODP-Datei?

Dateien mit der Erweiterung .odp stellen das Präsentationsdateiformat dar, das von OpenOffice.org im OASISOpen-Standard verwendet wird. Eine Präsentationsdatei ist eine Sammlung von Folien, wobei jede Folie aus Text, Bildern, Formatierungen, Animationen und anderen Medien bestehen kann. Diese Folien werden dem Publikum in Form von Diashows mit benutzerdefinierten Präsentationseinstellungen präsentiert. ODP-Dateien können von Anwendungen geöffnet werden, die dem OpenDocument-Format entsprechen (z. B. OpenOffice oder StarOffice).

## Kurze Geschichte

ODP-Dateiformatspezifikationen basieren auf dem als ODF-Spezifikationen entwickelten Standard. Diese Spezifikationen wurden in der Vergangenheit in Form von drei Versionen entwickelt und von OASIS wie folgt veröffentlicht:

`2005` - Version 1.0 wurde im Mai 2005 veröffentlicht
`2007` - Version 1.1 wurde im Februar 2007 veröffentlicht
`2011` - Version 1.2 wurde im September 2011 veröffentlicht

Beim Übergang von ODF 1.0 zu 1.1 gab es ziemlich kleine Änderungen. Die [ODF 1.2-Version] (https://www.oasis-open.org/standards#opendocumentv1.2) ist die neueste Version für ODF-Spezifikationen und sollte von Entwicklern für die Entwicklung von Anwendungen im Zusammenhang mit ODS-Lesen/Schreiben konsultiert werden.

## Dateiformatspezifikationen

Das OpenDocument-Format unterstützt die Dokumentendarstellung als einzelnes XML-Dokument sowie als Sammlung mehrerer Teildokumente innerhalb eines Pakets als [ZIP](https://docs.fileformat.com/Compression/ZIP/)-Archiv. Jede der Dateien aus dem ZIP-Archiv speichert einen Teil des vollständigen Dokuments. Jedes Unterdokument speichert einen bestimmten Aspekt des Dokuments. Beispielsweise enthält ein Filialdokument die Stilinformationen und ein anderes Filialdokument den Inhalt des Dokuments. Ein typisches ODF-Dokument hat die folgenden Komponenten:

* `content.xml` – Dokumentinhalt und automatische Stile, die im Inhalt verwendet werden.
* `styles.xml` – Stile, die im Dokumentinhalt verwendet werden, und automatische Stile, die in den Stilen selbst verwendet werden.
* `meta.xml` – Metainformationen des Dokuments, wie z. B. der Autor oder der Zeitpunkt des letzten Speichervorgangs.
* `settings.xml` – Anwendungsspezifische Einstellungen wie Fenstergröße oder Druckerinformationen.

Außerdem können im Paket viele andere Unterdokumente wie Miniaturansichten, Bilder usw. enthalten sein.

Tabellenkalkulationsdokumentdateien sind die Teilmenge von ODF-Dateien, in denen der Inhalt (Blätter) im Unterdokument content.xml gespeichert ist.

## Verweise

* [OpenDocument – Von Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

