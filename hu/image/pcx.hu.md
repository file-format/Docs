{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX fájlformátum - ecset bittérképes képfájl",
  "description":"További információ a PCX fájlformátumról és az API-król, amelyek PCX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Mi az a PCX fájl?

A PCX fájl, a Picture Exchange fájl, egy raszteres képfájl formátum, amelyet a PC Paintbrush alkalmazás natív fájlformátumaként használtak. A ZSoft Corporation (USA) fejlesztette ki DOS- és Windows-platformokra, és a [BMP](/hu/image/bmp/), [JPEG](/hu/image/jpeg/) és [ PNG](/hu/image/png/) fájlformátumok. A PCX fájlok kisebb méretűek, mivel RLE kódolással vannak tömörítve. A többoldalas [DCX](/hu/image/dcx/) fájlban használatos, amelyet elsősorban digitális faxfájlok létrehozására használnak.

## PCX fájlformátum

A PCX fájlok bináris fájlformátumban kerülnek a lemezre. A belső fájlformátum szerkezete a kis végi bájtok sorrendjét követi, és a következő három részből áll:

**`PCX fejléc`** – A PCX fejléc 128 bájt hosszú. Tartalmaz egy azonosítót, egy verziószámot, a kép méreteit, 16 palettaszínt, minden sík színsíkját és bitmélységét, valamint egy értéket a tömörítési módszerhez.

A PCX fejléc az alábbiakban látható, hivatkozással az Encyclopedia of Grafikai fájlformátumokból (2. kiadás).
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

**`Képadatok`** - A PCX képadatok közvetlenül a fejléc után következnek. A képadatokat a fejléc mezőbeállításától függően tömöríthetjük. Az adatok tárolása a PCX fájlban a megadott színsíkok számától függ. A képadatok sorokba vannak rendezve. Több sík esetén ezeket síkonként, soron belül tárolja a piros, zöld és kék adatok egymás utáni elrendezésében. Ez a minta megismétlődik a sík minden soránál.

## Hivatkozások

* [PCX – a Wikipedia által](https://en.wikipedia.org/wiki/PCX)

