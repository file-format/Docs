{
  "date" : "2021-04-08",
  "keywords" :[ "pkg-Datei", "pkg-Dateiformat", "was ist eine pkg-Datei", "Datei", "pkg-Beispiel", "pkg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Erweiterbares Archivdateiformat",
  "description":"Erfahren Sie mehr über das PKG-Dateiformat und APIs, die PKG-Dateien erstellen und öffnen können.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Was ist eine PKG-Datei?

Eine Datei mit der Erweiterung .pkg ist eine Installationspaketdatei, die zum Installieren von Software unter macOS verwendet wird. Neben Macintosh-Computern wird es auch auf dem iPhone verwendet. Die integrierte Apple-Installationsanwendung kann verwendet werden, um den Inhalt einer PKG-Datei zu installieren. Eine PKG-Datei ähnelt einer MSI-Datei, die auf dem Windows-Betriebssystem zur Installation von Software verwendet wird. Während der Installation können diese Paketdateien Meldungen protokollieren, die Ihnen eine Vorstellung davon geben, welche zusätzlichen Dinge von diesem Paket installiert werden.

## PKG-Dateiformat

PKR sind Binärdateien, die komprimiert werden, um die Gesamtdateigröße zu reduzieren. Seit OSX 10.5 wurden von Apple flache Pakete mit einzelnen Installationsdateien eingeführt. Diese unterscheiden sich von den früheren Verpackungsformaten, die als Bündel und nicht als einzelne Dateien geliefert wurden. Diese gebündelten Pakete enthielten eine strukturierte Verzeichnishierarchie, in der Dateien so gespeichert wurden, dass ihr Abruf über eine Indexdatei erleichtert wurde. Das flache PKG-Dateiformat ist eigentlich ein [XAR](/de/compression/xar/)-Archiv mit einem:

* Header - Definiert die Größe, Prüfsumme und Versionsinformationen
* Inhaltsverzeichnis - Ein XML-Dokument, das als UTF-8 codiert ist (und muss) und am Anfang der Datei gespeichert wird, wodurch es einfach ist, das Archiv zu durchsuchen, um einzelne Dateien zu extrahieren
* Heap – unstrukturierter Datenhaufen, auf den durch das Inhaltsverzeichnis verwiesen wird

## Verweise

* [Dateiformat für Flat-Pakete](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

