---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Pفرمت فایل YM - PYM Macro Preprocessor File
linktitle: PYM
description: Lدر مورد فرمت فایل PYM و APIهایی که می توانند فایل PYM را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## فایل PYM چیست؟

فایل PYM یک فایل پیش پردازشگر ماکرو بر اساس زبان برنامه نویسی پایتون است. این توسط VRVis Research توسعه یافته و میانبرهای ماکرو را ذخیره می کند. هنگامی که فایل PYM توسط مرحله پیش پردازش مفسر پایتون تفسیر می شود، این میانبرها به عنوان جایگزینی برای متن کامل خود گسترش می یابند. علاوه بر این، سومین عملیات اختیاری که می تواند توسط یک پیش پردازنده ماکرو انجام شود، گنجاندن فایل است. فایل های PYM را می توان در ویرایشگرهای متنی مانند Notepad، Notepad++، Apple TextEdit و VI در لینوکس باز کرد.

## فرمت فایل PYM

فایل های PYM به عنوان فایل های متنی ساده روی دیسک ذخیره می شوند. یک فایل PYM همچنین می‌تواند شامل فایل‌های دیگری با استفاده از دستور #include باشد.

### نحو PYM

عبارات PYM بین نشانگرهای #begin python و #end python مطابق شکل زیر گنجانده شده است.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### گسترش ماکرو PYM

بسط ماکرو PYM با دو دنباله یعنی <[ و ]> نشان داده می شود. اینها تگ های html خاصی هستند و می توانند در هر نقطه از یک خط ظاهر شوند. یک مثال کوچک PYM به شرح زیر است.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

خروجی اجرای این کار از طریق PYM به شرح زیر است:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## منابع ##

 * [PYM - یک پیش پردازنده ماکرو مبتنی بر پایتون](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [مترجمان PYM](https://github.com/interpreters/pym)

