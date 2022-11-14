{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX-bestandsindeling - Paintbrush Bitmap-afbeeldingsbestand",
  "description":"Meer informatie over PCX-bestandsindelingen en API's die PCX-bestanden kunnen maken en openen.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Wat is een PCX-bestand?

Een PCX-bestand, Picture Exchange-bestand, is een rasterafbeeldingsbestandsformaat dat werd gebruikt als native bestandsformaat voor de PC Paintbrush-toepassing. Het werd ontwikkeld door ZSoft Corporation, VS voor DOS- en Windows-platforms en werd aangenomen als het belangrijkste beeldbestandsformaat vóór de komst van [BMP](/nl/image/bmp/), [JPEG](/nl/image/jpeg/) en [ PNG](/nl/image/png/) bestandsindelingen. PCX-bestanden zijn kleiner omdat ze worden gecomprimeerd met behulp van de RLE-codering. Het wordt gebruikt in het [DCX](/nl/image/dcx/)-bestand met meerdere pagina's dat voornamelijk wordt gebruikt om digitale faxbestanden te maken.

## PCX-bestandsindeling

PCX-bestanden worden in binaire bestandsindeling op schijf opgeslagen. De structuur van de interne bestandsindeling volgt de kleine endian-bytevolgorde en heeft de volgende drie secties:

**`PCX-header`** - Een PCX-header is 128 bytes lang. Het bevat een identificatie, een versienummer, afbeeldingsafmetingen, 16 paletkleuren, nummerkleurvlakken en bitdiepte van elk vlak, en een waarde voor de compressiemethode.

PCX Header is zoals hieronder getoond met verwijzing uit Encyclopedia of graphic file formats (2e ed.).
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

**`Beeldgegevens`** - PCX-beeldgegevens volgen net na de kop. De afbeeldingsgegevens kunnen worden gecomprimeerd, afhankelijk van de lokale instelling in de koptekst. De opslag van gegevens in het PCX-bestand is afhankelijk van het aantal gespecificeerde kleurvlakken. Afbeeldingsgegevens zijn in rijen georganiseerd. In het geval van meerdere vlakken, worden deze per vlak binnen een rij opgeslagen in sequentiële rangschikking van rode, groene en blauwe gegevens. Dit patroon wordt herhaald voor elke lijn in het vlak.

## Referenties

* [PCX - Door Wikipedia](https://en.wikipedia.org/wiki/PCX)

