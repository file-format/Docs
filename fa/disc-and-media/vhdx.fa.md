{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل VHDX و API هایی که می توانند فایل های VHDX ایجاد و باز کنند آشنا شوید.",
  "title": "فرمت فایل VHDX - فایل VHDX چیست؟",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-fax"
}
},
  "lastmod": "2022-07-22"
}

## فایل VHDX چیست؟

یک فایل VHDX یک فایل تصویری دیسک با فرمت فایل Virtual Hard Disk v2 است. این شامل یک سیستم عامل کامل است که می تواند بارگیری شود و مانند هر ماشین معمولی برای آزمایش نرم افزار یا نرم افزار در حال اجرا که به یک سیستم عامل خاص نیاز دارد استفاده شود. یک VHDX، علیرغم اینکه یک تصویر کامل دیسک است، در یک فایل ذخیره می شود. نرم افزارهای ماشین مجازی مانند Parallels Desktop، Windows Virtual Machine و Virtual Box می توانند تصویر دیسک را بارگیری و باز کنند.

فایل VHDX را می توان با Hyper-V Manager به [VHD](/disc-and-media/vhd/) یا با VirtualBox به [VDI](/disc-and-media/vdi/) تبدیل کرد.

## فرمت فایل VHDX - اطلاعات بیشتر

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### پشتیبانی از هارد دیسک های مجازی در VHDX

از سه نوع هارد دیسک مجازی پشتیبانی می کند.

 1. ** هارد دیسک مجازی ثابت ** - هارد دیسک مجازی با اندازه داده ثابت اختصاص داده شده است. اندازه هارد دیسک مجازی با اضافه یا حذف داده ها تغییر نمی کند.

 1. ** هارد مجازی پویا ** - هارد دیسک مجازی با اندازه دیسک پویا. اندازه آن در هر زمان به اندازه داده های واقعی نوشته شده روی آن و ابرداده است. اندازه فایل آن به صورت پویا با افزودن یا حذف داده ها از آن افزایش می یابد.

 1. **تفاوت هارد دیسک مجازی** - جریان دیسک سخت مجازی را به عنوان مجموعه ای از بلوک های اصلاح شده در مقایسه با فایل هارد دیسک مجازی مادر نشان می دهد.

## منابع

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - توسط Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))


