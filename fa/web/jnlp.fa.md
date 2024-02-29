---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Jفرمت فایل NLP - فایل JNP چیستe?
linktitle: JNLP
description: Lدر مورد فرمت فایل JNLP و APIهایی که می توانند فایل JNLP را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## فایل JNLP چیست؟

یک فایل JNLP یک فایل Java Web Start (JWS) است که حاوی اطلاعات XML برای راه اندازی یک برنامه جاوا از طریق شبکه است. این در قالب پروتکل راه اندازی شبکه جاوا (JNLP) ذخیره شده است. این توسط فناوری Java Web Start (JWS) استفاده می شود که یک فناوری استقرار برنامه برای دانلود و اجرای یک برنامه کاربردی است. یک فایل JNLP حاوی آدرس راه دور سروری است که برنامه از آن دانلود و بر روی ماشین محلی راه اندازی می شود.

## فرمت فایل JNLP - اطلاعات بیشتر

فایل های JNLP به عنوان فایل های **[XML](/web/xml/)** ذخیره می شوند که در قالب متن قابل خواندن توسط انسان ذخیره می شوند. فایل XML دارای اطلاعاتی است که برای راه اندازی و اجرای یک برنامه جاوا از طریق شبکه استفاده می شود. JWS به شما امکان می دهد با کلیک کردن روی پیوند صفحه وب، برنامه ها را راه اندازی کنید. برنامه در صورتی دانلود می شود که قبلاً روی رایانه کاربر بارگیری نشده باشد.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. با این کار، فایل های JNLP دیگر پشتیبانی نمی شوند.

### چگونه فایل های JNLP را باز کنیم؟

برنامه هایی که می توانند **فایل های JNLP** را باز کنند عبارتند از **Microsoft Visual Studio Code**، **Notepad**، **Notepad++**، **Oracle Java Web Start**، **Karakun OpenWebStart**، و * *GitHub Atom**.

### مثال فایل JNLP

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**استفاده**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## چگونه فایل های JNLP را اجرا کنیم؟

با منسوخ شدن JWS، برنامه های توسعه یافته بر اساس فناوری JWS نمی توانند با آخرین نسخه جاوا اجرا شوند. با این حال، این برنامه‌های مبتنی بر JNLP را می‌توان با استفاده از OpenWebStart اجرا کرد که یک پیاده‌سازی مجدد منبع باز فناوری Java Web Start است. به موازات آخرین نسخه جاوا نصب می شود و متداول ترین ویژگی های Java Web Start و استاندارد JNLP را ارائه می دهد.

## منابع ##

* [Java Web Start چیست و چگونه راه اندازی می شود؟](https://www.java.com/en/download/help/java_webstart.html)

* [JNLP را با آخرین نسخه جاوا اجرا کنید] (https://openwebstart.com/)

* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


