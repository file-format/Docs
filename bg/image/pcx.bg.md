{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX файлов формат – файл с растерно изображение на четка за рисуване",
  "description":"Научете повече за файловия формат PCX и API, които могат да създават и отварят PCX файлове.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Какво е PCX файл?

PCX файл, Picture Exchange файл, е файлов формат на растерно изображение, който е използван като собствен файлов формат за приложението PC Paintbrush. Разработен е от ZSoft Corporation, САЩ за платформи DOS и Windows и е приет като основен файлов формат за изображения преди пристигането на [BMP](/bg/image/bmp/), [JPEG](/bg/image/jpeg/) и [ PNG](/bg/image/png/) файлови формати. PCX файловете са с по-малък размер, тъй като са компресирани с помощта на RLE кодиране. Използва се в многостраничния [DCX](/bg/image/dcx/) файл, който се използва основно за създаване на цифрови факс файлове.

## PCX файлов формат

PCX файловете се записват на диск в двоичен файлов формат. Структурата на вътрешния файлов формат следва подреждането на байтовете от малкия край и има следните три секции:

**`PCX Header`** - PCX Header е с дължина 128 байта. Той съдържа идентификатор, номер на версия, размери на изображението, 16 цвята на палитрата, числови цветни равнини и битова дълбочина на всяка равнина и стойност за метода на компресия.

PCX Header е както е показано по-долу с препратка от Енциклопедия на графичните файлови формати (2-ро издание).
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

**`Image Data`** - PCX данните за изображение следват точно след заглавката. Данните за изображението може да бъдат компресирани в зависимост от настройката на полето в заглавката. Съхранението на данни в PCX файла зависи от броя на зададените цветни равнини. Данните за изображението са организирани в редове. В случай на множество равнини, те се съхраняват по равнина в ред в последователно подреждане на червени, зелени и сини данни. Този модел се повтаря за всяка линия в равнината.

## Препратки

* [PCX – от Wikipedia](https://en.wikipedia.org/wiki/PCX)

