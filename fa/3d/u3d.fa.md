{
  "date": "2019-10-11",
  "keywords": [
"فایل u3d",
"فرمت فایل u3d",
"فایل u3d چیست",
"فایل",
"مثال u3d",
"پسوند فایل u3d",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "U3D - فرمت فایل سه بعدی جهانی",
  "description": "درباره فرمت فایل U3D و APIهایی که می‌توانند فایل‌های U3D را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3-fad"
}
},
  "lastmod": "2019-09-10"
}

## فایل U3D چیست؟

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. اسناد سه بعدی [PDF](/pdf/) از جاسازی اشیاء U3D پشتیبانی می‌کنند و می‌توانند در Adobe Reader (نسخه 7 و به بعد) مشاهده شوند.

فرمت U3D با در نظر گرفتن هدف ایجاد یک استاندارد جهانی برای ذخیره سازی و تبادل داده های سه بعدی توسعه داده شد. با این حال، این فرمت به جای استفاده به عنوان یک فرمت تبادلی، کاربرد اصلی خود را در رمزگذاری برای PDF سه بعدی می یابد. Acrobat 3D یک نوع فایل سه بعدی پشتیبانی شده را پس از تبدیل به PDF به U3D یا PRC تبدیل می کند.

## فرمت فایل U3D

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

اولین نسخه U3D بر نمایش‌های کلیدی ویژگی‌های گرافیک سه بعدی مانند هندسه، رنگ، بافت، نور، استخوان‌ها و انیمیشن‌های مبتنی بر تبدیل متمرکز بود. نسخه های دوم و سوم برخی از اشتباهات را در ویرایش اول تصحیح کردند و نسخه سوم رایج ترین نوع مورد استفاده در نرم افزارهای صنعتی بود. نسخه چهارم تعاریفی را برای موارد اولیه درجه بالاتر (سطوح منحنی) ارائه می دهد. [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) به صورت آنلاین برای مرجع کاربر در وب سایت ECMA در دسترس هستند.

### انواع داده در فایل های U3D

فایل باینری شامل انواع زیر خواهد بود: U8، U16، U32، U64، I16، I32، F32، F64 و String.

 * U8: یک عدد صحیح 8 بیتی بدون علامت
 * U16: یک عدد صحیح 16 بیتی بدون علامت
 * U32: یک عدد صحیح 32 بیتی بدون علامت
 * U64: یک عدد صحیح 64 بیتی بدون علامت
 * I16: یک عدد صحیح 16 بیتی امضا شده
 * F32: یک شناور تک دقیق IEEE.
 * F64: یک شناور با دقت دوگانه IEEE.
 * رشته: رشته ها در فایل U3D با یک عدد صحیح 16 بیتی بدون علامت شروع می شوند که طول کل کاراکترهای رشته را مشخص می کند. رشته ها همیشه به عنوان حساس به حروف کوچک و بزرگ پردازش می شوند.

## ساختار فایل U3D

یک فایل U3D حاوی مجموعه ای از بلوک ها است. در هر فایل U3D 3 نوع مختلف بلوک وجود دارد.

 * بلوک هدر فایل
 * بلوک اعلامیه
 * بلوک ادامه

اگر به داده های آن بلوک نیازی نباشد یا رمزگشا برای آن نوع بلوک در دسترس نباشد، لودر انتهای یک بلوک را تعیین می کند.

{{< figure src="../u3d.png" alt="فرمت فایل U3D" >}}

### بلوک هدر فایل
بلوک هدر فایل حاوی اطلاعات فایل است که توسط بارگذاری شده برای تعیین نحوه خواندن فایل استفاده می شود.

### بلوک اعلامیه

بلوک های اعلامیه حاوی اطلاعاتی در مورد اشیاء موجود در فایل هستند. اشیاء در یک بلوک اعلان باید تعریف شوند.

### بلوک ادامه

اطلاعات اضافی برای اشیاء اعلام شده در بلوک Declaration در بلوک Continuation ارائه می شود. هر بلوک Continuation باید با یک Block Declaration مرتبط باشد.


## منابع ##

* [فرمت فایل U3D - ویکی پدیا](https://en.wikipedia.org/wiki/Universal_3D)

* [مشخصات فرمت فایل ECMA U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


