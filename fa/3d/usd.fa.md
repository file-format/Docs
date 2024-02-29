{
  "date": "2021-02-01",
  "keywords": [
"دلار آمریکا",
"فایل usd",
"فرمت فایل usd",
"فرمت فایل",
"فایل",
"افزونه",
"3 بعدی"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD - فرمت توصیف صحنه جهانی",
  "description": "درباره فرمت فایل USD و APIهایی که می‌توانند فایل‌های USD را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-fad"
}
},
  "lastmod": "2021-02-01"
}

## فایل USD چیست؟

یک فایل با پسوند .usd یک فرمت فایل توصیف صحنه جهانی است که داده ها را به منظور تبادل و افزایش داده ها بین برنامه های کاربردی ایجاد محتوای دیجیتال رمزگذاری می کند. [USD](https://openusd.org/release/intro.html) که توسط Pixar توسعه داده شده است، توانایی مبادله دارایی های اصلی (مانند مدل ها) یا انیمیشن را فراهم می کند.

## فرمت فایل USD

فایل‌های USD می‌توانند فرمت باینری (همچنین به عنوان فایل‌های Crate نیز شناخته می‌شوند) یا فایل‌هایی با پشتیبانی ASCII داشته باشند. هر دوی این فرمت‌های فایل قابل تعویض هستند، جایی که می‌توان مراجع را بدون تغییر منابع به دارایی‌های USD. پیوند داد. فرمت فایل USD شامل مجموعه ای از کتابخانه های C++ با اتصالات پایتون برای اسکریپت است. این امکان مونتاژ و سازماندهی هر تعداد از عناصر صحنه سه بعدی مانند مجموعه های مجازی، صحنه ها و عکس ها را فراهم می کند تا آنها را از برنامه ای به برنامه دیگر منتقل کند.

### انواع داده USD

انواع داده های اساسی پشتیبانی شده توسط فرمت فایل USD در جدول زیر فهرست شده است.

|توکن نوع مقدار |نوع C++ |توضیحات|
---|---|---|
|بول|بول||
|uchar|uint8_t|عدد صحیح بدون علامت 8 بیتی|
|int|int32_t|عدد صحیح امضا شده 32 بیت|
|uint|uint32_t|عدد صحیح بدون علامت 32 بیتی|
|int64|int64_t|عدد صحیح امضا شده 64 بیت|
|uint64|uint64_t|عدد صحیح بدون علامت 64 بیتی|
|نیم|GfHalf|16 بیت ممیز شناور|
|شناور|شناور|میز شناور 32 بیتی|
|دوبل|دوبل|میز شناور 64 بیتی|
|timecode|SdfTimeCode|دوبار نشان دهنده زمان قابل حل|
|string|std::string|string stl|
|token|TfToken|رشته داخلی با مقایسه سریع و هش|
|asset|SdfAssetPath|مسیری قابل حل به دارایی دیگر را نشان می دهد|
|matrix2d|GfMatrix2d|ماتریس 2x2 دوتایی|
|matrix3d|GfMatrix3d|ماتریس 3x3 دوتایی|
|matrix4d|GfMatrix4d|4x4 ماتریس دوتایی|
|quatd|GfQuatd|کواترنیون با دقت دوگانه|
|quatf|GfQuatf|کواترنیون تک دقیق|
|quath|GfQuath|کواترنیون نیمه دقیق|
|double2|GfVec2d|بردار 2 دوبل|
|float2|GfVec2f|بردار 2 شناور|
|half2|GfVec2h|بردار 2 نیمه|
|int2|GfVec2i|بردار 2 اینچی|
|double3|GfVec3d|بردار 3 دوبل|
|float3|GfVec3f|بردار 3 شناور|
|half3|GfVec3h|بردار 3 نیمه|
|int3|GfVec3i|بردار 3 اینتی|
|double4|GfVec4d|بردار 4 دوبل|
|float4|GfVec4f|بردار 4 شناور|
|half4|GfVec4h|بردار 4 نیمه|
|int4|GfVec4i|وکتور 4 اینتی|

## مثال USD

نمونه ای از یک فایل USD در قالب فایل ASCII ساده به شرح زیر است.

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## منابع ##

* [معرفی USD](https://openusd.org/release/intro.html)

* [مرجع API USD](https://openusd.org/release/apiDocs.html)


