{
  "date": "2020-01-10",
  "keywords": [
"فایل dib",
"فرمت فایل dib",
"فایل dib چیست",
"فایل",
"نمونه dib",
"پسوند فایل dib",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "با فرمت فایل DIB و APIهایی که می توانند فایل های DIB را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-fab"
}
},
  "lastmod": "2020-01-10"
}

## فایل DIB چیست؟

یک بیت مپ مستقل از دستگاه (DIB) یک فایل تصویر شطرنجی است که از نظر ساختار مشابه فایل‌های بیت مپ استاندارد ([BMP]()/image/bmp/)) است. این شامل یک جدول رنگی است که نگاشت رنگ های RGB به مقادیر پیکسل را توصیف می کند. این DIB را قادر می سازد تا تصویر را در هر دستگاهی نمایش دهد. تقریباً با همه برنامه هایی که می توانند یک فایل استاندارد BMP را در ویندوز و همچنین macOS باز کنند، قابل باز شدن است. DIB فایل های باینری هستند و فرمت فایل پیچیده ای شبیه به BMP دارند. تصاویر DIB مستقل از قابلیت های خروجی دستگاه های رندر از نظر عمق رنگ و پیکسل بر اینچ هستند.

## مشخصات فرمت فایل DIB ##
یک DIB حاوی اطلاعات رنگ و ابعاد زیر است:

  * فرمت رنگ دستگاهی که تصویر مستطیلی روی آن ایجاد شده است.
  * وضوح دستگاهی که تصویر مستطیلی روی آن ایجاد شده است.
  * پالت دستگاهی که تصویر روی آن ایجاد شده است.
  * آرایه‌ای از بیت‌ها که سه‌گانه‌های قرمز، سبز، آبی (RGB) را به پیکسل در تصویر مستطیلی نگاشت می‌کند.
  * یک شناسه فشرده سازی داده که نشان دهنده طرح فشرده سازی داده ها (در صورت وجود) است که برای کاهش اندازه آرایه بیت ها استفاده می شود.

### فرمت DIB Data Block ###

DIB در زمینه بلوک حافظه در مقایسه با فایل های .DIB ذخیره شده روی دیسک می آید. بلوک حافظه شامل ساختاری است که مطابق با مشخصات API ویندوز برای DIB ها است. DIB واقعی شامل موارد زیر است:
  * یک هدر
  * پالت رنگ
  * داده های پیکسل

عملاً کار با داده های پالت، هدر و تصویر به گونه ای انجام می شود که گویی سه بلوک جداگانه از حافظه هستند. یک دسته به این بلوک حافظه مشترک با استفاده از GlobalAlloc اختصاص داده می شود و به عنوان HDIB شناخته می شود، که برای استخراج و کار با داده های هدر، جدول رنگ و پیکسل استفاده می شود.

### سازه های ###
اطلاعات موجود در یک DIB با ساختارهای مختلف نشان داده می شود. این شامل:

BITMAPinfo - اطلاعات ابعاد و رنگ را برای یک DIB تعریف می کند
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
از یک BITMAPINFOHEADER تشکیل شده است:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
به دنبال آن دو یا چند ساختار RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### بیت های داده ###
|بیت|توضیحات|
---|---|
|فرمت 1 بیتی (تک رنگ)|بیت مپ های تک رنگ از دو رنگ (سیاه و سفید) تشکیل شده است. با توجه به این تعداد رنگ محدود، این بیت مپ ها فضای کمتری روی دیسک می گیرند. bitBitCount درست یا نادرست را برای نمایش هر دو رنگ برمی گرداند. اگر bitBitCount==1 باشد، اکثر برنامه ها پالت را به طور کامل نادیده می گیرند.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. These bits representthe color of the pixel in the descending order.
|فرمت 8 بیتی (256 رنگ)|این فرمت 8 بیتی می تواند حداکثر 256 رنگ را نشان دهد. هر بایت در آرایه داده بیت مپ تصویر یک پیکسل را نشان می دهد. مقدار آن بایت تعداد ورودی پالت رنگی است که باید از 256 ورودی استفاده شود که توسط bmciColors نشان داده شده است.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. اما همانطور که می بینید، نیازی به آن نیست، زیرا داده های پیکسل خود حاوی اطلاعات رنگ هستند.
|فرمت 32 بیتی|تصاویر 32 بیتی حداکثر 2^24 رنگ دارند (biBitCount == 24).

## منابع ##
  * [بیت مپ های مستقل از دستگاه - توسط مایکروسافت](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

