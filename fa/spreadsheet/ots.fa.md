{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"فایل",
"افزونه",
"فرمت فایل",
"برتری داشتن",
"صفحه گسترده"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل OTS و APIهایی که می توانند فایل های OTS را ایجاد و باز کنند، بیاموزید.",
  "title": "OTS - فرمت فایل الگوی صفحه گسترده OpenDocument",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-fas"
}
}،
  "lastmod": "2021-01-19"
}

## فایل OTS چیست؟

یک فایل با پسوند .ots یک فایل الگوی صفحه گسترده OpenDocument است که با نرم افزار کاربردی Calc موجود در آپاچی اوپن آفیس ایجاد می شود. نرم افزار کاربردی Calc مشابه اکسل است که در مایکروسافت آفیس موجود است. فرمت فایل OTS برای ایجاد الگوهایی استفاده می شود که حاوی تنظیمات از پیش تعریف شده مربوط به سبک ها، فونت، داده ها، طرح صفحه گسترده و قالب بندی هستند. فایل‌های OTF دارای «mime-type application/vnd.oasis.opedocument.spreadsheet-template» هستند. این فایل‌های الگو را می‌توان به عنوان نقطه شروع برای تولید و ذخیره فایل‌های داده واقعی که در [ODS file format](/spreadsheet/ods/) ذخیره می‌شوند، استفاده کرد. فایل های OTS را می توان با برنامه هایی مانند OpenOffice و LibreOffice استفاده کرد.

## فرمت فایل OTS

فایل‌های OTS در فرمت فایل مبتنی بر OpenDocument XML OASIS ذخیره می‌شوند که شامل مجموعه‌ای از چندین سند فرعی با یک بسته به‌عنوان بایگانی [ZIP](/compression/zip/) است. هر آرشیو zip بخشی از سند کامل را ذخیره می کند و هر سند فرعی جنبه خاصی از سند را ذخیره می کند. به عنوان مثال، یک سند فرعی حاوی اطلاعات سبک و یک سند فرعی حاوی محتوای سند است. یک سند ODF معمولی دارای اجزای زیر است:

### OTS Content.xml

فایل content.xml حاوی محتوای واقعی سند است. با این حال، این شامل داده های باینری مانند تصاویر نمی شود.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml از فرمت فایل OTS

فایل styles.xml حاوی اطلاعات استایل است و به شدت برای قالب بندی و چیدمان استفاده می شود. انواع سبک ها عبارتند از:

 * سبک های پاراگراف
 * سبک های صفحه
 * سبک های شخصیت
 * سبک های قاب
 * لیست سبک ها

### Meta.xml

فایل meta.xml حاوی اطلاعاتی درباره فراداده فایل مانند نویسنده، آخرین تاریخ اصلاح و غیره است.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

فایل settings.xml شامل تنظیمات سطح سند مانند ضریب بزرگنمایی و موقعیت مکان نما است.

## منابع ##

* [مشخصات OpenDocument 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument - توسط Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


