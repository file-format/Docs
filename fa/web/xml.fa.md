{
  "date": "2019-10-11",
  "keywords": [
"xml",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"زبان نشانه گذاری توسعه پذیر"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل XML",
  "description": "درباره فرمت فایل XML و APIهایی که می توانند فایل های XML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xm-fal"
}
},
  "lastmod": "2019-09-10"
}

## فایل XML چیست؟

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## فرمت فایل XML

فرمت فایل XML بر اساس مدل شی سند XML (DOM) است که یک API برنامه نویسی برای اسناد HTML و XML است. XML DOM یک روش استاندارد برای دسترسی و دستکاری عناصر سند XML تعریف می کند. این یک نمای ساختار درختی از یک سند XML ایجاد می کند که می تواند برای دسترسی به تمام عناصر از طریق درخت DOM استفاده شود. عناصر موجود را می توان تغییر/حذف کرد و همچنین عناصر جدیدی را می توان در درخت XML ایجاد کرد. هر عنصر یک سند XML یک گره نامیده می شود. XML DOM مانند تصویر زیر است.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### رویکرد جهانی XML

قدرت XML با ساده‌سازی انتقال داده و تغییرات پلت‌فرم، آن را به زبانی جهانی برای ارتباط داده‌ها از طریق شبکه تبدیل می‌کند. این همچنین باعث می شود که تبادل داده ها بین سیستم های ناسازگار با ذخیره داده ها در قالب متن ساده امکان پذیر باشد. HTML برای نمایش داده ها در وب است، در حالی که XML برای تبادل داده است. جفت‌های برچسب نشانه‌گذاری مورد استفاده در XML عناصر کلیدی ساختار را برای خواندن برنامه‌ها تعریف می‌کنند.

## مثال XML

در زیر یک مثال ساده از کاتالوگ سی دی است که در آن هر رکورد حاوی اطلاعاتی در مورد سی دی ها مانند هنرمند، کشور، شرکت، قیمت و سال تولید است.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## منابع

* [XML - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/XML)


