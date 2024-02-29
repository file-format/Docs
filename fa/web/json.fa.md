---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Jفرمت فایل SON - فایل JSON چیستe?
linktitle: JSON
description: Lدر مورد فرمت فایل JSON و APIهایی که می توانند فایل JSON را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## فایل JSON چیست؟

JSON (JavaScript Object Notation) یک فرمت فایل استاندارد باز برای به اشتراک گذاری داده است که از متن قابل خواندن توسط انسان برای ذخیره و انتقال داده ها استفاده می کند. فایل‌های JSON با پسوند json. ذخیره می‌شوند. JSON به قالب بندی کمتری نیاز دارد و جایگزین خوبی برای [XML](/web/xml/) است. JSON از جاوا اسکریپت مشتق شده است اما یک فرمت داده مستقل از زبان است. تولید و تجزیه JSON توسط بسیاری از زبان های برنامه نویسی مدرن پشتیبانی می شود. *application/json* نوع رسانه ای است که برای JSON استفاده می شود.

## فرمت فایل JSON - تاریخچه مختصر

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON بر اساس استاندارد ECMA-262 3rd Edition—دسامبر 1999 که زیرمجموعه ای از جاوا اسکریپت است.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. در نوامبر 2017، ISO/IEC 21778:2017 به عنوان یک استاندارد بین المللی منتشر شد. RFC 8259 در 13 دسامبر 2017 توسط The Internet Engineering Task Force منتشر شد که نسخه فعلی استاندارد اینترنت STD 90 است.

## ساختار فایل JSON

داده‌های JSON به صورت جفت **کلید/مقدار** نوشته می‌شوند. کلید و مقدار با یک کولون (:) در وسط با کلید در سمت چپ و مقدار در سمت راست از هم جدا می شوند. جفت های کلید/مقدار مختلف با کاما(،) از هم جدا می شوند. کلید یک رشته است که با علامت های نقل قول دوتایی احاطه شده است، به عنوان مثال نام. مقادیر می توانند از انواع زیر باشند.

- شماره.
- رشته: دنباله ای از کاراکترهای یونیکد که با علامت های نقل قول دوتایی احاطه شده اند.
- `Boolean`: درست یا نادرست.
- «آرایه»: برای مثال، فهرستی از مقادیر احاطه شده با پرانتز مربع

``json
[سیب، موز، پرتقال]
```

- شیء: مجموعه ای از جفت های کلید/مقدار احاطه شده توسط بریس های فرفری، برای مثال

``json
{name: جک، سن: 30، favoriteSport : فوتبال}
```

اشیاء JSON همچنین می توانند برای نمایش ساختار داده ها تودرتو شوند. در زیر مثالی از یک شی JSON ارائه شده است.

### نمونه فرمت JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## حداکثر اندازه فایل JSON چقدر است؟

عملا هیچ محدودیتی برای حداکثر اندازه یک فایل JSON وجود ندارد. می تواند به اندازه فضای مورد نیاز محتویات ذخیره شود.

وقتی صحبت از استفاده از فرمت فایل JSON برای انتقال داده ها از طریق اینترنت می شود، باید مراقب منابع موجود رایانه بود. اگر داده های بزرگ JSON منتقل شود، اگر مرورگر مشتری حافظه محدودی داشته باشد، انتقال تحت تأثیر قرار می گیرد.


هیچ محدودیت سختی بر اساس مشخصات تعریف نشده است، اما باید مراقب باشید که منابع رایانه های کاربران خود را تمام نکنید، زیرا به سرعت تجربه کاربری آنها را کاهش می دهد و آنها احتمالاً برنامه شما را رها می کنند.

## JSON در مقابل XML

**XML** یکی دیگر از فرمت های رایج و پرکاربرد فایل برای تبادل داده از طریق اینترنت است. وقتی صحبت از تبادل داده بین برنامه‌ها می‌شود، توسعه‌دهندگان می‌توانند از هر دو فرمت فایل XML و JSON استفاده کنند. با این حال، JSON به دلایل زیر به عنوان راحت ترین راه برای تبادل داده بین برنامه ها از طریق اینترنت پذیرفته شده است.

 1. JSON در مقایسه با فرمت‌های فایل XML، نمای واضح و خواندنی داده‌ها را آسان‌تر می‌دهد
 1. JSON سربار انتقال داده از طریق اینترنت را کاهش می دهد زیرا تعداد کاراکترهای کمتری برای تعریف مجموعه داده های مشابه در مقایسه با XML دارد.
 1. زبان های برنامه نویسی مدرن تجزیه کننده های داخلی را برای تجزیه پاسخ JSON در وب ارائه می کنند.

## سوالات متداول

 * **فایل JSON برای چه مواردی استفاده می شود؟** فرمت فایل JSON را می توان به عنوان یک فرمت فایل میانی برای ذخیره داده های تولید شده مانند فرم ارسال شده در یک وب سایت استفاده کرد. همچنین به عنوان فایل فرمت داده برای هر زبان برنامه نویسی استفاده می شود و قابلیت همکاری بین انواع مختلف داده ها را فراهم می کند.
 * ** آیا فایل JSON و XML یکسان است؟ ** واقعاً اینطور نیست. JSON با XML تفاوت دارد زیرا JSON کوتاه‌تر است، می‌توان آن را سریع خواند و درست کرد، می‌تواند از آرایه‌ها استفاده کند و از تگ پایان استفاده نمی‌کند.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **چگونه JSON را به PDF تبدیل کنیم؟** می توانید از برنامه های آنلاین مانند Asopse.app برای Cells به [تبدیل فایل JSON به PDF] (https://products.aspose.app/cells/conversion/json-to-) استفاده کنید pdf).
 * **چگونه یک فایل JSON را در Word باز کنیم؟** می توانید از برنامه های آنلاین مانند Aspose.app برای Words برای [تبدیل فایل JSON به Word] (تبدیل فرمت JSON به WORD در اندروید از طریق جاوا) استفاده کنید.

## آیا می دانستید؟

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## منابع

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

