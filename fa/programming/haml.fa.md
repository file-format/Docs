{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل HAML - فایل کد منبع Haml",
  "description": "درباره فرمت فایل HAML و APIهایی که می توانند فایل HAML را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-fal"
}
},
  "lastmod": "2022-04-07"
}

## فایل HAML چیست؟

فایل HAML یک فایل زبان نشانه گذاری انتزاعی HTML است که حاوی کد منبع نوشته شده به زبان [Haml](https://haml.info/) است. می توان از آن به عنوان جایگزینی برای ERB (اسکریپت های قالب روبی) استفاده کرد. فایل HAML حاوی کد منبع الگو است که برای تولید HTML یک سند وب است. فایل های ERB را می توان با جایگزینی این فایل ها در پوشه app/views به Haml با تغییر پسوند فایل جایگزین کرد. فایل های HAML را می توان با هر ویرایشگر متنی مانند Microsoft Notepad، Notepad++، Apple TextEdit، باز کرد.

## فرمت فایل HAML

فایل‌های HAML فایل‌های منبعی هستند که به عنوان فایل‌های متنی ساده روی دیسک ذخیره می‌شوند. این شامل کد نوشته شده در نحو HAML است. HAML تگ های **<>** را با علامت **%** جایگزین می کند تا کد را ساده تر و آسان تر کند. همانطور که در مثال ساده زیر نشان داده شده است، فایل های ERB قابل تعویض توسط HAML هستند.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### مثال HAML

در زیر نمونه ای از Hello World از HAML آورده شده است.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
که به خروجی HTML زیر رندر می شود.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## منابع

* [HAML - Github](https://github.com/haml/haml)


