{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX-filformat - Paintbrush Bitmap Image File",
  "description":"Läs mer om PCX-filformat och API:er som kan skapa och öppna PCX-filer.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Vad är en PCX fil?

En PCX-fil, Picture Exchange-fil, är ett rasterbildsfilformat som användes som inbyggt filformat för PC Paintbrush-applikationen. Det utvecklades av ZSoft Corporation, USA för DOS- och Windows-plattformar och antogs som det huvudsakliga bildfilformatet före ankomsten av [BMP](/sv/image/bmp/), [JPEG](/sv/image/jpeg/) och [ PNG](/sv/image/png/) filformat. PCX-filer är mindre i storlek eftersom de komprimeras med RLE-kodning. Den används i den flersidiga [DCX](/sv/image/dcx/)-filen som främst används för att skapa digitala faxfiler.

## PCX filformat

PCX-filer sparas på skiva i binärt filformat. Den interna filformatstrukturen följer little endian byte-ordning och har följande tre sektioner:

**`PCX Header`** - En PCX Header är 128 byte lång. Den innehåller en identifierare, ett versionsnummer, bilddimensioner, 16 palettfärger, antal färgplan och bitdjup för varje plan och ett värde för komprimeringsmetod.

PCX Header är som visas nedan med referens från Encyclopedia of graphics filformat (andra upplagan).
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

**`Bilddata`** - PCX-bilddata följer strax efter rubriken. Bilddata kan komprimeras beroende på fältinställningen i rubriken. Lagringen av data i PCX-filen beror på antalet specificerade färgplan. Bilddata är organiserad i rader. I fallet med flera plan, lagras dessa plan inom rad i sekventiellt arrangemang av röd, grön och blå data. Detta mönster upprepas för varje linje i planet.

## Referenser

* [PCX - av Wikipedia](https://en.wikipedia.org/wiki/PCX)

