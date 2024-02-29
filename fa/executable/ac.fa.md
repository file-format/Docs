{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
}،
  "draft" : "false",
  "toc" : true,
  "description" : "درباره فرمت فایل AC و APIهایی که می‌توانند فایل‌های ACCDB را ایجاد و باز کنند، بیاموزید.",
  "title" : "فرمت فایل AC - فایل اسکریپت تنظیم خودکار",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-fa",
      "parent" : "executable"
}
}،
  "lastmod" : "2020-01-11"
}

## فایل AC چیست؟

فایل AC فایل اسکریپت Autoconf است. **Autoconf** یک بسته قابل توسعه از ماکروهای M4 است که اسکریپت های پوسته ای را برای پیکربندی خودکار بسته های کد منبع نرم افزار تولید می کند. این اسکریپت ها می توانند بسته ها را با بسیاری از انواع سیستم های مشابه یونیکس بدون دخالت دستی کاربر تطبیق دهند. Autoconf یک اسکریپت پیکربندی برای یک بسته از یک فایل الگو ایجاد می کند که ویژگی های سیستم عاملی را که بسته می تواند از آنها استفاده کند، در قالب تماس های ماکرو M4 فهرست می کند.

Producing configuration scripts using Autoconf requires GNU M4. شما باید GNU M4 (حداقل نسخه 1.4.6، اگرچه 1.4.13 یا جدیدتر توصیه می شود) را قبل از پیکربندی Autoconf نصب کنید تا اسکریپت پیکربندی Autoconf بتواند آن را پیدا کند. اسکریپت های پیکربندی تولید شده توسط Autoconf مستقل هستند، بنابراین کاربران آنها نیازی به داشتن Autoconf (یا GNU M4) ندارند.

## چگونه فایل AC را باز کنیم؟

AC مخفف Automatic Configuration است. این یک اسکریپت تولید شده توسط GNU Autoconf است که کد منبع نرم افزار را قادر می سازد تا با آزمایش ویژگی های لازم در بسته، با سیستم های مختلف Posix مانند سازگار شود. اسکریپت فایل AC نامیده می شود.

## اجزای اصلی ابزارهای خودکار

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools مجموعه ای از بسته های مرتبط است که در صورت استفاده با هم، بسیاری از مشکلات ایجاد نرم افزار قابل حمل را برطرف می کند. این ابزارها، همراه با چند فایل ورودی نسبتاً ساده ارائه شده توسط بالادست، برای ایجاد سیستم ساخت یک بسته استفاده می‌شوند.

**یک نمای کلی از نحوه قرارگیری اجزای اصلی ابزار خودکار با هم.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

در یک راه اندازی ساده:

- برنامه autoconf یک اسکریپت پیکربندی را از configure.in یا configure.ac تولید می کند.
- برنامه automake یک Makefile.in را از Makefile.am تولید می کند.
- اسکریپت «پیکربندی» برای تولید یک یا چند فایل Makefile از فایل‌های Makefile.in اجرا می‌شود.
- برنامه make از Makefile برای کامپایل برنامه استفاده می کند.

## منابع
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [مبانی ابزارهای خودکار] (https://devmanual.gentoo.org/general-concepts/autotools/index.html)



