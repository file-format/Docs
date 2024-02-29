{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - فرمت فایل Microsoft OneNote",
  "description": "درباره فرمت فایل ONETOC2 و APIهایی که می‌توانند فایل‌های ONETOC2 را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-fa2"
}
}،
  "lastmod": "2019-09-10"
}

## ONETOC2 چیست؟ ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

هنگامی که یک نوت بوک در OneNote 2016 ایجاد می کنید، به طور خودکار در قالب فایل جدید 2010-2016 ذخیره می شود. اگر می‌خواهید همه ویژگی‌های OneNote 2016، مانند معادلات ریاضی و یادداشت‌های مرتبط، به درستی کار کنند، به این قالب نیاز دارید.

## فرمت فایل ONETOC2 ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### ساختار فایل ###

یک فایل ذخیره تجدید نظر باید با ساختار **Header** شروع شود. باقیمانده فایل به بلوک های بایت تقسیم می شود، جایی که اندازه و ساختار هر بلوک توسط فیلدی که به آن ارجاع می دهد مشخص می شود. یک بلوک در صورتی قابل دسترسی است که با ساختار **Header** به آن ارجاع داده شود، یا اگر توسط یک فیلد در بلوک قابل دسترس دیگری ارجاع داده شود. داده های خارج از ساختار **Header** و هر بلوک قابل دسترسی باید نادیده گرفته شوند.

همه ساختارها بر روی مرزهای 1 بایتی تراز شده اند. همه اعداد صحیح امضا می شوند مگر اینکه طور دیگری مشخص شده باشد. همه فیلدها [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) هستند مگر اینکه طور دیگری مشخص شده باشد.

#### سرتیتر ####

سربرگ فایل ONE شامل تکه‌هایی است که شامل شناسه‌ها و فیلدهای منحصربه‌فرد مختلف برای نمایش اطلاعات فایل به شرح زیر است:

`guidFileType (16 بایت):` GUID که نوع فایل ذخیره بازبینی را مشخص می کند. باید یکی از مقادیر جدول زیر باشد.

|فرمت فایل|مقدار
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 بایت):` یک GUID که هویت این فایل ذخیره سازی نسخه را مشخص می کند. باید در سطح جهانی منحصر به فرد باشد.

`guidLegacyFileVersion (16 بایت):` باید {00000000-0000-0000-0000-000000000000} باشد و MUST نادیده گرفته شود.

`guidFileFormat (16 بایت):` GUID که مشخص می کند که فایل یک فایل ذخیره تجدید نظر است. باید {109ADD3F-911B-49F5-A5D0-1791EDC8AED8} باشد.

`ffvLastCodeThatWroteToThisFile (4 بایت):` یک عدد صحیح بدون علامت. بسته به نوع فایل، باید یکی از مقادیر جدول زیر باشد.

|فرمت فایل|مقدار
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 بایت):` یک عدد صحیح بدون علامت. بسته به فرمت فایل این فایل، باید یکی از مقادیر جدول زیر باشد.


|فرمت فایل|مقدار
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 بایت):` یک عدد صحیح بدون علامت. بسته به فرمت فایل این فایل، باید یکی از مقادیر جدول زیر باشد.
:


|فرمت فایل|مقدار
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 بایت):` یک عدد صحیح بدون علامت. بسته به فرمت فایل این فایل، باید یکی از مقادیر جدول زیر باشد.


|فرمت فایل|مقدار
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## منابع ##

* [[MS-ONESTORE] - قالب فایل OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


