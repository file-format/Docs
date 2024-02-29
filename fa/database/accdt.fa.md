{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
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
  "description": "درباره فرمت فایل ACCDT و API هایی که می توانند فایل های ACCDT را ایجاد و باز کنند، بیاموزید.",
  "title": "ACCDT - قالب فایل پایگاه داده قالب Microsoft Access 2007",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-fat"
}
}،
  "lastmod": "2020-11-12"
}

## فایل ACCDT چیست؟

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## فرمت فایل ACCDT

فایل های قالب ACCDT بر اساس مشخصات XML Open Office هستند و تمام داده ها در یک بسته ZIP موجود است. اطلاعات ساختار و محتوای پایگاه داده در فایل‌ها و فایل‌های متنی [XML](/web/xml/) موجود است و از طریق روابط به یکدیگر پیوند داده می‌شوند. می توانید نام یک فایل ACCDT را به پسوند [.zip](/compression/zip/) تغییر دهید و از هر نرم افزار فشرده سازی برای استخراج محتویات بایگانی ZIP استفاده کنید.

### ساختار فایل

فایل های ACCDT بسته هایی هستند که شامل مجموعه ای از قطعات مرتبط هستند. هر **بخش** اطلاعاتی را در مورد محتوای یک برنامه پایگاه داده با استفاده از XML، متن و فرمت های باینری ذخیره می کند که شامل موارد زیر است:

 * اشیاء پایگاه داده
 * فراداده مرتبط
 * ساختار بسته

#### پکیج

یک بسته یک بایگانی [ZIP](/compression/zip/) است که شامل چندین بخش است و با قراردادهای بسته بندی باز مشخص شده در [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html) مطابقت دارد. فایل های ACCDT باید حاوی حداقل یک بخش متادای الگو باشد که باید هدف یک رابطه باشد. این فراداده الگو قسمت شروع یک فایل ACCDT است.

#### قسمت

یک قسمت جریانی از بایت ها است که یک نوع مرتبط برای تعیین ماهیت و نوع محتوای ذخیره شده در آن دارد. شمارش قطعات، بخش‌های معتبر، انواع محتوای معتبر و روابط مورد نیاز بین تمام قسمت‌های یک بسته را مشخص می‌کند.

#### ارتباط

رابطه بسته - جایی که هدف بخشی است و منبع بسته به عنوان یک کل است.

ارتباط بخشی به قسمت - جایی که هدف بخشی است و منبع بخشی از بسته است.

رابطه صریح - جایی که یک منبع از محتوای یک بخش منبع با ارجاع یک عنصر رابطه با مقدار ویژگی ID آن ارجاع داده می شود.

رابطه ضمنی - رابطه ای که صریح نیست.

رابطه داخلی - جایی که هدف بخشی از بسته است.

رابطه خارجی - جایی که هدف یک منبع خارجی است که در بسته نیست.

## منابع ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

