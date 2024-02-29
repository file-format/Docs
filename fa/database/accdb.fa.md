{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
"افزونه",
"فایل",
"فرمت فایل",
"نوع فایل پایگاه داده",
"فرمت فایل پایگاه داده",
"فایل های پایگاه داده"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل ACCDB و APIهایی که می‌توانند فایل‌های ACCDB را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل ACCDB - فایل پایگاه داده Microsoft Access 2007",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-fab"
}
},
  "lastmod": "2020-11-12"
}

## فایل ACCDB چیست؟

یک فایل با پسوند accdb. یک فایل پایگاه داده Microsoft Access 2007 است که داده های کاربران را در جداول ذخیره می کند. از ذخیره سازی پشتیبانی می کند
فرم های سفارشی، پرس و جوهای SQL و سایر داده ها. پس از اینکه مایکروسافت به ساختار فایل مبتنی بر XML تغییر مکان داد، فایل‌های ACCDB جایگزین فایل‌های [MDB](/database/mdb/) شدند. فایل های ACCDB هنوز هم می توانند با سازگاری قدیمی به MDB تبدیل شوند. با این حال، ACCDB فرمت فایل پایگاه داده دسترسی به طور گسترده در حال حاضر استفاده می شود. مایکروسافت همچنین از ویژگی‌های اضافی در قالب ACCDB مانند امکان ذخیره فایل‌های پیوست، داده‌های باینری و پشتیبانی از فیلد چند ارزشی پشتیبانی می‌کند.

## فرمت فایل ACCDB

مانند MDB، هیچ مشخصات عمومی برای فرمت فایل ACCDB در دسترس نیست. مایکروسافت از دسترسی برنامه‌ریزی شده به این فایل‌ها از طریق استاندارد Open Database Connectivity (ODBC) و Visual Basic for Applications (VBA) پشتیبانی می‌کند.

### یک بینش

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. در فایل‌های ACCDB، به نظر می‌رسد این نشانگر سازگاری فایل را نشان می‌دهد تا نسخه موتور ACE که برای ایجاد آن استفاده شده است.

## منابع

* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [موتور پایگاه داده جت مایکروسافت] (https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [از کدام فرمت فایل اکسس استفاده کنم؟](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


