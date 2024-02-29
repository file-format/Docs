{
  "date": "2022-03-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSO - فایل مرجع ماکرو آفیس مایکروسافت",
  "description": "درباره فایل MSO و APIهایی که می‌توانند فایل‌های MSO را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MSO",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ms-fao"
}
},
  "lastmod": "2022-03-12"
}

## فایل MSO چیست؟

An MSO file is a data container file format that is created when an HTML message is sent using Microsoft Outlook. This happens mostly with Microsoft Office 2000 applications. In most of the cases, the email message is attached with the name **Oledata.mso** file. The email recipient, when opens such an email, can view the file correctly even if they don't have the same software installed. MSO files refer to [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## فرمت فایل مایکروسافت MSO

فایل‌های MSO در قالب فایل سند مرکب مایکروسافت (MCDF) ذخیره می‌شوند که با نام‌های پیوند و جاسازی شی (OLE) یا مدل شیء مؤلفه (COM) فرمت فایل باینری اجرای فایل ترکیبی ذخیره‌سازی ساختاریافته نیز شناخته می‌شود.

### ساختار فرمت فایل MSO

The internal file format structure of MSO file format is well-defined in the [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) section of MCDF documentation.  The File Allocation Table (FAT) manages the sector allocation and sector chains. It contains an array of 32-bit sector numbers. Each index in the array represents a sector number whereas its value represents the next sector in the chain or a special value.

## منابع

* [COM Structured Storage] (https://en.wikipedia.org/wiki/COM_Structured_Storage)

* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

