{
  "date": "2019-10-11",
  "keywords": [
"فایل csproj",
"csproj",
"افزونه",
"قالب",
"فایل csproj چیست؟",
"فرمت فایل csproj"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "درباره فرمت فایل CSPROJ و APIهایی که می‌توانند فایل‌های CSPROJ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-faj"
}
},
  "lastmod": "2021-05-21"
}

## فایل CSProj چیست؟
فایل‌های با پسوند CSPROJ یک فایل پروژه C# را نشان می‌دهند که شامل فهرست فایل‌های موجود در یک پروژه به همراه ارجاع به مجموعه‌های سیستم است. هنگامی که یک پروژه جدید در Microsoft VIiual Studio شروع می شود، یک فایل csproj. به همراه فایل راه حل اصلی ([.sln](/programming/sln/)) دریافت می کنید. اگر بیش از یک اسمبلی در یک پروژه وجود داشته باشد، تعداد مساوی فایل پروژه نیز وجود خواهد داشت که در آن فایل .sln همه آنها را به عنوان بخشی از پروژه به هم متصل می کند. محتویات این فایل تمامی الزامات مورد نیاز برای ساخت پروژه را تعریف می‌کند، مانند محتوای مورد نیاز، پلتفرم نیازمندی‌ها، اطلاعات نسخه‌سازی، تنظیمات وب سرور یا سرور پایگاه داده و وظایفی که باید انجام شوند. محتویات یک فایل پروژه در قالب فایل XML مرتب شده است و می تواند در هر ویرایشگر متنی برای ویرایش و همچنین مشاهده باز شود. همچنین یک دید منطقی به فایل های پروژه برای چیدمان مناسب می دهد.

## فرمت فایل CSPROJ #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

بخش‌های زیر عناصر فرمت فایل را برای فایل پروژه توضیح می‌دهند.

### عنصر پروژه ###

عنصر [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) عنصر اصلی هر فایل پروژه است. این طرح XML را برای فایل پروژه شناسایی می کند و می تواند شامل ویژگی هایی برای تعیین نقاط ورودی برای فرآیند ساخت باشد.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### خواص و شرایط

Properties نشان دهنده اطلاعات لازم برای ساخت یک پروژه است. چنین ویژگی هایی در یک عنصر [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) تعریف می شوند. این ویژگی‌ها از جفت‌های کلید-مقدار تشکیل شده‌اند که نام عنصر ویژگی، کلید ویژگی و محتوای عنصر، مقدار ویژگی را تعیین می‌کند. به عنوان مثال، می توانید ویژگی هایی با نام ServerName و ConnectionString برای ذخیره یک نام سرور ثابت و رشته اتصال تعریف کنید.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

شرایط را می توان از طریق عناصر به منظور تعیین معیارهای ارزیابی عنصر مشخص کرد. این مورد با کلمه Condition مشخص می شود در حالی که ویژگی را به شکل زیر تعریف می کند:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

هنگامی که MSBuild این تعریف ویژگی را پردازش می کند، ابتدا بررسی می کند که آیا یک مقدار ویژگی **$(OutputRoot)** موجود است یا خیر. اگر مقدار ویژگی خالی باشد - به عبارت دیگر، کاربر مقداری برای این ویژگی ارائه نکرده است - شرط به **true** و مقدار ویژگی روی **..\Publish\Out تنظیم می شود.**

### آیتم ها و گروه های آیتم

یک فایل پروژه ورودی هایی را برای فرآیند ساخت تعریف می کند که در واقع انواع مختلف فایل هستند. در نامگذاری MSBuild، این ورودی ها با عناصر Item نشان داده می شوند و در یک عنصر [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) تعریف می شوند. درست مانند عناصر **Property**، می توانید یک عنصر **Item** را هر طور که دوست دارید نام گذاری کنید. با این حال، شما باید یک ویژگی **Include** را برای شناسایی فایل یا علامت عامی که مورد نشان می دهد، مشخص کنید.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### اهداف و وظایف

یک عنصر [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) یک دستورالعمل ساخت (یا کار) را نشان می دهد. MSBuild شامل انبوهی از وظایف از پیش تعریف شده است. مثلا:

* وظیفه **کپی** فایل ها را در یک مکان جدید کپی می کند.

* وظیفه **Csc** کامپایلر Visual C# را فراخوانی می کند.

* وظیفه **Vbc** کامپایلر ویژوال بیسیک را فراخوانی می کند.

* وظیفه **Exec** یک برنامه مشخص را اجرا می کند.

* وظیفه **پیام** پیامی را به یک لاگر می نویسد.


وظایف همیشه باید در عناصر [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) قرار گیرند. عنصر **Target** مجموعه ای از یک یا چند کار است که به صورت متوالی اجرا می شوند و یک فایل پروژه می تواند شامل چندین هدف باشد.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## منابع

* [درک فایل پروژه - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- فایل)


