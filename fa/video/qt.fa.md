{
  "date": "2021-02-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل QT - فایل سریع فیلم",
  "keywords": [
"QT",
"ویدیوی QuickTime",
"فرمت qt",
"نحوه پخش فایل های qt",
"فایل فیلم سریع",
"QTFF",
"ویدئو",
"سیب"
],
  "description": "با فرمت فایل QT و APIهایی که می توانند فایل های QT را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "QT",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-q-fat"
}
},
  "lastmod": "2021-02-16"
}

## فایل QT چیست؟

یک فایل با پسوند .qt یک فایل محفظه چند رسانه ای است که توسط چارچوب QuickTime برای ذخیره محتوای فایل چندرسانه ای استفاده می شود. فرمت فایل QuickTime (QTFF) توسط شرکت اپل توسعه یافته است. یک فایل محفظه چندرسانه ای است که حاوی صدا، ویدئو یا متن برای پخش در آینده است. این فرمت انتخابی برای تبادل رسانه های دیجیتال بین دستگاه ها، برنامه ها و سیستم عامل ها است. فایل‌های QT نیز در قالب [MOV](/video/mov/) ذخیره می‌شوند که توسط Apple Inc نیز توسعه داده شده است. برخی از برنامه‌هایی که می‌توانند فایل‌های QT را باز کنند عبارتند از Apple QuickTime Player، پخش‌کننده رسانه VLC، و Media Player Classic با بسته کدک K-Lite.

## فرمت فایل QT

QTFF شی گرا است که مجموعه ای انعطاف پذیر از اشیاء را برای سهولت تجزیه و بسط در معرض دید قرار می دهد. هر آهنگ در یک فایل QT حاوی یک جریان رسانه ای رمزگذاری شده دیجیتالی یا یک مرجع داده به جریان رسانه ای است که در فایل دیگری قرار دارد. ساختار داده سلسله مراتبی متشکل از اشیایی به نام اتم ها به عنوان کانتینرهای مسیر عمل می کند. مشخصات قالب فایل برای [QT file format](https://developer.apple.com/documentation/quicktime-file-format) به طور رسمی توسط Apple Inc برای مرجع توسعه دهنده در دسترس است.

### Media description

The media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information is stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### اتم ها

Atom واحد اصلی فایل QuickTime است. دو میدان اصلی در هر اتمی قبل از هر میدان دیگری وجود دارد: فیلدهای اندازه و نوع. فیلد اندازه اندازه اتم را نشان می دهد در حالی که فیلد نوع نوع داده های ذخیره شده در اتم را نشان می دهد. ذاتاً، اتم‌ها سلسله مراتبی هستند، به این معنی که یک اتم می‌تواند حاوی اتم‌های دیگری باشد که همچنان می‌توانند حاوی اتم‌های دیگری باشند. طرح یک اتم نمونه در تصویر زیر نشان داده شده است.

هر اتم دارای دو بخش سرصفحه و داده است. هدر شامل فیلدهای اندازه و نوع و قسمت داده حاوی داده های واقعی است. علاوه بر این، هر زمینه در زیر توضیح داده شده است:

#### اندازه اتم

هدر و محتویات اتم با یک عدد صحیح 32 بیتی به نام اندازه اتم نشان داده می شود. فیلد اندازه شامل اندازه اتم بر حسب بایت است که در یک عدد صحیح بدون علامت 32 بیتی بیان شده است.

#### نوع اتم

نوع اتم نیز با یک عدد صحیح 32 بیتی نشان داده می‌شود که بیشتر به عنوان یک میدان چهار کاراکتری با مقدار knemonic در نظر گرفته می‌شود، مانند 'moov' (0x6D6F6F76) برای اتم فیلم، یا 'trak' (0x7472616B) برای یک اتم مسیر هنگامی که نوع اتم شناخته شد، امکان تفسیر داده های آن را فراهم می کند.

![alt text](../QT_Sample_Atom.png "QT File Format")

## ساختار فایل ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV با نوع فرعی که باید qt باشد تعریف شده است. برای نوشتن فایل MOV، تکه‌های تکراری مورد نیاز است تا زمانی که نوع ناشناخته شناسایی شود.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. در افست 32 (هگز: 20) قطعه دوم قرار دارد که دارای اندازه 8 و نوع **mdat** (هگز: 6D 64 61 74) است.

قطعه بعدی در آفست 32+8#40 (هگز: 28) قرار دارد و دارای اندازه 3,263,028 (هگز: 00 31 CA 34) و نوع **mdat** (هگز: 6D 64 61 74) در افست 44 (هگز). : 2C). قطعه بعدی در افست 40 + 3,263,028#3,263,068 (هگز: 00 31 CA 5C) قرار دارد و دارای اندازه 21,189 (هگز: 00 00 52 C5) و نوع **moov** (هگز: 6D 76F) در 6F است. 1,836,019,574 (هگزا: 00 31 CA 60). این آخرین قطعه است، بنابراین حجم کل فایل 3,263,068+21,189#3,284,257 بایت است.

## منابع ##

* [فرمت فایل QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)

* [فرمت فایل QuickTime - ویکی پدیا](https://en.wikipedia.org/wiki/QuickTime_File_Format)


