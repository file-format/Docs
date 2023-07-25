{
  "date" : "2019-10-11",
  "keywords" :[ "bmp-Datei", "bmp-Dateiformat", "was ist eine bmp-Datei", "Datei", "bmp-Beispiel", "bmp-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Bilddateiformat",
  "description":"Erfahren Sie mehr über das BMP-Dateiformat und APIs, die BMP-Dateien erstellen und öffnen können.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Was ist eine BMP-Datei? #

Dateien mit der Erweiterung .BMP stellen Bitmap-Bilddateien dar, die zum Speichern digitaler Bitmap-Bilder verwendet werden. Diese Bilder sind grafikadapterunabhängig und werden auch als DIB-Dateiformat (Device Independent Bitmap) bezeichnet. Diese Unabhängigkeit dient dem Zweck, die Datei auf mehreren Plattformen wie Microsoft Windows und Mac zu öffnen. Das BMP-Dateiformat kann Daten als zweidimensionale digitale Bilder sowohl im Monochrom- als auch im Farbformat mit verschiedenen Farbtiefen speichern.

## Spezifikationen des BMP-Dateiformats ##

Geräteunabhängige Bitmaps dienen als Hilfsmittel zum Austausch von Bitmaps zwischen Geräten und Anwendungen. Aufgrund der ständigen Weiterentwicklung dieses Dateiformats können die in den Kopfzeilen enthaltenen Informationen je nach Version von Bitmap unterschiedlich sein. Eine einzelne Bitmap-Datei besteht aus Strukturen mit fester sowie variabler Größe in einer bestimmten Reihenfolge.

Strukturen in einer Bitmap-Datei sind in der folgenden Reihenfolge angeordnet:


|Struktur|Optional|Größe|Zweck
---|---|---|---|
|Datei-Header|Nein|14|Zum Speichern allgemeiner Informationen über die Bitmap-Bilddatei
|DIB Header|No|Fixed-Size|Zum Speichern detaillierter Informationen über das Bitmap-Bild und zum Definieren des Pixelformats
|Zusätzliche Bitmasken|Ja|12 oder 16 Bytes|Um das Pixelformat zu definieren
|Farbpalette|Semi-optional|Variable Größe|Zur Definition von Farben, die von den Bitmap-Bilddaten verwendet werden
|Gap1|Yes|Variable-size|Strukturausrichtung
|Pixel-Array|Nein|Variable-Größe|Das Pixelformat wird durch den DIB-Header oder zusätzliche Bitmasken definiert.
|Gap2|Yes|Variable-size|Strukturausrichtung
|ICC-Farbprofil|Ja|Variable Größe|Um das Farbprofil für das Farbmanagement zu definieren

Wenn ein Bitmap-Bild in den Speicher geladen wird, wird es zu einer DIB-Struktur, die von Windows über seine GDI-API verwendet wird. Der Dateikopf ist nicht Teil dieser Datenstruktur. Die Farbe kann statt aus expliziten RGB-Farbdefinitionen auch aus 16-Bit-Einträgen bestehen, die Indizes für die aktuell referenzierte Palette darstellen. Schauen wir uns einige davon im Detail an, insbesondere die Kopfzeilen.

### Kopfzeile der Bitmap-Datei ###

Ein Bitmap-Datei-Header ähnelt anderen Datei-Headern, die zum Identifizieren der Datei verwendet werden. Da es verschiedene Varianten des BMP-Dateiformats gibt, sind die ersten 2 Bytes des BMP-Dateiformats das Zeichen „B“ und dann das Zeichen „M“ in der ASCII-Codierung. Alle Integer-Werte werden im Little-Endian-Format gespeichert.

|Offset Hex|Offset Dez|Größe|Zweck
---|---|---|---|
|00|0|2 Bytes|Das Header-Feld, das verwendet wird, um die BMP- und DIB-Datei zu identifizieren, ist 0x42 0x4D in Hexadezimal, dasselbe wie BM in ASCII. Es kann folgende mögliche Werte haben.* **BM** – Windows 3.1x, 95, NT, ... usw. * **BA** – OS/2-Struct-Bitmap-Array * **CI** – OS/2-Struct Farbsymbol * **CP** – OS/2 konstanter Farbzeiger * **IC** – OS/2 Struktursymbol * **PT** – OS/2 Zeiger
|02|2|4 Byte|Die Größe der BMP-Datei in Byte
|06|6|2 Bytes|Reserviert; Der tatsächliche Wert hängt von der Anwendung ab, die das Bild erstellt
|08|8|2 Bytes|Reserviert; Der tatsächliche Wert hängt von der Anwendung ab, die das Bild erstellt
|0A|10|4 Bytes|Der Offset, dh die Startadresse, des Bytes, in dem die Bitmap-Bilddaten (Pixel-Array) zu finden sind.

#### DIB-Header (Bitmap-Informationsheader) ####

Die detaillierten Informationen über das Bild werden durch diesen Header dargestellt. Basierend auf diesen Informationen wird die Anwendung bestimmt, die verwendet wird, um das Bild auf dem Bildschirm anzuzeigen. Alle diese Header enthalten ein DWORD-Feld (32 Bit), das ihre Größe angibt, sodass eine Anwendung den im Bild verwendeten Header leicht ermitteln kann. Dies liegt im Wesentlichen daran, dass das DIB-Format mehrfach erweitert wurde. Es folgt der DIB-Header mit aufgelisteten Feldern.

#### Farbpalette ####

Eine BMP-Farbpalette ist ein Array von Strukturen, die die RGB-Intensitätswerte jeder Farbe in der Farbpalette eines Anzeigegeräts angeben. Jedes Pixel in den Bitmap-Daten speichert einen einzelnen Wert, der als Index in der Farbpalette verwendet wird. Die im Element an diesem Index gespeicherten Farbinformationen geben die Farbe dieses Pixels an. Die Verfügbarkeit von Farbe in einer Bitmap-Datei variiert wie folgt:

* Ein-, 4- und 8-Bit – enthalten voraussichtlich immer eine Farbpalette
* Sechzehn, 24 und 32 Bit – enthalten niemals Farbpaletten
* Sechzehn- und 32-Bit-BMP-Dateien - enthalten Bitfeld-Maskenwerte anstelle der Farbpalette

#### Pixelspeicher ####

Bitmap-Pixel werden als in Zeilen gepackte Bits gespeichert, wobei die Größe jeder Zeile durch Auffüllen auf ein Vielfaches von 4 Bytes (ein 32-Bit-DWORD) aufgerundet wird. Die Gesamtmenge an Bytes, die zum Speichern der Pixel eines Bildes erforderlich sind, kann nicht direkt durch einfaches Zählen der Bits berechnet werden. Da ein Auffüllen beteiligt ist, ist der Effekt des Aufrundens der Größe jeder Zeile auf ein Vielfaches von 4 Bytes erforderlich. Am Ende der Zeilen sind Füllbytes (nicht zwingend 0) anzuhängen, um die Länge der Zeilen auf ein Vielfaches von vier Bytes zu bringen. Wenn das Pixelarray in den Speicher geladen wird, muss jede Zeile an einer Speicheradresse beginnen, die ein Vielfaches von 4 ist.

Das Bild wird tatsächlich durch die 32-Bit-DWORDs-Darstellung des Pixelarrays beschrieben. Normalerweise werden Pixel "von unten nach oben" gespeichert, beginnend in der unteren linken Ecke, von links nach rechts und dann Reihe für Reihe von unten nach oben im Bild. Pixelformate und ihre Auswirkungen sind unten aufgeführt:

* Das 1-Bit-pro-Pixel-Format (1 bpp) unterstützt zwei unterschiedliche Farben (z. B. Schwarz und Weiß).
* Das 2-Bit-pro-Pixel-Format (2bpp) unterstützt 4 verschiedene Farben und speichert 4 Pixel pro 1 Byte, wobei das Pixel ganz links in den beiden höchstwertigen Bits liegt. Jeder Pixelwert ist ein 2-Bit-Index in eine Tabelle mit bis zu 4 Farben.
* Das 4-Bit-pro-Pixel-Format (4 bpp) unterstützt 16 verschiedene Farben und speichert 2 Pixel pro 1 Byte, wobei sich das Pixel ganz links im höherwertigen Halbbyte befindet. Jeder Pixelwert ist ein 4-Bit-Index in eine Tabelle mit bis zu 16 Farben.
* Das 8-Bit-pro-Pixel-Format (8 bpp) unterstützt 256 verschiedene Farben und speichert 1 Pixel pro 1 Byte. Jedes Byte ist ein Index in eine Tabelle mit bis zu 256 Farben.
* Das 16-Bit-pro-Pixel-Format (16 bpp) unterstützt 65536 verschiedene Farben und speichert 1 Pixel pro 2-Byte-WORD. Jedes WORT kann die Alpha-, Rot-, Grün- und Blau-Abtastwerte des Pixels definieren.
* Das 24-Bit-Pixelformat (24 bpp) unterstützt 16.777.216 verschiedene Farben und speichert 1 Pixelwert pro 3 Bytes. Jeder Pixelwert definiert die roten, grünen und blauen Samples des Pixels (8.8.8.0.0 in RGBAX-Notation). Genauer gesagt in der Reihenfolge: Blau, Grün und Rot (8 Bits pro Abtastung).
* Das 32-Bit-pro-Pixel-Format (32 bpp) unterstützt 4.294.967.296 verschiedene Farben und speichert 1 Pixel pro 4-Byte-DWORD. Jedes DWORD kann die Alpha-, Rot-, Grün- und Blauproben des Pixels definieren.

## Verweise ##

* [Windows MetaFile-Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP-Dateiformat](https://en.wikipedia.org/wiki/BMP_file_format)

