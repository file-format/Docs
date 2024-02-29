---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sفرم فایل TEPat
linktitle: STEP
description: Lدر مورد فرمت فایل STEP و APIهایی که می توانند فایل STEP را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## فایل STEP چیست؟

فایل STEP یک فرمت تبادل داده پرکاربرد برای طراحی به کمک کامپیوتر (CAD) است. در سال 1994 توسط کمیته ISO با نام ISO 10303-21 استاندارد شد. ISO 10303-21 مکانیسم رمزگذاری را برای نمایش داده ها در زبان مدل سازی داده EXPRESS تعریف می کند. یک فایل STEP- با نام های p21-File و STEP Physical File نیز شناخته می شود. پسوندهای فایل مورد استفاده برای STEP-file عبارتند از .stp و .step.

## تاریخچه پایه

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. ویرایش دوم در سال 2002 منتشر شد که شامل تصحیح و پسوند برای چندین بخش داده بود. نسخه سوم در سال 2016 منتشر شد که بخش‌های لنگر و مرجع را اضافه کرد که اجازه می‌داد موجودیت‌ها و مقادیر در فایل‌های خارجی ذخیره شوند. پشتیبانی UTF-8 از رشته ها اضافه شد. امضاهای دیجیتال برای تأیید محتویات فایل و اعتبارسنجی اعتبار اضافه شدند. پشتیبانی برای فشرده سازی و ذخیره سازی ساختار تبادل با استفاده از ZIP نیز اضافه شد.

## فرمت فایل STEP

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; اولین شخصیت های اولین رکورد هستند. نظرات با کاراکترهای /* و */ احاطه شده اند. آخرین رکورد حاوی END-ISO-10303-21; اگر فایل STEP با نسخه 2002 مطابقت داشته باشد. در صورتی که با نسخه 2016 مطابقت داشته باشد، ممکن است یک یا چند امضای دیجیتال بعد از END-ISO-10303-21; وجود داشته باشد. نابود کننده. شکست خط با \N\ و شکست صفحه با \F\ نشان داده می شود.

فایل STEP به بخش‌هایی تقسیم می‌شود و نام آن‌ها شرایط رزرو شده است. تمام بخش ها با رکورد ENDSEC خاتمه می یابند و باید به ترتیب نشان داده شده در زیر باشند.

- **HEADER**: این قسمت اجباری و غیر قابل تکرار است. از موجودیت های زیر تشکیل شده است:
  - file_description (mandatory)
  - "file_name (اجباری)"
  - "file_schema (اجباری)"
  - "schema_population (اختیاری)"
  - "file_population (اختیاری)"
  - "section_language (اختیاری)"
  - "section_context (اختیاری)"
- **ANCHOR**: یک قسمت غیر تکراری اختیاری است که در نسخه 2016 معرفی شده است. نام های خارجی را برای نمونه ها تعریف می کند تا بتوان به آنها ارجاع داد.
- **REFERENCE**: یک قسمت غیر تکراری اختیاری است که در نسخه 2016 نیز معرفی شده است. هر ورودی در این بخش یک نام نمونه ورودی/مقدار را به یک نمونه/مقدار در یک فایل خارجی مرتبط می‌کند.
- **DATA**: یک بخش قابل تکرار اختیاری است که حاوی محتوای اصلی نمونه مدل است.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## منابع

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

