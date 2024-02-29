{
  "date": "2019-12-09",
  "keywords": [
"فایل 3mf",
"فرمت فایل 3mf",
"فایل 3mf چیست",
"فایل",
"نمونه 3mf",
"پسوند فایل 3mf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "درباره فرمت فایل 3MF و APIهایی که می توانند فایل های 3MF را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-faf"
}
},
  "lastmod": "2019-12-09"
}

## فایل 3MF چیست؟

3MF، فرمت ساخت سه بعدی، توسط برنامه های کاربردی برای ارائه مدل های اشیاء سه بعدی به انواع دیگر برنامه ها، پلت فرم ها، خدمات و چاپگرها استفاده می شود. برای جلوگیری از محدودیت‌ها و مشکلات موجود در سایر قالب‌های فایل سه بعدی، مانند [STL](/cad/stl/)، برای کار با آخرین نسخه چاپگرهای سه بعدی ساخته شده است. 3MF فرمت فایل نسبتا جدیدی است که توسط کنسرسیوم 3MF توسعه و منتشر شده است. این به اندازه کافی غنی است که بتواند یک مدل را به طور کامل توصیف کند، اطلاعات داخلی، رنگ و سایر ویژگی ها را حفظ می کند که آن را برای پشتیبانی از نوآوری های جدید در چاپ سه بعدی قابل توسعه می کند. این قالب قابل گسترش است، می‌تواند به طور گسترده مورد استفاده قرار گیرد و از مشکلاتی که سایر فرمت‌های فایل پرکاربرد را تحت تأثیر قرار می‌دهند، عاری است.

## تاریخچه مختصر فرمت فایل 3MF

محدودیت‌های موجود در قالب‌های فایل‌های توصیفی مدل موجود، مانند STL و موارد دیگر، برندهای پیشرو را به جمع‌آوری و فرمول‌بندی فرمت فایل قابل توسعه‌تر برای چاپ سه‌بعدی سوق می‌دهد. یک نکته مهم این بود که چگونه برنامه ها باید داده های مدل را به چاپگرهای سه بعدی منتقل کنند. از این رو کنسرسیوم 3MF برای پشتیبانی از فرمت فایل سه بعدی جدید به نام 3MF با هدف گسترش آن به اندازه کافی برای پاسخگویی به نیازهای چاپ سه بعدی به وجود آمد. شرکت‌های متعددی از جمله مایکروسافت، اتودسک، داسو سیستمز، نت‌فاب، SLM، اچ‌پی و غیره در این کنسرسیوم حضور داشتند. مایکروسافت فرمت فایل سه بعدی خود را که در حال انجام است به عنوان نقطه شروعی برای توسعه بیشتر مشخصات مشترک توسط کنسرسیوم 3MF اهدا کرد.

## فرمت فایل 3MF - اطلاعات بیشتر

3MF یک قالب داده مبتنی بر XML است - XML فشرده قابل خواندن برای انسان - که شامل تعاریف داده های مربوط به تولید سه بعدی، از جمله قابلیت توسعه شخص ثالث برای داده های سفارشی است. فرمت فایل 3MF با در نظر گرفتن محدودیت ها و مشکلاتی که سایر فرمت های فایل سه بعدی با آن مواجه هستند طراحی شده است. این منجر به فرمول بندی فرمت فایل 3MF می شود که عبارت است از:

* **کامل:** حاوی تمام اطلاعات مدل، مواد و اموال لازم در یک آرشیو واحد

* **قابل خواندن توسط انسان:** استفاده از ساختارهای رایج مانند OPC، [ZIP](/compression/zip/)، و XML برای تسهیل توسعه

* **ساده:** مشخصات کوتاه و واضح که توسعه را آسان و اعتبارسنجی را سریع می کند

* **توسعه پذیر:** استفاده از فضاهای نام XML امکان ایجاد پسوندهای عمومی و خصوصی را با حفظ سازگاری فراهم می کند.

* ** بدون ابهام: ** آزمون های زبان واضح و انطباق تضمین می کند که فایل همیشه از دیجیتال تا فیزیکی سازگار است.

* **رایگان:** دسترسی و اجرای مشخصات 3MF همیشه عاری از حق امتیاز، حق ثبت اختراع و مجوز است و خواهد بود.


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## مشخصات فرمت فایل 3MF

فرمت فایل 3MF از مشخصات بسته بندی باز در قالب آرشیو ZIP برای مدل فیزیکی خود استفاده می کند. این شامل مجموعه ای از قطعات و روابط کاملاً تعریف شده است که هدف خاصی را در سند تکمیل می کند. این همچنین باعث می شود که فرمت از ویژگی بسته شامل امضاهای دیجیتال و تصاویر کوچک پیروی کند.

### سند 3MF - یک مرور کلی

یک سند معمولی 3MF به صورت زیر است:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**نام**|**توضیحات**|**منبع رابطه**|**الزامی/اختیاری**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Core Properties|بخش OPC که حاوی خصوصیات سند مختلف است.|بسته|اختیاری
|منشا امضای دیجیتال|قسمت OPC که ریشه امضاهای دیجیتال در بسته است.|بسته|اختیاری
|امضای دیجیتال|قطعات OPC که هرکدام شامل یک امضای دیجیتال است.|منشا امضای دیجیتال|اختیاری
|گواهی امضای دیجیتال|قطعات OPC که حاوی گواهی امضای دیجیتال است.|امضای دیجیتال|اختیاری
|PrintTicket|تنظیماتی را ارائه می‌دهد که هنگام خروجی‌گیری شی(های) سه بعدی در بخش مدل سه بعدی استفاده می‌شوند.|مدل سه بعدی|اختیاری
|تصویر کوچک|حاوی یک تصویر کوچک JPEG یا PNG است که اشیاء سه بعدی را در بسته یا بسته به طور کلی نشان می دهد.|بسته|اختیاری
|بافت سه بعدی|حاوی بافتی است که برای اعمال رنگ به یک شیء سه بعدی در قسمت مدل سه بعدی (موجود برای برنامه های افزودنی) | مدل سه بعدی|اختیاری
|قطعات سفارشی|قطعات OPC مرتبط با ابرداده|بسته|اختیاری

بخش‌های [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships)، [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models)، [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources)، [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) و [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) سند مشخصات، اطلاعات دقیقی درباره سند 3MF ارائه می‌دهند.

## منابع ##

* [مشخصات فرمت فایل 3MF](https://github.com/3MFConsortium/spec_core)

* [3MF - توسط Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


