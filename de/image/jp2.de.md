{
  "date" : "2019-10-11",
  "keywords" :[ "jp2-Datei", "jp2-Dateiformat", "was ist eine jp2-Datei", "Datei", "jp2-Beispiel", "jp2-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Bilddateiformat",
  "description":"Erfahren Sie mehr über das JP2-Dateiformat und APIs, die JP2-Dateien erstellen und öffnen können.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Was ist eine JP2-Datei? ##

JPEG 2000 (**JP2**) ist ein Bildkodierungssystem und modernster Bildkomprimierungsstandard. Es verwendet die Wavelet-Technologie, um verlustfreie Inhalte in beliebiger Qualität auf einmal zu kodieren. Darüber hinaus hat JPEG 2000 ohne wesentliche Einbußen bei der Codierungseffizienz die Fähigkeit, auf denselben Inhalt zuzugreifen und ihn effizient in eine Vielzahl anderer Auflösungen und Qualitäten zu decodieren. Die Codeströme in JPEG 2000 sind erheblich skalierbar, da sie interessierende Regionen aufweisen, die die Möglichkeit für einen räumlichen Direktzugriff bereitstellen.

JPEG 2000 zeichnet sich als einer der am besten skalierbaren Standards aus. Verschiedene Teile eines Bildes können mit unterschiedlichen Qualitäten gespeichert werden. Eine bemerkenswerte Leistungssteigerung kann erreicht werden, indem der Codestrom auf verschiedene Arten geordnet wird. Nichtsdestotrotz erfordert JP2 als Ergebnis dieser Flexibilität komplexe und rechentechnisch anspruchsvolle Codierer/Decoder. Im Vergleich zu JPEG erzeugt JPEG 2000 nur Klingelartefakte, die Ringe in der Nähe des Bildrands erzeugen und verschwommen sein können, während JPEG 8 × 8-Blöcke für visuelle Artefakte verwendet, die sowohl Klingel- als auch Blockartefakte sein können. Besitzt bis zu 16384 verschiedene Komponenten mit Abmessungen in Terapixel und einer Genauigkeit, die bis zu 38 Bit/Sample betragen kann.

## Geschichte ##

Im Jahr 2000 entwarf das Komitee der Joint Photographic Experts Group JP2 mit dem Ziel, ihren eigenen, auf der diskreten Kosinustransformation basierenden JPEG-Standard mit dieser neuen Wavelet-basierten Methode zu verbessern. Das JPEG-Komitee wollte seine Basismethoden lizenzgebührenfrei zur Verfügung stellen. Im JP2-Lizenzwettbewerb unter 20 Unternehmen gewannen sie mit knapper Mehrheit. JPEG 2000 wurde zum ISO-Standard erklärt, obwohl die meisten Webbrowser seit 2017 nicht bereit sind, JPEG 2000 zu unterstützen.

## Teile des Bildkodierungssystems JPEG 2000 ##

Im Folgenden sind die Hauptteile aufgeführt, die die vollständige Suite von Standards für JPEG 2000 bilden.


|Teil|Titel|Beschreibung|Nummer
---|---|---|---|
|Teil 1|Kerncodierungssystem| Definiert die Syntax des Codestreams. Verschiedene Phasen beim Decodieren von JPEG 2000-Bildern. Erläutert das grundlegende Dateiformat JP2, Metadaten und bereitzustellende IP-Rechte.|ISO/IEC 15444-1
|Teil 2|Erweiterungen|Definiert Erweiterungen für den Dateiformat-Codestream und ermöglicht HDR-Beispieldemonstrationen, Farbraumspezifikation, Zuschneiden, geometrische Transformationen; diverse Animationen, Metadaten und mehrere Codestreams.|ISO/IEC 15444-2
|Teil 3|Motion JPEG 2000 (MJ2 oder MJP2)|Führen Sie ein Dateiformat für Bewegungssequenzen ein, das Bilder in einem unabhängigen Codestrom kodiert.|ISO/IEC 15444-3
|Teil 4|Konformität|Beschreibt Testtechniken zum Kodieren und Dekodieren und prüft Dateien sowohl auf Bare-Code-Streams als auch auf JP2-Dateien.|ISO/IEC 15444-4
|Teil 5|Referenzsoftware|Besteht aus zwei Quellcodepaketen (Java, C), die das Core-Codierungssystem implementieren und unter Open-Source-Lizenzen verfügbar sind.|ISO/IEC 15444-5
|Teil 6|Zusammengesetztes Bilddateiformat|Definiert das JPM-Dateiformat und ermöglicht mehrseitiges Dokument-Imaging für faxähnliche Anwendungen. Unterstützt die Verwendung von JBIG2 und JPEG.|ISO/IEC 15444-6
|Teil 8|JPEG 2000 Secured (JPSEC)|Gewährleistet die Sicherheit von Transaktionen, Inhalten und Technologien und ermöglicht gesicherte JPEG 2000-Bitströme.|ISO/IEC 15444-8
|Teil 9|JPIP|Definiert Tools in einer vernetzten Umgebung für den Zugriff auf Metadaten und Bilder und gibt interaktive und effiziente Protokolle an|ISO/IEC 15444-9
|Teil 10|JP3D|Volumetrische Erweiterung von Teil 1 und führt die Z-Dimension ein. Erweitert das Konzept von Kacheln, Codeblöcken, Bezirken und 3D-Region-of-Interest-Barrierefreiheitsfunktionen.|ISO/IEC 15444-10
|Teil 11|JPWL|Befasst sich mit gut organisierter Übertragung über ein fehleranfälliges drahtloses Netzwerk. Diese Erweiterung ist kompatibel mit Decodern|ISO/IEC 15444-11
|Teil 13|Encoder der Einstiegsklasse|Definiert eine Encoder-Implementierung der Einstiegsklasse des Core-Codierungssystems.|ISO/IEC 15444-13
|Teil 14|JPXML|Eine Darstellung in XML und erläutert Markierungssegmente und Methoden für den Zugriff auf die internen Daten von Bilddaten.|ISO/IEC 15444-14
|Teil 15|HTJ2K (in Entwicklung)|Spezifiziert einen alternativen Blockcodierungsalgorithmus. Der Algorithmus bietet einen zehnfach erhöhten Durchsatz und verlustfreie Codierung/Decodierung.|

## JP2-Dateiformat ##

JPEG 2000 definiert das Dateiformat sowie den Codestrom auf die gleiche Weise wie JPEG-1. Obwohl Bildbeispiele ausschließlich von JPEG 2000 beschrieben werden, enthält JPEG-1 andere zusätzliche Informationen über den Farbraum und die Auflösung, die für die Codierung des Bildes unerlässlich sind. Wird ein Bild als JPEG 2000-Datei gespeichert, wird als Endung **.jp2** verwendet. Dieses Dateiformat wird durch die JPEG 2000 Teil-2-Erweiterung weiter verbessert, die Animationsmechanismen und die Konfiguration zahlreicher Codeströme in einem einzigen Bild definiert. Die Erweiterung **.jpx** wird verwendet, wenn Bilder in diesem erweiterten Dateiformat gespeichert werden. Da Codestream-Daten nicht primär in Dateien gespeichert werden, ist für diesen Zweck keine Standarderweiterung definiert. Zu Testzwecken erhält es jedoch häufig die Erweiterung **.jpc** oder **.j2k**. Im Gegensatz zu JPEG-1 wählt JPEG 2000 eine andere Art der Codierung von Metadaten im XML-Format. Als Referenz zwischen den Exif-Tags und den XML-Komponenten wird der Standard 12234-1.4 (vom ISO TC42-Komitee) verwendet. JPEG 2000 kann einen ISO-Standard enthalten, darin XMP.

### Brocken ###
JPEG 2000-Dateien bestehen aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header: 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst) und 4-Byte-Chunk-Typ – eine der vordefinierten Signaturen: „jP“ oder „jP2“.

Der zweite Chunk muss vom Typ „ftyp“ sein und hat einen Untertyp bei Offset 8. JPEG 2000 definiert durch den Untertyp, der einer der folgenden Werte sein muss: „jp2“ (Dateityp \*.JP2), „jp20“ (file Typ \*.JPA), "jpm " (Dateityp \*.JPM), "jpx " (Dateityp \*.JPX).

Iterierende Chunks, bis ein unbekannter Typ erkannt wird, erstellen wir eine JPEG 2000-Bild-/Videodatei.

### Farbtransformation ###

Zunächst ist die Transformation von Bildern aus dem RGB-Farbraum in einen anderen Farbraum erforderlich. Dazu gibt es zwei Möglichkeiten: Irreversible Color Transform (ICT) und Reversible Color Transform (RCT). Ersteres verwendet YC,,B,,C,,R,, Farbraum und muss in Fix/Gleitkomma implementiert werden, während später ein modifizierter YUV-Farbraum und von Natur aus umkehrbar ist.// //Nicht auf RGB-Modell, JPEG beschränkt 2000-Sprache verwendet die Transformation mehrerer Komponenten.

### Fliesen ###

Wenn die Farbtransformation abgeschlossen ist, wird das Bild in rechteckige Bereiche umgewandelt, die als Kacheln bezeichnet werden und separat transformiert und codiert werden können. Die Größe aller Kacheln ist gleich oder das gesamte Bild kann als eine einzelne Kachel betrachtet werden. Der Decoder nutzt die Vorteile der Kachelung und verbraucht weniger Speicher oder kann einige Kacheln teilweise codieren. Obwohl diese Technik einen Nachteil der Qualitätsverschlechterung des Bildes hat.

### Wavelet-Transformation ###

Das Bild nach dem Kacheln ist eine Wavelet-Transformation, die entweder irreversibel oder reversibel sein kann und unter Verwendung des Faltungs- oder Lifting-Schemas implementiert wird.

### Kompressionsrate ###

Abhängig von den physikalischen Eigenschaften eines Bildes wird ein Komprimierungsgewinn von 20 % erzielt. Die räumliche Redundanzvorhersage von JPEG 2000 spielt eine wichtige Rolle im Komprimierungsprozess, und Bilder mit hoher Auflösung erzielen tendenziell den größten Vorteil.

## Vom Standard bediente Anwendungen ##

* Aufnahme, Bearbeitung und Speicherung von Frame-basierten HD-Videos
* Medizinische Bilder und Biometrie
* Satellitenbilder, Fernerkundung und Bewegungserkennung
* Client/Server-Kommunikation, Netzwerkverteilung und -speicherung.
* Digitales Kino, Live-HDTV-Feed-Beitrag, digitalisiertes audiovisuelles Material

## Verweise ##

* [Überblick über JPEG 2000](https://jpeg.org/jpeg2000)
* [JPEG 2000-Bildkodierungssystem](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

