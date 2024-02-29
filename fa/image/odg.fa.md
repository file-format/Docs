{
  "date": "2019-10-11",
  "keywords": [
"فایل odg",
"فرمت فایل odg",
"فایل odg چیست",
"فایل",
"مثال odg",
"پسوند فایل odg",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل ODG",
  "description": "درباره فرمت فایل ODG و APIهایی که می‌توانند فایل‌های ODG را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-fag"
}
}،
  "lastmod": "2019-09-10"
}

## فایل ODG چیست؟

فرمت فایل ODG توسط برنامه Draw Apache OpenOffice برای ذخیره عناصر طراحی به عنوان یک تصویر برداری استفاده می شود. از مشخصات فرمت فایل مبتنی بر XML پیروی می کند که توسط استانداردهای پیشرفته اطلاعات ساختاری (OASIS) مشخص شده است. ODG نقشه ها را به عنوان تصاویر برداری با استفاده از نقاط، خطوط و منحنی ها نشان می دهد. علاوه بر OpenOffice، LibreOffice و سایر برنامه ها نیز از کار با فرمت فایل ODG پشتیبانی می کنند. سایر قالب‌های پشتیبانی شده توسط OpenOffice، برای مثال، عبارتند از: [ODT](/word-processing/odt/)، ODF، [ODP](/presentation/odp/) و [ODS](/spreadsheet/ods/).


## مشخصات فرمت فایل ODG

فرمت فایل ODG بر اساس فرمت OpenDocument است که فرمت سند XML ساختار یافته با طرحواره ای کاملاً تعریف شده است.
هر جزء ساختاری یک فرمت OpenDocument با عنصری نشان داده می شود که دارای ویژگی های مرتبط است. ساختار مبتنی بر XML برای همه انواع سند مانند سند متنی، صفحه گسترده یا فایل طراحی مشترک است. یک سند می تواند شامل سبک های مختلف باشد. ساختار فایل OpenDocument از عناصر زیر تشکیل شده است.
  * ریشه سند
  * MetaData سند
  * عناصر بدنه و انواع سند
  * تنظیمات برنامه
  * اسکریپت ها
  * اعلامیه های صورت قلم
  * سبک ها
  * سبک‌ها و طرح‌بندی صفحه

##  ریشه های سند ##

یک عنصر ریشه سند شامل کل سند است و عنصر اصلی یک فایل در قالب OpenDocument است. همان نوع عناصر ریشه سند برای همه انواع سند مانند متن، اسناد، صفحات گسترده و اسناد ترسیمی قابل اعمال است.

### عناصر ریشه ###
یک سند XML تنها با عنصر ریشه خود نشان داده می شود. پنج عنصر مختلف ریشه پشتیبانی شده به شرح زیر است.

`<office:document> ` - سند آفیس را در یک سند singleXML کامل کنید.
`<office:document-content> ` - محتوای سند و سبک های خودکار مورد استفاده در محتوا.
`<office:document-styles> ` - سبک های مورد استفاده در محتوای سند و سبک های خودکار مورد استفاده در خود سبک ها.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - تنظیمات خاص برنامه، مانند اندازه پنجره یا اطلاعات چاپگر.

### MetaData سند ODG ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### عنصر بدنه و انواع سند ###
بدنه سند نوع محتوای موجود در سند را با استفاده از عنصر نوع سند نشان می دهد. این انواع اسناد عبارتند از:
  * اسناد متنی
  * ترسیم اسناد
  * اسناد ارائه
  * اسناد صفحه گسترده
  * اسناد نمودار
  * اسناد تصویری

### تنظیمات برنامه ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * تنظیمات سند به عنوان مثال چاپگر پیش فرض
  * مشاهده تنظیمات به عنوان مثال سطح زوم

### اسکریپت ها ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### اعلامیه های صورت قلم ###

اعلان چهره فونت حاوی اطلاعاتی در مورد فونت های استفاده شده توسط نویسنده یک سند است. این اطلاعات به یافتن این فونت ها در سیستم های دیگر کمک می کند.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### سبک ###
سبک های زیر توسط قالب OpenDocument پشتیبانی می شوند.

«سبک‌های رایج» - به نمایش‌های XML چنین سبک‌هایی، سبک‌ها گفته می‌شود
«سبک‌های خودکار» - حاوی ویژگی‌های قالب‌بندی است که در نمای رابط کاربری یک سند، به یک شی مانند یک پاراگراف اختصاص داده می‌شود.
Mater Styles - یک سبک رایج که حاوی اطلاعات قالب‌بندی و محتوای اضافی است که هنگام اعمال سبک همراه با محتوای سند نمایش داده می‌شود. نمونه ای از یک سبک اصلی صفحات اصلی هستند.

## منابع ##
  * [فرمت سند باز OASIS برای برنامه های اداری] (https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [فرمت OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

