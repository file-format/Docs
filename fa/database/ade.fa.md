{
  "date": "2021-08-29",
  "keywords": [
"ade",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"دسترسی مایکروسافت"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل ADE و APIهایی که می توانند فایل های ADE را ایجاد و باز کنند آشنا شوید.",
  "title": "ADE - به فایل پسوند پروژه دسترسی پیدا کنید",
  "linktitle": "ADE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ad-fae"
}
},
  "lastmod": "2021-08-29"
}

## فایل ADE چیست؟

یک فایل با پسوند ade. یک فایل پروژه Microsoft Access است که حاوی خروجی کامپایل شده اطلاعات موجود در فایل پروژه Microsoft Access ADP است. اطلاعات موجود در فایل پروژه Access، به غیر از ویژوال بیسیک برای برنامه ها (VBA)، به صورت کامپایل شده در فایل های ADE موجود است. داده ها در قالب فشرده در این فایل ها ذخیره می شوند تا حجم فایل کاهش یابد و عملکرد در Access بهبود یابد. از آنجایی که ADE خروجی کامپایل شده فایل پروژه Access است، هر کد منبع VBA که بخشی از پروژه است، با عدم اجازه دادن به آن برای بخشی از خروجی محافظت می شود. فایل های ADE را می توان در Microsoft Access 365 باز کرد.

## فرمت فایل ADE - اطلاعات بیشتر

ADE فایل های پایگاه داده دسترسی کامپایل شده هستند که به عنوان فایل های باینری در دیسک ذخیره می شوند. ساختار فایل داخلی این فایل ها مشخص نیست.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. این مشکل به این دلیل رخ می دهد که Access 2010 SP1 از نسخه جدیدتر فایل VBE7.dll (نسخه 7.00.1619) استفاده می کند.

## منابع

* [مشکل با دسترسی به فایل‌های ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [Which Access File Formats to Use](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


