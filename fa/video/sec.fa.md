---
date: 2022-03-25
keywords: sec, .sec, sec file format, .sec file format, .sec extension, sec extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lدر مورد فرمت فایل SEC و APIهایی که می توانند فایل SEC را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Sفرمت فایل EC - Samsung Security Video File
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## فایل SEC چیست؟

فایل SEC یک فایل ویدئویی است که با سیستم نظارت DVR سامسونگ ایجاد می شود. ویدئو از دوربین های مداربسته گرفته شده و روی دیسک با فرمت SEC ذخیره می شود. ویدئوی ضبط شده SEC را می توان با نرم افزار ویدئویی سامسونگ که می تواند فید ویدئو را از چندین دوربین مدیریت کند، پخش کرد.

## فرمت فایل SEC - اطلاعات بیشتر

فایل های SEC حاوی جریان h264/AVC با استفاده از فرمت فایل اختصاصی هستند. هدر یک فایل SEC با شماره مدل SRD-1670D شروع می شود. اطلاعات تاریخ و زمان در انتهای فایل درج شده است.

### فایل SEC را به AVI تبدیل کنید

فایل SEC را می توان با استفاده از FFmpeg به فرمت فایل استاندارد [AVI](/video/avi/) تبدیل کرد.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## منابع ##

- [Samsung and SEC Files](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

