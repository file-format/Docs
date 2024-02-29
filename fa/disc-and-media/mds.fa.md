{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "درباره فرمت فایل MDS و APIهایی که می‌توانند فایل‌های MDS را ایجاد و باز کنند، بیاموزید.",
  "title" : "فرمت فایل MDS - Media Descriptor File Sidecar",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-fa",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## فایل MDS چیست؟

MDS (Media Descriptor Sidecar File) یک فایل مرتبط با نرم افزار Alcohol 120% و Daemon Tools است که هر دو برای ایجاد و مدیریت درایوهای CD و DVD مجازی استفاده می شوند. فایل MDS حاوی اطلاعاتی در مورد چیدمان داده های روی دیسک، از جمله مکان همه فایل ها و ساختار دیسک است. این به درایو مجازی اجازه می‌دهد تا رفتار یک دیسک فیزیکی را شبیه‌سازی کند، به طوری که نرم‌افزار می‌تواند داده‌های روی دیسک مجازی را مانند یک دیسک واقعی بخواند.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## ارتباط با الکل 120%

Alcohol 120% یک نرم افزار محبوب برای ایجاد و مدیریت درایوهای CD و DVD مجازی است و از فرمت فایل MDS برای ذخیره و دسترسی به تصاویر دیسک استفاده می کند. فرمت فایل MDS اختصاصی Alcohol 120% است و فقط توسط نرم افزار Alcohol 120% یا سایر نرم افزارهایی که از آن پشتیبانی می کنند باز و استفاده می شود.

## چگونه فایل MDS را باز کنیم؟

برای باز کردن یک فایل MDS در الکل 120٪، باید نرم افزار را روی رایانه خود نصب کنید. هنگامی که Alcohol 120% را نصب کردید، می توانید فایل MDS را با انجام کارهای زیر باز کنید:

1. راه اندازی الکل 120٪.
2. روی منوی File کلیک کنید و Open را انتخاب کنید.
3. به محل فایل MDS در رایانه خود بروید و آن را انتخاب کنید.
4. فایل MDS اکنون با الکل 120% باز می شود و از شما خواسته می شود فایل تصویر مربوطه (مانند ISO، BIN یا CUE) را انتخاب کنید.
5. پس از انتخاب فایل تصویر، Alcohol 120% تصویر را روی یک درایو مجازی نصب می کند.

یا اگر Alcohol 120% به عنوان برنامه پیش‌فرض برای باز کردن فایل‌های MDS تنظیم شده باشد، می‌توانید با دوبار کلیک کردن روی آن یک فایل MDS را باز کنید. همچنین می توانید از نرم افزارهای دیگری که از فرمت MDS پشتیبانی می کنند مانند Daemon Tools، Virtual CloneDrive، Virtual Drive Manager و MagicISO استفاده کنید.

## منابع
* [الکل 120% - نرم افزار رایت سی دی و دی وی دی](https://www.alcohol-soft.com/)


