---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: Lدر مورد فرمت فایل SPC و APIهایی که می توانند فایل SPC را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## فایل SPC چیست؟

یک فایل با پسوند spc. یک فایل گواهی امنیتی دیجیتال است که با فرمت PKCS # 7 ایجاد شده است. چندین برنامه، این فایل های گواهی را برای تبادل امن اطلاعات ایجاد می کنند. تعداد کمی از این برنامه ها عبارتند از OpenSSL و برنامه Signcode.exe همراه با .NET Framework مایکروسافت. مانند سایر فایل‌های گواهی مانند [.cer](/web/cer/)، [.p7c](/web/p7c/) و [.ssp](/web/ssp/)، فایل‌های SPC حاوی اطلاعات کلید عمومی هستند که با یک کلید خصوصی رمزگذاری شده‌اند. این کلید عمومی را می توان به صورت عمومی با کاربران به اشتراک گذاشت در حالی که کلید خصوصی محرمانه است.

## فرمت فایل SPC - اطلاعات بیشتر

فایل‌های SPC به‌عنوان فایل‌های باینری در دیسک ذخیره می‌شوند که می‌توانند در هر ویرایشگر متنی باز شوند، اما توسط انسان قابل خواندن نیستند. اینها بر اساس آخرین نسخه PKCS # 7 هستند که [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315) در دسترس است.

## منابع

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [مرجع SSP] (https://scalate.github.io/scalate/documentation/ssp-reference.html)


