{
  "date" : "2021-02-01",
  "keywords" :["usd", "usd file", "usd file format", "file format", "file", "extension", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"USD - تنسيق وصف المشهد العالمي" ,
  "description":"تعرف على تنسيق ملف USD وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات USD." ,
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2021-02-01"
}

## ما هو ملف USD؟

الملف ذو الامتداد .usd هو تنسيق ملف Universal Scene Description الذي يقوم بترميز البيانات بغرض تبادل البيانات والزيادة بين تطبيقات إنشاء المحتوى الرقمي. تم تطويره بواسطة Pixar ، [USD](https://openusd.org/release/intro.html) يوفر القدرة على تبادل الأصول الأولية (مثل النماذج) أو الرسوم المتحركة.

## تنسيق ملف USD

يمكن أن تحتوي ملفات USD على تنسيق ثنائي (يُعرف أيضًا باسم ملفات Crate) أو ملفات مدعومة من ASCII. كلا تنسيقي الملفات هذين قابلين للتبديل حيث يمكن ربط المراجع بأصول .usd بدون تغيير المصادر. يتكون تنسيق ملف USD من مجموعة من مكتبات C ++ مع روابط Python للبرمجة النصية. إنه يتيح تجميع وتنظيم أي عدد من عناصر المشهد ثلاثي الأبعاد مثل المجموعات الافتراضية والمشاهد واللقطات لنقلها من تطبيق إلى آخر.

### أنواع البيانات بالدولار الأمريكي

يتم سرد أنواع البيانات الأساسية التي يدعمها تنسيق ملف USD في الجدول التالي.

| رمز نوع القيمة | نوع C ++ | الوصف |
---|---|---|
| منطقي | منطقي ||
| uchar | uint8_t | 8 بت عدد صحيح بدون إشارة |
| int | int32_t | عدد صحيح موقعة 32 بت |
| uint | uint32_t | عدد صحيح بدون إشارة 32 بت |
| int64 | int64_t | عدد صحيح موقع 64 بت |
| uint64 | uint64_t | 64 بت عدد صحيح بدون إشارة |
| نصف | GfHalf | نقطة عائمة 16 بت |
| تعويم | عائم | نقطة عائمة 32 بت |
| مزدوج | مزدوج | نقطة عائمة 64 بت |
| timecode | SdfTimeCode | مزدوج يمثل وقتًا قابلاً للحل |
| سلسلة | الأمراض المنقولة جنسياً :: سلسلة | سلسلة stl |
| token | TfToken | سلسلة داخلية مع مقارنة وتجزئة سريعة |
يمثل | الأصول | SdfAssetPath | مسارًا قابلًا للحل إلى أصل | آخر
| matrix2d | GfMatrix2d | مصفوفة مزدوجة 2x2 |
| matrix3d | GfMatrix3d | 3x3 مصفوفة مزدوجة |
| matrix4d | GfMatrix4d | مصفوفة زوجي 4x4 |
| رباعي | GfQuatd | رباعية الدقة |
| quatf | GfQuatf | رباعية أحادية الدقة |
| quath | GfQuath | رباعي نصف الدقة |
| double2 | GfVec2d | متجه لـ 2 زوجي |
| float2 | GfVec2f | متجه من 2 عوامات |
| half2 | GfVec2h | متجه من نصفين |
| int2 | GfVec2i | متجه لـ 2 ints |
| double3 | GfVec3d | متجه لـ 3 أزواج |
| float3 | GfVec3f | متجه لـ 3 عوامات |
| half3 | GfVec3h | متجه لـ 3 أنصاف |
| int3 | GfVec3i | متجه لـ 3 ints |
| double4 | GfVec4d | متجه لـ 4 أزواج |
| float4 | GfVec4f | متجه لـ 4 عوامات |
| half4 | GfVec4h | متجه لـ 4 أنصاف |
| int4 | GfVec4i | متجه لـ 4 ints |

## مثال بالدولار الأمريكي

فيما يلي مثال على ملف USD بتنسيق ملف ASCII عادي.

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
## مراجع ##

* [مقدمة إلى الدولار الأمريكي](https://openusd.org/release/intro.html)
* [مرجع USD API](https://openusd.org/release/apiDocs.html)

