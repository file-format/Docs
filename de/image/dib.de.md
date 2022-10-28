{
  "date" : "2020-01-10",
  "keywords" :[ "dib-Datei", "dib-Dateiformat", "was ist eine dib-Datei", "Datei", "dib-Beispiel", "dib-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Erfahren Sie mehr über das DIB-Dateiformat und APIs, die DIB-Dateien erstellen und öffnen können.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Was ist eine DIB-Datei?

Eine geräteunabhängige Bitmap (DIB) ist eine Rasterbilddatei, die in ihrer Struktur den standardmäßigen Bitmap-Dateien ([BMP]()/image/bmp/)) ähnelt. Es enthält eine Farbtabelle, die die Zuordnung von RGB-Farben zu den Pixelwerten beschreibt. Dadurch kann DIB Bilder auf jedem Gerät darstellen. Es kann mit fast allen Anwendungen geöffnet werden, die eine Standard-BMP-Datei sowohl unter Windows als auch unter macOS öffnen können. DIB sind Binärdateien und haben ein komplexes Dateiformat ähnlich wie BMP. DIB-Bilder sind in Bezug auf Farbtiefe und Pixel pro Zoll unabhängig von den Ausgabefähigkeiten der Wiedergabegeräte.

## Spezifikationen des DIB-Dateiformats ##
Eine DIB enthält die folgenden Farb- und Dimensionsinformationen:

* Das Farbformat des Geräts, auf dem das rechteckige Bild erstellt wurde.
* Die Auflösung des Geräts, auf dem das rechteckige Bild erstellt wurde.
* Die Palette für das Gerät, auf dem das Bild erstellt wurde.
* Ein Array von Bits, das rote, grüne, blaue ( RGB ) Tripletts auf Pixel im rechteckigen Bild abbildet.
* Eine Datenkomprimierungskennung, die das Datenkomprimierungsschema (falls vorhanden) angibt, das verwendet wird, um die Größe des Bitarrays zu reduzieren.

### DIB-Datenblockformat ###

DIB steht im Vergleich zu .DIB-Dateien, die auf Datenträgern gespeichert sind, im Zusammenhang mit Speicherblöcken. Der Speicherblock weist eine Struktur auf, die den Windows-API-Spezifikationen für DIBs entspricht. Die aktuelle DIB besteht aus:
* Eine Überschrift
* Farbpalette
* Pixeldaten

Praktisch wird mit Paletten-, Header- und Bilddaten so gearbeitet, als wären sie drei separate Speicherblöcke. Ein Handle für diesen gemeinsamen Speicherblock wird mithilfe von GlobalAlloc zugewiesen und ist als HDIB bekannt, das zum Extrahieren und Arbeiten mit Header-, Farbtabellen- und Pixeldaten verwendet wird.

### Strukturen ###
Informationen, die in einer DIB enthalten sind, werden durch verschiedene Strukturen dargestellt. Diese beinhalten:

BITMAPInfo – Definiert die Dimensions- und Farbinformationen für DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Es besteht aus einem BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
gefolgt von zwei oder mehr RGBQAD-Strukturen.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Daten Bits ###
|Bits|Beschreibung|
---|---|
|1-Bit-Format (monochrom)|Monochrom-Bitmaps bestehen aus zwei Farben (schwarz und weiß). Aufgrund dieser begrenzten Anzahl von Farben nehmen diese Bitmaps weniger Platz auf der Disc ein. Der bitBitCount gibt wahr oder falsch für die Darstellung beider Farben zurück. Die meisten Anwendungen überspringen die Palette vollständig, wenn bitBitCount==1.
|4-Bit-Format (VGA oder 16 Farben)|Jedes Byte Bilddaten repräsentiert zwei Pixel und bitBitCount==4. Diese Bits repräsentieren die Farbe des Pixels in absteigender Reihenfolge.
|8-Bit-Format (256 Farben)|Dieses 8-Bit-Format kann maximal 256 Farben darstellen. Jedes Byte im Bitmap-Datenarray des Bildes repräsentiert ein einzelnes Pixel. Der Wert dieses Bytes ist die Nummer des zu verwendenden Farbpaletteneintrags aus den 256 Einträgen, wie sie durch bmciColors dargestellt werden.
|24-Bit-Format (TrueColor)|Diese Bitmaps können maximal 2^24 Farben haben (biBitCount == 24). Jede Drei-Byte-Sequenz im Bitmap-Datenarray repräsentiert die relativen Intensitäten der drei primären Farbtöne eines Pixels. Die Farbtöne werden als Werte im Bereich von 0 bis 255 beschrieben und in den drei Bytes in der Reihenfolge Blau, Grün und Rot gespeichert. Dies ist ein wichtiger Unterschied, da die meisten Verweise auf Farben in Windows die entgegengesetzte Reihenfolge verwenden: Rot/Grün/Blau, also denken Sie an „BGR“, wenn Sie mit TrueColor-Bildern arbeiten, anstatt an „RGB“. Eine Farbpalette kann angegeben werden, um den Zeichenprozess für Windows zu beschleunigen, in diesem Fall wird biClrUsed nicht 0 sein. Aber wie Sie sehen können, wird es nicht benötigt, da die Pixeldaten selbst die Farbinformationen enthalten.
|32-Bit-Format|32-Bit-Bilder haben maximal 2^24 Farben (biBitCount == 24).

## Verweise ##
* [Geräteunabhängige Bitmaps – von Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

