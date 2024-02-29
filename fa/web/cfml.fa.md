{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML - ColdFusion Markup Language File",
  "description": "درباره اینکه یک فایل CFML چیست و APIهایی که می توانند فایل های CFML را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-fal"
}
},
  "lastmod": "2021-08-19"
}

## فایل CFML چیست؟

یک فایل با پسوند cfml. یک فایل ColdFusion Markup Language است که برای ایجاد صفحه وب استفاده می شود. این به مجموعه قوانینی اشاره دارد که برای تعریف نحوه توسعه برنامه ColdFusion توسط برنامه نویس استفاده می شود. ColdFusion یک زبان برنامه نویسی است که برای ایجاد برنامه های وب دو طرفه به سرعت و با فناوری های کمتر از سایر فناوری ها مانند [ASP](/web/asp/)، [PHP](/programming/php/) و غیره استفاده می شود. برخی از برنامه هایی که می توانند فایل های CML را باز کنند عبارتند از Adobe. ColdFusion 2018، Adobe ColdFusion Builder و Adobe Dreamweaver.

## فرمت فایل CFML - اطلاعات بیشتر

فایل‌های CFML فایل‌های نشانه‌گذاری هستند و حاوی عناصر وب در قالب تگ هستند. اینها فایل های متنی هستند که می توانند در هر ویرایشگر متنی باز و ویرایش شوند. فایل‌های CFML از چندین تگ تشکیل شده‌اند که شبیه به [HTML](/web/html/) هستند و معمولاً شامل یک تگ باز و بسته می‌شوند. این تگ ها همچنین می توانند شامل یک یا چند ویژگی باشند.

### نحو برچسب ها

در زیر نحو تعمیم یافته تگ های CFML آمده است.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

بیشتر تگ ها ویژگی ها را می پذیرند و به صورت زیر تعریف می شوند.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

برخی از این تگ ها نیز چندین ویژگی را با نحو زیر می پذیرند.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## مثال کد CFML

در اینجا یک مثال است که از یک تگ CFML واقعی - تگ cfoutput استفاده می کند:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## منابع

* [ColdFusion] (https://www.quackit.com/coldfusion/tutorial/)


