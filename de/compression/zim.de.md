{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM-Dateiformat - OpenZIM-Archivdatei",
  "description":"Erfahren Sie mehr über das ZIM-Dateiformat und APIs, die ZIM-Dateien erstellen und öffnen können.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Was ist eine ZIM-Datei? ##

Dateien mit der Erweiterung .zim sind Archive, die erstellt wurden, um Wiki-Inhalte offline zu speichern. Es gilt als das am besten geeignete offene Dateiformat zum Speichern von Wikipedia auf einem USB-Stick. Es speichert Website-Inhalte in einem kompakten Format. Sein Name kommt von "Zeno IMproved", dem früheren Zeno-Dateiformat. ZIM wird von [openZIM ](https://openzim.org/)project verwaltet, das von Wikimedia CH gesponsert und von der Wikimedia Foundation unterstützt wird. ZIM-Dateien können von Anwendungen wie Kiwix und ZIMReader geöffnet werden. Das OpenZIM-Projekt hat die Implementierung des ZIM-Dateiformats auf [Github](https://github.com/openzim) für Beiträge der OpenSource-Community gehostet.

## ZIM-Dateiformatspezifikationen

Das ZIM-Dateiformat wurde auf der Grundlage von [Zeno-Dateiformat](https://openzim.org/wiki/Zeno_file_format) entwickelt und ist nicht abwärtskompatibel. Die Formatspezifikationen des ZIM-Dateiformats sind [online verfügbar](https://openzim.org/wiki/ZIM_file_format) von openZIM als Referenz für Entwickler. OpenZIM hat eine C++-Open-Source-Implementierung, [LibZim](https://openzim.org/wiki/Zimlib), zum Lesen und Schreiben von ZIM-Dateien bereitgestellt.

Das ZIM-Dateiformat verwendet die LZMA2-Komprimierung, um den Inhalt kompakt zu machen.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM-Dateiformat" >}}


### ZIM-Header

Eine ZIM-Datei beginnt mit einem Header, der bei Offset 0 ist. Alle Bestandteile basieren auf Little-Endian und alle Ganzzahlen sind Ganzzahlen ohne Vorzeichen, dh uint_16, uint_32, uint_64.

|Feldname |Typ| Offset| Länge| Beschreibung|
---|---|---|---|---|
|magischeZahl| ganze Zahl| 0| 4| Magische Nummer zur Erkennung des Dateiformats, muss 72173914 (0x44D495A) sein|
|Hauptversion| ganze Zahl| 4| 2| Hauptversion des ZIM-Dateiformats (5 oder 6)|
|Nebenversion| ganze Zahl| 6| 2| Nebenversion des ZIM-Dateiformats|
|uuid| ganze Zahl| 8| 16| eindeutige ID dieser Zim-Datei|
|Artikelzahl| ganze Zahl| 24| 4| Gesamtzahl der Artikel|
|clusterCount| ganze Zahl| 28| 4| Gesamtzahl der Cluster|
|urlPtrPos| ganze Zahl| 32| 8| Position der Verzeichnis-Zeigerliste, geordnet nach URL|
|titlePtrPos| ganze Zahl| 40| 8| Position der Verzeichnis-Zeigerliste, geordnet nach Titel|
|clusterPtrPos| ganze Zahl| 48| 8| Position der Cluster-Pointer-Liste|
|mimeListPos| ganze Zahl| 56| 8| Position der MIME-Type-Liste (auch Header-Größe)|
|Hauptseite| ganze Zahl| 64| 4| Hauptseite oder 0xffffffff falls keine Hauptseite|
|LayoutSeite| ganze Zahl| 68| 4| Layoutseite oder 0xffffffffff wenn keine Layoutseite|
|checksumPos| ganze Zahl| 72| 8| Zeiger auf die md5-Prüfsumme dieser Datei ohne die Prüfsumme selbst. Dieser zeigt immer 16 Bytes vor das Ende der Datei.|

## Verweise ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

