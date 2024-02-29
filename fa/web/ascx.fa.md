{
  "date": "2019-10-11",
  "keywords": [
"ascx",
"فایل ascx",
"فرمت فایل ascx",
"نوع فایل ascx",
"فایل",
"نوع",
"فایل ascx چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل ASCX",
  "description": "درباره فایل ASCX و APIهایی که می‌توانند فایل‌های ASCX را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "ASCX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asc-fax"
}
},
  "lastmod": "2020-09-10"
}

## فایل ASCX چیست؟

یک فایل با پسوند ascx. یک کنترل کاربر است که به عنوان یک جزء قابل استفاده مجدد در صفحات وب استفاده می شود. در هر وب سایت ASP با کشیدن آن از جعبه کنترل به صفحه ارجاع داده می شود. کنترل‌های کاربران ASCX به عنوان منبع مرکزی به پروژه اضافه می‌شوند و در نتیجه هرگونه تغییر در کنترل کاربر در کل وب‌سایت منعکس می‌شود. برخلاف فایل‌های ASMX که مکانیزمی را برای برقراری ارتباط بین ۲ شی از طریق اینترنت تعریف می‌کنند، فایل‌های ASCX کنترل‌های کاربر برای جاسازی در صفحات یا وب‌سایت هستند.

## فرمت فایل ASCX

فایل‌های ASCX در قالب متن ساده نوشته می‌شوند و می‌توانند از کدهای پشت ویژگی مانند صفحات وب استفاده کنند که به .ascx.cs ختم می‌شود. کد نشانه گذاری کنترل های کاربر با دستور @Control همانطور که در مثال زیر نشان داده شده است شروع می شود.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

این کنترل کاربر وب را می توان در بسیاری از صفحات مانند پاورقی صفحه، هدر یا نوعی ناوبری سایت مورد استفاده مجدد قرار داد. کنترل‌های کاربر وب دارای ویژگی‌ها، روش‌ها و رویدادهایی مانند هر کنترل دیگری هستند که آنها را در تنظیم رفتار بصری آنها مفید می‌سازد.

### مثالی از ثبت کنترل های کاربر در web.config

به منظور استفاده از یک کنترل کاربر در بسیاری از صفحات، کنترل وب را می توان در web.config ثبت کرد. این اجازه می دهد تا به جای ثبت نام در هر صفحه به صورت جداگانه، از کنترل تمام وب سایت استفاده کنید. کد نمونه زیر نحوه ثبت کنترل وب در web.config را برای نمایش به عنوان فوتر در کل وب سایت تعریف می کند.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## منابع

 * [ASCX در مقابل ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
 * [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

