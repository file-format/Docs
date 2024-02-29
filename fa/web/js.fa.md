---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Jفرم فایل Sat
linktitle: JS
description: Lدر مورد فرمت فایل JS و APIهایی که می توانند فایل JS را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## فایل JS چیست؟ ##

JS (جاوا اسکریپت) فایل هایی هستند که حاوی کد جاوا اسکریپت برای اجرا در صفحات وب هستند. فایل های جاوا اسکریپت با پسوند .js ذخیره می شوند. در داخل سند [HTML](/web/html/)، می‌توانید کد جاوا اسکریپت را با استفاده از \ جاسازی کنید <script>\</script> یک فایل JS را تگ کرده یا شامل شود. مانند فایل‌های [CSS](/web/css/)، فایل‌های JS را می‌توان در چندین سند HTML برای استفاده مجدد کد گنجاند. جاوا اسکریپت می تواند برای دستکاری HTML DOM استفاده شود.

## تاریخچه مختصر ##

جاوا اسکریپت اولین بار به عنوان بخشی از مرورگر Navigator در سپتامبر 1995 با نام LiveScript توسط Netscape ارسال شد. سه ماه بعد به جاوا اسکریپت تغییر نام داد. در سال 1996، مایکروسافت مترجم Navigator را برای ایجاد JScript مهندسی معکوس کرد. JScript با اینترنت اکسپلورر منتشر شد و بسیار متفاوت از جاوا اسکریپت بود.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 در سال 1998 منتشر شد، ECMAScript 3 در سال 1999، و کار بر روی ECMAScript 4 در سال 2000 آغاز شد اما هرگز به نتیجه نرسید.

جسی جیمز گرت در سال 2005 یک مقاله سفید منتشر کرد که در آن اصطلاح *آژاکس* را ابداع کرد. این از جاوا اسکریپت به عنوان ستون فقرات برای ایجاد برنامه‌های کاربردی وب استفاده می‌کرد که داده‌ها را در پس‌زمینه بارگیری می‌کرد و از بارگیری مجدد کامل صفحه جلوگیری می‌کرد. این منجر به ایجاد کتابخانه هایی مانند JQuery، Prototype، Dojo و غیره شد.

Google released the Chrome browser with the V8 JavaScript engine in 2008. در اوایل سال 2009، توافقی برای ترکیب تمام کارهای مرتبط و پیشبرد جاوا اسکریپت انجام شد. این منجر به انتشار استاندارد ECMAScript 5 در دسامبر 2009 شد.

## نحوه استفاده از فایل های JS ##

برای استفاده از یک فایل JS، آن را در سند HTML قرار دهید. شما از تگ پیوند برای درج فایل مانند شکل زیر استفاده می کنید.

```html
<script src="site.js"></script>
```

ویژگی *src* تگ *script* حاوی مسیر فایل JS است. با انجام این کار، قابلیت JS به سند HTML اضافه می شود.

## دستور JS ##

فایل‌های جاوا اسکریپت می‌توانند شامل متغیرها، عملگرها، توابع، شرایط، حلقه‌ها، آرایه‌ها، اشیاء و غیره باشند. در زیر مروری کوتاه بر نحو جاوا اسکریپت ارائه شده است.

- هر دستور با نقطه ویرگول (;) به پایان می رسد.
- از کلمه کلیدی *var* برای اعلام متغیرها استفاده کنید.
- Supports arithmetic operators ( + - * / ) برای محاسبه مقادیر.
- نظرات تک خطی با // اضافه می شوند و نظرات چند خطی با /* و */ احاطه می شوند.
- همه شناسه ها به حروف کوچک و بزرگ حساس هستند یعنی *modelNo* و *modelno* دو متغیر متفاوت هستند.
- توابع با استفاده از کلمه کلیدی *function* تعریف می شوند.
- آرایه ها را می توان با استفاده از براکت [] تعریف کرد.
- JS از عملگرهای مقایسه مانند ==، !=، >=، !== و غیره پشتیبانی می کند.
- کلاس ها را می توان با استفاده از کلمه کلیدی *class* تعریف کرد.

## مثال استفاده از JS ##

در زیر یک نمونه استفاده ساده از فایل جاوا اسکریپت را نشان می دهد.

### سند HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### کد JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## منابع ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

