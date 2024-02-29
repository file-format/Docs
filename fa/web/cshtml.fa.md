{
  "date": "2019-10-11",
  "keywords": [
"cshtml",
"فایل cshtml",
"فرمت فایل cshtml",
"نوع فایل cshtml",
"فایل",
"نوع",
"فایل cshtml چیست"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSHTML - صفحه وب ASP.NET Razor",
  "description": "درباره فرمت فایل CSHTML و APIهایی که می‌توانند فایل‌های CSHTML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CSHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cshtm-fal"
}
},
  "lastmod": "2021-04-29"
}

## فایل CSHTML چیست؟

یک فایل با پسوند cshtml. یک فایل HTML [C#](/programming/cs/) است که در سمت سرور توسط موتور Razor Markup برای ارائه فایل‌های صفحه وب به مرورگر کاربر استفاده می‌شود. این کدگذاری سمت سرور شبیه به صفحه استاندارد ASP.NET است که امکان ایجاد محتوای وب پویا را به هنگام نوشتن صفحه وب روی مرورگر فراهم می کند. سرور قبل از ارسال صفحه تولید شده به مرورگر، کد سمت سرور را در داخل صفحه اجرا می کند. کارهای پیچیده مانند دسترسی به پایگاه های داده و ارائه نماهای پیچیده. فایل های CSHTML را می توان با استفاده از Microsoft Visual Studio تولید و برنامه ریزی کرد.

## فرمت فایل CSHTML

فایل های CSHTML فایل های متنی هستند که از نحو مشخص شده توسط موتور نشانه گذاری Razor پیروی می کنند. Razor از هر دو C# و VB.NET پشتیبانی می کند و یادگیری و استفاده از آن نسبت به ASP و ASP.NET کلاسیک آسان است. w3schools یک راهنمای ساده و در عین حال موثر برای کدنویسی [syntax of C# and VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) Razor دارد.

### مثال CSHTML

در زیر نمونه کد سی شارپ مورد استفاده در فایل CSHTML برای Razor است.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

کد VB.NET معادل برای Razor به شرح زیر است.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## منابع

* [Razor Syntax Reference - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)


