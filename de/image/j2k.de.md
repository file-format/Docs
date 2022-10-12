{
  "date" : "2019-10-11",
  "keywords" :[ "j2k-Datei", "j2k-Dateiformat", "was ist eine j2k-Datei", "Datei", "j2k-Beispiel", "j2k-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Erfahren Sie mehr über das J2K-Dateiformat und APIs, die J2K-Dateien erstellen und öffnen können.",
  "linktitle" :"J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Was ist eine J2K-Datei?

Eine **J2K**-Datei ist ein Bild, das mit der Wavelet-Komprimierung anstelle der DCT-Komprimierung komprimiert wurde. Dieses Dateiformat wird von JPEG-2000-Dateien (Joint Photographic Experts Group) verwendet. J2K-Dateien speichern Metadateninformationen über die Bilddatei in XML, im Gegensatz zu .jpeg oder .jpg, die zu diesem Zweck das EXIF-Format verwenden. J2K-Dateien unterstützen 15-Bit-Farbe, Alpha-Transparenz und verlustfreie Komprimierung. Es gibt mehrere kommerzielle APIs zum Decodieren von JPEG 2000-Bildern, wie z. B. J2K-Codec. Eine J2K-Datei kann unter Windows OS mit den Standard-Bildbetrachtern geöffnet werden.

## J2K-Dateiformat ##

Das J2K-Dateiformat ist dasselbe wie das von JPEG 2000, das häufig als .jp2 und .jpc gespeichert wird. Dadurch folgen J2K-Dateien demselben Ansatz zur Codierung von Metadaten im XML-Format, bei dem der Standard 12234-1 als Referenz zwischen den Exif-Tags und den XML-Komponenten verwendet wird. Es wird weiter durch die JPEG 2000 Teil-2-Erweiterung verbessert, die den Animationsmechanismus und die Code-Stream-Konfigurationen in einem einzigen Bild kombiniert. Solche Dateien im erweiterten Dateiformat werden als .jpx gespeichert.

### Layout einer JPEG2000-Datei ###

JPEG2000 unterstützt eine Vielzahl von Anwendungen basierend auf der Konformität für erweiterbare Dateiformate. Obwohl der einfachste Typ ein einzelnes Bild enthalten kann, können komplexere Typen eine Reihe von Bildern enthalten, die übereinander gestapelt oder zeitbasiert sequenziert sind.

#### JP2-Box ####
Es ist der oberste Baustein des JP2-Dateiformats und enthält ein Typ- und ein Längenfeld im Header sowie einen Datenabschnitt. Der bemerkenswerteste Boxtyp ist die Contiguous Codestream Box. Diese Box speichert in ihrem Datenabschnitt den JPEG2000-Codestream.

#### JPEG2000 CodeStream ####

Der JPEG2000 CodeStream ist eine Folge von Bytes, die zum Decodieren des JPEG2000-komprimierten Bildes erforderlich ist. Falls die Datei nichts anderes als diesen Codestream enthält, wird sie als Raw-Codestream-Datei bezeichnet. Normalerweise ist ein JPEG-Codestream die Anwendung des JPEG2000-Komprimierungsalgorithmus auf ein Bild, obwohl dies nicht die einzige Möglichkeit ist.

#### Fliesenteile ####

Ein JPEG2000-codiertes Bild ist eine Sammlung von Dateneinheiten, die als Pakete bezeichnet werden. Diese Pakete werden im Codestrom innerhalb von Paketgruppen, die Kachelteile genannt werden, verwaltet. Vor dem Codieren eines Bildes teilt der Encoder das Bild in ein rechteckiges Raster aus Blöcken, Kacheln genannt, wobei jede Kachel unabhängig von anderen Kacheln separat kodiert wird.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000-Dateiformat" >}}

## J2K-Komprimierung ##
JPEG 2000 verwendet die Wavelet-Komprimierungstechnologie, die es aufgrund der Tatsache schnell macht, dass relativ wenige Pixel in jedem Ansichtsfenster oder Fenster angezeigt werden, in dem der Betrachter das Bild anzeigt. Dies kann durch die Tatsache betont werden, dass bei sehr großen Bildern (in Gigabyte) nur wenige Megabyte Pixel auf dem Bildschirm erscheinen. Dies hilft dabei, nur den Teil der Bilddaten schnell abzurufen und wiederzugeben, der erforderlich ist, um die Anzeigepixel zu füllen. Dies erfordert auch eine Hochgeschwindigkeits-Dekomprimierungstechnologie, um den Bildabrufmechanismus zum schnellen Erstellen der erforderlichen Bilddaten zu beschleunigen.

J2K nutzt die schnelle Dekomprimierung und ruft nur die notwendigen Informationen für Pixeldaten ab, um einen Teil der sichtbaren Bilder schnell auf den Bildschirmen darzustellen. J2K ist in erster Linie für die Anzeige von Daten konzipiert und nicht für deren Bearbeitung.

## J2K-Identifikation ##
JPEG 2000-Dateien haben Signaturbytes 6A 50 20 20.

### Mime-Typen ###
Zu den registrierten Mime-Typen für JPEG 2000-Dateien gehören:
* Bild/jp2
* Bild/jpx
* Bild/jpm
* video/mj2

## Verbesserungen gegenüber dem JPEG-Standard ##
Zu den Verbesserungen gegenüber dem JPEG-Standard gehören:
* Überlegene Komprimierungsleistung
* Darstellung mit mehreren Auflösungen
* Progressive Übertragung nach Pixel und Auflösungsgenauigkeit
* Auswahl zwischen verlustfreier oder verlustbehafteter Komprimierung
* Fehlerresilienz, flexibles Dateiformat
* Unterstützung für hohen Dynamikbereich
* Räumliche Informationen des Seitenkanals

## Verweise ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

