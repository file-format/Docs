---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sفرم فایل assat
linktitle: Sass
description: Lدر مورد فرمت فایل Sass و APIهایی که می توانند فایل Sass را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## فایل SASS چیست؟ ##

Sass (سبک شیت های نحوی عالی) یک زبان برنامه نویسی پیش پردازنده است. در [CSS](/web/css/) کامپایل شده و با پسوند .sass ذخیره می شود. Sass از دو نحو تشکیل شده است، اصلی بر اساس تورفتگی هایی که از پسوند .sass استفاده می کند و SCSS جدیدتر با قالب بندی بلوکی مانند CSS که از پسوند .scss استفاده می کند.

## چرا از Sass ## استفاده کنید

Sass واقعاً در حفظ استایل ها مفید است زیرا ویژگی های زیادی مانند معرفی متغیرها، تودرتو، میکس ها، واردات و وراثت انتخابگر را ارائه می دهد که کار با سبک ها را سرگرم کننده می کند.

## نحوه استفاده از فایل های SASS ##

فایل‌های SASS مستقیماً در سند [HTML](/web/html/) گنجانده نمی‌شوند، بلکه به فایل‌های CSS که در فایل‌های HTML موجود هستند تبدیل می‌شوند. شما می توانید Sass سیستم خود را با دنبال کردن دستورالعمل های داده شده در [Official Sass Site](https://sass-lang.com/install) نصب کنید.

Sass را می توان با تبدیل یک فایل SASS از قبل ذخیره شده یا با مشاهده تغییرات و تبدیل فایل به CSS تبدیل کرد. دستورات هر دو در زیر آورده شده است.

### یکبار تبدیل کنید ###

پارامتر اول دستور فایل SASS مبدا و پارامتر دوم فایل CSS خروجی است.

```cmd
sass main.sass main.css
```

### مراقب تغییرات باشید ###

دستور فوق را می توان با یک پرچم *watch* اضافی اجرا کرد که دستور را در حال اجرا نگه می دارد و به محض ذخیره فایل Sass، CSS خروجی تولید می شود.

```cmd
sass --watch main.sass main.css
```

## Sass Syntax ##

Sass از متغیرها، تودرتو، میکسین، واردات، وراثت انتخابگر و غیره پشتیبانی می کند. در زیر نمونه هایی از این ویژگی ها آورده شده است.

### متغیرها ###

از متغیرها می توان برای تنظیم اطلاعات قابل استفاده مجدد مانند رنگ اصلی یا بالشتک برای یک دکمه استفاده کرد. این می تواند مفید باشد اگر در آینده نیاز به تغییر آن اطلاعات داشته باشید، فقط آن را در یک مکان تغییر دهید و در همه جا به روز شود.

**ساس**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

انتخابگرهای CSS را می توان مشابه سلسله مراتب HTML تو در تو قرار داد. در مثال زیر، دهانه در داخل بلوک h1 تودرتو شده است.

**ساس**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

مخلوط ها برای گروه بندی خواص مشابه با هم استفاده می شوند که در مکان های مختلف استفاده می شوند. Mixin ها همچنین از پارامترها پشتیبانی می کنند.

**ساس**

**اعلام میکسن**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**استفاده از میکسن**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Extend/Inheritance می تواند در مواردی مفید باشد که ویژگی های یک انتخابگر باید با انتخابگر دیگری به اشتراک گذاشته شود. در مثال زیر، انتخابگر *.error-notice* تمام ویژگی های انتخابگر *.error-text* را می گیرد و ویژگی های حاشیه و padding را اضافه می کند.

**ساس**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

اگر سبک‌های خود را بر اساس عملکرد یا هر ساختار دیگری که دنبال می‌کنید در فایل‌های مختلف ساختار دهید، وارد کردن می‌تواند مفید باشد. می‌توانید همه این فایل‌ها را در یک فایل SASS اولیه که بعداً به CSS تبدیل می‌شود، وارد کنید. هنگام وارد کردن، نیازی نیست پسوند فایل را در دستورالعمل واردات مشخص کنید. Sass تمام فایل های SASS را مستقیماً کامپایل می کند. برای جلوگیری از وارد کردن فایل‌ها برای کامپایل شدن مستقیم، می‌توانید با اضافه کردن زیرخط(_) در ابتدای نام، آنها را جزئی کنید. جزئی ها مشابه فایل های Sass معمولی وارد می شوند.

**ساس**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

CSS خروجی دارای سبک های تمام فایل های وارد شده خواهد بود.

## منابع ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

