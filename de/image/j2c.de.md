{
  "date" : "2019-10-11",
  "keywords" :[ "j2c-Datei", "j2c-Dateiformat", "was ist eine j2c-Datei", "Datei", "j2c-Beispiel", "j2c-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Erfahren Sie mehr über das J2C-Dateiformat und APIs, die J2C-Dateien erstellen und öffnen können.",
  "linktitle" :"J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Was ist eine J2C-Datei?

Eine Datei mit der Erweiterung .j2c ist eine Variante des JPEG-Dateiformats und wird mit der Wavelet-Komprimierung komprimiert. Es hat ein nahezu identisches Markierungs- und Segmentsystem wie das JPEG 2000-Dateiformat. Das J2C-Dateiformat entspricht der Definition in Teil 1 des JPEG 2000-Stands, der sowohl verlustbehaftete als auch verlustfreie Komprimierung unterstützt. Der JPEG 2000-Codestream wurde entwickelt, um in [JP2](/de/image/jp2/) oder ein anderes Dateiformat eingebettet zu werden, obwohl er auch in einer eigenen Datei erscheinen kann. Eine J2C-Datei kann mit Adobe Photoshop 2020, Adobe Illustrator 2020 und Corel Paintshop Pro geöffnet werden.

## J2C-Dateiformat

Das J2C-Dateiformat ist dasselbe wie das von JPEG 2000, das häufig als .jp2 und .jpc gespeichert wird. Dadurch folgen J2C-Dateien demselben Ansatz zur Codierung von Metadaten im XML-Format, bei dem der Standard 12234-1 als Referenz zwischen den Exif-Tags und den XML-Komponenten verwendet wird. Es wird weiter durch die JPEG 2000 Teil-2-Erweiterung verbessert, die den Animationsmechanismus und die Code-Stream-Konfigurationen in einem einzigen Bild kombiniert. Solche Dateien im erweiterten Dateiformat werden als [.jpx](/de/image/jpx/) gespeichert.

### Layout einer JPEG2000-Datei

JPEG2000 unterstützt eine Vielzahl von Anwendungen basierend auf der Konformität für erweiterbare Dateiformate. Obwohl der einfachste Typ ein einzelnes Bild enthalten kann, können komplexere Typen eine Reihe von Bildern enthalten, die übereinander gestapelt oder zeitbasiert sequenziert sind.

#### JP2-Box
Es ist der oberste Baustein des JP2-Dateiformats und enthält ein Typ- und ein Längenfeld im Header sowie einen Datenabschnitt. Der bemerkenswerteste Boxtyp ist die Contiguous Codestream Box. Diese Box speichert in ihrem Datenabschnitt den JPEG2000-Codestream.

#### JPEG2000 CodeStream

Der JPEG2000 CodeStream ist eine Folge von Bytes, die zum Decodieren des JPEG2000-komprimierten Bildes erforderlich ist. Falls die Datei nichts anderes als diesen Codestream enthält, wird sie als Raw-Codestream-Datei bezeichnet. Normalerweise ist ein JPEG-Codestream die Anwendung des JPEG2000-Komprimierungsalgorithmus auf ein Bild, obwohl dies nicht die einzige Möglichkeit ist.

#### Fliesenteile ####

Ein JPEG2000-codiertes Bild ist eine Sammlung von Dateneinheiten, die als Pakete bezeichnet werden. Diese Pakete werden im Codestrom innerhalb von Paketgruppen, die Kachelteile genannt werden, verwaltet. Vor dem Codieren eines Bildes teilt der Encoder das Bild in ein rechteckiges Raster aus Blöcken, Kacheln genannt, wobei jede Kachel unabhängig von anderen Kacheln separat kodiert wird.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000-Dateiformat" >}}

## J2C-Komprimierung
JPEG 2000 verwendet die Wavelet-Komprimierungstechnologie, die es aufgrund der Tatsache schnell macht, dass relativ wenige Pixel in jedem Ansichtsfenster oder Fenster angezeigt werden, in dem der Betrachter das Bild anzeigt. Dies kann durch die Tatsache betont werden, dass bei sehr großen Bildern (in Gigabyte) nur wenige Megabyte Pixel auf dem Bildschirm erscheinen. Dies hilft dabei, nur den Teil der Bilddaten schnell abzurufen und wiederzugeben, der erforderlich ist, um die Anzeigepixel zu füllen. Dies erfordert auch eine Hochgeschwindigkeits-Dekomprimierungstechnologie, um den Bildabrufmechanismus zum schnellen Erstellen der erforderlichen Bilddaten zu beschleunigen.

J2C nutzt die schnelle Dekomprimierung und ruft nur die notwendigen Informationen für Pixeldaten ab, um einen Teil der sichtbaren Bilder schnell auf den Bildschirmen darzustellen. J2C ist in erster Linie für die Anzeige von Daten konzipiert und nicht für deren Bearbeitung.

## J2C-Identifikation
JPEG 2000-Dateien haben die Signaturbytes „FF 4F FF 51“.

### Mime-Typen
Zu den registrierten Mime-Typen für JPEG 2000-Dateien gehören:
* Bild/j2c
* Bild/jpx
* Bild/jpm
* video/mj2

## Verbesserungen gegenüber dem JPEG-Standard
Zu den Verbesserungen gegenüber dem JPEG-Standard gehören:
* Überlegene Komprimierungsleistung
* Darstellung mit mehreren Auflösungen
* Progressive Übertragung nach Pixel und Auflösungsgenauigkeit
* Auswahl zwischen verlustfreier oder verlustbehafteter Komprimierung
* Fehlerresilienz, flexibles Dateiformat
* Unterstützung für hohen Dynamikbereich
* Räumliche Informationen des Seitenkanals

## Verweise ##
* [Taubmann, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

