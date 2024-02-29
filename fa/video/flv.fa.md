---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lدر مورد فرمت فایل FLV و APIهایی که می توانند فایل FLV را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Fفرم فایل LVat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## فایل FLV چیست؟ ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. سیستم های Adobe به دلیل محدودیت های FLV در سال 2007 F4V را ایجاد کردند.

### رمزگذاری ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. نسخه 8 فلش پلیر از جریان های بیتی ویدیویی On2 TrueMotion VP6 پشتیبانی می کند. این فرمت فشرده سازی توصیه شده برای Flash Player 8 و بالاتر است. FLV از صدا در MP3، Nellymoser Asao Codec و کدک منبع باز Speex پشتیبانی می کند. همچنین از صدای فشرده نشده یا فرمت ADPCM پشتیبانی می کند. AAC (HE-AAC/AAC SBR، AAC Main Profile و AAC-LC) توسط نسخه های اخیر Flash Player 9 پشتیبانی می شود.

## ساختار ##

فایل های FLV از Header و Packets تشکیل شده اند. یک فایل FLV با Header شروع می شود. سربرگ دارای فیلدهای زیر است.

- **امضا**: مقدار آن FLV است
- **Version**: Its default value is 1. فقط 0x01 معتبر است.
- **پرچم ها**: 0x04 برای صدا و 0x01 برای ویدیو استفاده می شود بنابراین 0x05 هم برای صدا و هم برای تصویر استفاده می شود.
- **Header Size**: The default value is 9. برای رد شدن از سرصفحه توسعه یافته جدیدتر استفاده می شود.

بعد از هدر Packets می آید. فایل FLV به بسته های متعددی به نام تگ های FLV تقسیم می شود که دارای هدرهای 15 بایتی هستند. بسته‌ها حاوی ابرداده‌های صوتی، تصویری، اسکریپت‌ها، اطلاعات رمزگذاری و محموله هستند. بسته های FLV دارای فیلدهای زیر هستند.

- **رزرو شده**: برای FMS رزرو شده و باید 0 باشد.
- **Filter**: نشان دهنده فیلتر بودن یا نبودن بسته ها است.
  - "**0**: نیازی به پیش پردازش نیست. این برای فایل های رمزگذاری نشده استفاده می شود."
  - "**1**: پیش پردازش مورد نیاز است. این برای فایل های رمزگذاری شده استفاده می شود"
- **نوع بسته**: نوع محتوای بسته را مشخص می کند.
  - "**8**: صوتی"
  - "**9**: ویدئو"
  - "**18**: داده های اسکریپت"
- **اندازه داده**: این نشان دهنده طول پیام است.
- **Timestamp Lower**: این مهر زمانی را در میلی ثانیه ذخیره می کند که در آن داده های برچسب اعمال می شود. برای بسته اول روی NULL تنظیم شده است.
- **Timestamp Upper**: برنامه افزودنی برای ایجاد مقدار uint32_be.
- **Stream ID**: برای اولین استریم روی NULL تنظیم شده است.
- **Payload Data**: این داده بر اساس نوع بسته است.

## منابع ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

