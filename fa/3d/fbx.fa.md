{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"فایل",
"افزونه",
"قالب",
"فرمت فایل سه بعدی"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "Your file format guide to know what is an FBX file and APIs that can create and open them.",
  "title": "FBX - FilmBox 3D File Format",
  "linktitle": "FBX",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-fbx"
}
}،
  "lastmod": "2019-09-10"
}

## فایل FBX چیست؟

FBX، FilmBox، یک فرمت فایل سه بعدی محبوب است که در ابتدا توسط Kaydara برای MotionBuilder توسعه داده شد. در سال 2006 توسط Autodesk Inc خریداری شد و اکنون یکی از اصلی ترین فرمت های تبادل سه بعدی است که توسط بسیاری از ابزارهای سه بعدی استفاده می شود. FBX در هر دو فرمت فایل باینری و ASCII موجود است. این قالب برای ایجاد قابلیت همکاری بین برنامه های کاربردی ایجاد محتوای دیجیتال ایجاد شد. ابزارهای زیادی برای تبدیل از/به فرمت فایل FBX وجود دارد.

## فرمت فایل FBX - اطلاعات بیشتر

FBX یک فرمت اختصاصی است و مشخصات فرمت فایل باینری آن به طور رسمی در دسترس نیست. یک C++ FBX SDK توسط Autodesk برای خواندن، نوشتن و تبدیل به/از فایل FBX ارائه شده است. یک اسکریپت واردات و صادرات Python برای FBX نیز در نرم افزار Blender موجود است که از FBX SDK استفاده نمی کند.

### ساختار فایل مبتنی بر متن

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* شناسه NodeType (نام کلاس)

* چندین ویژگی مرتبط با آن، عناصر تاپل انواع داده های اولیه معمولی هستند: ##float، integer، string## و غیره.

* لیستی که شامل گره هایی با همان فرمت (به صورت بازگشتی) است.


اینها را می توان به صورت منطقی به صورت زیر نشان داد:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

برخی از گره های استاندارد به عنوان لیست ضمنی تعریف می شوند که در آن هر مورد از یک لیست تودرتو تشکیل شده است. هر برنامه‌ای که قصد دسترسی به هندسه FBX را دارد، باید این مطالب را تجزیه کند و معنای مفیدی از آن بسازد. نمونه ای از فایل FBX مبتنی بر متن به شرح زیر است:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## ساختار فایل باینری فایل های FBX

همانطور که قبلاً گفته شد، مشخصات فرمت فایل FBX به صورت عمومی برای FBX در دسترس نیست. از آنجایی که Blender Foundation فرمت فایل FBX را بدون استفاده از SDK ارائه شده توسط شرکت پیاده‌سازی می‌کند، برخی از جزئیات مربوط به فرمت فایل باینری [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) به عنوان بخشی از اجرای آن است.

ساختار فایل های باینری به ترتیب زیر است:

* سرتیتر

* ثبت شی

* پاورقی


### سربرگ FBX

اطلاعات هدر فایل از 27 بایت تشکیل شده است.

* بایت 0 - 20: Kaydara FBX Binary \x00 (فایل جادویی، با 2 فاصله در انتها، سپس یک پایان دهنده NULL).

* بایت های 21 - 22: [0x1A, 0x00]## (ناشناخته اما همه فایل های مشاهده شده این بایت ها را نشان می دهند).

* بایت 23 - 26: int بدون امضا، شماره نسخه. به عنوان مثال 7300 برای نسخه 7.3.


### رکورد شی ###

Header توسط یک رکورد شی دنبال می شود که یک رکورد گره کامل با نام خالی و لیست دارایی خالی است. به صورت بازگشتی شامل کل تشکیل پرونده است.

### پاورقی ###

بخش FBX Footer در انتهای فایلی قرار دارد که محتوای آن ناشناخته است.

## فرمت های ضبط ##

سوابق موجود در یک فایل FBX به صورت زیر دسته بندی می شوند:

