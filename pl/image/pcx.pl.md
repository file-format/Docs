{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku PCX - Plik obrazu bitmapowego pędzla",
  "description":"Poznaj format plików PCX i interfejsy API, które mogą tworzyć i otwierać pliki PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Czym jest plik PCX?

Plik PCX, plik Picture Exchange, to format pliku obrazu rastrowego, który był używany jako natywny format pliku dla aplikacji PC Paintbrush. Został opracowany przez firmę ZSoft Corporation w USA dla platform DOS i Windows i został przyjęty jako główny format plików graficznych przed pojawieniem się formatów [BMP](/pl/image/bmp/), [JPEG](/pl/image/jpeg/) i [ PNG](/pl/image/png/). Pliki PCX są mniejsze, ponieważ są kompresowane przy użyciu kodowania RLE. Jest używany w wielostronicowym pliku [DCX](/pl/image/dcx/), który jest używany głównie do tworzenia plików faksów cyfrowych.

## Format pliku PCX

Pliki PCX są zapisywane na dysku w formacie pliku binarnego. Wewnętrzna struktura formatu pliku jest zgodna z kolejnością bajtów little endian i ma następujące trzy sekcje:

**`Nagłówek PCX`** - Nagłówek PCX ma długość 128 bajtów. Zawiera identyfikator, numer wersji, wymiary obrazu, 16 palet kolorów, liczbę płaszczyzn kolorów i głębię bitową każdej płaszczyzny oraz wartość metody kompresji.

Nagłówek PCX jest taki, jak pokazano poniżej z odniesieniem do Encyklopedii formatów plików graficznych (wyd. 2).
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

**`Dane obrazu`** — dane obrazu PCX pojawiają się zaraz po nagłówku. Dane obrazu mogą zostać skompresowane w zależności od ustawienia pola w nagłówku. Przechowywanie danych w pliku PCX zależy od liczby określonych płaszczyzn kolorów. Dane obrazu są uporządkowane w wierszach. W przypadku wielu płaszczyzn są one przechowywane według płaszczyzny w rzędzie w sekwencyjnym układzie danych koloru czerwonego, zielonego i niebieskiego. Ten wzór jest powtarzany dla każdej linii w płaszczyźnie.

## Bibliografia

* [PCX – z Wikipedii](https://en.wikipedia.org/wiki/PCX)

