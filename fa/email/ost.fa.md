{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST - فرمت فایل ذخیره‌سازی Outlook",
  "description": "درباره فرمت فایل OST و APIهایی که می‌توانند فایل‌های OST را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-fat"
}
},
  "lastmod": "2019-09-10"
}

## فایل OST چیست؟

OST یا Offline Storage Files نشان دهنده داده های صندوق پستی کاربر در حالت آفلاین در دستگاه محلی پس از ثبت نام در Exchange Server با استفاده از Microsoft Outlook است. این به طور خودکار در اولین استفاده از Microsoft Outlook پس از اتصال به سرور ایجاد می شود. پس از ایجاد فایل، داده ها با سرور ایمیل همگام می شوند تا در صورت قطع شدن ارتباط از سرور ایمیل، به صورت آفلاین نیز در دسترس باشند. فایل‌های OST می‌توانند از موارد صندوق پستی مانند ایمیل‌ها، مخاطبین، اطلاعات تقویم، یادداشت‌ها، وظایف و سایر داده‌های مشابه استفاده کنند. کاربران می توانند ایمیل ها و سایر موارد داده را در فایل OST حتی در صورت عدم اتصال به سرور ایجاد کنند، اما این موارد با سرور همگام سازی نمی شوند. پس از برقراری ارتباط، فایل محلی مجدداً با سرور همگام می شود تا هم سرور و هم نسخه محلی در یک سطح اطلاعات باشند.

## فرمت فایل OST

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* فرمت ANSI 32 بیتی

* فرمت یونیکد 64 بیتی


فرمت فایل PST [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)، که توسط مایکروسافت موجود است، برای فرمت فایل OST به عنوان مجوز حق اختراع رایگان و غیرقابل فسخ از طریق Open Specification Promise نیز قابل اعمال است. از عناصر متمایز زیر تشکیل شده است:

* هدر فرار

* داده های هدر فایل

* گره شاخه شاخص

* گره برگ شاخص

* (پرونده) شاخص افست

* (مورد) نمایه توصیفگر

* توصیفگرهای محلی

* نوع جدول آیتم


### اطلاعات سرصفحه

ساختار HEADER فایل OST در همان ابتدای فایل در فاصله صفر قرار دارد. این شامل اطلاعات فراداده در مورد فایل OST و اطلاعات ROOT برای دسترسی به ساختارهای داده لایه NDB است که در بالا توضیح داده شد. ساختار HEADER برای نسخه های Unicode و ANSI OST File Format متفاوت است.

سرصفحه با یک کلمه جادویی 4 بایتی **!BDN** شروع می شود که با بایت (0x21، 0x42، 0x44، 0x4E) نشان داده می شود. یک عدد جادویی 2 بایتی دیگر، **SM** (0x53، 0x4D)، در آفست 8 از ابتدای فایل قرار دارد. اطلاعات نسخه (ANSI یا Unicode) در فاصله 10 از شروع فایل قرار دارد. مقدار هگز (0x17) فایل OST Unicode را مشخص می کند در حالی که 0x0E یا 0x0F فرمت فایل ANSI را نشان می دهد.

|فیلد|توضیحات
---|---|
|dwMagic (4 بایت)|باید { 0x21, 0x42, 0x44, 0x4E } (!BDN) باشد
|dwCRCPpartial (4 بایت)|مقدار CRC 32 بیتی 471 بایت داده که از wMagicClient شروع می شود (0ffset 0x0008)
|wMagicClient (2 بایت)|باید { 0x53, 0x4D } باشد.
|wVer (2 بایت)|نسخه فرمت فایل. اگر فایل یک فایل ANSI PST است، این مقدار باید 14 یا 15 باشد و اگر فایل یک فایل PST یونیکد باشد، باید 23 باشد.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. سازندگان یک فایل PST جدید بر اساس این سند باید این مقدار را به 19 مقداردهی اولیه کنند.
|bPlatformCreate (1 بایت)|این مقدار باید روی 0x01 تنظیم شود.
|bPlatformAccess (1 بایت)|این مقدار باید روی 0x01 تنظیم شود.
|dwReserved (8 بایت)|
|bidUnused (8 بایت فقط یونیکد)| هنگام ایجاد فرمت فایل Unicode PST، بالشتک استفاده نشده اضافه شد.
|bidNextP (یونیکد: 8 بایت؛ ANSI: 4 بایت)|BID صفحه بعدی. صفحات دارای یک شمارنده ویژه برای تخصیص مقادیر bidIndex هستند. مقدار bidIndex برای BID برای صفحات از این شمارنده تخصیص داده می شود.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. برای جزئیات بیشتر، بخش 2.2.2.2 را ببینید.
|dwUnique (4 بایت)|این مقدار یکنواخت افزایش می یابد که هر بار که ساختار HEADER فایل PST تغییر می کند، تغییر می کند. عملکرد این مقدار ارائه یک مقدار منحصر به فرد و اطمینان از متفاوت بودن HEADER CRC ها پس از هر تغییر هدر است.
|rgnid[] (128 بایت)|آرایه ثابتی از 32 NID، که هر کدام مربوط به یکی از 32 NID_TYPE ممکن (NID_TYPE، NID_TYPE_NORMAL_FOLDER، NID_TYPE_SEARCH_FOLDER، NID_TYPE_NORMAL_MESSAGE_MESSAGE,NIDC_TYPE)
|qwUnused (8 بایت)|فضای استفاده نشده; باید روی صفر تنظیم شود. فقط فرمت فایل یونیکد PST.
| ریشه (یونیکد: 72 بایت؛ ANSI: 40 بایت)| ساختار ریشه (بخش 2.2.2.5).
|dwAlign (4 بایت)|بایت های تراز استفاده نشده. باید روی صفر تنظیم شود. فقط فرمت فایل یونیکد PST.
|rgbFM (128 بایت)|FMap منسوخ شده. این دیگر استفاده نمی شود و باید با 0xFF پر شود. خوانندگان باید ارزش این بایت ها را نادیده بگیرند.
|rgbFP (128 بایت)|FPMap منسوخ شده. این دیگر استفاده نمی شود و باید با 0xFF پر شود. خوانندگان باید ارزش این بایت ها را نادیده بگیرند.
|bSentinel (1 بایت)|باید روی 0x80 تنظیم شود.
|bCryptMethod (1 بایت)|نشان می دهد که چگونه داده های داخل فایل PST کدگذاری می شوند. باید روی یکی از مقادیر از پیش تعریف شده (NDB_CRYPT_NONE، NDB_CRYPT_PERMUTE، NDB_CRYPT_CYCLIC) تنظیم شود.
|rgbReserved (2 بایت)| رزرو شده؛ باید روی صفر تنظیم شود.
|bidNextB (8 بایت)|مقدار BID موجود بعدی را نشان می دهد. فقط فرمت فایل یونیکد PST.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. برای جزئیات بیشتر، بخش 2.2.2.2 را ببینید.
|dwCRCFull (4 بایت)|مقدار CRC 32 بیتی 516 بایت داده از wMagicClient تا bidNextB، شامل. فقط فرمت فایل یونیکد PST.
|ullReserved (8 بایت)|Reserved; باید روی صفر تنظیم شود. فقط فرمت فایل ANSI PST.
|dwReserved (4 بایت)|Reserved; باید روی صفر تنظیم شود. فقط فرمت فایل ANSI PST.
|rgbReserved2 (3 بایت)|
|bرزرو شده (1 بایت) |
|rgbReserved3 (32 بایت) |

## منابع

* [فرمت فایل Outlook Personal Folders (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [مشخصات فرمت فایل پوشه شخصی](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


