{
  "date": "2019-10-11",
  "keywords": [
"فایل emf",
"فرمت فایل emf",
"فایل emf چیست",
"فایل",
"مثال emf",
"پسوند فایل emf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF - فرمت متافایل پیشرفته",
  "description": "درباره فرمت فایل EMF و APIهایی که می‌توانند فایل‌های EMF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-faf"
}
},
  "lastmod": "2019-09-10"
}

## فایل EMF چیست؟

**فرمت متافایل پیشرفته (EMF)** تصاویر گرافیکی را مستقل از دستگاه ذخیره می کند. متافایل های EMF شامل رکوردهای با طول متغیر به ترتیب زمانی هستند که می توانند تصویر ذخیره شده را پس از تجزیه در هر دستگاه خروجی ارائه دهند. این رکوردهای با طول متغیر می توانند تعاریف اشیاء محصور، دستورات برای ترسیم، و ویژگی های گرافیکی برای ارائه دقیق تصویر حیاتی باشند. وقتی دستگاهی یک متافیل EMF را با استفاده از محیط گرافیکی خود باز می‌کند، نسبت‌ها، ابعاد، رنگ‌ها و سایر ویژگی‌های گرافیکی تصویر اصلی بدون توجه به پلت فرم دستگاه باز می‌ماند.

## تاریخچه مختصر ##

در سال 1990، مایکروسافت فرمت فایل تصویری Windows Metafile ([WMF](/image/wmf/)) را برای مایکروسافت ویندوز طراحی کرد. Metafiles ویندوز فرمت 16 بیتی است که ممکن است حاوی برخی از اجزای بیت مپ باشد. در سال 1993، Win32/GDI Metafile پیشرفته (EMF) را معرفی کرد، نسخه جدیدتری با انعطاف پذیری و مقیاس پذیری پیشرفته. EMF همچنین به عنوان دستورات زبان گرافیکی برای اجرای درایورهای چاپگر استفاده می شود. مایکروسافت اکنون فرمت متافایل پیشرفته (EMF) را در قالب ویندوز (WMF) توصیه می کند. زمانی که ویندوز XP معرفی شد، نسخه Enhanced Metafile Format Plus (EMF+) منتشر شد. این نسخه جدیدتر راه خود را با سریال‌سازی تماس‌های GDI+ API پیدا می‌کند، همچنین WMF/EMF تماس‌های GDI را ضبط می‌کند. یک نسخه فشرده gzip از EMF وجود دارد که به نام EMZ شناخته می شود.

## فرمت متافیل EMF ##

در زیر عناصر ضروری فرمت متافایل پیشرفته آمده است:

* EMR_HEADER (نسخه، اندازه، وضوح تصویر در هنگام ایجاد)

* جدولی برای اشیاء GDI

* یک پالت رزرو شده (اختیاری)

* رکوردهای متافیل مرتب شده در ساختار آرایه (تنظیمات ویژگی، اشیاء تعریف شده، دستورات ترسیم)

* رکورد EMR_EOF (آخرین رکورد در متافیل EMF)


## نسخه EMF ##
* **Original**: نسخه اصلی رکورد لازم برای حفظ تصویر اصلی و حفظ آن را مستقل از دستگاه مشخص می کند. علاوه بر این از رکورد حاوی اشیاء گرافیکی و دستورات برای طراحی پشتیبانی می کند.

* **نسخه 1**: نسخه دوم EMF انعطاف پذیری و استقلال دستگاه را با افزودن رکورد فرمت پیکسل و ارائه برای استفاده از دستور OpenGL بهبود بخشید.

* **نسخه 2**: نسخه سوم با افزودن سیستم متریک برای اندازه گیری فواصل سطح دستگاه، دقت را افزایش داد و رکورد را مقیاس پذیرتر کرد.


## رکوردهای متافایل پیشرفته ##

رکوردهای متافایل به شکل آرایه مرتب می شوند. این رکوردها دارای ساختار ENHMETARECORD و طول متغیر هستند. ENHMETARECORD داده هایی را مشخص می کند که توابع GDI را برای ایجاد یک تصویر با استفاده از فرمت متافایل پیشرفته تعریف می کنند. ساختار **ENHMETAHEADER** همیشه اولین رکورد در این قالب است. این هدر EMF حاوی اطلاعات زیر است.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

حداقل یک رکورد EMF باید در هر متافایل وجود داشته باشد. اطلاعات عبور از یک رکورد به رکورد دیگر به رکوردهای EMF بستگی دارد، بنابراین این رکوردها باید در مجاورت یکدیگر مرتب شوند. در هر رکوردی در متافیل به جز EOF_record، طول آن رکورد خاص برای انتقال به رکورد بعدی تعیین می‌شود.

## ایجاد متافایل پیشرفته ##

از عملکرد **CreateEnhMetaFile** برای ایجاد یک متافیل پیشرفته استفاده می شود. آرگومان های این توابع برای ابعاد و ذخیره سازی تصویر روی دیسک/حافظه استفاده می شود. علاوه بر این، این عملکرد به ابعاد دستگاهی که تصویر برای اولین بار در آن ظاهر شد (دستگاه مرجع) و زمینه دستگاه مرجع (DC) نیاز دارد. بنابراین هنگام فراخوانی تابع **CreateEnhMetaFile**، آرگومان های مدیریت این DC باید ارائه شوند. سینتکس تابع به صورت زیر است:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** دسته به دستگاه مرجع.

**lptoFilename:** اشاره گر به نام فایل.

**lprc:** ساختار اشاره گر به بیضی ابعاد تصویر را بر حسب میلی متر مشخص می کند.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## عملیات متافایل پیشرفته ##

در زیر کارهایی وجود دارد که می توان با استفاده از دسته به یک متافیل پیشرفته انجام داد.

* نمایش و ویرایش برای تصویر ذخیره شده.

* تولید نسخه های متافایل پیشرفته.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* رنگ های موجود در پالت را خلاصه کنید.


## اشیاء گرافیکی ##

در عملیات طراحی و نقاشی، اشیاء گرافیکی را می توان با سوابق ایجاد شی ایجاد کرد و برای استفاده بیشتر ذخیره کرد. یک رکورد «EMR_SELECTOBJECT» می‌تواند این اشیاء گرافیکی را با استفاده از زمینه دستگاه پخش بازیابی کند. قلم‌ها، پالت‌ها، براش‌ها، فضاهای رنگی، فونت‌ها و اشیاء موجود برخی از انواع اشیاء قابل استفاده مجدد هستند.

## ترتیب بایت ##

فرمت Little-Endian برای ذخیره داده ها در رکوردهای متافیل استفاده می شود.

## نسخه ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. نسخه‌های توسعه‌یافته دارای پیش‌بینی برای رکوردهای OpenGL و یک توصیفگر اختیاری برای قالب پیکسل داخلی هستند. یک دستگاه اندازه گیری در میلی لیتر برای ابعاد نمایش داده شده اضافه شده است.

## منابع ##

* [فراتفایل با فرمت پیشرفته | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [فرمت و مشخصات متافایل پیشرفته](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


