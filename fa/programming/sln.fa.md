{
  "date": "2019-10-11",
  "keywords": [
"فایل sln",
"نحوه اجرای فایل sln",
"sln",
"افزونه",
"قالب",
"فایل sln چیست؟",
"فرمت فایل sln",
"راه حل ویژوال استودیو",
"راه حل ویژوال استودیو در مقابل پروژه"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "درباره فرمت فایل SLN و APIهایی که می‌توانند فایل‌های SLN را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-fan"
}
}،
  "lastmod": "2019-09-10"
}

## فایل SLN چیست؟
یک فایل با پسوند .SLN یک فایل **راه حل ویژوال استودیو** را نشان می دهد که اطلاعات مربوط به سازماندهی پروژه ها را در یک فایل راه حل نگه می دارد. محتویات چنین فایل راه حلی به صورت متن ساده در داخل فایل نوشته می شود و با باز کردن فایل در هر ویرایشگر متنی قابل مشاهده/ویرایش است. اطلاعات موجود در یک فایل راه حل ثابت می ماند و برای بارگیری اطلاعات مرتبط با راه حل مانند [projects ](/programming/csproj/) و سایر اطلاعات مورد نیاز استفاده می شود. فایل های پروژه ای که فایل راه حل به آنها ارجاع می دهد حاوی اطلاعات اضافی برای فعال کردن محیط برای پر کردن سلسله مراتب با موارد آن پروژه است. هیچ داده ای در فایل sln. ذخیره نمی شود، اگرچه اطلاعات پروژه را می توان در صورت نیاز در فایل .sln نوشت.

## **تاریخچه نسخه های SLN** ##

نسخه فرمت راه حل با هر راه حل Microsoft Visual Studio با گذشت زمان تکامل یافته است. جزئیات در مورد این موارد به شرح زیر است.


|نسخه ویژوال استودیو|نسخه فرمت راه حل
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **محتویات یک فایل راه حل** ###

یک فایل راه حل شامل چندین بخش است که توسط محیط برای بارگذاری پروژه خوانده می شود. نمونه ای از محتویات فایل .sln مطابق شکل زیر است.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **اعلامیه پروژه** ###

یک فایل راه حل می تواند حاوی بیش از یک اعلان پروژه و همچنین انواع پروژه های متفاوت باشد. به عنوان مثال، یک فایل راه حل واحد می تواند شامل یک پروژه CSharp و همچنین یک پروژه VB.NET باشد. این انواع در یک راه حل با استفاده از [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) متمایز می شوند. بیانیه پروژه فوق را می توان برای درک واضح به شرح زیر تعمیم داد.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID برای انواع مختلف پروژه منحصر به فرد است و توسط راه حل خوان برای شناسایی نوع پروژه استفاده می شود. در این مورد، F184B08F-C81C-45F6-A57F-5ABD9991F28F نشان می دهد که یک پروژه VB.NET است.

`Project GUID:` GUID منحصر به فرد پروژه که آن را از سایر پروژه های موجود در راه حل متمایز می کند. شناسه منحصر به فرد یک پروژه در راه حل این امکان را برای پروژه های دیگر موجود در راه حل فراهم می کند تا به آن دسترسی داشته باشند.

بر اساس اطلاعات موجود در بخش پروژه فایل .sln، محیط هر فایل پروژه را بارگذاری می کند. سپس خود پروژه مسئول پر کردن سلسله مراتب پروژه و بارگذاری پروژه های تو در تو است. هر تغییری که در راه حل ایجاد شود، پس از ذخیره یا بسته شدن پروژه، به فایل راه حل ذخیره می شود.

## راه حل ویژوال استودیو در مقابل پروژه

**پروژه:** منطقاً وقتی شروع به ایجاد یک برنامه یا نرم افزار با استفاده از ویژوال استودیو می کنید، یک پروژه جدید را شروع می کنید. یک پروژه شامل تمام فایل های ضروری مانند کد منبع، نمادها، تصاویر، فایل های داده و موارد دیگر است که در یک برنامه اجرایی، وب سایت یا یک کتابخانه کامپایل می شوند.

**راه حل:** یک راه حل شامل یک یا چند پروژه است. بنابراین راه حل درست مانند یک ظرف برای پروژه های ویژوال استودیو است. منطقاً می‌توان گفت که شخصی می‌خواهد یک راه‌حل کامل برای کسب‌وکار خود از جمله وب‌سایت، اپلیکیشن دسک‌تاپ، سرویس آرامش‌بخش و اپلیکیشن موبایل دریافت کند.

### **منابع** ###

* [Solution File - توسط MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [GUIDهای نوع پروژه](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


