{
  "date": "2022-03-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل NUPKG - فایل بسته NuGet",
  "description": "درباره فرمت فایل NUPKG و APIهایی که می‌توانند فایل‌های NUPKG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "NUPKG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nupk-fag"
}
},
  "lastmod": "2022-03-09"
}

## فایل NUPKG چیست؟

فایل NUPKG یک فایل بسته است که حاوی کد منبع است که توسط نرم افزار NuGet برای ایجاد بسته هایی برای استفاده در پروژه های دات نت استفاده می شود. مؤلفه NuGet Package Manager به عنوان بخشی از Microsoft Visual Studio برای واکشی بسته ها از مخزن میزبان بسته های آنلاین نصب شده است. فایل‌های NUPKG به توسعه‌دهندگان کمک می‌کنند تا با استفاده از NuGet Package Manager به جای دانلود و نصب دستی بسته‌های توسعه، آخرین بسته‌ها را از [Nuget.org](https://nuget.org) واکشی کنند. فایل‌های NUPKG از فایل‌های NUSPEC ساخته می‌شوند و پس از واکشی، بسته را روی سیستم کاربر نصب می‌کنند.

## فرمت فایل NUPKG

فایل‌های NUPKG آرشیوهای [ZIP](/compression/zip/) هستند که شامل کتابخانه‌های بسته‌بندی شده درون آن هستند. پس از دانلود، می توان آن را به .zip تغییر نام داد و با هر گونه ابزار استاندارد zip مانند WinZIP، 7-Zip و Apple Archive Utility استخراج کرد.

## ارجاع

* [Nuget.org] (https://nuget.org)

* [Quickstart: نصب و استفاده از یک بسته در Visual Studio (فقط ویندوز)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- استودیو)

* [چگونه یک بسته Nuget ایجاد و منتشر کنیم](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)


