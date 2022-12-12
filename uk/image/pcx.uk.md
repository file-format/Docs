{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу PCX - Файл растрового зображення пензля",
  "description":"Дізнайтеся про формат файлу PCX та API, які можуть створювати та відкривати файли PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Що таке файл PCX?

Файл PCX, файл Picture Exchange, — це формат файлу растрового зображення, який використовувався як рідний формат файлу для програми PC Paintbrush. Він був розроблений ZSoft Corporation, США для платформ DOS і Windows і був прийнятий як основний формат файлу зображень до появи [BMP](/uk/image/bmp/), [JPEG](/uk/image/jpeg/) і [ PNG](/uk/image/png/) формати файлів. Файли PCX мають менший розмір, оскільки вони стиснуті за допомогою кодування RLE. Він використовується в багатосторінковому файлі [DCX](/uk/image/dcx/), який в основному використовується для створення файлів цифрових факсів.

## Формат файлу PCX

Файли PCX зберігаються на диск у двійковому форматі. Внутрішня структура формату файлу відповідає порядку байтів у порядку байтів і складається з таких трьох розділів:

**`PCX Header`** - заголовок PCX має довжину 128 байт. Він містить ідентифікатор, номер версії, розміри зображення, 16 кольорів палітри, числові площини кольорів і бітову глибину кожної площини, а також значення методу стиснення.

Заголовок PCX виглядає як показано нижче з посиланням на Енциклопедію форматів графічних файлів (2-е видання).
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

**`Image Data`** - дані зображення PCX йдуть відразу після заголовка. Дані зображення можуть бути стиснуті залежно від налаштувань поля в заголовку. Зберігання даних у файлі PCX залежить від кількості вказаних кольорових площин. Дані зображення організовано в рядки. У випадку кількох площин, вони зберігаються по площинах у рядку в послідовному розташуванні червоних, зелених і синіх даних. Цей шаблон повторюється для кожної лінії на площині.

## Список літератури

* [PCX - Вікіпедія](https://en.wikipedia.org/wiki/PCX)

