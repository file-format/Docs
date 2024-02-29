{
  "date": "2021-09-06",
  "keywords": [
"btr",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"پایگاه داده Btrieve"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل BTR و APIهایی که می‌توانند فایل‌های BTR را ایجاد و باز کنند، بیاموزید.",
  "title": "BTR - فایل پایگاه داده Btrieve",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bt-far"
}
},
  "lastmod": "2021-09-06"
}

## فایل BTR چیست؟

یک فایل با پسوند .btr یک فایل پایگاه داده است که توسط برنامه پایگاه داده تراکنشی [Btrieve](https://www.actian.com/) ایجاد شده است. بر خلاف سیستم های مدیریت پایگاه داده رابطه ای (RBMS)، Btrieve بر اساس روش دسترسی متوالی فهرست شده (ISAM) است که راهی برای ذخیره داده ها برای بازیابی سریع است. فایل BTR مجموعه‌ای از رکوردها را ذخیره می‌کند و برای تولید گزارش‌ها طبق نیاز استفاده می‌شود. فایل های BTR را می توان با استفاده از Pervasive Btrieve Database Manager، Pervasive PSQL Maintenance Utility و Legend Software BTRIEVE Viewer باز کرد.

## ساختار فایل BTR - اطلاعات بیشتر

ساختار داده داخلی و تراز هر بایت در ساختار یک فایل BTR برای عموم در دسترس نیست. با این حال، Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * گنو C/C++
 * میکرو فوکوس COBOL
 * مایکروسافت ویژوال بیسیک
 * Microsoft Visual C++
 * Watcom C/C++

بازیابی اطلاعات از یک فایل BTR به فایل DDF مرتبط با آن بستگی دارد. بدون DDF، بازیابی اطلاعات از چنین فایلی آسان نخواهد بود.

## منابع

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

