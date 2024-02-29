{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"بسته کاربردی ردیف داده"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DACPAC و APIهایی که می‌توانند فایل‌های DACPAC را ایجاد و باز کنند، بیاموزید.",
  "title": "DACPAC - بسته کاربردی ردیف داده",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-fac"
}
}،
  "lastmod": "2021-09-06"
}

## فایل DACPAC چیست؟

فایلی با پسوند dacpac. (مخفف Data Tier AppliCation Package) یک فایل پایگاه داده است که با برنامه Microsoft SQL Server ایجاد شده است و شامل مدل پایگاه داده برای نمایش اشیاء پایگاه داده است. از آنجایی که شامل مدل کامل پایگاه داده است، برای بازیابی یک پایگاه داده از جزئیات موجود در مدل استفاده می شود. فایل‌های DACPAC معمولاً به تیم‌های استقرار برای نصب در محل مشتری برای بازیابی پایگاه داده تحویل داده می‌شوند. اینها را می توان با باز کرد
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## فرمت فایل DACPAC - اطلاعات بیشتر

فایل‌های بسته داده DACPAC در واقع فایل‌های ZIP فشرده‌شده هستند که حاوی چندین فایل [XML](/web/xml/) هستند که حاوی اطلاعاتی درباره مدل پایگاه داده، مانند جداول و نماها هستند که برای بازیابی پایگاه داده استفاده می‌شوند. برای مشاهده محتویات فایل‌های DACPAC، نام فایل‌ها را از .dacpac به [.zip](/compression/zip/) تغییر دهید و بایگانی فشرده را با استفاده از هر ابزار رفع فشرده‌سازی استخراج کنید.

در زیر چند فایل موجود در یک فایل DACPAC وجود دارد.

 * [Content_Types].xml
```
<?xml version=1.0 encoding=utf-8?>
<Types
xmlns=http://schemas.openxmlformats.org/package/2006/content-types>
<Default Extension=xml ContentType=text/xml />
</Types>
```
 * DacMetadata.xml

```
<?xml version=1.0 encoding=utf-8?>
<DacType xmlns=http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02>
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
 * Origin.xml

 * model.xml

لازم به ذکر است که DACPAC حاوی DATA و سایر اشیاء در سطح سرور نیست. این فایل می تواند شامل تمام انواع شیئی باشد که ممکن است در پروژه SSDT نگهداری شوند.

## منابع

* [برنامه های ردیف داده - مزایا] (https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [استقرار یک برنامه ردیف داده - مایکروسافت](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
