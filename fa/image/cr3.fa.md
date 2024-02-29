{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فرمت فایل CR3 - فایل تصویری Canon Raw 3",
  "description":"درباره فرمت فایل CR3 و APIهایی که می توانند فایل های CR3 را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-fa",
      "parent" : "image"
}
}،
  "lastmod" : "2022-03-26"
}

## فایل CR3 چیست؟

یک فایل CR3 یک فرمت فایل تصویری RAW کانن است که توسط دوربین های دیجیتال منتخب کانن ایجاد می شود. این توسط Canon برای جایگزینی فرمت فایل CR2 معرفی شد و توسط برخی از دستگاه های دیجیتال کانن استفاده می شود. فایل‌های CR3 داده‌های اصلی تصویر بدون تلفات پردازش‌نشده گرفته‌شده توسط دوربین را ذخیره می‌کنند. استفاده از این تصاویر خام، تصاویری با کیفیت بالا ارائه می دهد و فضای زیادی را برای ویرایش در اختیار عکاسان می گذارد. فایل‌های CR3 علاوه بر داده‌های تصویر اصلی، اطلاعات فراداده تصویر را نیز ذخیره می‌کنند.

## فرمت فایل CR3

فایل‌های CR3 به‌عنوان فایل باینری در قالب فایل رسانه پایه ISO (ISO/IEC 14496-12) روی دیسک ذخیره می‌شوند و همچنین شامل [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid) سفارشی می‌شود. همچنین شامل [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) است که ترکیبی از JPEG-LS (کدگذاری Rice-Golomb + RLE) و JPEG-2000 (LeGall 5/3 DWT + کمیت‌سازی) است.

## برچسب های سفارشی CR3

فایل های CR3 حاوی برچسب های سفارشی برای اهداف مختلف هستند. برخی از این تگ ها به شرح زیر است.

| شناسه برچسب| نام تگ| قابل نوشتن | ارزش ها / یادداشت ها|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Tags|
|'CMT1' |IFD0| - |--> برچسب های EXIF|
|'CMT2' |ExifIFD| - |--> برچسب های EXIF|
|'CMT3' |MakerNoteCanon| - |--> برچسب های Canon|
|'CMT4' |GPSInfo| - |--> برچسب های GPS|
|'CNCV' |CompressorVersion| نه| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |تصویر کوچک| نه| |

## منابع

 * [فرمت فایل CR2](http://lclevy.free.fr/cr2/)
 * [برچسب‌های Canon](https://exiftool.org/TagNames/Canon.html#uuid)

