{
  "date": "2020-11-11",
  "keywords": [
"MDB",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"فایل های پایگاه داده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل MDB و APIهایی که می توانند فایل های MDB را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل MDB - یک فایل پایگاه داده Microsoft Access",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-fab"
}
},
  "lastmod": "2020-11-11"
}

## فایل MDB چیست؟

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. نسخه‌های جانبی Microsoft Access از فرمت‌های فایل [ACCDB](/database/accdb/) استفاده می‌کنند که آخرین فرمت فایل تا به امروز است. فایل های MDB را می توان با برنامه هایی مانند Microsoft Access، MDB Viewer، MDBOpener باز کرد و به فرمت های ACCDB، [CSV](/spreadsheet/csv/)، Excel و غیره تبدیل کرد.

## فرمت فایل MDB

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### صفحات

طبق راهنمای غیر رسمی MDB، یک فایل MDB از صفحات با اندازه ثابت تشکیل شده است (2048 بایت برای Jeb DB3 و 4096 بایت برای Jet DB 4). بایت اول نوع صفحه را نشان می دهد. انواع صفحه کلیدی در زیر آمده است:

«صفحه اول:» حاوی اطلاعات سرصفحه پایگاه داده است که شامل شناسایی نسخه Jet DB است که فایل با آن سازگار است. علاوه بر این، اطلاعات امنیتی فایل و نقشه استفاده از صفحه را نیز شامل می شود.

`صفحه تعریف جدول:` صفحه تعریف جدول ستون ها، انواع داده ها، فهرست و سایر اطلاعات را مشخص می کند. در صورت نیاز از صفحات اضافی استفاده می‌کند و شامل نقشه‌ای از صفحات است که حاوی داده‌های ردیف این جدول است.

`صفحات داده:` صفحات داده، محفظه های داده واقعی هستند که داده ها توسط ردیف ها ذخیره می شوند. از صفحات فرعی برای ذخیره مقادیر داده طولانی استفاده می کند.

یک پایگاه داده مایکروسافت اکسس ممکن است از چندین فایل تشکیل شده باشد که اجازه می دهد از محدودیت های اندازه فایل و جدول فراتر رود. این کار قرار دادن فرم ها و کدها را در یک فایل MDB جلویی روی دسکتاپ کاربر و داده ها را در فایل های MDB دیگر روی سرورهای متصل به شبکه تسهیل می کند.

## منابع ##

* [مشخصات دسترسی] (https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [راهنمای غیر رسمی MDB] (http://jabakobob.net/mdb/)


