{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"زبان صفحه سبک قابل توسعه"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل XSLT",
  "description": "درباره فرمت فایل XSLT و APIهایی که می‌توانند فایل‌های XSLT را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-fat"
}
},
  "lastmod": "2021-01-20"
}

## فایل XSLT چیست؟

یک فایل با پسوند xslt. یک فایل تغییر شکل زبان قابل توسعه است که برای تبدیل و استایل دادن به یک فایل XML با استفاده از دستورالعمل‌های XSL استفاده می‌شود. این قالب برای تبدیل اسناد XML به فرمت های خروجی استاندارد مانند یک سند متنی یا صفحه وب .html استفاده می شود. این تبدیل یک سند جدید بر اساس محتوای سند XML موجود ایجاد می کند. XSLT به لحاظ نظری قادر به محاسبات دلخواه است.

## فرمت فایل XSLT

فرمت فایل XLST حاوی دستورالعمل های تبدیل در قالب متن ساده است که در هر ویرایشگر متنی قابل مشاهده است. سه تجدید نظر در این زبان صورت گرفته است.

* `XSLT 1.0` - XSLT 1.0 به عنوان یک توصیه W3C در نوامبر 1999 منتشر شد.

* `XSLT 2.0` - شامل تغییراتی مانند دستکاری رشته با استفاده از عبارات منظم، توابع و عملگرها برای دستکاری تاریخ، زمان و مدت زمان، اسناد خروجی متعدد، گروه بندی، و سیستم نوع غنی تر و بررسی نوع قوی تر.

* `XSLT 3.0` - در 8 ژوئن 2017 بخشی از توصیه W3C شد و ویژگی‌های اصلی جدید شامل تبدیل جریان، بسته‌هایی برای بهبود ماژولار بودن شیت‌های سبک بزرگ، مدیریت بهتر خطاهای پویا با، به عنوان مثال، یک دستورالعمل xsl:try، است. و پشتیبانی از نقشه ها و آرایه ها، XSLT را قادر می سازد تا JSON و همچنین XML را مدیریت کند.


### مثال XSLT

مثال زیر از [w3schools](https://www.w3schools.com/xml/xsl_intro.asp) گرفته شده است.
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## منابع ##

* [XSLT - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/XSLT)

* [عناصر XSLT](https://en.wikipedia.org/wiki/XSLT_elements)


