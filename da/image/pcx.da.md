{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCX-filformat - Paintbrush Bitmap-billedfil",
  "description": "Lær om PCX-filformat og API'er, der kan oprette og åbne PCX-filer.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-dax"
}
},
  "lastmod": "2022-03-16"
}

## Hvad er en PCX fil?

En PCX-fil, Picture Exchange-fil, er et rasterbilledfilformat, der blev brugt som native filformat til PC Paintbrush-applikationen. Det blev udviklet af ZSoft Corporation, USA til DOS- og Windows-platforme og blev brugt som det primære billedfilformat før ankomsten af filformaterne [BMP](/image/bmp/), [JPEG](/image/jpeg/) og [PNG](/image/png/). PCX-filer er mindre i størrelse, da de komprimeres ved hjælp af RLE-kodning. Det bruges i den flersidede [DCX](/image/dcx/)-fil, der primært bruges til at oprette digitale faxfiler.

## PCX filformat

PCX-filer gemmes på disk i binært filformat. Den interne filformatstruktur følger lille endian byte-rækkefølge og har følgende tre sektioner:

**`PCX Header`** - En PCX Header er 128 bytes lang. Den indeholder en identifikator, et versionsnummer, billeddimensioner, 16 paletfarver, talfarveplaner og bitdybde for hvert plan og en værdi for komprimeringsmetoden.

PCX Header er som vist nedenfor med reference fra Encyclopedia of graphics filformater (2. udgave).
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

**`Billeddata`** - PCX-billeddata følger lige efter overskriften. Billeddataene kan blive komprimeret afhængigt af feltindstillingen i overskriften. Lagringen af data i PCX-filen afhænger af antallet af specificerede farveplaner. Billeddata er organiseret i rækker. I tilfælde af flere fly gemmes disse efter plan inden for række i sekventielt arrangement af røde, grønne og blå data. Dette mønster gentages for hver linje i planet.

## Referencer

* [PCX - af Wikipedia](https://en.wikipedia.org/wiki/PCX)


