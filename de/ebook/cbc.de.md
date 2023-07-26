{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "Erweiterung", "Datei", "Format", "Comic-Bücher", "Comic-Bücher-Dateiformat", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das CBC-Dateiformat und APIs, die CBC-Dateien erstellen und öffnen können.",
  "title" :"CBC - Dateiformat der Comic-Sammlung",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Was ist eine CBC-Datei?

Eine Datei mit der Erweiterung .cbc ist eine komprimierte Sammlung von Comicbuchdateien für eBooks und enthält [CBZ](/de/ebook/cbz/)- und [CBR](/de/ebook/cbr/)-Dateien. Es wird von [Calibre](https://calibre-ebook.com/) verwendet, einer eBook-Konvertierungsanwendung, einem plattformübergreifenden Open-Source-E-Book-Manager, mit dem Sie Ihre eBooks verwalten und in verschiedene Formate konvertieren können . Eine CBC-Datei enthält eine .txt-Datei, comics.txt, die andere Dateien auflistet, die Teil des Archivs sind. Mehrere Anwendungen sind online verfügbar, die CBC-Dateien in [AZW3](/de/ebook/azw3/), [EPUB](/de/ebook/epub/), [FB2](/de/ebook/fb2/), [MOBI](/de/ebook/ mobi/), [TXT](/de/word-processing/txt/), [PDF](/de/pdf/) und andere gängige Dateiformate.

## CBC-Dateiformat

CBC-Dateien sind komprimierte Archive, die CBZ, CBR und eine Textdatei zum Auflisten des Inhalts enthalten. Die Textdatei comics.txt ist UTF8-codiert und enthält eine Liste der CBC-Dateien, die von Lesern zum Organisieren ihrer Sammlungen verwendet werden sollen. Eine CBC-Datei hat normalerweise mehrere Attribute, die die Organisation dieser Sammlung ermöglichen, wie z. B. Comic, Kategorie, Herausgeber, Serie, Ausgabe und Künstler.

Der Inhalt einer Beispiel-CBC-Datei ist wie folgt aufgeführt:

* comics.txt - Textdatei, die eine Liste von CBR- und CBZ-Dateien enthält
* 1.cbz
* 2.cbz
* 3.cbz
* CBZ-Datei(en)

wobei die Datei comics.txt den Inhalt wie folgt auflistet:

* 1.cbz: Erstes Kapitel
* 2.cbz: Zweites Kapitel
* 3.cbz: Drittes Kapitel

Leser verarbeiten die comics.txt-Datei und generieren das Inhaltsverzeichnis basierend auf den bereitgestellten Daten.

## Verweise

* [Calibre](https://calibre-ebook.com/)

