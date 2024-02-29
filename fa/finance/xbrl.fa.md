{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - فرمت فایل گزارشگری تجاری و مالی",
  "description":"درباره فرمت فایل XBRL و APIهایی که می‌توانند فایل‌های XBRL را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl-fa",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## فایل XBRL چیست؟

یک فایل با پسوند xbrl. (زبان گزارش‌دهی تجاری eXtensible) یک چارچوب آزادانه و جهانی برای تبادل اطلاعات تجاری است. اکنون به طور گسترده به عنوان یکی از فرمت های استاندارد استفاده می شود که جایگزین گزارش های کاغذی قدیمی با سوابق دیجیتال مفیدتر و دقیق تر شده است. داده های مبادله شده با استفاده از فایل های XBRL شامل دفتر کل، جزئیات مالی و ترازنامه است. از تگ های داده پشتیبانی می کند که امکان پردازش داده ها را از مرحله آماده سازی تا تجزیه و تحلیل انواع اطلاعات تجاری را فراهم می کند. فایل های XBRL را می توان با استفاده از نرم افزارهایی مانند Rivet Software Dragon View XBRL Viewer و API هایی مانند [Aspose.Finance](https://products.aspose.com/finance/) باز کرد.

## فرمت فایل XBRL

XBRL یک استاندارد بین المللی باز برای گزارش کسب و کار دیجیتال است که به طور گسترده در سطح جهانی استفاده می شود. این یک زبان مبتنی بر [XML](/web/xml/) است که از عناصر XBRL، معروف به برچسب، برای توصیف هر مورد از داده‌های کسب‌وکار برای فرمول‌بندی داده‌ها برای مرتب‌سازی و تجزیه و تحلیل گزارش استفاده می‌کند. مشخصات فرمت فایل XBRL توسط XBRL International, Inc، با [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) در حال حاضر در دسترس کاربران توسعه و منتشر شده است.

### ساختار سند XBRL

اطلاعات کامل در مورد [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) می تواند توسط برنامه نویسان برای نوشتن برنامه های کاربردی برای کار با این فرمت فایل ارجاع داده شود. یک XBRL از یک نمونه XBRL و مجموعه ای از طبقه بندی ها تشکیل شده است.

**` XBRL Instance` ** - نمونه XBRL با شروع می شود<xbrl> عنصر ریشه یک سند XML بزرگ می تواند حاوی بیش از یک نمونه XBRL باشد که در آن جاسازی شده است.

**`XBRL Taxonomy`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) به عنوان ساختار طرحواره XML و مجموعه ای از عناصر پیوندهای خارجی مستقیماً ارجاع داده شده تعریف می شود. یک طرح طبقه بندی مقیاس پذیر که ارجاعات پایگاه پیوند را نشان می دهد به شرح زیر است.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## منابع ##

* [XBRL - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/XBRL)

* [زبان گزارش‌دهی تجاری توسعه‌پذیر (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)


