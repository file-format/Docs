{
  "date": "2023-05-15",
  "keywords": [
"فایل vcproj",
"فایل vcproj چیست",
"نمونه ای از فایل vcproj",
"فایل vcproj شامل چه چیزی است",
"فرمت فایل vcproj چیست؟",
"فایل",
"پسوند فایل vcproj",
"افزونه"
]،
  "author": {
    "display_name": "Shakeel Faiz"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل VCPROJ - فایل پروژه ویژوال C++",
  "description": "درباره فرمت VCPROJ و APIهایی که می‌توانند فایل‌های VCPROJ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
      "parent": "programming"
}
}،
  "lastmod": "2023-05-15"
}

## فایل VCPROJ چیست؟

A VCProj file, also known as Visual C++ Project file, is an XML-based file that stores configuration and settings for project in Microsoft Visual Studio. VCProj files are primarily used in older versions of Visual Studio, up to Visual Studio 2010. از Visual Studio 2012، فایل های پروژه به فرمت جدید به نام VCXProj تغییر یافت.

فایل VCProj حاوی اطلاعاتی در مورد فایل‌های کد منبع پروژه، تنظیمات ساخت، گزینه‌های کامپایلر، تنظیمات پیوند دهنده و سایر پیکربندی‌های خاص پروژه است. این تعریف می کند که پروژه چگونه ساخته می شود و چه فایل هایی در پروژه گنجانده شده است.

## نمونه ای از فایل VCPROJ

در اینجا مثالی از شکل ظاهری فایل VCProj آورده شده است:

```
<?xml version="1.0" encoding="Windows-1252"?>
<VisualStudioProject
	ProjectType="Visual C++"
	Version="9.00"
	Name="MyProject"
	ProjectGUID="{01234567-89AB-CDEF-0123-456789ABCDEF}"
	Keyword="Win32Proj"
	>
	<Platforms>
		<Platform
			Name="Win32"
		/>
	</Platforms>
	<ToolFiles>
	</ToolFiles>
	<Configurations>
		<Configuration
			Name="Debug|Win32"
			ConfigurationType="1"
			InheritedPropertySheets="$(VCInstallDir)VCProjectDefaults\UpgradeFromVC71.vsprops"
		>
			<Tool
				Name="VCCLCompilerTool"
				AdditionalIncludeDirectories=".\include"
				PreprocessorDefinitions="_DEBUG;WIN32;_WINDOWS"
				RuntimeLibrary="3"
				UsePrecompiledHeader="0"
			/>
			<Tool
				Name="VCLinkerTool"
				AdditionalDependencies="kernel32.lib user32.lib"
				OutputFile="$(OutDir)\MyProject.exe"
				LinkIncremental="2"
				SuppressStartupBanner="true"
			/>
		</Configuration>
	</Configurations>
	<References>
	</References>
</VisualStudioProject>

```

## فایل VCPROJ شامل چه چیزی است؟

یک فایل VCProj شامل عناصر و تنظیمات مختلف مربوط به پروژه Visual C++ در Microsoft Visual Studio است. در اینجا برخی از اطلاعات کلیدی که در فایل VCProj یافت می شود آورده شده است:

- **Project Information:** The VCProj file includes project-level information such as the project name, project type, version, and unique identifier (GUID) for the projec-fat.
- **پلتفرم ها و پیکربندی ها:** پلتفرم ها و پیکربندی های پشتیبانی شده توسط پروژه را مشخص می کند. پلتفرم‌ها پلتفرم هدف را تعریف می‌کنند، مانند Win32، x64، یا ARM، در حالی که پیکربندی‌ها پیکربندی‌های ساخت متفاوتی مانند Debug یا Release را تعریف می‌کنند.
- **فایل های منبع:** فایل VCProj فایل های کد منبع را که بخشی از پروژه هستند، شامل فایل های ++C، فایل های هدر، فایل های منبع و سایر فایل های مرتبط فهرست می کند. هر فایل معمولاً با مسیر نسبی خود به دایرکتوری پروژه مشخص می شود.
- **تنظیمات ساخت:** شامل تنظیمات مربوط به فرآیند ساخت، مانند گزینه های کامپایلر، گزینه های پیوند دهنده، تعاریف پیش پردازنده، فهرست های اضافی شامل، و وابستگی های اضافی است. این تنظیمات نحوه ساخت و پیوند پروژه را مشخص می کند.
- **سرصفحه های از پیش کامپایل شده:** فایل VCProj می تواند مشخص کند که آیا پروژه از هدرهای از پیش کامپایل شده استفاده می کند یا خیر، و اگر چنین است، کدام فایل به عنوان هدر از پیش کامپایل شده عمل می کند.
- **اطلاعات خروجی:** فایل خروجی یا فایل های تولید شده توسط فرآیند ساخت را تعریف می کند، مانند فایل اجرایی، کتابخانه پیوند پویا (DLL)، یا کتابخانه ایستا (LIB). مسیر فایل خروجی و نام را می توان در فایل VCProj پیکربندی کرد.
- ** مراجع:** فایل VCProj ممکن است حاوی ارجاعاتی به پروژه های دیگر یا کتابخانه های خارجی باشد که پروژه به آنها وابسته است. این مراجع به حل وابستگی ها در طول فرآیند ساخت کمک می کند.
- **مراحل ساخت سفارشی:** اگر پروژه به مراحل ساخت سفارشی اضافی مانند اجرای اسکریپت ها یا اجرای ابزارهای خارجی نیاز دارد، فایل VCProj می تواند شامل دستورالعمل هایی برای این مراحل باشد.
- **اشکال زدایی و استقرار:** فایل VCProj ممکن است شامل تنظیمات مربوط به اشکال زدایی، استقرار و سایر پیکربندی های خاص پروژه باشد.

## فرمت فایل VCPROJ چیست؟

فرمت فایل VCProj بر اساس XML (زبان نشانه گذاری eXtensible) است که یک زبان نشانه گذاری استاندارد برای نمایش داده های ساخت یافته است. فرمت XML امکان سازماندهی و ذخیره سازی اطلاعات و تنظیمات خاص پروژه را در یک ساختار سلسله مراتبی می دهد.

## منابع
* [Project and Solution Files](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)


