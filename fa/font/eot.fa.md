{
  "date": "2020-08-20",
  "keywords": [
"فایل eot",
"فرمت فایل eot",
"فایل eot چیست",
"فایل",
"مثال eot",
"پسوند فایل eot",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT - فرمت فایل فونت TrueType",
  "description": "درباره فرمت فایل EOT و APIها برای ایجاد و باز کردن فایل‌های EOT بیاموزید.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-fat"
}
},
  "lastmod": "2020-10-21"
}

## فایل EOT چیست؟

یک فایل با پسوند .eot یک فونت OpenType است که در یک سند جاسازی شده است. اینها بیشتر در فایل های وب مانند صفحه وب استفاده می شوند. این توسط مایکروسافت ایجاد شده است و توسط محصولات مایکروسافت از جمله فایل ارائه پاورپوینت [.pps](/presentation/pps/) پشتیبانی می‌شود. این فایل کاربرد اصلی ندارد و به نوعی سند همراه با سند اصلی یا صفحه وب است. مشابه فونت‌های OTF، EOT از خطوط Postscript و TrueType برای گلیف‌ها پشتیبانی می‌کند. فایل‌های EOT از نظر اندازه کوچک‌تر هستند به این دلیل که با استفاده از فشرده‌سازی LZ فشرده می‌شوند. EOT از یک ابزار مایکروسافت برای ایجاد یک فونت از فونت های موجود TTF/OTF استفاده می کند.

## تاریخچه مختصر

فونت EOT در سال 2007 به عنوان بخشی از CSS3 به W3C ارسال شد اما به دلیل الزامات آن برای نصب دائمی بر روی سیستم از راه دور دلیل رد آن شد. در مارس 2008 دوباره ارسال شد، اما W3C در نهایت [Web Font Format](/font/woff/) (WOFF) را انتخاب کرد که در آن زمان استاندارد شد.

## فرمت فایل EOT

جزئیات فرمت فایل EOT را می توان در [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat) پیدا کرد و ساختار استفاده شده توسط این قالب فونت را تشریح می کند. EOT از یک ساختار EMBEDDEDFONT تشکیل شده است که اطلاعات اولیه کافی در مورد نام فونت hte و کاراکترهای پشتیبانی شده را ارائه می دهد. بسته‌بندی این اطلاعات به نمایندگی‌های کاربر اجازه می‌دهد از باز کردن بسته‌بندی، فشرده‌سازی یا نصب فونت در صورت وجود فونت در دستگاه خودداری کنند.

### ساختار EMBEDDEDFONT
ساختار EMBEDDEDFONT سه تجدید نظر شده است، با افزودن داده های اضافی در پایان ساختار با هر بازبینی. آخرین ویرایش ساختار EMBEDDEDFONT همانطور که در زیر نشان داده شده است.

