{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فرمت فایل TCX- فایل XML مرکز آموزشی",
  "description":"درباره فرمت فایل TCX و APIهایی که می‌توانند فایل‌های TCX را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-fa",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## فایل TCX چیست؟

فایل TCX (Training Center XML) یک فرمت تبادل داده است که برای به اشتراک گذاری داده ها بین دستگاه های تناسب اندام استفاده می شود. در سال 2008 با محصول مرکز آموزشی گارمین معرفی شد. داده های تمرینی مانند ضربان قلب، آهنگ دویدن، سرعت دوچرخه، کالری و زمان دور در قالب [XML](/web/xml/) در فایل TCX ذخیره می شود. علاوه بر این، اطلاعات خلاصه در مورد مسیر تمرین نیز در فایل TCX گنجانده شده است. فایل‌های TCX مشابه فایل‌های [FIT](/gis/fit/) هستند که با دستگاه‌های پوشیدنی ورزشی Garmin ایجاد می‌شوند.

## فرمت فایل TCX - اطلاعات بیشتر

فایل‌های TCX به‌عنوان فایل‌های XML روی دیسک ذخیره می‌شوند و هر رکورد به‌عنوان یک فعالیت ذخیره می‌شود. یک فعالیت شامل تمام داده‌های یک تمرین مانند زمان، زمان دور، شناسه، ضربان قلب، شدت، آهنگ و اطلاعات مسیر است که شامل جفت‌های موقعیت به همراه مهر زمانی برای آن موقعیت طولانی مدت مشابه {{HYPERLINK1 است. }} فایل ها.

### نسخه های فرمت فایل TCX

دو نسخه از این فرمت با طرحواره های XML مخصوص به خود که توسط Garmin میزبانی می شوند وجود دارد. در زیر به تعدادی از آنها اشاره می شود:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## پروتکل داده TCX

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## منابع ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


