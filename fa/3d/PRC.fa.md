---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Pفرم فایل RCat
linktitle: PRC
description: Lدر مورد فرمت فایل PRC و APIهایی که می توانند فایل PRC را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## فرمت های فایل PRC
پسوندهای prc. برای فرمت فایل فشرده سه بعدی نمایش محصول و قالب فایل کتاب الکترونیکی توسط MobiPocket استفاده می شود.

## فایل فشرده نمایندگی محصول (PRC) چیست؟

PRC (Product Representation Compact) یک فرمت فایل سه بعدی است که برای ذخیره، بارگیری و نمایش داده های سه بعدی به ویژه از سیستم های CAD (طراحی به کمک رایانه) بهینه شده است. این یک فایل باینری متوالی است که به روشی قابل حمل نوشته شده است. PRC می تواند برای جاسازی داده های سه بعدی در یک فایل PDF استفاده شود. PRC از اکثر ساختارهای اصلی CAD مانند مجموعه ها و قطعات، درختان موجودیت های سه بعدی، نمایش هندسه دقیق، نمایش مثلثی و نشانه گذاری پشتیبانی می کند. PRC از پسوند prc. استفاده می کند و نوع رسانه اینترنتی مورد استفاده *model/prc* است.

PRC یک فرمت فایل چند منظوره است که بر اساس استفاده از آن می توان با استفاده از فشرده سازی معمولی برای نمایش مستقیم داده های CAD یا با استفاده از فشرده سازی بالا برای کاهش اندازه فایل ذخیره کرد. داده های سه بعدی ذخیره شده در یک PDF با استفاده از فرمت PRC با برنامه های CAM و CAE قابل همکاری است.

### مشخصات فرمت فایل نمایش محصول فشرده (PRC).

یک فایل PRC دارای یک بخش هدر اصلی است که توسط یک یا چند ساختار فایل به دنبال آن یک فایل مدل در انتها قرار می گیرد. ساختار فایل دارای یک هدر است که با بخش های داده زیر همراه است:

- **Globals**: شامل ساختارها و رنگ های فایل ارجاع شده، سبک خط و سیستم مختصات برای هر موجودیت درختی ساختار فایل است.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tessellation**: شامل تمام داده های Tessellated (مثلثی) در موجودیت های برگ درخت (اقلام نمایش و نشانه گذاری) است.
- **هندسه**: شامل تمام داده های هندسی و توپولوژی دقیق موجودیت های برگ درخت (اقلام نمایشی) است.
- **هندسه اضافی**: حاوی داده های خلاصه هندسه است. این اجازه می دهد تا فایل تا حدی بدون بارگیری کل هندسه بارگذاری شود.

ساختار زیر ساختار یک فایل PRC معمولی است.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## فایل کتاب الکترونیکی MobiPocket با پسوند PRC چیست
فرمت فایل کتاب الکترونیکی که توسط یک شرکت فرانسوی به نام **Mobipocket** معرفی شده است نیز از پسوند .prc استفاده می کند. در ابتدا، Mobipocket یک برنامه رایگان برای چندین دستگاه هوشمند مانند رایانه های لوحی، رایانه های شخصی PDA و تلفن های هوشمند راه اندازی کرد. پسوند .prc در واقع با .mobi یکسان است، اما به ویژه برای PDA هایی که فقط از پسوندهای **.prc** یا **.pdb** پشتیبانی می کنند استفاده می شود.

### مشخصات فرمت فایل Mobipocket PRC
فرمت فایل MobiPocket PRC بر اساس استاندارد Open eBook با استفاده از XHTML است و همچنین می تواند شامل جاوا اسکریپت و فریم باشد. پشتیبانی از پرس و جوهای SQL بومی برای استفاده با پایگاه داده های جاسازی شده نیز در دسترس است.

Mobipocket Reader دارای یک کتابخانه صفحه اصلی است. خوانندگان می توانند صفحات خالی را در هر قسمت از کتاب وارد کنند و نقاشی های متغیر اضافه کنند. اشیایی مانند حاشیه نویسی ها، نشانک ها، اصلاحات، یادداشت ها و نقاشی ها از یک مکان قابل مدیریت هستند. تصاویر به فرمت GIF تبدیل می شوند و حداکثر اندازه آنها 64K است که برای تلفن های همراه با صفحه نمایش کوچک کافی است. Mobipocket Reader دارای نشانک های الکترونیکی و یک فرهنگ لغت داخلی است.

خواننده دارای یک حالت تمام صفحه برای خواندن و پشتیبانی از بسیاری از PDA ها، ارتباطات و تلفن های هوشمند است. محصولات Mobipocket از اکثر سیستم عامل های Palm، Windows، Symbian، BlackBerry پشتیبانی می کنند، اما از اندروید پشتیبانی نمی کنند. خواننده تحت Linux یا Mac OS X با استفاده از WINE کار می کند.

## منابع

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

