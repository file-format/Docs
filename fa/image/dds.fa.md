{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل DDS- فایل تصویر سطحی DirectDraw",
  "description": "درباره فرمت فایل DDS و APIهایی که می‌توانند فایل‌های DDS را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-fas"
}
},
  "lastmod": "2022-04-02"
}

## فایل DDS چیست؟

یک فایل DDS یک فایل تصویر شطرنجی است که از فرمت کانتینر DirectDraw Surface (DDS) استفاده می کند. این تکسچرهای غیر فشرده و فشرده (DXTn) را ذخیره می کند و انواع مختلفی را برای ذخیره انواع مختلف داده ها پیاده سازی می کند. همچنین از چندین نوع مختلف داده مانند بافت‌های تک لایه، بافت‌های دارای mipmaps، نقشه‌های مکعبی، نقشه‌های حجمی و آرایه‌های بافت پشتیبانی می‌کند. این فایل‌های DDS را قادر می‌سازد تا مدل‌های واحد بافت بازی ویدیویی را علاوه بر عکس‌های دیجیتال و پس‌زمینه دسکتاپ ویندوز ذخیره کنند. فرمت فایل DDS توسط مایکروسافت برای استفاده با DirectX SDK توسعه داده شد.

## فرمت فایل DDS

فایل های DDS به صورت فایل های باینری ذخیره می شوند و می توانند با DirectX SDK استفاده شوند. از قدرت DirectX برای توسعه برنامه های رندر بلادرنگ مانند بازی های سه بعدی استفاده می کند.

### طرح بندی فایل DDS

[DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) توسط مایکروسافت به تفصیل مستند شده است. یک فایل DDS باینری حاوی اطلاعات زیر است.

 * یک DWORD (شماره جادویی) حاوی مقدار کد چهار کاراکتری DDS (0x20534444).
 * A description of the data in the file.

DDS_HEADER داده ها را توصیف می کند و DDS_PIXELFORMAT قالب پیکسل را توصیف می کند. این هر دو جایگزین ساختارهای منسوخ DDSURFACEDESC2، DDSCAPS2 و DDPIXELFORMAT DirectDraw 7 می شوند.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) جزئیات فنی این قالب فایل را بیشتر توضیح می دهد.

## منابع

* [DDS - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [راهنمای مرجع فنی فرمت فایل ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)


