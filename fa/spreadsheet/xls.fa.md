{
  "date": "2019-12-16",
  "keywords": [
"XLS",
"فایل",
"افزونه",
"فرمت فایل",
"برتری داشتن",
"صفحه گسترده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "راهنمای فرمت فایل شما برای اینکه بدانید یک فایل XLS چیست و APIهایی که می توانند آنها را ایجاد و باز کنند.",
  "title": "فرمت فایل XLS چیست؟ از کارشناسان فرمت فایل بیاموزید!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-fas"
}
},
  "lastmod": "2019-12-16"
}

## فایل XLS چیست؟

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## تاریخچه مختصر

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* نسخه 8 (منتشر شده با آفیس 97): VBA به عنوان یک زبان استاندارد معرفی شد و برچسب های حذف شده زبان طبیعی برای اولین بار در این نسخه گنجانده شد. همچنین برای اولین بار دستیار اداری گیره کاغذ را معرفی کرد.

* نسخه 9 (منتشر شده با office 2000): فقط تغییرات جزئی در نسخه 9 وجود داشت که در آن دستیار اداری گیره کاغذ می توانست به طور همزمان چندین شی را که قبلاً امکان پذیر نبود، نگه دارد.

* نسخه 10 (منتشر شده با آفیس XP): این نسخه هیچ پیشرفت محسوسی نداشت.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## مشخصات فرمت فایل XLS ##

داده ها در یک فایل XLS به صورت جریان های باینری در قالب یک فایل ترکیبی که در سند [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx) توسط مایکروسافت توضیح داده شده است مرتب می شوند.

#### جریان و فرعی ####

یک کتاب کار با جریان کتاب کار نشان داده می شود. هر کاربرگ در یک کتاب کار با Substreams نشان داده می شود. علاوه بر این، دارای زیرجریان نمودار نمودار، فرعی صفحه ماکرو، یا زیرجریان صفحه گفتگو است که زیرجریان جهانی را دنبال می کند. هر جریان باینری یا زیرجریان که حاوی داده های کتاب کار است باید به صورت یک سری رکوردهای باینری نوشته شود.

#### رکورد ####

اطلاعات مربوط به ویژگی‌ها در یک کتاب کار به‌عنوان رکوردی ذخیره می‌شود که یک دنباله بایت با طول متغیر است. یک رکورد باینری از سه جزء زیر تشکیل شده است:

**نوع رکورد:** نوع رکورد یک عدد صحیح بدون علامت دو بایتی است که مشخص می کند چه نوع اطلاعاتی توسط رکورد مشخص می شود و ساختار داده های رکورد مخصوص این رکورد چگونه مرتب شده و ساختار می یابد. مقادیر نوع رکورد باید مقداری از Record Enumeration (بخش 2.3) باشد یا رکورد باید از معماری رکورد آینده استفاده کند (بخش 2.1.6).

**اندازه رکورد**: اندازه رکورد یک عدد صحیح بدون علامت دو بایتی است که تعداد بایت هایی را مشخص می کند که اندازه کل داده های رکورد را مشخص می کند. اندازه رکورد باید بزرگتر یا مساوی 0 باشد و باید کمتر یا مساوی 8224 باشد.

**Record Data:** جزء داده رکورد حاوی فیلدهایی است که با نوع رکورد خاصی مطابقت دارند و باقیمانده رکورد را تشکیل می دهند. ترتیب و ساختار فیلدها برای یک نوع رکورد معین در بخش مربوط به آن نوع رکورد مشخص شده است. اندازه جزء داده رکورد باید برابر با اندازه رکورد باشد. فیلدها در جزء داده رکورد می توانند حاوی مقادیر ساده، آرایه های مقادیر، ساختارهای چند فیلد، آرایه های فیلدها و آرایه های ساختار باشند.

#### جدول سلولی ####

سلول ها بلوک های اساسی یک کتاب کار هستند که محتویات کتاب کار مانند متن، فرمول ها و داده های عددی را ذخیره می کنند. سلول ها رکورد داده های ذخیره شده را از طریق ساختار داده ای به نام جدول سلولی نگهداری می کنند. خود جدول سلولی در توالی رکوردهایی ذخیره می شود که با قوانین CELLTABLE تعریف شده در سند مشخصات مطابقت دارد. این شامل یک سری بلوک های ردیفی است که در آن ردیف ها در بلوک های ردیفی مرتب شده اند. هر بلوک سطر شامل سطرهایی از سطر اول حاوی داده تا سطر آخر حاوی داده است.

