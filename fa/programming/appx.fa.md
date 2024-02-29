{
  "date": "2021-04-22",
  "keywords": [
"فایل appx",
"افزونه",
"قالب",
"نحوه باز کردن فایل appx",
"فرمت فایل appx"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "APPX - فایل APPX چیست؟",
  "description": "درباره فرمت فایل APPX و APIهایی که می‌توانند فایل‌های APPX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-fax"
}
}،
  "lastmod": "2021-12-16"
}

## فایل APPX چیست؟

یک فایل APPX یک فرمت فایل بسته قابل توزیع است که برای توزیع و نصب یک برنامه کاربردی استفاده می شود. با ویندوز 8 معرفی شد تا در فروشگاه ویندوز مایکروسافت منتشر شود. این شامل تمام فایل های مورد نیاز برای نصب یک برنامه ویندوز است. اینها شامل اطلاعات فراداده، فایل‌ها و اطلاعات اعتبار هستند. فرمت فایل بسته بندی مدرن تر MSIX است که در حال حاضر در مقایسه با APPX بیشتر مورد استفاده قرار می گیرد.

## فرمت فایل APPX - اطلاعات بیشتر

فایل های APPX به عنوان فایل های فشرده در قالب فایل [ZIP](/compression/zip/) ذخیره می شوند. این باعث می شود که کل بسته به عنوان یک فایل بایگانی با حجم فایل کاهش یافته که به راحتی در فروشگاه مایکروسافت آپلود شود.

## چگونه فایل های موجود در فایل APPX را مشاهده کنیم؟

برای مشاهده محتویات یا فایل های داخل یک فایل APPX مراحل زیر باید دنبال شود.

 1. از آنجایی که فایل‌های APPX به صورت فایل‌های ZIP فشرده ذخیره می‌شوند، نام فایل را به پسوند zip. تغییر دهید
 1. برای استخراج فایل های موجود در فایل APPX از هر ابزار رفع فشرده سازی مانند 7-Zip، WinZip یا WinRAR استفاده کنید.

## چگونه یک فایل APPX ایجاد کنیم؟

دو روش برای ایجاد فایل های APPX وجود دارد.

 1. استفاده از MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) برای ایجاد بسته‌های برنامه (msix یا .appx.) و فایل‌های بسته بسته برنامه .msixbundle یا .appxbundle استفاده می‌شود. علاوه بر این، می تواند فایل ها را از یک بسته برنامه استخراج کند. MakeApp.exe با Windows 10 SDK موجود است و می توان از خط فرمان استفاده کرد.
 1. استفاده از Microsoft Visual Studio - توسعه دهندگان معمولاً [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) از Microsoft Visual Studio استفاده می کنند. پس از تکمیل توسعه برنامه و آماده شدن برنامه برای انتشار، می توان فایل بسته APPX را با انتشار آن از داخل ویژوال استودیو ایجاد کرد.

## منابع

 * [یک بسته یا بسته MSIX با MakeAppx.exe ایجاد کنید](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [ایجاد فایل‌های APPX با استفاده از Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

