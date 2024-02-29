{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"فایل",
"افزونه",
"فرمت فایل",
"فایل پروژه VB",
"راهنمای برنامه نویسی"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "درباره فرمت فایل VBPROJ و APIهایی که می توانند فایل های VBPROJ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-faj"
}
}،
  "lastmod": "2020-09-10"
}

## فایل VBPROJ چیست؟

یک فایل با پسوند vbproj. یک فایل پروژه مایکروسافت ویژوال بیسیک است که توسط موتور MSBuild مایکروسافت برای ساخت پروژه ها در یک راه حل ویژوال استودیو استفاده می شود. شبیه فایل [CSPROJ](/programming/csproj/) برای پروژه های دات نت است که در [C#](/programming/cs/) نوشته شده است. موتور MSBuild اطلاعات موجود در گروه های مختلف را از فایل های VBPROJ می خواند و فایل خروجی را تولید می کند. یک فایل VBPROJ می‌تواند حاوی اطلاعات مربوط به شناسه‌های جهانی، کلاس‌ها و ویژگی‌هایی باشد که پروژه را تعریف می‌کنند. فایل های VBPROJ را می توان با استفاده از Microsoft Visual Studio و هر ویرایشگر متن رایج مانند Notepad در سیستم عامل های Windows و MacOS باز و ویرایش کرد.

## فرمت فایل VBPROJ - اطلاعات بیشتر

فایل‌های VBPROJ فایل‌های متنی هستند که در قالب فایل [XML](/web/xml/) بر اساس [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019) نوشته می‌شوند. یک فایل VBPROJ حاوی اطلاعاتی در قالب تگ های XML است که اطلاعات مربوط به آن گروه خاص از تنظیمات را تعریف می کند. به شدت توصیه می شود که این فایل های تنظیمات را در Microsoft Visual Studio IDE باز و ویرایش کنید.

### عناصر VBPROJ

عناصر تشکیل دهنده یک فایل تنظیمات VB مانند تصویر زیر است.

{{< figure src="../vbproj.png" alt="فرمت فایل VBPROJ" >}}

The following table gives a brief description of these elements.

|عنصر|توضیحات|
---|---|
|پروژه| عنصر ریشه هر فایل پروژه و می تواند شامل ویژگی هایی برای تعیین نقاط ورودی برای فرآیند ساخت علاوه بر شناسایی طرح XML برای فایل پروژه باشد|
|خواص و شرایط| ویژگی ها از جفت های کلید-مقدار تشکیل شده و در یک عنصر PropertyGroup تعریف می شوند. نام عنصر خاصیت نمایانگر کلید ویژگی و محتوای عنصر مقدار ویژگی را مشخص می کند.|
|Items and ItemGroups|اقلام موجود در فایل پروژه ورودی‌های فرآیند ساخت هستند، مانند فایل‌های کد فایل، فایل‌های پیکربندی، فایل‌های فرمان، و سایر موارد مورد نیاز به عنوان بخشی از فرآیند ساخت. آیتم ها هستند و باید در یک عنصر ItemGroup تعریف شوند.|
|اهداف و وظایف| یک عنصر Task نشان دهنده یک دستورالعمل ساخت (یا وظیفه) فردی است. MSBuild شامل بسیاری از وظایف از پیش تعریف شده مانند Copy، CSC، VBC، Exec است. وظایف همیشه باید در یک عنصر «هدف» که مجموعه‌ای از یک یا چند کار است که به صورت متوالی اجرا می‌شوند، وجود داشته باشد و یک فایل پروژه می‌تواند شامل چندین هدف باشد.|

## منابع

* [درک فایل پروژه] (https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


