{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"فایل های پایگاه داده"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل LDF و API هایی که می توانند فایل های LDF را ایجاد و باز کنند آشنا شوید.",
  "title": "LDF - فرمت فایل اصلی پایگاه داده سرور SQL",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-faf"
}
}،
  "lastmod": "2020-08-12"
}

## فایل LDF چیست؟

یک فایل با پسوند .ldf یک فایل گزارش است که توسط Microsoft SQL Server نگهداری می شود که یک سیستم مدیریت پایگاه داده رابطه ای (RDBMS) است. تمام تراکنش های انجام شده بر روی فایل های پایگاه داده اولیه ([MDF](/database/mdf/)) (مانند درج، به روز رسانی، حذف) در فایل LDF ثبت می شود. فایل های LDF اجزای حیاتی هر پایگاه داده هستند. در صورت خرابی سیستم، فایل log برای بازگرداندن پایگاه داده به حالت ثابت استفاده می شود. اگر تراکنش ها به طور کامل متعهد نباشند، فایل لاگ تراکنش ها می تواند حجمش افزایش یابد. فایل های LDF را می توان با نرم افزار Microsoft SQL Server باز کرد.

## عملیات ثبت شده در فایل LDF

یک فایل log SQL عملیات زیر را ثبت می کند:

 * شروع و پایان هر معامله.

 * هر تغییر داده (درج، به روز رسانی یا حذف). این همچنین شامل تغییرات رویه‌های ذخیره‌شده سیستم یا بیانیه‌های زبان تعریف داده (DDL) در هر جدول، از جمله جداول سیستم می‌شود.

 * هر میزان و تخصیص صفحه یا تخصیص.

 * ایجاد یا انداختن جدول یا فهرست.

## فرمت فایل LDF

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. از آنجایی که عملیات در یک سریال ضبط می شود، تغییری که توسط LSN2 توضیح داده شده است، پس از ثبت رکورد LSN1 انجام شد. رکوردهای یک تراکنش خاص با استفاده از نشانگرهایی که استفاده می‌شوند به عقب مرتبط می‌شوند و بازگشت تراکنش را سرعت می‌بخشند.
 
## منابع

 * [فایل‌های پایگاه داده و گروه‌های فایل](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Transaction Log Architecture and Management Guide](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -نسخه 15)

