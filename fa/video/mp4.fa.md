---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lحدود فرمت فایل MP4 و APIهایی که می توانند فایل MP4 را ایجاد و باز کنند، کسب کنیدs.
title: Mفرم فایل P4at
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## فایل MP4 چیست؟ ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## تاریخچه مختصر ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. اولین نسخه (ISO/IEC 14496-1:2001) MP4 بازبینی MPEG-4 قسمت 1 بود: مشخصات سیستم ها که در سال 1999 منتشر شد. :2004 که ساختار کلی فایل های رسانه ای مبتنی بر زمان را تعریف کرد. در نتیجه، از آن به عنوان پایه ای برای سایر فرمت های فایل استفاده می شود.

## ساختار فایل های MP4 ##

MP4 یک فایل کانتینری قابل توسعه است، به این معنی که ساختار دقیقی را تعریف نمی کند و ساختار و سلسله مراتب سفارشی را برای هر نوع رسانه امکان پذیر می کند. داده‌های فایل MP4 به دو بخش تقسیم می‌شود، بخش اول شامل داده‌های مربوط به رسانه و بخش دوم حاوی متادیتا است. داده‌های رسانه حاوی صدا یا تصویر است و ابرداده پرچم‌هایی را برای دسترسی تصادفی، مهرهای زمانی و غیره نشان می‌دهد.
ساختارهای MP4 معمولاً به عنوان اتم یا جعبه نامیده می شوند. حداقل اندازه یک اتم 8 بایت است (4 بایت اول اندازه را مشخص می کند و 4 بایت بعدی نوع را مشخص می کند). در اینجا لیستی از اتم های سطح ریشه موجود در فایل های MP آمده است:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: حاوی اطلاعات بارگیری/دانلود پیش رونده ویدئو است.
- **moov**: ظرفی برای تمام ابرداده های فیلم.
- **moof**: ظرفی با قطعات ویدئویی.
- **mfra**: ظرفی با دسترسی تصادفی به قطعه ویدیو
- **mdat**: محفظه داده برای رسانه.
- **stts**: جدول نمونه به زمان.
- **stsc**: جدول نمونه به تکه.
- **stsz**: اندازه های نمونه (قاب بندی)
- **متا**: محفظه ای با اطلاعات فراداده.

در اینجا لیستی از اتم های سطح دوم استفاده شده در MP4 آمده است:

- **mvhd**: حاوی اطلاعات هدر ویدیو با جزئیات کامل ویدیو است.
- **trak**: کانتینری با مسیر فردی.
- **udta**: کانتینری با اطلاعات کاربر و مسیر.
- **iods**: توصیف کننده فایل MP4

## منابع ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

