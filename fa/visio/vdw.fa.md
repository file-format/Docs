{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "فرمت فایل VDW - Visio Graphics Service",
  "description":"درباره فرمت فایل VDW و API هایی که می توانند فایل های VDW ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-fa",
      "parent" : "visio"
}
}،
  "lastmod" : "2019-09-10"
}
## فایل VDW چیست؟

VDW فرمت فایل Visio Graphics Service است که جریان‌ها و ذخیره‌سازی‌های مورد نیاز برای ارائه یک طراحی وب را مشخص می‌کند. طراحی وب مجموعه‌ای از صفحات طراحی، اشکال، فونت‌ها، تصاویر، اتصالات داده‌ها و اطلاعات به‌روزرسانی نمودار است که می‌تواند به صورت وکتور یا ترسیم رستری ارائه شود. فایل‌های VDW را می‌توان در Microsoft Visio نیز باز کرد، اما در درجه اول برای استفاده در وب ذخیره می‌شوند. Microsoft Visio قابلیت تبدیل فایل‌های Visio را به چندین فرمت فایل از جمله [PNG](/image/png/)، [BMP](/image/bmp/)، [PDF](/pdf/) و موارد دیگر ارائه می‌دهد.

## **VDW** فرمت فایل

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|![Possible Implementation of a File](/web/vdw.png "Possible Implementation of a File")

## منابع

* [[MS-VGSFF]: Visio Graphics Service (vdw) فرمت فایل](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


