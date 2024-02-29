{
  "date": "2022-06-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل GZIP - فایل بایگانی فشرده گنو",
  "description": "درباره اینکه یک فایل GZIP چیست و APIهایی که می‌توانند فایل‌های GZIP را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "GZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-gzi-fap"
}
},
  "lastmod": "2022-06-26"
}

## فایل GZIP چیست؟

یک فایل GZIP یک آرشیو فشرده است که با الگوریتم فشرده سازی استاندارد [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) ایجاد می شود. بایگانی فشرده ممکن است حاوی چندین فایل از جمله فایل های فشرده، دایرکتوری ها و فایل های خرد باشد. بیشتر سیستم‌های یونیکس شامل ابزار کمپرسور منبع باز gzip (GNU Zip) برای فشرده‌سازی/فشرده‌سازی فایل‌ها هستند. فایل های GZIP را می توان با برنامه هایی مانند [WinZip](https://www.winzip.com/en/) باز کرد.

## فرمت فایل GZIP - اطلاعات بیشتر

GZIP از الگوریتم [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) برای فشرده‌سازی فایل‌ها در آرشیو استفاده می‌کند. دو RFC، [RFC1952](https://tools.ietf.org/html/rfc1952) و [RFC 1951](https://tools.ietf.org/html/rfc1951) به ترتیب مشخصات فرمت gzip wrapper را تعیین می‌کنند و فرمت داده‌های فشرده را کاهش می‌دهند.

فایل‌های GZIP اغلب در قالب فایل [GZ](/compression/gz/) ذخیره می‌شوند.

## منابع

* [gzip](http://www.gzip.org/)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: مشخصات فرمت فایل GZIP](https://datatracker.ietf.org/doc/html/rfc1952)، توسط IETF

* [RFC 1951] (https://tools.ietf.org/html/rfc1951)


