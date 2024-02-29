---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sفرمت فایل CSS - Sass Cascading Style Sheet
linktitle: SCSS
description: Lدر مورد فرمت فایل SCSS و APIهایی که می توانند فایل SCSS را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## فایل SCSS چیست؟ ##

SCSS دومین نحو از Sass (Syntactically Awesome Stylesheet) است که به جای تورفتگی از براکت استفاده می کند. SCSS به گونه ای طراحی شده است که یک فایل CSS3 معتبر یک فایل SCSS معتبر نیز باشد. فایل های SCSS با پسوند .scss ذخیره می شوند.

## چرا از SCSS ## استفاده کنید

از آنجایی که طراحی وب سایت ها پیچیده می شود و در نتیجه فایل های بزرگ [CSS](/web/css/) ایجاد می شود. نگهداری چنین فایل هایی سخت تر است. اینجاست که SCSS وارد می شود. SCSS متغیرها، تودرتو، میکسین ها، واردات و وراثت انتخابگر را در توسعه CSS معرفی می کند. این اضافات کار با طراحی را بسیار سرگرم کننده تر می کند.

## نحوه استفاده از فایل های SCSS ##

فایل‌های SCSS مستقیماً در سند [HTML](/web/html/) مانند CSS گنجانده نمی‌شوند. در عوض، فایل‌های SCSS به فایل‌های CSS که در فایل‌های HTML گنجانده شده‌اند، تبدیل می‌شوند. برای نصب SCSS روی سیستم خود، دستورالعمل های داده شده در [Official Sass Site](https://sass-lang.com/install) را دنبال کنید.
برای تبدیل SCSS به CSS، می توانید یک فایل SCSS از قبل ذخیره شده را تبدیل کنید یا مراقب تغییرات باشید و با ذخیره فایل تبدیل کنید. دستورات هر دو در زیر آورده شده است.

### یکبار تبدیل کنید ###

پارامتر اول فایل SCSS منبع و پارامتر دوم فایل CSS خروجی است.

```cmd
sass main.scss main.css
```

### مراقب تغییرات باشید ###

این دستور دارای یک پرچم *watch** اضافی است که دستور را در حال اجرا نگه می دارد و به محض ذخیره فایل SCSS، CSS خروجی تولید می شود.

```cmd
sass --watch main.scss main.css
```

## نحو SCSS ##

SCSS از متغیرها، تودرتو، میکسین ها، واردات، وراثت انتخابگر و غیره پشتیبانی می کند. در زیر نمونه هایی از این ویژگی ها آورده شده است.

### متغیرها ###

با استفاده از متغیرها، می توانید اطلاعات قابل استفاده مجدد مانند رنگ اصلی یا رنگ پس زمینه را برای دکمه ذخیره تنظیم کنید. اگر نیاز به تغییر آن اطلاعات دارید، این کار مفید است، فقط آن را در یک مکان تغییر دهید و هر کجا که استفاده شود به روز می شود.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS تولید شده**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### تودرتو ###

شما می توانید انتخابگرهای CSS را مشابه سلسله مراتب HTML قرار دهید. در مثال زیر، دهانه در داخل بلوک h1 قرار گرفته است.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS تولید شده**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### ترکیبات ###

میکس ها را می توان برای گروه بندی خواص مشابه با هم که در مکان های مختلف با هم استفاده می شود استفاده کرد. شما همچنین می توانید پارامترها را به mixins ارسال کنید.

**SCSS**

**اعلام میکسن**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**استفاده از میکسن**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**CSS تولید شده**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### توسعه دادن، گسترش ###

Extend/Inheritance در مواردی مفید است که ویژگی های یک انتخابگر باید با انتخابگر دیگری به اشتراک گذاشته شود. در مثال زیر، انتخابگر *.error-notice* تمام ویژگی های انتخابگر *.error-text* را می گیرد و ویژگی های حاشیه و padding را اضافه می کند.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**CSS تولید شده**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### وارد كردن ###

واردات می تواند در تفکیک نگرانی ها مفید باشد. می توانید استایل ها را به گونه ای تقسیم کنید که سبک های سرصفحه در یک فایل جداگانه، سبک های پاورقی در یک فایل جداگانه، تمام متغیرهای رنگی استفاده شده در استایل ها می توانند در یک فایل جداگانه باشند و غیره. با استفاده از این تکنیک، سبک ها مرتب می مانند شما فقط فایل ها را در فایل SCSS اصلی خود وارد کنید، همانطور که در مثال زیر نشان داده شده است. لازم نیست پسوند فایل را در دستورالعمل واردات مشخص کنید. Sass تمام فایل های SCSS را مستقیماً کامپایل می کند. برای جلوگیری از وارد کردن فایل‌هایی که مستقیماً کامپایل شوند، می‌توانید با اضافه کردن زیرخط(_) قبل از نام آن‌ها را جزئی کنید. می‌توانید جزئی‌هایی مشابه فایل‌های SCSS معمولی را بدون زیرخط وارد کنید.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

CSS خروجی دارای سبک های تمام فایل های وارد شده خواهد بود.

## منابع ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