قالب بندی داده یا ردیف در یک رکورد ردیف برای هر بلوک ردیف ذخیره می شود. هر سلولی که حاوی داده یا قالب بندی سلول های فردی است با یک رکورد نشان داده می شود. قالب‌بندی مرتبط با یک سلول می‌تواند از قالب‌بندی سلول منفرد، قالب‌بندی ردیف، قالب‌بندی ستون یا قالب پیش‌فرض سلول مشتق شود. ترتیب اولویت برای قالب‌بندی، قالب‌بندی سلولی با بالاترین اولویت است، به دنبال آن قالب‌بندی ردیف، و سپس قالب‌بندی ستون، و سپس قالب پیش‌فرض سلول قرار دارد. سلول هایی که حاوی داده نیستند و دارای قالب بندی جداگانه نیستند، ذخیره نمی شوند.

#### فرمول ها ####

فرمول دنباله ای از مقادیر، ارجاعات سلولی، نام ها، توابع یا عملگرها در یک سلول است که با هم مقدار جدیدی تولید می کنند. فرمول ها در یک نمایش نشانه گذاری شده به نام عبارات تجزیه شده ذخیره می شوند. یک عبارت تجزیه شده در زمان اجرا به فرمول متنی برای نمایش و ویرایش کاربر تبدیل می شود. فرمول سلول توسط رکورد Formula مشخص می شود. فرمول های آرایه توسط رکورد آرایه مشخص می شوند. فرمول های مشترک توسط رکورد ShrFmla مشخص می شوند.

#### نمودار ####

برگه نمودار یک نمودار را مشخص می کند، یک تصویر گرافیکی که داده ها یا روابط بین مجموعه های داده را به صورت بصری نشان می دهد، و یک حافظه پنهان داده نمودار، یک کپی محلی از داده هایی که در داده های نمودار استفاده می شود وجود ندارد یا اگر پیوندهایی به خارجی دارند. منابع داده خراب هستند نمودار گروه‌های یک یا دو محوری را مشخص می‌کند، مجموعه‌ای از محورها را که داده‌های نمودار بر اساس آن ترسیم می‌کنند، و مجموعه‌ای از سری‌ها، خطوط روند و نوار خطای مشخص شده در نمودار را مشخص می‌کند. هر گروه محوری یک تا چهار گروه نمودار را مشخص می کند که نوع تجسم مورد استفاده برای نمایش داده ها را مشخص می کند. هر سری، خط روند و نوار خطا یک گروه نمودار را مشخص می کند که با آن مرتبط است.

#### فراداده ####

فراداده داده های اضافی مرتبط با یک سلول خاص یا محتوای آن است. فراداده فقط برای اهداف توسعه پذیری آینده در BIFF8 ثبت می شود.

#### جداول محوری ####

PivotTable مکانیزمی است برای خلاصه کردن داده های منبع برای بدست آوردن یک نمای کلی از توزیع آن داده ها. در یک PivotTable، ستون های قابل اجرا از داده های منبع تبدیل به فیلدهایی می شوند که می توانند برای خلاصه کردن داده ها استفاده شوند. وقتی داده‌های منبع PivotTable، داده‌های منبع OLAP هستند، سلسله مراتب OLAP و برخی دیگر از موجودیت‌های OLAP به فیلدهایی در PivotTable تبدیل می‌شوند.
یک PivotTable دارای دو بخش اصلی است، یک PivotCache و یک نمای PivotTable. ممکن است چندین نما از PivotTable بر اساس یک PivotCache غیر OLAP وجود داشته باشد.

#### سبک ها ####

این نمای کلی توضیح می‌دهد که چگونه اطلاعات قالب‌بندی و حفاظت برای سلول‌ها در یک صفحه (1) مشخص می‌شود. قالب بندی سلول از چندین مجموعه ویژگی تشکیل شده است:

* ویژگی های فونت (پررنگ، مورب، رنگ فونت، اندازه فونت و غیره...)

* ویژگی های پر کردن (رنگ پیش زمینه، رنگ پس زمینه، الگو، گرادیان، و غیره ...)

* ویژگی های تراز (تراز چپ، مرکز، راست، و غیره…)

* ویژگی های حاشیه (چپ، راست، بالا، پایین، ضخیم یا نازک، رنگ، و غیره...)

* ویژگی های قالب بندی اعداد (تاریخ، زمان، تعداد ارقام اعشار، و غیره...)

* ویژگی های حفاظتی (قفل شده، پنهان و غیره ...)


این ویژگی ها، به طور کلی، نحوه نمایش و چاپ یک سلول خاص را توصیف می کنند.

## منابع ##

* [[MS-XLS] - ساختار قالب فایل باینری اکسل](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] - فرمت فایل باینری فایل ترکیبی](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


