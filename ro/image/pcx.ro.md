{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PCX - Fișier imagine bitmap cu pensulă",
  "description":"Aflați despre formatul de fișier PCX și despre API-urile care pot crea și deschide fișiere PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Ce este un fișier PCX?

Un fișier PCX, fișier Picture Exchange, este un format de fișier imagine raster care a fost folosit ca format de fișier nativ pentru aplicația PC Paintbrush. A fost dezvoltat de ZSoft Corporation, SUA pentru platformele DOS și Windows și a fost adoptat ca principal format de fișier de imagine înainte de apariția [BMP](/ro/image/bmp/), [JPEG](/ro/image/jpeg/) și [ PNG](/ro/image/png/) formate de fișiere. Fișierele PCX au dimensiuni mai mici, deoarece sunt comprimate folosind codificarea RLE. Este utilizat în fișierul cu mai multe pagini [DCX](/ro/image/dcx/) care este utilizat în principal pentru a crea fișiere fax digitale.

## Format de fișier PCX

Fișierele PCX sunt salvate pe disc în format binar. Structura internă a formatului de fișier urmează ordinea little endian byte și are următoarele trei secțiuni:

**`PCX Header`** - Un antet PCX are 128 de octeți. Conține un identificator, un număr de versiune, dimensiunile imaginii, 16 culori ale paletei, numărul de planuri de culoare și adâncimea de biți a fiecărui plan și o valoare pentru metoda de compresie.

Antetul PCX este așa cum se arată mai jos, cu referințe din Enciclopedia formatelor de fișiere grafice (ed. a 2-a).
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

**`Date de imagine`** - Datele de imagine PCX urmează imediat după antet. Datele imaginii pot fi comprimate în funcție de setarea câmpului din antet. Stocarea datelor în fișierul PCX depinde de numărul de planuri de culoare specificate. Datele imaginii sunt organizate pe rânduri. În cazul mai multor planuri, acestea sunt stocate pe plan în rând, în aranjament secvenţial de date roşu, verde şi albastru. Acest model se repetă pentru fiecare linie din plan.

## Referințe

* [PCX - După Wikipedia](https://en.wikipedia.org/wiki/PCX)

