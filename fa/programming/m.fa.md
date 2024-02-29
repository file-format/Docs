{
  "date": "2019-10-11",
  "keywords": [
"فایل M",
"م",
"افزونه",
"قالب",
"فرمت فایل M"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M - فایل کد منبع متلب",
  "description": "درباره فایل کد منبع Matlab .m و APIهایی که می‌توانند فایل‌های MF را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fam"
}
},
  "lastmod": "2020-09-10"
}

# M - فایل های کد منبع Matlab

## فایل M (Matlab) چیست؟

یک فایل با پسوند .m یک فایل کد منبع است که توسط Matlab استفاده می شود، یک پلت فرم برنامه نویسی و محاسبات عددی که برای تجزیه و تحلیل، توسعه الگوریتم ها و مدل سازی شبیه سازی استفاده می شود. مانند سایر فرمت‌های فایل برنامه‌نویسی، یک فایل M حاوی کد منبع است که دستورات Matlab را برای ترسیم نمودارها، اجرای شبیه‌سازی‌ها و سایر عملیات‌های ریاضی اجرا می‌کند. یک شبیه‌سازی متلب می‌تواند روی چندین فایل .m باشد که می‌تواند برنامه را در اسکریپت‌ها، کلاس‌ها، توابع یا اعلان‌ها طبقه‌بندی کند. فایل های Matlab M را می توان با هر ویرایشگر متنی باز کرد.

## فرمت فایل Matlab M - اطلاعات بیشتر

فایل های Matlab .m فایل های متنی هستند که حاوی کدهای برنامه نویسی در زبان برنامه نویسی Matlab هستند. اینها را می توان در هر ویرایشگر متنی باز و ویرایش کرد و دوباره ذخیره کرد تا در نرم افزار Matlab اجرا شود. Matlab خود حاوی یک ویرایشگر زنده است که برای ایجاد اسکریپت هایی استفاده می شود که ترکیبی از کد، خروجی و متن فرمت شده است.

### فایل های تابع Matlab

مانند سایر زبان های برنامه نویسی، می توانید یک فایل .m ایجاد کنید که فقط شامل تعریف تابعی است که فقط یک کار خاص را انجام می دهد. چنین فایل هایی با پسوند .m نیز ذخیره می شوند و فقط عملکرد مربوط به آن تابع را پیاده سازی می کنند.

### .M فایل مثال

در زیر یک مثال فایل تابع Matlab است که زمان صرف شده برای یک شی که از ارتفاع h رها شده است را محاسبه می کند.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

برای فراخوانی این تابع از ویرایشگر Matlab یا از یک فایل .m دیگر می توان از کد زیر استفاده کرد.
```C++
TimeToGround(100)
```

## منابع

 * [Matlab - فرمت‌های فایل پشتیبانی شده](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [با استفاده از Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - فایل پیاده سازی Objective-C

## فایل M (Objective-C) چیست؟

یک فایل M همچنین به عنوان فایل پیاده سازی نامیده می شود که حاوی کد منبع یک کلاس است که به زبان Objective-C نوشته شده است، یک زبان برنامه نویسی که برای نوشتن برنامه های نرم افزاری برای OS X و iOS استفاده می شود. Objective-C زبان برنامه نویسی اصلی است که توسط API های اصلی اپل یعنی Cocoa و Cocoa Touch برای این پلتفرم ها استفاده می شود. یک برنامه نرم افزاری توسعه یافته به این زبان ممکن است حاوی چندین فایل .m باشد که شامل اجرای کلاس های برنامه است. اینها را می توان با استفاده از Apple XCode، jEdit و سایر ویرایشگرهای متن رایج باز کرد.

## فرمت فایل Objective-C M - اطلاعات بیشتر

فایل های M در قالب متن ساده با استفاده از دستور برنامه نویسی Objective-C نوشته می شوند. هر متد یک کلاس باید با تمام کدهای لازم در این فایل های پیاده سازی تعریف شود. این فایل‌های پیاده‌سازی M می‌توانند یک یا چند فایل هدر h را مطابق با نیاز وارد کنند. دستور import به کامپایلر می‌گوید که کجا فایل هدر متعلق به این فایل پیاده‌سازی را پیدا کند. بیانیه واردات به صورت زیر نوشته شده است.

```C++
#import "network.h"
```

سپس هر پیاده سازی فایل M با دستورالعمل «@implementation» و به دنبال آن نام فایل کلاس پیاده سازی شروع می شود. سپس تمام روش‌هایی که در فایل هدر تعریف شده‌اند، اجرا می‌شوند.

### نمونه فرمت فایل M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## منابع
 * [درباره هدف C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [راهنمای Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

