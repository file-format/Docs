{
  "date": "2021-01-21",
  "keywords": [
"فایل ai",
"فرمت فایل ai",
"فایل ai چیست",
"فایل",
"ai مثال",
"پسوند فایل ai",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI - فایل آثار هنری Adobe Illustrator",
  "description": "درباره فرمت فایل AI و APIهایی که می توانند فایل های هوش مصنوعی ایجاد و باز کنند، بیاموزید.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-fai"
}
},
  "lastmod": "2021-01-21"
}

## فایل هوش مصنوعی چیست؟

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## فرمت فایل هوش مصنوعی

AI فرمت فایل اختصاصی Adobe Illustrator است و از رویکرد دو مسیره مشابه PGF برای ذخیره فایل‌های سازگار با EPS استفاده می‌کند. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) یک مرجع دقیق توسعه دهنده برای جزئیات داخلی این قالب فایل ارائه می دهد. تمام اسناد (فایل‌ها) ایجاد شده توسط Adobe Illustrator اسناد زبان پست اسکریپت هستند و دارای دو بخش اصلی مطابق با قراردادهای ساختار اسناد هستند: یک «پرولوگ» و یک «اسکریپت».

### پرولوگ

بخش prolog اطلاعات مورد نیاز برای تفسیر فایل را در بر می گیرد. یک مثال می تواند کادر محدود کننده ای باشد که شامل تمام علامت های صفحه است. همچنین حاوی اطلاعات منابعی مانند فونت ها و تعاریف رویه است. این منابع به طور منطقی در مجموعه هایی به نام procset گروه بندی می شوند و شامل روش های صریح برای مقداردهی اولیه و خاتمه رویه های خود هستند.

### اسکریپت

عناصر گرافیکی در صفحه توسط اسکریپت توصیف می شوند. یک اسکریپت حاوی ارجاعاتی به عملگرها و رویه های موجود در پرولوگ، همراه با عملوندها و داده ها است. سه بخش منطقی یک اسکریپت عبارتند از:

 * Setup Sequence - که منابع تعریف شده در پرولوگ را مقداردهی اولیه و فعال می کند
 * دنباله عملگرهای توصیفی
 * تریلر که منابع را غیرفعال می کند

عملگرها در اسکریپت دنباله ای از عناصر گرافیکی هستند که به زبانی که توسط procsets در prolog تعریف شده اند نوشته شده اند. این توالی‌ها شامل مجموعه‌ای از عناصر داده، تعاریف ویژگی‌های گرافیکی و فراخوانی‌های رویه‌های تعریف‌شده در مجموعه‌ها هستند.

### برچسب های شی

تگ های شی برای پیوست کردن اطلاعات سفارشی به یک شی هنری Adobe Illustrator استفاده می شود. برچسب ها شامل یک

 * شناسه برچسب
 * نوع برچسب
 * داده ها

## منابع
* [مشخصات فرمت فایل Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [فرمت فایل AI توسط PaintShopPro] (https://www.paintshoppro.com/en/pages/ai-file/)


