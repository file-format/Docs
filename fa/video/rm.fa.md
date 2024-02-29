---
date: 2019-10-11
keywords: rm, .rm, rm file format, .rm file format, .rm extension, RealMedia file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lدر مورد فرمت فایل RM و APIهایی که می توانند فایل RM را ایجاد و باز کنند، کسب درآمد کنیدs.
title: Rفرم فایل Mat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## فایل RM چیست؟ ##

RealMedia یک فرمت کانتینر چندرسانه ای اختصاصی است که توسط RealNetworks توسعه یافته و از پسوند .rm استفاده می کند. با ترکیب [RealAudio (RA)](/audio/ra/) و [RealVideo(RV)](/video/rv/) برای پخش جریانی از طریق اینترنت استفاده می‌شود. این جریان ها دارای نرخ بیت ثابت هستند. برای نرخ بیت متغیر، RealNetworks فرمت RealMedia Variable Bitrate (RMVB) را توسعه داد. RealMedia برای پخش محتوا از طریق اینترنت مناسب است و به عنوان مثال می تواند برای پخش زنده تلویزیون استفاده شود.

## ساختار فایل RealMedia ##

یک فایل RealMedia از یک سری تکه تشکیل شده است که هر کدام دارای ساختار زیر است:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

در زیر انواع تکه های موجود در فایل RealMedia آمده است:

- **سرصفحه فایل RealMedia (.RMF)**: این باید اولین تکه در فایل RealMedia باشد. فقط یک قطعه RMF در یک فایل موجود است. حاوی اطلاعاتی در مورد تعداد هدرها است.
- **سرصفحه مشخصات فایل (PROP)**: حاوی اطلاعاتی در مورد خصوصیات کلی فایل RealMedia است. تنها یک تکه از این نوع در هر فایل RealMedia وجود دارد.
- **سرصفحه ویژگی های رسانه (MDPR)**: این قطعه حاوی اطلاعاتی در مورد ویژگی های جریان است. حاوی اطلاعاتی در مورد نوع جریان و کدک مورد استفاده است. یک تکه MDPR برای هر جریان در فایل وجود دارد.
- **Content description header (CONT)**: This chunk contains text information like the title or author for the content in the RealMedia file. This chunk is for information purposes only.
- **سرصفحه داده (DATA)**: این قطعه شامل گروهی از بسته های داده است.
- **سرصفحه فهرست (INDX)**: این تکه بعد از تمام تکه های DATA آمده و حاوی ورودی های فهرست است. یک فایل می تواند بیش از یک تکه INDX داشته باشد.

## پشتیبانی از فرمت های صوتی و تصویری ##

### فرمت های صوتی ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: سیپرو
- آشپز: آشپزی
- atrc: ATRAC3
- ralf: قالب RealAudio Lossless
- raac: LC-AAC
- راپ: HE-AAC

### فرمت های ویدئویی ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+، RV20
- RV30: پیش ساز H.264
- RV40: پیش ساز H.264، RV40
- RVTR: H.263+ (RV20)

## منابع ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

