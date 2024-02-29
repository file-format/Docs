
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل AML - فایل زبان نشانه گذاری Microsoft Assistance",
  "description":"درباره اینکه فایل AML چیست و APIهایی که می توانند فایل های AML را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml-fa",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - فایل زبان نشانه گذاری Microsoft Assistance

## فایل AML چیست؟

فایل AML (Assistance Markup Language) یک فایل XML است که با Microsoft Assistance Markup Language (MAML) تولید شده است. این توسط مایکروسافت برای ارائه کمک آنلاین برای سیستم عامل مایکروسافت ویندوز توسعه یافته است. قبل از این، راهنمای ویندوز در قالب فایل HTML [CHM](/web/chm/) کامپایل شده در دسترس بود. فایل‌های AML یک سند ساختاریافته ارائه می‌کنند که به برنامه اجازه می‌دهد کد منبع ایجاد کند و از صفحات راهنما پشتیبانی کند. این اجازه می دهد تا اسناد و عناصر تشکیل دهنده آنها را بر اساس زمینه آنها تعریف کنید. فایل‌های راهنمای AML به‌صورت آنلاین منتشر می‌شوند و می‌توان آن‌ها را طوری پیکربندی کرد که از به‌روزرسانی‌های بسته موجود به‌صورت آنلاین به‌روزرسانی شوند.

## ساختار فایل MAML

فایل‌های AML تولید شده با استفاده از MAML به‌عنوان فایل‌های [XML](/web/xml/) ذخیره می‌شوند که می‌توانند برای بیان طیف وسیعی از مفاهیم فعال استفاده شوند. همچنین می‌تواند راهنمای هدایت‌شده (جادوگر محتوای فعال) را ارائه دهد که فایل راهنما را با جادوگر گام به گام برای کاربر تعاملی می‌کند.

An AML file generated using the MAML follows its authoring structure that can be divided into segments like:

 * مفهومی
 * سوالات متداول
 * واژه نامه
 * روش
 * ارجاع
 * محتوای قابل استفاده مجدد
 * وظیفه
 * عیب یابی و
 * آموزش

## چگونه فایل های MAML ایجاد کنیم؟

فایل های MAML را می توان با استفاده از یکی از روش های زیر ایجاد کرد:

 * استفاده از Sandcastle - از مجموعه ای از طرحواره ها و برنامه های اجرایی برای تولید فایل راهنما استفاده می کند. با این حال، این ابزار متوقف شده است.
 * استفاده از DocProject - یک افزونه Microsoft Visual Studio که می تواند از داخل Microsoft Visual Studio برای تولید محتوای راهنما اجرا شود.

فایل‌های MAML را می‌توان با استفاده از Sandcastle، مجموعه‌ای از طرحواره‌های XSL. و برنامه‌های اجرایی ایجاد کرد. همچنین ممکن است با استفاده از DocProject، یک افزونه ابزار نویسندگی کمک Microsoft Visual Studio ایجاد شوند.

## منابع

 * [راهنمایی مبتنی بر XML با استفاده از PlatyPS ایجاد کنید](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
 * [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - فایل زبان ماکرو Arc

## فایل ARC Macro AML چیست؟

یک فایل AML (ARC Macro Language) یک فایل اسکریپت است که با برنامه ArcInfo Workstation GIS تولید شده است. این زبان به زبان ARC Macro نوشته شده است که یک زبان الگوریتمی سطح بالا برای ایجاد برنامه های GIS در ArcInfo است. AML توسط ESRI در سال 1986 طراحی شد و هدف آن ایجاد برنامه های کاربردی از خط فرمان سیستم ARCINFO GIS بود. به عنوان فایل اسکریپت نویسی، فایل های AML می توانند حاوی دستورات اسکریپت برای انجام تعدادی از وظایف مانند ایجاد اجزای رابط کاربری و دستکاری داده های نقشه باشند.

## فرمت فایل AML - اطلاعات بیشتر

AML که فایل های اسکریپت نویسی است، اطلاعات را به عنوان فایل متنی ساده روی دیسک ذخیره می کند. از دستور AML پیروی می کند که بر اساس زبان پوسته CPL سیستم عامل PRIMOS است. زبان AML با چارچوب geoprocessing ESRI جایگزین شده است که بخشی از مجموعه ArcGIS است و از ArcObjects برای ارائه پشتیبانی برنامه نویسی از طریق VBA یا Python استفاده می کند.

## منابع

 * [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
 * [استفاده از AML با ابزارهای اسکریپت](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

