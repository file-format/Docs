{
  "date": "2021-02-25",
  "keywords": [
"فایل ttc",
"فرمت فایل ttc",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC - قالب فایل مجموعه TrueType",
  "description": "یک فایل TrueType Collection (TTC) چندین فونت را در یک فایل واحد ترکیب می کند. هر دو اپل و مایکروسافت از TTF در سیستم عامل های مک و ویندوز استفاده کردند.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-fac"
}
},
  "lastmod": "2021-02-25"
}

## فایل TTC چیست؟
TTC به اختصار TrueType Collection یک فرمت True Type است. یک فایل TTC می تواند چندین فایل فونت را در آن ترکیب کند. این فایل‌ها برای ترکیب فونت‌های متعددی که حروف مشترک بسیاری دارند، مفید هستند. قبل از ویندوز 2000، فایل‌های TTC در نسخه‌های چینی، ژاپنی و کره‌ای ویندوز استفاده می‌شد، اما بعداً پشتیبانی برای همه مناطق در دسترس بود.


## ساختار فایل مجموعه فونت 
یک فایل TTC از یک جدول TTC Header، فهرست راهنمای جدول و چندین جدول OpenType تشکیل شده است. سربرگ TTC باید در ابتدای فایل پیدا شود. یک فهرست جدول کامل برای هر فونت باید وجود داشته باشد. قالب TableDirectory باید مشابه آنچه در یک فایل غیر مجموعه وجود دارد باشد. شمارش جدول در همه دایرکتوری های یک فایل TTC از ابتدای یک فایل TTC محاسبه می شود.
جداول در یک فایل TTC از طریق فهرست جدول فونت های مربوطه خود ارجاع داده می شوند. تعدادی از جداول OpenType باید چندین بار ظاهر شوند، یک بار برای هر فونت اضافه شده در TTC. در حالی که سایر جداول ممکن است توسط چندین فونت در فایل TTC به اشتراک گذاشته شوند.

### سربرگ TTC
دو نسخه از جدول TTC Header تاکنون موجود است:
- نسخه 1.0 برای فایل های TTC بدون امضای دیجیتال استفاده می شود.
- نسخه 2.0 را می توان برای فایل های TTC با یا بدون امضای دیجیتال استفاده کرد.
در اینجا جداول TTC Header هر دو نسخه آمده است:

**TTC Header نسخه 1.0:**

|نوع|نام|توضیحات|
---|---|---|
|TAG|ttcTag|رشته شناسه مجموعه قلم: 'ttcf' (برای فونت هایی با خطوط اصلی CFF یا CFF2 و همچنین خطوط TrueType استفاده می شود)|
|uint16|majorVersion|نسخه اصلی TTC Header، = 1.|
|uint16|minorVersion|نسخه کوچک TTC Header = 0.|
|uint32|numFonts|تعداد فونت در TTC|
|Offset32|tableDirectoryOffsets[numFonts]|آرایه ای از افست ها به TableDirectory برای هر فونت از ابتدای فایل|

**TTC Header نسخه 2.0:**

|نوع|نام|توضیحات|
---|---|---|
|TAG|ttcTag |رشته شناسه مجموعه قلم: 'ttcf'|
|uint16| majorVersion |نسخه اصلی TTC Header، = 2.|
|uint16| minorVersion |نسخه کوچک TTC Header، = 0.|
|uint32| numFonts |تعداد فونت در TTC|
|Offset32| tableDirectoryOffsets[numFonts] |آرایه ای از آفست ها به TableDirectory برای هر فونت از ابتدای فایل|
|uint32| dsigTag |برچسب نشان دهنده وجود جدول DSIG، 0x44534947 ('DSIG') (در صورت عدم امضای تهی)|
|uint32| dsigLength |طول (بر حسب بایت) جدول DSIG (در صورت عدم امضای تهی)|
|uint32| dsigOffset |تغییر (بر حسب بایت) جدول DSIG از ابتدای فایل TTC (در صورت عدم امضای تهی)|

## منابع
 * [فایل فونت OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (ویکی پدیا)](https://en.wikipedia.org/wiki/TrueType)

