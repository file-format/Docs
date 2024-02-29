{
  "date": "2020-08-20",
  "keywords": [
"فایل cff",
"فرمت فایل cff",
"فایل cff چیست",
"فایل",
"نمونه cff",
"پسوند فایل cff",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "CFF - فرمت فایل فونت فشرده",
  "description": "درباره فرمت فایل CFF و APIها برای ایجاد و باز کردن فایل های CFF بیاموزید.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-faf"
}
}،
  "lastmod": "2020-10-21"
}

## فایل CFF چیست؟

یک فایل با پسوند cff. یک فرمت فونت فشرده است و به عنوان PostScript Type 1 یا CIDFont نیز شناخته می شود. CFF به عنوان یک ظرف برای ذخیره فونت های متعدد با هم در یک واحد واحد به نام FontSet عمل می کند. طراحی فونت‌های CFF امکان جاسازی کد زبان PostScript را می‌دهد که به انعطاف‌پذیری و گسترش بیشتر قالب برای استفاده در محیط‌های چاپگر اجازه می‌دهد. فایل های فونت CFF را می توان با استفاده از API هایی مانند [Aspose.Font](https://products.aspose.com/font) باز و تبدیل کرد.

## فرمت فایل CFF

فایل‌های CFF فایل‌های باینری هستند که حاوی طرح‌بندی داده‌های ساخت‌یافته، دارای انواع داده‌های تعریف‌شده، هدر، سازمان‌دهی حروف و لغت‌نامه‌های جدول هستند. جزئیات بیشتر در مورد این موارد را می توان در [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff) یافت.

### طرح بندی داده ها
طرح داده فرمت فایل CFF مطابق شکل زیر است.

|ورود|نظر|
---|---|
|سربرگ|–|
|NameINDEX|–|
|برترین DICT INDEX|–|
|رشته INDEX|–|
|Global Subr INDEX|–|
|کدگذاری–چارت ها|–|
|FDSelect|فقط CIDFonts|
|CharStrings INDEX|در فونت|
|قلم DICT INDEX|در هر قلم، فقط CIDFonts|
| DICT خصوصی|در فونت|
|Local Subr INDEX|در فونت یا هر DICT خصوصی برای CIDFonts|
|اعلامیه های کپی رایت و علامت تجاری|–|

### انواع داده

انواع داده های CFF در جدول زیر نشان داده شده است.

|نام|محدوده|توضیحات|
---|---|---|
|Card8|0 –255|عدد بدون علامت 1 بایت|
|Card16|0 – 65535|عدد بدون علامت 2 بایت|
|Offset|متغیر|1، 2، 3 یا 4 بایت افست (مشخص شده توسط قسمت OffSize)|
|OffSize|1–4|عدد بدون علامت 1 بایت اندازه یک فیلد یا فیلدهای Offset را مشخص می کند|
|SID|0 – 64999|شناسه رشته 2 بایت|

### سرتیتر

داده های باینری با هدر با فرمت نشان داده شده در جدول زیر شروع می شود.

|نوع|نام|توضیحات|
---|---|---|
|Card8|مرجع|قالب کردن نسخه اصلی (شروع از 1)|
|Card8|مینور|نسخه مینور را قالب بندی کنید (شروع از 0)|
|Card8|hdrSize| اندازه سربرگ (بایت)|
|OffSize|offSize|اندازه افست مطلق (0)|

## منابع

 * [جدول فرمت فونت فشرده](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [فرمت فایل CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [مجموعه نمودار CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

