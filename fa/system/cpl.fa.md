{
  "date": "2021-06-29",
  "keywords": [
"CPL",
"افزونه",
"فایل",
"قالب",
"سیستم",
"فایل کنترل پنل",
"پنجره ها",
"برنامه ها",
"کامپیوتر",
"کاربرد"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CPL - فایل کنترل پنل",
  "description": "درباره فرمت فایل CPL و APIهایی که می‌توانند فایل‌های CPL را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cp-fal"
}
},
  "lastmod": "2021-06-29"
}

## فایل CPL چیست؟ ##

یک فایل CPL نوعی فایل سیستم است. توسط سیستم عامل ویندوز استفاده می شود. یک فایل CPL مخفف Control Panel File است. این فایل ها فایل های باینری هستند که با کنترل پنل در سیستم عامل مایکروسافت ویندوز باز می شوند و برای نمایش و باز کردن ابزارهای موجود در کنترل پنل مانند ماوس، نمایشگر، شبکه و غیره استفاده می شوند. فایل‌های CPL معمولاً در پوشه سیستم در دستگاه شما ذخیره می‌شوند. این فایل ها نباید به صورت دستی باز شوند.


## فرمت فایل CPL ##

فایل‌های CPL مختلف در سیستم عامل ویندوز شما برای نمایش آیتم‌های مختلف کنترل پنل متصل هستند. همه آیتم های کنترل پنل به یک فایل CPL پیوند داده شده اند و پسوند .cpl به آیتم های آنها پیوست شده است.

برخی از انواع رایج فایل های CPL با فرمت آنها عبارتند از:

* Inetcpl.cpl - برای ویژگی های اینترنت در دستگاه شما

* Appwiz.cpl - برای افزودن یا حذف ویژگی های برنامه ها در دستگاه شما

* Desk.cpl - برای ویژگی های نمایش

* Main.cpl – برای ویژگی های مربوط به ماوس، فونت ها، صفحه کلید و چاپگرها. 

* Netcpl.cpl - برای خواص مرتبط با شبکه

* System.cpl - برای ویژگی های مربوط به سیستم و افزودن جادوگر سخت افزار جدید

* TimeDate.cpl - برای ویژگی های تاریخ یا زمان

* Mlcfg32.cpl - برای ویژگی های Microsoft Exchange یا Windows Messaging

* Intl.cpl - این مربوط به ویژگی های تنظیمات منطقه ای است

* Modem.cpl - برای ویژگی های مرتبط با مودم

* Themes.cpl – تم ها و ویژگی های دسکتاپ را ذخیره می کند. 

* Password.cpl - برای ویژگی های رمز عبور

* Mmsys.cpl - برای ویژگی های چند رسانه ای

* Wgpocpl.cpl - مربوط به Microsoft Mail Post Office است


## تاریخچه مختصر ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. هنوز هم در تمام نسخه‌های ویندوز استفاده می‌شود و تمام ویژگی‌های آیتم‌های کنترل پنل با استفاده از این نوع فایل ذخیره می‌شوند.

## مثال CPL ##

نمونه فایل CPL در زیر قابل مشاهده است:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
