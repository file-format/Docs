{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"html قابل توسعه"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "XHTML - فرمت فایل زبان نشانه گذاری فرامتن قابل توسعه",
  "description": "درباره فرمت فایل XHTML و APIهایی که می توانند فایل های XHTML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-fal"
}
}،
  "lastmod": "2019-09-10"
}

## فایل XHTML چیست؟

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. این فایل ها برای باز کردن یا مشاهده در یک مرورگر وب مناسب هستند. XHTML به گونه ای طراحی شده است که ساختارمندتر، اسکریپت نویسی کمتر و عمومی باشد. با استفاده از تمام امکانات موجود XML و بیشتر مستقل از دستگاه. XHTML مجموعه ای به طور کلی ارزشمند از عناصر و ویژگی ها را با گزینه های پسوند در ترکیب با شیوه نامه ها ارائه می دهد. ویژگی ها از مجموعه ویژگی های ابرداده استفاده می شوند. XHTML با تابع کردن همه عناصر ارائه **[HTML](/web/html/)** به شیوه نامه ها، انعطاف پذیری و دسترسی را فراهم می کند. استایل شیت ها نسبت به این عناصر نمایشی تطبیق پذیرتر هستند. مشخصات HTML 4.01، HTML5 و XHTML به صورت پویا توسط کنسرسیوم جهانی وب (W3C) در حال توسعه است.

## تاریخچه مختصر فرمت فایل XHTML

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. با این حال، در سال 2005، یک گروه کاری (WHATWG) تشکیل شد که هدف آن بهبود HTML معمولی مستقل از XHTML بود. WHATWG در نهایت کار بر روی HTML5 را به موازات XHTML 2 آغاز کرد.

## فرمت فایل XHTML

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. فایل‌های XHTML مبتنی بر XML هستند و هدف آن کار با عوامل کاربر بر اساس XML است. فایل های XHTML مطابق با XML هستند. ابزار استاندارد XML برای مشاهده، ویرایش و تایید فایل های XHTML استفاده می شود. برنامه های وابسته به مدل شی سند HTML یا مدل شی سند XML [DOM] می توانند از طریق اسناد XHTML کار کنند. امروزه با انتخاب XHTML، توسعه دهندگان محتوا می توانند از تمام مزایای مرتبط XML بدون نگرانی در مورد سازگاری رو به جلو یا عقب محتوای خود لذت ببرند.

مجموعه ای از عناصر مرتبط یک ماژول در XHTML می سازد. فرم ها یا ماژول جدول ممکن است حاوی فرم ها یا عناصر جدول مختلفی باشد که می توانند در یک صفحه وب نمایش داده شوند. هدف ماژولارسازی جداسازی عناصر HTML در مجموعه‌ای از عناصر مرتبط متعدد بود. به طوری که توسعه دهندگان محتوا می توانند از مزایای انتخاب ماژول برای انواع مختلف دستگاه ها استفاده کنند. علاوه بر این، ماژول ها به عوامل کاربر اجازه می دهند عناصر را بدون از دست دادن سازگاری با استاندارد XHTML انتخاب کنند. نیازهای تجزیه XHTML مانند XML است در حالی که HTML خودش را تمرین می کند.

### مطابقت سند

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. انطباق سند دو نوع است.

یک سند کاملاً منطبق بر پایه XML است که فقط به خدمات اجباری تعریف شده در این مشخصات نیاز دارد. برای فایل های XHTML باید معیارهای زیر رعایت شود:

* یک فایل باید با محدودیت های تعریف شده در DTD ها و در پیوست B مطابقت داشته باشد.

* عنصر پایه فایل باید html باشد.

* عنصر پایه فایل باید حاوی اعلان فضای نام XHTML باشد و باید به صورت زیر تعریف شود:


```
http://www.w3.org/1999/xhtml.
```

* عنصر پایه ممکن است به صورت زیر نوشته شود:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

زودتر از عنصر پایه، یک DOCTYPE باید اعلان شود، که شناسه عمومی آن باید به یکی از سه تعریف نوع سند (DTD) اشاره کند. شناسه سیستم ممکن است برای مطابقت با قراردادهای فعلی سیستم تغییر یابد.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

در اسناد XML، تعیین اعلانات XML در همه اسناد ضروری نیست. با این حال توسعه دهندگان محتوا وسوسه می شوند که از اعلان های XML در تمام اسناد XHTML خود استفاده کنند. این اعلان‌ها اجباری هستند یا زمانی که رمزگذاری کاراکتر سند با UTF-8 /16 متفاوت است یا هیچ کدگذاری توسط یک پروتکل حاکم مشخص نشده است. مثال زیر از یک سند XHTML، اعلان های XML را تعریف می کند

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

یک عامل کاربر منطبق باید قوانین زیر را رعایت کند:

* تجزیه و ارزیابی سند XHTML توسط یک عامل کاربر انجام می شود که سازگاری آن را با توصیه XML 1.0 تضمین می کند.

* در صورت تأیید اعتبار عامل کاربر، باید اعتبار اسناد را برای DTD های ارجاع شده آنها مطابق XML بررسی کند. هنگامی که فایل XHTML توسط عامل کاربر به عنوان XML عمومی پردازش می شود، ویژگی های نوع ID به عنوان شناسه های قطعه تایید می شود.


اگر یک عامل کاربر به یک عنصر ناشناخته برخورد کند، معیارهای اجباری که باید انجام دهد به شرح زیر است.

* محتویات آن عنصر ناشناخته را پردازش کنید

* ویژگی و مقدار آن را نادیده بگیرید

* از مقدار مشخصه ارائه شده به عنوان پیش فرض استفاده کنید.


هنگامی که عامل کاربر به یک اعلان مرجع موجودیت برخورد می کند که زودتر پردازش نشده است، باید به عنوان کاراکتر پردازش شود (با علامت & شروع می شود و با نقطه ویرگول ختم می شود). در طول پردازش محتوا، نویسه‌ها یا ارجاعات موجودیت شخصیتی که توسط عامل کاربر قابل پیش‌بینی هستند اما قابل بازگردانی نیستند، ممکن است از هر رندر جایگزینی استفاده کنند که معنای مشابهی را به همراه داشته باشد. در چنین حالتی، سند باید به گونه ای نمایش داده شود که کاربر متوجه شود که فرآیند رندر عادی نبوده است. برای پردازش فضای خالی، عامل کاربر باید به تعریف از کاراکترهای CSS [CSS2] نگاه کند.

## سازگاری با XHTML به عقب

The back ward compatibility of XHTML 1.  اسناد به خوبی با عوامل کاربر HTML 4 آشنا هستند، اگر قوانین مناسب رعایت شوند. XHTML 1.1 به جز حاشیه نویسی های روبی کاملاً سازگار است، حتی اگر مرورگرهای HTML 4 آنها را نادیده بگیرند. XHTML 2.0 نسبتاً کمتر سازگار است، با این وجود این مشکل تا حدی از طریق استفاده از اسکریپت برطرف شده است.

## منابع

* [تاریخچه XHTML: از دهه 1990 تا امروز] (https://www.brighthub.com/internet/web-development/articles/109224.aspx)


