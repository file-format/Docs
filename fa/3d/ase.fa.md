{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"فایل",
"قالب",
"نوع فایل",
"افزونه",
"فایل ASE چیست؟"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل ASE و APIهایی که می توانند فایل های ASE را باز و ایجاد کنند آشنا شوید.",
  "title": "ASE - Autodesk ASCII Scene Export File",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-fae"
}
},
  "lastmod": "2021-01-22"
}

## فایل ASE چیست؟

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## فرمت فایل ASE - اطلاعات بیشتر

فایل های ASE فایل های متنی ذخیره شده در فرمت ASCII هستند که می توانند در هر ویرایشگر متنی باز شوند. یک فایل ASE می تواند شامل انواع زیر از اطلاعات ارائه شده توسط Autodesk باشد.

### گزینه های خروجی

 * تعریف مش - تعریف هر مش را صادر می کند، از جمله اطلاعات راس و چهره برای اشیاء هندسی. علاوه بر این، روشن کردن این مورد، موارد موجود در کادر گروه Mesh Options را فعال می‌کند که در زیر توضیح داده شده است.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * تبدیل کلیدهای انیمیشن - شامل داده های انیمیشن تبدیل برای اشیاء است. اگر جسم یک دوربین هدف یا نورافکن باشد، این شامل داده های انیمیشن هدف می شود.
 * مش متحرک - یک تعریف مش کامل از هر n فریم را صادر می کند. فرکانس توسط چرخنده خروجی کنترلر که در زیر توضیح داده شده است، مشخص می شود. هر بلوک حاوی همان اطلاعات مشخص شده در کادر گروه Mesh Options است که در زیر توضیح داده شده است. روشن کردن این مورد می‌تواند منجر به یک فایل بزرگ، حتی برای صحنه‌های کوچک شود.
 * «تنظیمات دوربین متحرک/ نور» - داده‌های انیمیشن دوربین‌ها و نورها را صادر می‌کند، مانند رنگ، شدت، سقوط، سوگیری نقشه و غیره. همانطور که توسط چرخنده خروجی کنترلر مشخص شده است، هر n فریم یک بلوک را خروجی می دهد.
 * مفاصل حرکتی معکوس - تنظیمات مفصل IK را در شاخه Hierarchy صادر می کند.

### انواع شی

موارد در اینجا به شما امکان می دهند مشخص کنید که کدام دسته از شی را می خواهید در خروجی قرار دهید. می توانید اشیاء هندسی، اشکال، دوربین ها، چراغ ها و اشیاء کمکی را شامل کنید.

 * هندسی
 * شکل ها
 * دوربین ها
 * چراغ ها
 * یاوران

### گزینه های مش

 * Mesh Normals - حالت عادی و راس را صادر می کند. نرمال صورت در ابتدا فهرست شده است و به دنبال آن نرمال های سه راس پشتیبان صورت آمده است. روشن کردن این باعث می شود که یک فایل بسیار بزرگتر ایجاد شود.
 * «مختصات نگاشت» - فهرستی از رئوس و وجوه نگاشت را مطابق با ساختارهای TVert و TVFace که در کیت توسعه نرم افزار 3ds Max توضیح داده شده است صادر می کند. اگر یک شی از نقشه‌برداری چهره استفاده می‌کند، فهرست نقشه چهره حاوی مختصات UVW برای هر چهره صادر می‌شود.
 * رنگ های رأس - رنگ های راس را صادر می کند.

### خروجی کنترلر

 * استفاده از کلیدها - مقادیر کلید را صادر می کند. اگر کنترلر از کلیدها استفاده نمی کند، از روش نمونه برداری نیرو استفاده می شود. در مورد کنترل‌کننده‌های تبدیل، گزینه Use Keys تنها در صورتی کار می‌کند که همه کنترل‌کننده‌های تبدیل Linear/TCB یا Bezier باشند. اگر یکی از مسیرهای تبدیل از نوع متفاوتی از کنترلر استفاده کند، روش نمونه گیری نیرو برای همه مسیرهای تبدیل استفاده می شود.
 * «نمونه‌های اجباری» - مقادیر کنترل‌کننده را بر اساس فرکانس مشخص‌شده در فریم‌ها به ازای هر کنترل‌کننده نمونه نمونه‌برداری می‌کند.

## منابع

 * [Autodesk - صادرات به ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

