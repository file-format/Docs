{
  "date" : "2019-10-11",
  "keywords" :[ "Exif-Datei", "Exif-Dateiformat", "Was ist eine Exif-Datei", "Datei", "Exif-Beispiel", "Exif-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Erfahren Sie mehr über das EXIF-Dateiformat und APIs, die EXIF-Dateien erstellen und öffnen können.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine EXIF-Datei?
EXIF steht für „Exchangeable Image File Format“, die Definition, die erstmals 1985 von der [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) gegeben wurde. Der Standard wird von Japan Electronics und verwaltet Information Technology Industries Association (JEITA) ab heute. EXIF ist ein Standard für die Spezifikationen von Bild- und Tonformaten, die hauptsächlich von Digitalkameras und Scannern verwendet werden.

Der EXIF-Standard schließt die Tagging- und Metadateninformationen mit der Bilddatei ein. Metadaten können Informationen wie Kameramodell, Verschlusszeit, Datum und Uhrzeit, Blende, Hersteller, Belichtungszeit, X-Auflösung, Y-Auflösung usw. enthalten. Normalerweise werden die EXIF-Daten standardmäßig ausgeblendet. Um die EXIF-Daten anzuzeigen, muss man die Ansichtseigenschaften in der Bildanzeigeanwendung auswählen. Exif-Metadaten können auch Miniaturansichten zusammen mit technischen und primären Bilddaten in einer einzigen Bilddatei enthalten.

## Geschichte und Versionen ##

* Im Oktober 1995 erstellte JEIDA Version 1. In dieser Version definierte JEIDA die Struktur, die aus Bilddatenformat und Attributinformationen sowie grundlegenden Tags besteht.
* Nov. 1997, Version 1.1 wurde mit den meisten Tags aus Version 1 eingeführt, aber auch mit zusätzlichen Bestimmungen für optionale Attributinformationen und Formatoperationen.
* Juni 1998, Version 2 mit sRGB-Farbraum, komprimierten Thumbnails und Audiodateien.
* Dezember 1998, Version 2.1 mit erweiterten Speicher- und Attributinformationen.
* Februar 2002, Version 2.2, verbesserte Version 2.1 mit zusätzlicher Druckweiterverarbeitung.
* September 2003, Version 2.21 mit optionalem Farbraum, bekannt als Adobe RGB.

## EXIF-Dateiformat

EXIF verwendet die folgenden Dateiformate mit dem Zusatz spezifischer Metadaten.

1. [JPEG](/de/image/jpeg/) - Diskrete Kosinustransformation (DCT) für komprimierte Bilddateien.
1. [TIFF](/de/image/tiff/) Rev. 6.0 (RGB oder YCbCr) für unkomprimierte Bilddateien.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) für Audiodateien (Linear [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) oder ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM für unkomprimierte Audiodaten und [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) für komprimierte Audiodaten).

### Von EXIF verwendeter Marker ###

Der Marker 0xFFE0~~0xFFEF ist "Anwendungsmarker", der von der Benutzeranwendung verwendet wird. Beispielsweise verwenden ältere Digitalkameras JFIF (JPEG File Interchange Format) zum Speichern von Bildern. JFIF verwendet den APP0 (0xFFE0) Marker zum Einfügen von Digitalkamera-Konfigurationsdaten und Miniaturbildern. Darüber hinaus verwendet EXIF auch einen Anwendungsmarker zum Einfügen von Daten, aber EXIF verwendet den APP1 (0xFFE1)-Marker, um einen Konflikt mit dem JFIF-Format zu vermeiden. Alle EXIF-Dateiformate beginnen mit diesem Format.


|SOI-Markierung|APP1-Markierung|APP1-Daten|Andere Markierung
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Es beginnt mit dem SOI (0xFFD8) Marker, also ist es eine JPEG-Datei. Dann folgt sofort APP1 Marker. Alle EXIF-Daten werden in diesem APP1-Datenbereich gespeichert. Der Teil „SSSS“ in der oberen Tabelle bedeutet die Größe des APP1-Datenbereichs (EXIF-Datenbereich). Bitte beachten Sie, dass die Größe "SSSS" auch die Größe des Deskriptors selbst beinhaltet. Nach dem „SSSS“ starten die APP1-Daten. Der erste Teil sind spezielle Daten zur Identifizierung, ob EXIF oder nicht, ASCII-Zeichen "EXIF" und 2 Bytes von 0x00 verwendet werden. Nach dem APP1-Markerbereich folgen die anderen JPEG-Marker.

### Exif-Datenstruktur ###

Eine grobe Struktur der EXIF-Daten (APP1) ist unten dargestellt. Wie oben besprochen, beginnen EXIF-Daten mit dem ASCII-Zeichen „EXIF“ und 2 Bytes von 0x00, dann folgen EXIF-Daten. EXIF verwendet das TIFF-Format zum Speichern von Daten.


|FFE1|APP1-Markierung
---|---|
|SSSS|APP1-Daten|APP1-Datengröße
|45786966 0000|Exif-Header
|49492A00 08000000|TIFF-Kopfzeile
|XXXX. . . .|IFD0 (Hauptbild)|Verzeichnis
|LLLLLLLL|Link zu IFD1
|XXXX. . . .|Datenbereich von IFD0
|XXXX. . . .|Exif SubIFD|Verzeichnis
|00000000|Ende des Links
|XXXX. . . .|Datenbereich von Exif SubIFD
|XXXX. . . .|IFD1(Miniaturbild)|Verzeichnis
|00000000|Ende des Links
|XXXX. . . .|Datenbereich von IFD1
|FFD8XXXX. . . XXXXFFD9|Miniaturbild

#### TIFF-Header ####

Der 8-Byte-Dateiheader [TIFF](/de/image/tiff/) enthält die folgenden Informationen:

`Bytes 0-1:` Die innerhalb der Datei verwendete Byte-Reihenfolge. Zulässige Werte sind: „II“ (4949.H) „MM“ (4D4D.H).

Im „II“-Format ist die Byte-Reihenfolge sowohl für 16-Bit- als auch für 32-Bit-Ganzzahlen immer vom niederwertigsten Byte zum höchstwertigen Byte. Dies wird als Little-Endian-Byte-Reihenfolge bezeichnet. Im „MM“-Format ist die Byte-Reihenfolge sowohl für 16-Bit- als auch für 32-Bit-Ganzzahlen immer von der höchstwertigen zur niederwertigsten. Dies wird Big-Endian-Byte-Reihenfolge genannt.

`Bytes 2-3:` Eine willkürliche, aber sorgfältig gewählte Zahl (42), die die Datei weiter als TIFF-Datei identifiziert. Die Byte-Reihenfolge hängt vom Wert der Bytes 0-1 ab.

`Bytes 4-7:` Der Offset (in Bytes) des ersten IFD. Das Verzeichnis kann sich an einer beliebigen Stelle in der Datei nach dem Header befinden, muss jedoch an einer Wortgrenze beginnen. Insbesondere kann ein Bilddateiverzeichnis den Bilddaten folgen, die es beschreibt. Leser müssen den Zeigern folgen, wo immer sie hinführen. Der Begriff Byte-Offset wird in diesem Dokument immer verwendet, um sich auf eine Position in Bezug auf den Anfang der TIFF-Datei zu beziehen. Das erste Byte der Datei hat einen Offset von 0.

#### Bilddateiverzeichnis ####

Ein IFD enthält Informationen über das Bild sowie Zeiger auf die eigentlichen Bilddaten. Es besteht aus einer 2-Byte-Zählung der Anzahl von Verzeichniseinträgen (dh der Anzahl von Feldern), gefolgt von einer Folge von 12-Byte-Feldeinträgen , gefolgt von einem 4-Byte-Offset des nächsten IFD (oder 0, wenn keine). Es muss mindestens 1 IFD in einer TIFF-Datei vorhanden sein und jedes IFD muss mindestens einen Eintrag haben.

##### IFD-Eintrag #####

Jeder 12-Byte-IFD-Eintrag hat das folgende Format.


|Bytes|Beschreibung
---|---|
|0-1|Das Tag, das das Feld identifiziert
|2-3|Der Feldtyp
|4-7|Zählung des angegebenen Typs
|8-11|Der Wert-Offset, der Datei-Offset (in Bytes) des Werts für das Feld. Der Wert soll an einer Wortgrenze beginnen; der entsprechende Value Offset ist somit eine gerade Zahl. Dieser Datei-Offset kann auf eine beliebige Stelle in der Datei zeigen, sogar nach den Bilddaten

Ein TIFF-Feld ist eine logische Einheit, die aus einem TIFF-Tag und seinem Wert besteht. Dieses logische Konzept wird als IFD-Eintrag implementiert, plus der tatsächliche Wert, falls er nicht in den Wert/Offset-Teil passt, die letzten 4 Bytes des IFD-Eintrags. Die Begriffe TIFF-Feld und IFD-Eintrag sind in den meisten Zusammenhängen austauschbar.

#### Vorschaubild ####

Das Exif-Format enthält ein Miniaturbild des Bildes (außer Ricoh RDC-300Z). Normalerweise befindet es sich neben dem IFD1. Es gibt 3 Formate für Miniaturansichten; JPEG-Format (JPEG verwendet YCbCr), RGB-TIFF-Format, YCbCr-TIFF-Format.

##### Miniaturbild im JPEG-Format #####

Wenn der Wert des Compression(0x0103)-Tags in IFD1 „6“ ist, ist das Miniaturbildformat JPEG. Die meisten Exif-Bilder verwenden das JPEG-Format für Miniaturansichten. In diesem Fall können Sie den Offset des Thumbnails durch das JpegIFOffset(0x0201)-Tag in IFD1, die Größe des Thumbnails durch das JpegIFByteCount(0x0202)-Tag erhalten. Das Datenformat ist das gewöhnliche JPEG-Format, beginnt bei 0xFFD8 und endet bei 0xFFD9. Es scheint, dass das JPEG-Format und eine Größe von 160 x 120 Pixel das empfohlene Thumbnail-Format für Exif2.1 oder höher sind.

##### Miniaturbild im TIFF-Format #####

Wenn der Wert des Compression(0x0103)-Tags in IFD1 „1“ ist, ist das Miniaturbildformat keine Komprimierung (TIFF-Bild genannt). Der Startpunkt der Thumbnail-Daten ist das StripOffset(0x0111)-Tag, die Größe des Thumbnails ist die Summe des StripByteCounts(0x0117)-Tags.

## Verweise ##

* [EXIF – von Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [EXIF-Dateiformat](https://www.media.mit.edu/pia/Research/deepview/exif.html)