|نوع داده|نام ورودی|توضیحات|
---|---|---|
|unsigned long|EOTSize|طول کل ساختار بر حسب بایت (شامل داده های رشته و فونت)|
|unsigned long|FontDataSize|طول فونت OpenType (FontData) به بایت|
|unsigned long|نسخه|شماره نسخه این فرمت - 0x00020002|
|بلند بدون امضا|پرچم|پرچم پردازش|
|byte[10]|FontPANOSE|مقدار PANOSE برای این فونت - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan مراجعه کنید|
|byte|Charset|در ویندوز این از TEXTMETRIC.tmCharSet مشتق شده است. این مقدار مجموعه کاراکتر فونت را مشخص می کند. DEFAULT_CHARSET (0x01) هیچ ترجیحی را نشان نمی دهد. - به https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica مراجعه کنید|
|byte|Italic|اگر بیت ITALIC در OS/2.fsSelection تنظیم شده باشد، مقدار 0x01 خواهد بود - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss مراجعه کنید|
|unsigned long|Weight|مقدار وزن این فونت - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc مراجعه کنید|
|کوتاه بدون امضا|fsType|پرچم هایی را تایپ کنید که اطلاعاتی درباره مجوزهای جاسازی ارائه می دهند - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst مراجعه کنید|
| کوتاه بدون امضا|MagicNumber|شماره جادویی برای فایل EOT - 0x504C. برای بررسی خرابی داده ها استفاده می شود.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (بیت های 0-31) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur مراجعه کنید|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (بیت های 32-63) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur مراجعه کنید|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (بیت های 64-95) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur مراجعه کنید|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (بیت های 96-127) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur مراجعه کنید|
|بدون علامت طولانی|CodePageRange1|CodePageRange1 (بیت های 0-31) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr مراجعه کنید|
|unsigned long|CodePageRange2|CodePageRange2 (بیت های 32-63) - به https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr مراجعه کنید|
| بدون امضا طولانی|CheckSumAdjustment|head.CheckSumAdjustment - به https://learn.microsoft.com/en-us/typography/opentype/spec/head مراجعه کنید|
|unsigned long|Reserved1|Reserved - باید 0| باشد
|بدون امضا طولانی|رزرو شده2|رزرو شده - باید 0 باشد|
|بدون امضا طولانی|رزرو شده3|رزرو شده - باید 0 باشد|
|unsigned long|Reserved4|Reserved - باید 0| باشد
|کوتاه بدون علامت|Padding1|بالشتک برای حفظ تراز طولانی. مقدار padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|FamilyNameSize|تعداد بایت های استفاده شده توسط آرایه FamilyName|
|byte|FamilyName[FamilyNameSize]|آرایه از UTF-16 کاراکتر به طول بایت FamilyNameSize. این رشته زبان انگلیسی Font Family است که در جدول نام فونت یافت می شود (شناسه نام = 1) - به https://learn.microsoft.com/en-us/typography/opentype/spec/name مراجعه کنید|
|unsigned short|Padding2|مقدار Padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|StyleNameSize|تعداد بایت های استفاده شده توسط StyleName|
|byte|StyleName[StyleNameSize]|آرایه از UTF-16 کاراکتر به طول بایت StyleNameSize. این رشته Font Subfamily زبان انگلیسی است که در جدول نام فونت (شناسه نام = 2) یافت می شود - به https://learn.microsoft.com/en-us/typography/opentype/spec/name مراجعه کنید|
|unsigned short|Padding3|مقدار Padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|VersionNameSize|تعداد بایت های استفاده شده توسط VersionName|
|بایت|VersionName[VersionNameSize]|آرایه UTF-16 کاراکتر به طول بایت VersionNameSize. این رشته نسخه انگلیسی زبان موجود در جدول نام فونت است (شناسه نام = 5) - به https://learn.microsoft.com/en-us/typography/opentype/spec/name مراجعه کنید|
|unsigned short|Padding4|مقدار Padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|FullNameSize|تعداد بایت های استفاده شده توسط FullName|
|byte|FullName[FullNameSize]|آرایه UTF-16 کاراکتر به طول بایت های FullNameSize. این رشته نام کامل زبان انگلیسی است که در جدول نام فونت یافت می شود (شناسه نام = 4) - به https://learn.microsoft.com/en-us/typography/opentype/spec/name مراجعه کنید|
|unsigned short|Padding5|مقدار Padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|RootStringSize|تعداد بایت های استفاده شده توسط آرایه RootString|
|byte|RootString[RootStringSize]|آرایه از UTF-16 کاراکتر به طول بایت RootStringSize.|
|unsigned long|RootStringCheckSum|مقدار CheckSum RootString. الگوریتم پردازش RootStringChecksum را در زیر ببینید.|
|unsigned long|EUDCCodePage|مقدار صفحه کد برای پشتیبانی از فونت EUDC مورد نیاز است.|
|unsigned short|Padding6|مقدار Padding همیشه باید روی 0x0000 تنظیم شود.|
|unsigned short|SignatureSize|تعداد بایت های استفاده شده توسط آرایه Signature. در حال حاضر رزرو شده و باید روی 0x0000 تنظیم شود.|
|بایت|امضا[SignatureSize]|در حال حاضر رزرو شده است. اگر SignatureSize 0x0000 باشد، طولی برای این آرایه وجود ندارد.|
|unsigned long|EUDCFlags|پرچم پردازش برای فونت EUDC. مقادیر معمولی ممکن است TTEMBED_XORENCRYPTDATA و TTEMBED_TTCOMPRESSED باشد.|
|unsigned long|EUDCFontSize|تعداد بایت های استفاده شده توسط آرایه Signature.|
|byte|EUDCFontData[EUDCFontSize]|تعداد بایت های استفاده شده برای داده های فونت EUDC. اگر EUDCFontSize 0x00000000 باشد، طولی برای این آرایه وجود ندارد.
|byte|FontData[FontDataSize]|داده های فونت این فایل EOT. داده ها ممکن است فشرده یا XOR رمزگذاری شوند که توسط پرچم های پردازش نشان داده شده است.|

## منابع

 * [فرمت فایل EOT] (https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [جاسازی قلم](https://en.wikipedia.org/wiki/Font_embedding)

