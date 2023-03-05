{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла PCX — файл растрового изображения Paintbrush",
  "description":"Узнайте о формате файла PCX и API-интерфейсах, которые могут создавать и открывать файлы PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## .PCX вариант №

Файл PCX, файл Picture Exchange, представляет собой формат файла растрового изображения, который использовался в качестве собственного формата файла для приложения PC Paintbrush. Он был разработан корпорацией ZSoft, США, для платформ DOS и Windows и был принят в качестве основного формата файла изображения до появления [BMP](/ru/image/bmp/), [JPEG](/ru/image/jpeg/) и [ Форматы файлов PNG](/ru/image/png/). Файлы PCX имеют меньший размер, поскольку они сжаты с использованием кодировки RLE. Он используется в многостраничном файле [DCX](/ru/image/dcx/), который в основном используется для создания файлов цифровых факсов.

## Формат файла PCX

Файлы PCX сохраняются на диск в двоичном формате. Структура внутреннего формата файла соответствует порядку байтов с прямым порядком байтов и состоит из следующих трех разделов:

**`Заголовок PCX`** — длина заголовка PCX составляет 128 байт. Он содержит идентификатор, номер версии, размеры изображения, 16 цветов палитры, количество цветовых плоскостей и разрядность каждой плоскости, а также значение метода сжатия.

Заголовок PCX показан ниже со ссылкой на Энциклопедию форматов графических файлов (2-е изд.).
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

**`Image Data`** — данные изображения PCX следуют сразу после заголовка. Данные изображения могут быть сжаты в зависимости от настройки поля в заголовке. Хранение данных в файле PCX зависит от количества указанных цветовых плоскостей. Данные изображения организованы в строки. В случае нескольких плоскостей они хранятся по плоскостям в строке в последовательном порядке красных, зеленых и синих данных. Этот шаблон повторяется для каждой строки на плоскости.

## использованная литература

* [PCX — Википедия](https://en.wikipedia.org/wiki/PCX)

