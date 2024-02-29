{
  "date": "2020-08-20",
  "keywords": [
"فایل otf",
"فرمت فایل otf",
"فایل otf چیست",
"فایل",
"نمونه otf",
"پسوند فایل otf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF - فرمت فایل فونت TrueType",
  "description": "درباره فرمت فایل OTF و APIهایی که می‌توانند فایل‌های OTF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-faf"
}
},
  "lastmod": "2020-09-21"
}

## فایل OTF چیست؟

یک فایل با پسوند otf. به فرمت فونت OpenType اشاره دارد. قالب فونت OTF مقیاس پذیرتر است و ویژگی های موجود قالب های [TTF](/font/ttf/) را برای تایپوگرافی دیجیتال گسترش می دهد. OTF که توسط مایکروسافت و ادوبی توسعه داده شده است، ویژگی های قالب های فونت PostScript و TrueType را ترکیب می کند. این باعث می‌شود فرمت OTF با اکثریت سیستم‌های نوشتاری سازگار باشد و به همین دلیل است که به طور یکنواخت در پلتفرم‌های کامپیوتری اصلی استفاده می‌شود. فرمت فونت OpenType توسط Mac OS X و Windows 2000 و بالاتر پشتیبانی می شود.

## تاریخچه مختصر

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. این تغییرات همچنین شامل معرفی یک قالب فونت مناسب‌تر است که ویژگی‌های قالب‌های فونت نوع 1 (پست اسکریپت) Adobe را نیز برآورده می‌کند.

ادوبی در سال 1996 به مایکروسافت پیوست تا از هر دو فرمت فونت TrueType اپل و نوع 1 خود استفاده کند. این منجر به ترکیب هر دو قالب فونت زیرین برای غلبه بر محدودیت ها و افزودن پسوندهای جدید شد. این فناوری جدید در همان سال با نام **OpenType** معرفی شد.

## مشخصات فرمت فایل OTF

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### انواع داده OTF
فایل های OTF از انواع داده های زیر استفاده می کنند که همه در Big Endian هستند.

|نوع داده| توضیحات|
---|---|
|uint8| عدد صحیح بدون علامت 8 بیتی.|
|int8| عدد صحیح امضا شده 8 بیتی.|
|uint16| عدد صحیح بدون علامت 16 بیتی.|
|int16| عدد صحیح امضا شده 16 بیتی.|
|uint24| عدد صحیح بدون علامت 24 بیتی.|
|uint32| عدد صحیح بدون علامت 32 بیتی.|
|int32| عدد صحیح امضا شده 32 بیتی.|
|ثابت| شماره نقطه ثابت امضا شده 32 بیتی (16.16)|
|FWORD| int16 که مقداری را در واحدهای طراحی فونت توصیف می کند.|
|UFWORD| uint16 که مقداری را در واحدهای طراحی فونت توصیف می کند.|
|F2DOT14| عدد ثابت امضا شده 16 بیتی با کسری 14 بیتی کم (2.14).|
|LONGDATETIME| تاریخ و زمان به تعداد ثانیه از ساعت 12:00 نیمه شب، 1 ژانویه 1904، UTC نشان داده شده است. مقدار به عنوان یک عدد صحیح 64 بیتی امضا شده نشان داده می شود.|
| برچسب| آرایه ای از چهار uint8 (طول = 32 بیت) که برای شناسایی جدول، محور تغییر طراحی، اسکریپت، سیستم زبان، ویژگی یا خط مبنا استفاده می شود|
|Offset16| افست کوتاه به جدول، همان uint16، افست NULL = 0x0000|
|Offset32| افست طولانی به جدول، همان uint32، افست NULL = 0x00000000|
|نسخه16نقطه16| مقدار بسته بندی شده 32 بیتی با شماره نسخه اصلی و فرعی. (به اعداد نسخه جدول مراجعه کنید.)|

### فهرست جداول OTF

یک فایل OTF با یک فهرست جدول شروع می شود. این دایرکتوری مجموعه سطح بالایی از جداول در فایل فونت است. بسته به تعداد فونت های یک فایل، فهرست جدول ممکن است در مکان های متفاوتی در فایل قرار گیرد. به عنوان مثال، در صورتی که فایل فونت فقط یک فونت داشته باشد، دایرکتوری جدول از بایت 0 فایل شروع می شود. در صورت وجود چندین مجموعه فونت OpenType،
شروع دایرکتوری جدول در TTCHeader نشان داده شده است.

|نوع |نام |توضیحات|
---|---|---|
|uint32 |sfntVersion| 0x00010000 یا 0x4F54544F ('OTTO')|
|uint16| numTables |تعداد جداول.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16، که در آن ** یک عملگر قدرت است).|
|uint16 |entrySelector Log2 از حداکثر توان 2 کمتر یا مساوی numTables (log2(searchRange/16)، که برابر است با floor(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - محدوده جستجو).|
|tableRecord| tableRecords[numTables] |آرایه رکوردهای جدول—یکی برای هر جدول سطح بالای فونت|


### رکورد جدول

برای هر جدول سطح بالای فونت، یک جدول ثبت وجود دارد که از فیلدهای زیر تشکیل شده است.

|نوع| نام| توضیحات|
---|---|---|
| برچسب| جدول برچسب| شناسه جدول.|
|uint32| چک سام| چک جمع برای این جدول.|
|Offset32| افست| افست از ابتدای فایل فونت.|
|uint32| طول طول این میز.|

هر جدول در فایل فونت OpenType با نام هایی نشان داده می شود که به عنوان برچسب های جدول شناخته می شوند. برای همه رکوردهای آرایه ضروری است که به ترتیب صعودی بر اساس برچسب مرتب شوند.

## منابع
 * [مشخصات فونت OpenType توسط مایکروسافت](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [نمایش اجمالی TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

