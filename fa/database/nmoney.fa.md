{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل NMONEY و APIهایی که می‌توانند فایل‌های NMONEY را ایجاد و باز کنند، بیاموزید.",
  "title": "فایل NMONEY - فرمت فایل حساب دنارو",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-fay"
}
},
  "lastmod": "2023-05-17"
}

## فایل NMONEY چیست؟

فایل NMONEY یک فایل پایگاه داده ذخیره سازی داده های مالی است که حاوی سوابق تراکنش های مالی است. توسط Nickvision توسعه داده شد و در نرم افزار Nickvision Denaro که یک نرم افزار مالی شخصی است استفاده شد. داده های ذخیره شده در یک فایل NOMONEY شامل اطلاعات تراکنش های اعتباری و بدهکاری به یک حساب است.

فایل های NOMONEY را می توان با برنامه [Github](https://github.com/NickvisionApps/Denaro) باز کرد.

## درباره نرم افزار دنارو

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### امکانات ارائه شده توسط Denaro

 * چندین حساب را به طور همزمان با محبوب ترین و آشناترین رابط برگه آن مدیریت کنید
 * تراکنش ها را بر اساس نوع، گروه یا تاریخ فیلتر کنید
 * تراکنش هایی مانند صورتحساب هایی که هر ماه اتفاق می افتد را تکرار کنید
 * انتقال پول از یک حساب به حساب دیگر
 * داده ها را از یک حساب به عنوان یک فایل CSV صادر کنید و یک فایل CSV، OFX یا QIF را وارد کنید تا تراکنش ها را به یک حساب اضافه کنید.

## فرمت فایل دنارو - اطلاعات بیشتر

فایل های دنارو با فرمت فایل باینری روی دیسک ذخیره می شوند. داده های مالی به عنوان یک فایل پایگاه داده در فرمت فایل **.SQLITE3** ذخیره می شود. SQLITE یک فایل پایگاه داده SQL سبک وزن است که با نرم افزار SQLite ایجاد شده است. این موتور پایگاه داده مستقلی را ارائه می دهد که قادر به ارائه پایگاه داده کاملاً برجسته و بسیار قابل اعتماد است. فایل های پایگاه داده SQLite را می توان برای به اشتراک گذاشتن محتوای غنی بین سیستم ها به سادگی با تبادل این فایل ها از طریق شبکه استفاده کرد. پیوندهای SQLite برای زبان های برنامه نویسی مانند C، [C#](/programming/cs/)، [C++](/programming/cpp/)، [Java](/programming/java/)، [PHP](/programming/php/) و بسیاری دیگر وجود دارد.

## منابع

 * [Nickvision](https://nickvision.org/)
 * [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

