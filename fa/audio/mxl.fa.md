---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lدر مورد فرمت فایل MXL و APIهایی که می توانند فایل MXL را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Mفرمت فایل XL - فشرده MusicXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## فایل MXL چیست؟

یک فایل MXL فرم فشرده شده فرمت فایل MusicXML است که یک فرمت استاندارد باز برای تبادل نت های موسیقی دیجیتال است. فایل‌های MusicXML متن ساده از نظر اندازه بزرگ هستند و استفاده از چنین فایل‌هایی به عنوان فرمت توزیع برگه با اندازه فایل بزرگ تحت تأثیر قرار گرفت. این مشکل با [MusicXML](https://www.musicxml.com/) 2.0 با معرفی فرمت فایل MXL که فایل ها را به اندازه کافی فشرده می کند تا اندازه فایل مشابه فایل های MIDI اصلی کاهش یابد، برطرف شد. نوع رسانه توصیه شده برای فایل های MXL application/vnd.recordare.musicxml است.

## فرمت فایل MXL

فایل‌های MXL به صورت فایل‌های [ZIP](/compression/zip/) فشرده شده [XML](/web/xml/) با پسوند فایل mxl. ذخیره می‌شوند. فایل های MXL با الگوریتم DEFLATE همانطور که در [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt) مشخص شده است فشرده می شوند.

### ساختار فایل MXL

هر فایل MXL دارای یک فرمت XML مبتنی بر ZIP است که باید یک فایل META-INF/container.xml داشته باشد که نقطه شروع نسخه MusicXML فایل را توصیف می کند. هیچ فایل xsd. متناظری برای فرمت فایل MXL تعریف نشده است.

یک فایل container.xml ساده دارای محتویات زیر است. این مثال از فایل Dichterliebe01.mxl موجود در وب سایت MakeMusic گرفته شده است.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
در این مثال،<container> عنصر عنصر سند است. را<rootfiles> عنصر می تواند شامل یک یا چند باشد<rootfile> عناصر، با اولین<rootfile> عنصری که ریشه MusicXML را توصیف می کند. یک فایل MusicXML که به عنوان یک فایل استفاده می شود<rootfile> ممکن است<score-partwise> ،<score-timewise> ، یا<opus> به عنوان عنصر سند آن

## منابع

* [فایل های فشرده شده MXL] (https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt)


