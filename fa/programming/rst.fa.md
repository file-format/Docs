{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل RST- فایل متنی بازسازی شده",
  "description": "با فرمت فایل RST و APIهایی که می توانند فایل های RST را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-fat"
}
},
  "lastmod": "2022-04-11"
}

## فایل RST چیست؟

فایل RST یک فرمت فایل مستندات فنی است که عمدتاً در جامعه برنامه نویسی پایتون استفاده می شود. این یک فایل متنی است که به زبان نشانه گذاری reStructuredText نوشته شده است که سبک ها و قالب بندی را در اسناد متنی ساده برای تولید اسناد اعمال می کند. فایل‌های RST از نظرات و اطلاعات دیگر در کد برنامه‌های پایتون برای ایجاد مستندات فنی برنامه استفاده می‌کنند. با این حال، اینها همچنین می توانند حاوی متنی باشند که می توانند به صفحات وب ساده و [eBooks](/ebook/) تبدیل شوند. برای باز کردن فایل های RST می توان از ویرایشگرهای متنی مانند Github Atom، GNU Emacs (cross-platform)، Microsoft Notepad (ویندوز)، Apple TextEdit (Mac) و Vim (Linux) استفاده کرد.

## فرمت فایل RST

فایل های RST حاوی کدهایی هستند که به زبان نشانه گذاری reStructuredText نوشته شده است. این بخشی از پروژه Docutils Python Doc-SIG (گروه علایق ویژه اسناد) است که مجموعه‌ای از ابزارها را برای پایتون مشابه Javadoc برای جاوا فراهم می‌کند. تجزیه کننده فرمت فایل RST در Docutils تعبیه شده است و می تواند اطلاعات را از برنامه های پایتون برای قالب بندی آنها در اسناد برنامه استخراج کند.

### reStructuredText مثال RST

بیایید یک متن نمونه نوشته شده در فرمت فایل RST را به صورت زیر در نظر بگیریم.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

هنگامی که این متن به یک پردازنده rST مانند Docutils وارد می شود، خروجی به صورت زیر است.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## ارجاع ##

* [reStructuredText - توسط ویکی پدیا](https://en.wikipedia.org/wiki/ReStructuredText)