* سوابق گره

* سوابق اموال


### فرمت ضبط گره ###

هر فرمت ضبط گره نام دارد و دارای طرح حافظه زیر است.


|اندازه (بایت)|نوع تاریخ|نام
--- | ---|---|
|4|UInt32|EndOffset
|4|UIint32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NameLength|char|نام
|?|?|ویژگی[n]، جایی که n = 0:PropertyListLen
|اختیاری| |
|?|?|NestedList
|13|uint8[]|ثبت صفر

جایی که:

* «EndOffset» فاصله از ابتدای فایل تا انتهای رکورد گره است (یعنی اولین بایت از هر چیزی که بعد می آید). از این می توان برای رد شدن آسان از سوابق ناشناخته یا غیر ضروری استفاده کرد.

* "NumProperties" تعداد خصوصیات در تاپل مقدار مرتبط با گره است. لیست تودرتو به عنوان آخرین عنصر به عنوان ویژگی محاسبه نمی شود.

* `PropertyListLen` طول لیست دارایی است. این اندازه مورد نیاز برای ذخیره ویژگی های ##NumProperties## است که به نوع داده ویژگی ها بستگی دارد.

* "NameLen" طول نام شیء، به کاراکتر است. به نظر می رسد تنها موردی که این عدد 0 است، لیست های سطح بالایی باشد.

* "Name" نام شیء است. پایان صفر وجود ندارد.

* `Property[n]` nامین ویژگی است. برای فرمت، ویژگی بخش Record Format را ببینید. ویژگی ها به صورت متوالی و بدون بالشتک نوشته می شوند.

* "NestedList" لیست تودرتو است که حضور آن با یک رکورد NULL در انتهای آن مشخص می شود.


وجود یک ورودی لیست تودرتو را می توان با بررسی اینکه آیا بایت باقی مانده است تا رسیدن به EndOffset تعیین می شود. اگر چنین است، رکورد شی بعدی باید مستقیماً بعد از آخرین ویژگی خوانده شود. سپس رکورد شیء به دنبال 13 بایت صفر است که سپس با EndOffset ترکیب می شود. هدف یا نیاز ورودی NULL مشخص نیست و ممکن است به برخی از ویژگی های قالب اشاره کند.

### فرمت ثبت اموال ###

یک Property Record حاوی جزئیاتی در مورد ویژگی هایی است که بخشی از Node هستند. یک رکورد دارای طرح حافظه زیر است:


|اندازه (بایت)|نوع داده|نام
--- | --- | ---
|1|char|TypeCode
|?|?|داده

TypeCode کدهای کاراکتری را نشان می دهد که در گروه هایی که نیاز به مدیریت مشابه دارند مرتب شده اند. TypeCode ها را می توان در انواع زیر دسته بندی کرد و TypeCode می تواند یکی از کدهای کاراکتر در بین این انواع باشد.

#### انواع اولیه ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

داده ها در رکورد نوع اسکالر اولیه دقیقاً نمایش باینری مقدار، به ترتیب بایت اندکی اند.

#### انواع آرایه ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

داده برای نوع آرایه پیچیده تر است و در ساختار زیر است.


|اندازه (بایت)|نوع داده|نام
--- | --- | ---
|4|Uint32|طول آرایه
|4|Uint32|رمزگذاری
|4|Uint32|طول فشرده
|?|?|مطالب

### انواع خاص ###

در زیر انواع خاص TypeCodes آمده است.

```
S: String
R: raw binary data
```

هر دوی این TypeCode ها به صورت زیر نمایش داده می شوند:


|اندازه (بایت)|نوع داده|نام
--- | --- | ---
|4|Uin32|طول
|طول| |

رشته با پایانه صفر نیست و ممکن است حاوی 0 کاراکتر باشد (این در واقع در برخی از ویژگی های FBX استفاده می شود).

## منابع ##

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [مشخصات فرمت فایل باینری FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)


