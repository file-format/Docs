{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX-Dateiformat - Paintbrush-Bitmap-Bilddatei",
  "description":"Erfahren Sie mehr über das PCX-Dateiformat und APIs, die PCX-Dateien erstellen und öffnen können.",
  "linktitle" :"PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Was ist eine PCX-Datei?

Eine PCX-Datei, Picture Exchange-Datei, ist ein Rasterbilddateiformat, das als natives Dateiformat für die Anwendung PC Paintbrush verwendet wurde. Es wurde von der ZSoft Corporation, USA, für DOS- und Windows-Plattformen entwickelt und vor der Einführung von [BMP](/de/image/bmp/), [JPEG](/de/image/jpeg/) und [ PNG](/de/image/png/) Dateiformate. PCX-Dateien sind kleiner, da sie mit der RLE-Codierung komprimiert werden. Es wird in der mehrseitigen Datei [DCX](/de/image/dcx/) verwendet, die hauptsächlich zum Erstellen digitaler Faxdateien verwendet wird.

## PCX-Dateiformat

PCX-Dateien werden im Binärdateiformat auf der Disc gespeichert. Die interne Dateiformatstruktur folgt der Little-Endian-Byte-Reihenfolge und besteht aus den folgenden drei Abschnitten:

**`PCX-Header`** - Ein PCX-Header ist 128 Byte lang. Es enthält eine Kennung, eine Versionsnummer, Bildabmessungen, 16 Palettenfarben, die Anzahl der Farbebenen und die Bittiefe jeder Ebene sowie einen Wert für das Komprimierungsverfahren.

Der PCX-Header ist wie unten gezeigt unter Bezugnahme auf die Encyclopedia of Graphics File Formats (2. Aufl.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Bilddaten`** - PCX-Bilddaten folgen direkt nach dem Header. Die Bilddaten können je nach Feldeinstellung im Header komprimiert werden. Die Speicherung von Daten in der PCX-Datei hängt von der Anzahl der angegebenen Farbebenen ab. Bilddaten sind in Zeilen organisiert. Im Falle mehrerer Ebenen werden diese nach Ebene innerhalb einer Reihe in sequentieller Anordnung von Rot-, Grün- und Blaudaten gespeichert. Dieses Muster wird für jede Linie in der Ebene wiederholt.

## Verweise

* [PCX – von Wikipedia](https://en.wikipedia.org/wiki/PCX)

