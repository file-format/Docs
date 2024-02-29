{
  "date": "2021-04-22",
  "keywords": [
"فایل msix",
"افزونه",
"قالب",
"نحوه باز کردن فایل msix",
"فرمت فایل msix"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX - فایل MSIX چیست؟",
  "description": "درباره فایل MSIX و APIهایی که می‌توانند فایل‌های MSIX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-fax"
}
},
  "lastmod": "2021-12-16"
}

## فایل MSIX چیست؟

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. این قالب فایل بسته مدرن در مقایسه با [APPX](/programming/appx/) و MSI است که در نهایت به این فرمت فایل جدید حذف خواهد شد. می توان از آن برای استقرار برنامه های Win32، WPF و Windows Forms استفاده کرد. فایل های MSIX قابل اعتماد هستند و شبکه و فضای دیسک را هدف قرار می دهند. توسعه دهندگان از اینها برای توزیع برنامه ها به کاربران نهایی از طریق فروشگاه مایکروسافت (که قبلاً به نام Windows Store شناخته می شد) استفاده می کنند.

## فرمت فایل MSIX - اطلاعات بیشتر

فایل‌های MSIX [ZIP](/compression/zip/)-فشرده شده‌اند و همه فایل‌ها در داخل فایل بسته‌بندی شده گنجانده شده‌اند. علاوه بر فایل‌های مربوط به برنامه، فایل MSIX حاوی فایل‌های پیکربندی [.xml](/web/xml/) است که حاوی اطلاعات مربوط به نصب برنامه است.

## داخل یک بسته MSIX چیست؟

یک بسته MSIX از فایل های زیر تشکیل شده است.

 * AppxBlockMap.xml - که به عنوان فایل نقشه بلوک بسته شناخته می شود، یک سند XML است که حاوی لیستی از فایل های برنامه با نمایه ها و هش های رمزنگاری برای هر بلوک داده ای است که در بسته ذخیره می شود.
 * «AppxManifest.xml» - یک سند XML که حاوی اطلاعات مورد نیاز برای استقرار، نمایش و به‌روزرسانی یک برنامه MSIX است. این اطلاعات شامل هویت بسته، وابستگی‌های بسته، قابلیت‌های مورد نیاز، عناصر بصری و نقاط توسعه‌پذیری است.
 * AppxSignature.p7x - فایلی که هنگام امضای بسته ایجاد می شود. همه بسته های MSIX باید قبل از نصب امضا شوند. با AppxBlockmap.xml، پلتفرم قادر است بسته را نصب کرده و اعتبار سنجی شود.

## منابع

 * [نمایش کلی MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [ایجاد فایل‌های APPX با استفاده از Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

