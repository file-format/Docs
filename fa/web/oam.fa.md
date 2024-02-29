{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فایل OAM - فرمت فایل ویجت متحرک Adobe Edge",
  "description" : "درباره اینکه یک فایل OAM چیست و APIهایی که می توانند فایل OAM را ایجاد و باز کنند، بدانید.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-fa",
      "parent" : "web"
}
}،
  "lastmod" : "2023-01-30"
}

## فایل OAM چیست؟

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
کاربران می توانند با انتشار از یک پروژه Edge Animate (فایل AN) فایل های OAM ایجاد کنند.

## فرمت فایل OAM

یک فایل OAM به عنوان بایگانی فشرده شده [ZIP](/compression/zip/) در دیسک ذخیره می شود. این بدان معناست که می‌توانید پسوند فایل را به .zip تغییر نام دهید و با هر ابزار فشرده‌سازی مانند WinZIP یا WinRAR استخراج کنید. حجم فایل کاهش یافته انتقال و اشتراک گذاری انیمیشن را با سایر کاربران از طریق اینترنت آسان تر می کند.

### ساختار فایل OAM

ساختار فایل داخلی یک فایل .oam اختصاصی است و توسط Adobe به صورت عمومی مستند نشده است. با این حال، مشخص است که فایل‌های .oam حاوی مجموعه‌ای از فایل‌ها و منابع (مانند گرافیک، صدا و کد اکشن اسکریپت) هستند که در یک فایل واحد بسته‌بندی شده‌اند. محتویات یک فایل .oam ممکن است شامل فایل‌های [XML](/web/xml/)، فایل‌های SWF و فایل‌های منبع دیگر باشد. ساختار دقیق فایل .oam به نسخه خاصی از Adobe Animate که برای ایجاد آن استفاده شده است و همچنین به نوع انیمیشن و دارایی های موجود در فایل بستگی دارد.

یک فایل OAM حاوی اطلاعات زیر است.

`دارایی ها:` اطلاعاتی در مورد دارایی های گرافیکی، صوتی و تصویری مورد استفاده در انیمیشن.

`رفتارها:` شرح اقدامات و تعاملاتی که در انیمیشن رخ می دهد.

کد اکشن اسکریپت: کدی که برای کنترل رفتار و تعامل انیمیشن استفاده می شود.

`تنظیمات انتشار:` اطلاعات مربوط به پلتفرم و قالبی که انیمیشن در آن منتشر خواهد شد، مانند HTML5 یا AIR.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## چگونه فایل OAM را باز کنیم؟

برای باز کردن فایل های OAM می توانید از برنامه های زیر استفاده کنید.

 * Adobe Edge Animate CC (توقف شده)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## منابع

* [انتشار OAM] (https://helpx.adobe.com/animate/using/OAM-publishing.html)


