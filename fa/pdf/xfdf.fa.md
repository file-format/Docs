{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل XFDF - فایل XFDF چیست؟",
  "description": "درباره فایل XFDF و APIهایی که می‌توانند فایل‌های XFDF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-faf"
}
},
  "lastmod": "2019-09-10"
}

## فایل XFDF چیست؟

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## فرمت فایل XFDF - اطلاعات بیشتر

فایل های XFDF در قالب فایل XML ذخیره می شوند که یک فرمت جهانی است که برای واردات و صادرات داده ها استفاده می شود. ساختار فایل XFDF از یک هدر و به دنبال آن مقادیر فیلد و داده های عناصر تشکیل شده است که در زیر نشان داده شده است.

|عنصر|ویژگی|محتوا|
---|---|---|
|\<XFDF> ||بالاترین عنصر|
|\<fields> ||همه مقادیر فیلد این الگو|
|<field (T)> |نام |نام فیلد|
|<value (V)> |مقدار |مقدار فیلد|

## منابع

* [پشتیبانی از فرمت FDF توسط Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

