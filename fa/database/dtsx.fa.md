{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"فایل های پایگاه داده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل DTSX و API هایی که می توانند فایل های DTSX را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل DTSX - فایل تنظیمات DTS سرور SQL",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-fax"
}
},
  "lastmod": "2020-08-12"
}

## فایل DTSX چیست؟

یک فایل با پسوند .dtsx (Data Transformation Services Package XML) یک فایل خدمات تبدیل داده (DTS) است که توسط Microsoft SQL برای ارجاع به مراحل/قوانین انتقال داده برای انتقال داده ها از یک پایگاه داده به پایگاه داده دیگر استفاده می شود. این شامل تغییرات و هر مرحله پردازش اختیاری است که ممکن است در طول انتقال داده بین نقطه مبدأ و مقصد مورد نیاز باشد. SQL Server Integration Services (SSIS)، جزء Microsoft SQL Server، از فایل های DTSX برای شناسایی مراحل پردازش داده ها بین سرورهای پایگاه داده استفاده می کند. فایل های DTSX را می توان با Microsoft SQL Server 2019 باز کرد.

## فرمت فایل DTSX

حرکت داده ها بین سرورهای پایگاه داده نیازمند قوانین و مراحل پردازش برای اطمینان از یکپارچگی داده ها در طول این عملیات است. SSIS تضمین می‌کند که همه این فعالیت‌ها، برای انتقال و مطابقت داده‌ها از منابع مختلف در یک سازمان، به راحتی انجام می‌شوند. اینجاست که DTSX می آید که ساختارهایی را تعریف می کند که باید توسط SSIS برای ایجاد مراحلی که در آن داده ها می توانند پردازش شوند، همانطور که در این مراحل دنبال می شود، تعریف می کند.

جریان داده ای که توسط DTSX توضیح داده شده است همانطور که در تصویر زیر نشان داده شده است.

{{< figure src="../DataFlowDTSX.png" alt="جریان داده DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## منابع

 * [فرمت DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [فرمت DTSX 2 - توسط مایکروسافت](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

