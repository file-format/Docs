{
  "date" : "2019-10-11",
  "keywords" :[ "ott-Datei", "ott-Dateiformat", "was ist eine ott-Datei", "Datei", "ott-Beispiel", "ott-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - OpenDocument-Vorlagendatei",
  "description":"Erfahren Sie mehr über das OTT-Dateiformat und APIs, die OTT-Dateien erstellen und öffnen können.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine OTT-Datei?

Dateien mit der Erweiterung OTT stellen Vorlagendokumente dar, die von Anwendungen in Übereinstimmung mit dem OpenDocument-Standardformat von OASIS generiert wurden. Diese werden mit Textverarbeitungsprogrammen wie dem kostenlosen OpenOffice Writer erstellt und können Einstellungen enthalten, die zum Generieren neuer Dokumente aus diesen Vorlagendateien verwendet werden können. Zu diesen Einstellungen gehören Seitenränder, Ränder, Kopfzeilen, Fußzeilen und andere Seiteneinstellungen. Solche Vorlagen werden in offiziellen Dokumenten wie Firmenbriefköpfen und standardisierten Formularen verwendet.

## Kurze Geschichte ##

ODP-Dateiformatspezifikationen basieren auf dem als ODF-Spezifikationen entwickelten Standard. Diese Spezifikationen wurden in der Vergangenheit in Form von drei Versionen entwickelt und von OASIS wie folgt veröffentlicht:

**2005:** Version 1.0 wurde im Mai 2005 veröffentlicht

**2007:** Version 1.1 wurde im Februar 2007 veröffentlicht

**2011:** Version 1.2 wurde im September 2011 veröffentlicht

Beim Übergang von ODF 1.0 zu den 1.1-Versionen gab es ziemlich geringfügige Änderungen. Die [ODF 1.2-Version] (https://www.oasis-open.org/standards#opendocumentv1.2) ist die neueste Version für ODF-Spezifikationen und sollte von Entwicklern für die Entwicklung von Anwendungen im Zusammenhang mit ODS-Lesen/Schreiben konsultiert werden.

## Dateiformatspezifikationen

Das OpenDocument-Format unterstützt die Dokumentendarstellung als einzelnes XML-Dokument sowie als Sammlung mehrerer Teildokumente innerhalb eines Pakets als [ZIP](/de/Compression/ZIP/)-Archiv. Jede der Dateien aus dem ZIP-Archiv speichert einen Teil des vollständigen Dokuments. Jedes Unterdokument speichert einen bestimmten Aspekt des Dokuments. Beispielsweise enthält ein Filialdokument die Stilinformationen und ein anderes Filialdokument den Inhalt des Dokuments. Ein typisches ODF-Dokument hat die folgenden Komponenten:

* content.xml – Dokumentinhalt und im Inhalt verwendete automatische Stile.
* styles.xml – Stile, die im Dokumentinhalt verwendet werden, und automatische Stile, die in den Stilen selbst verwendet werden.
* meta.xml – Dokumentiere Metainformationen, wie zum Beispiel den Autor oder den Zeitpunkt der letzten Speicheraktion.
* settings.xml – Anwendungsspezifische Einstellungen wie Fenstergröße oder Druckerinformationen.

Abgesehen davon können im Paket viele andere Unterdokumente wie Miniaturansichten von Dokumenten, Bilder usw. enthalten sein. Dokumentdateien sind die Teilmenge von ODF-Dateien, in denen der Inhalt (Blätter) im Unterdokument //content.xml// gespeichert ist.

## Verweise ##

* [OpenDocument – Von Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
