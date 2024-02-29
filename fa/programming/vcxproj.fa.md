{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"فایل",
"افزونه",
"فرمت فایل",
"پروژه ویژوال C++",
"راهنمای برنامه نویسی"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "درباره فرمت فایل VCXPROJ و API هایی که می توانند فایل های VCXPROJ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-faj"
}
},
  "lastmod": "2020-09-10"
}

## فایل VCXPROJ چیست؟

فایلی با پسوند vcxproj. یک فایل پروژه Microsoft Visual C++ است که اطلاعات پروژه [C++](/programming/cpp/) را ذخیره می‌کند. این شامل اطلاعاتی است که توسط سیستم پروژه MSBuild برای کامپایل و ساخت خروجی نهایی استفاده می شود. VCXPROJ پروژه های Visual C++ مانند پروژه [CSPROJ](/programming/csproj/) برای پروژه های دات نت است. فایل‌های VCXPROJ حاوی هیچ کدی نیستند، بلکه به تمام کلاس‌ها، اهداف و ویژگی‌های تعریف شده برای پروژه برای ساخت پروژه اشاره دارند. اینها را می توان در ویرایشگرهای متن ساده یا ترجیحاً در Microsoft Visual Studio IDE باز کرد.


## فرمت فایل VCXPROJ - اطلاعات بیشتر

فایل‌های VCXPROJ فایل‌های متنی هستند که در قالب فایل [XML](/web/xml/) ایجاد می‌شوند. اینها را می توان در هر ویرایشگر متنی باز کرد، اما به شدت توصیه می شود که از Microsoft Visual Studio IDE برای باز کردن و ویرایش این فایل ها استفاده کنید. اینها برای ویرایش دستی طراحی نشده اند. اشتباهات می توانند باعث از کار افتادن IDE یا رفتار غیرمنتظره شوند.

محتویات یک نمونه فایل VCXPROJ به شرح زیر است.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### عناصر فایل VCXPROJ

یک فایل معمولی VCXPROJ حاوی تعدادی عنصر است که در مثال XML بالا دیده می شود. [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) توسط مایکروسافت هر عنصر فایل را به تفصیل توضیح می‌دهد و از دیدگاه توسعه‌دهنده قابل ارجاع است.

#### عنصر پروژه

این گره ریشه فایل VCXPROJ است. MSBuild از این عنصر برای خواندن نسخه ساخت و هدف پیش فرض برای کامپایل استفاده می کند.

#### عنصر ProjectConfigurations ItemGroup

این شامل اطلاعات پیکربندی پروژه است که می تواند شامل روش ساخت (اشکال زدایی یا انتشار)، کامپایل 32 یا 64 بیتی، گزینه های بهینه سازی و موارد دیگر باشد. اطلاعات این گروه توسط IDE برای بارگذاری پروژه استفاده می شود.

#### عناصر پیکربندی پروژه

عناصر ProjectConfiguration در یک فایل VCXPROJ حاوی اطلاعاتی در مورد ساخت و پلت فرمی است که پروژه برای آن بارگذاری شده است. نام آن باید از فرمت «$(پیکربندی)|$(پلتفرم)» پیروی کند.

#### عنصر Globals PropertyGroup

این بخش شامل تنظیماتی است که اطلاعاتی را برای سطح پروژه ارائه می دهد مانند:

 * ProjectGuid
 * فضای نام ریشه
 * ApplicationType یا ApplicationTypeRevision


## منابع

* [ساختار VCXPROJ - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Project Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


