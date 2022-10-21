{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Rocket eBook-Gerät von Nuvo Media", "Datei", "Erweiterung", "Format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das RB-Dateiformat für das Rocket eBook-Gerät von Nuvo Media und APIs, die RB-Dateien erstellen und öffnen können.",
  "title" :"RB - Rocket eBook-Datei",
  "linktitle" :"RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Was ist eine RB-Datei?

Die Datei mit der Erweiterung .rb enthält den Rocket eBook-Inhalt. Das Rocket eBook ist eigentlich ein Gerät von Nuvo Media; Sie veröffentlichten dieses Gerät im Jahr 1998. Rocket eBook ist zwar in der Lage, Bilder anzuzeigen, jedoch nur in Schwarzweiß. Es hat einen Bildschirm von 106 dpi oder 480 x 320 Pixel auf einem 4,5 x 3-Zoll-Touchscreen. Das Rocket eBook wird über eine serielle Schnittstelle mit einem Computer verbunden, um eBooks im RB-Dateiformat herunterzuladen. Die RB-Dateien können DRM verwenden, aber diese Technologie wird in modernen eBooks nicht verwendet. Die RB-Datei enthält üblicherweise eine HTML-Datei mit den Bildern und eine Pseudo-OPF-Datei mit allen Metadaten (.info).

## Technische Spezifikation des RB-Dateiformats ##

Eine magische Zahl (in Hex) erscheint in den ersten 4 Bytes der Datei: B0 0C B0 0C.

Es scheint, dass die nächsten zwei Bytes eine Versionsnummer sind, wie "02 00", die für Hauptversion 2 und Nebenversion 0 steht.

Die nächsten vier Bytes enthalten den Text "NUVO", gefolgt von 4 Bytes von 00h.

Die nächsten 4 Byte sind das Datum, an dem das Buch erstellt wurde, codiert als int16. Dies bringt uns zum Offset 0Eh. Die alte Version von ORocketLibrary codierte den vollen Jahreswert (dh 1999 war "CF 07", 2000 war "D0 07"). In der neueren Version wird tm_year wörtlich gespeichert, dh 100 für das Jahr 2000 ("64 00"). Nach dem Jahr kommt ein int8, das die 1-relative Monatszahl darstellt, und ein int8, das den Tag des Monats darstellt.

Die nächsten 6 Bytes sind 00h. Zur Zeiteinstellung können diese reserviert werden.

Der absolute Offset des "Table of Contents" ist in einem int32 bei Offset 18h enthalten.

Danach folgt ein int32, das die Länge der .rb-Datei enthält. Dies wird verwendet, um festzustellen, ob die Dateien vollständig sind oder nicht.

Dieser ganze Byteblock (20h bis 128h) scheint nur von einem verschlüsselten Titel benötigt zu werden. Bei unverschlüsselten Titeln sind sie immer Null.

In den meisten Fällen folgt das Inhaltsverzeichnis (bei Offset 128). Es beginnt mit einer int32-Zählung der Anzahl der „Seiten“-Einträge (.rb-Dateiabschnitte) im Inhaltsverzeichnis. Jeder Eintrag besteht aus einem Namen (mit Nullen aufgefüllt zu 32 Bytes), gefolgt von 3 int32s: die Länge des Datensegments, die Position in der .rb-Datei und ein Flag für diesen Eintrag. Ab heute sind die bekannten Werte: 1 (verschlüsselt), 2 (Informationsseite) und 8 (deflationiert). Die Namen werden nach Bedarf angepasst, um sicherzustellen, dass sie alle eindeutig sind.

## Verweise

* [E-Reader – Von MobileRead](https://en.wikipedia.org/wiki/E-Reader)

