---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Cفرم فایل SSat
linktitle: CSS
description: Lدر مورد فرمت فایل CSS و APIهایی که می توانند فایل CSS را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## فایل CSS چیست؟ ##

CSS (Cascading Style Sheets) فایل‌هایی هستند که نحوه نمایش عناصر HTML را بر روی صفحه، کاغذ و غیره توضیح می‌دهند. با HTML، می‌توانید سبک‌های جاسازی شده داشته باشید یا سبک‌ها را می‌توان در یک stylesheet خارجی تعریف کرد. برای جاسازی سبک ها، \ <style>\</style> برچسب ها استفاده می شود. شیوه نامه های خارجی در فایل هایی با پسوند css ذخیره می شوند. با CSS خارجی، می توانید آن را در چندین صفحه HTML قرار دهید تا سبک آن صفحات را به روز کنید. حتی یک فایل CSS را می توان برای استایل دادن به یک وب سایت کامل استفاده کرد.

## تاریخچه مختصر ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. این منجر به ایجاد CSS2 در نوامبر 1997 شد که به عنوان یک توصیه W3C در 12 مه 1998 منتشر شد. این نسخه از دستگاه های رسانه ای خاص مانند چاپگرها، فونت های قابل دانلود، جداول و موقعیت یابی عناصر پشتیبانی می کند. در ژوئن 1999، CSS3 به توصیه W3C تبدیل شد. این مستندات را به ماژول هایی تقسیم کرد که در آن هر ماژول دارای ویژگی های افزونه تعریف شده در CSS2 بود.

## نحوه استفاده از فایل های CSS ##

برای استفاده از یک فایل CSS، آن را در قسمت head سند HTML قرار دهید. شما از تگ پیوند برای درج فایل مانند شکل زیر استفاده می کنید.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

ویژگی *href* تگ پیوند حاوی مسیر فایل CSS است. با انجام این کار، استایل های کاربردی موجود در فایل CSS موجود در سند HTML اعمال می شود.

## نحو CSS ##

یک قانون CSS از دو جزء، انتخابگر و اعلان تشکیل شده است. یک انتخابگر به عنصری در سند HTML اشاره می کند. این می تواند یک تگ عنصر، نام کلاس، نام شناسه، چندین تگ که سلسله مراتب را نشان می دهد و غیره باشد. یک اعلان شامل تعریف سبک متشکل از ویژگی و مقدار است. ویژگی ویژگی عنصری را که می خواهید تغییر دهید مشخص می کند و مقدار مقدار جدید آن را مشخص می کند. هر قانون CSS می تواند چندین اعلان داشته باشد. در زیر نمونه ای از قانون CSS است.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

در مثال بالا، **h1** را به عنوان انتخابگر داریم که تمام تگ های h1 در سند HTML را انتخاب می کند. این قانون دارای دو اعلان است، یکی برای وزن فونت و دیگری برای رنگ. *font-weight* و *color* خواص و *700* و *forestgreen* به ترتیب مقادیر آنها هستند.

## مثال استفاده از CSS ##

در زیر نمونه سند HTML و شیوه نامه مورد استفاده برای استایل دادن به آن را نشان می دهد. تصویر مقایسه نیز برای مقایسه اسناد HTML سبک و ساده اضافه شده است

### سند HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS Stylesheet ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### مقایسه خروجی ###

سمت چپ تصویر سند HTML را بدون سبک های اعمال شده و سمت راست سند HTML را با سبک های اعمال شده نمایش می دهد.

{{< figure src="../CssExample.jpg" alt="تصویر نمونه" >}}

## منابع ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

