{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل PCX - فایل تصویری Bitmap Paintbrush",
  "description": "درباره فرمت فایل PCX و APIهایی که می‌توانند فایل‌های PCX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-fax"
}
}،
  "lastmod": "2022-03-16"
}

## فایل PCX چیست؟

یک فایل PCX، فایل Exchange Picture، یک فرمت فایل تصویری شطرنجی است که به عنوان فرمت فایل بومی برای برنامه پینت براش کامپیوتر استفاده می‌شود. توسط ZSoft Corporation، ایالات متحده آمریکا برای پلتفرم‌های DOS و Windows توسعه داده شد و قبل از ورود فرمت‌های فایل [BMP](/image/bmp/)، [JPEG](/image/jpeg/) و [PNG](/image/png/) به عنوان فرمت اصلی فایل تصویری استفاده شد. فایل های PCX از نظر اندازه کوچکتر هستند زیرا با استفاده از رمزگذاری RLE فشرده می شوند. در فایل چند صفحه ای [DCX](/image/dcx/) که عمدتاً برای ایجاد فایل های فکس دیجیتال استفاده می شود، استفاده می شود.

## فرمت فایل PCX

فایل های PCX در قالب فایل باینری روی دیسک ذخیره می شوند. ساختار فرمت فایل داخلی از ترتیب کمی بایت اندیان پیروی می کند و دارای سه بخش زیر است:

**`PCX Header`** - یک هدر PCX 128 بایت طول دارد. این شامل یک شناسه، شماره نسخه، ابعاد تصویر، 16 رنگ پالت، تعداد صفحات رنگ و عمق بیت هر صفحه، و مقداری برای روش فشرده سازی است.

PCX Header مطابق شکل زیر با ارجاع از دایره المعارف فرمت های فایل های گرافیکی (ویرایش دوم) است.
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

**`Image Data`** - داده های تصویر PCX درست بعد از هدر قرار می گیرند. داده های تصویر ممکن است بسته به تنظیمات فیلد در هدر فشرده شوند. ذخیره سازی داده ها در فایل PCX به تعداد صفحات رنگی مشخص شده بستگی دارد. داده های تصویر در ردیف ها سازماندهی می شوند. در مورد چند صفحه، اینها توسط صفحه در ردیف در ترتیب متوالی داده های قرمز، سبز و آبی ذخیره می شوند. این الگو برای هر خط در هواپیما تکرار می شود.

## منابع

* [PCX - توسط Wikipedia](https://en.wikipedia.org/wiki/PCX)


