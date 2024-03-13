{
  "date": "2021-02-01",
  "keywords": [
"ABŞ dolları",
"usd faylı",
"usd fayl formatı",
"fayl formatı",
"fayl",
"uzadılması",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD - Universal Səhnə Təsviri Format",
  "description": "USD fayl formatı və USD fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-azd"
}
},
  "lastmod": "2021-02-01"
}

## USD faylı nədir?

.usd uzantılı fayl rəqəmsal məzmun yaratma proqramları arasında məlumat mübadiləsi və genişləndirilməsi məqsədilə məlumatları kodlayan Universal Səhnə Təsviri fayl formatıdır. Pixar tərəfindən hazırlanmış [USD](https://openusd.org/release/intro.html) elementar aktivləri (modellər kimi) və ya animasiyanı dəyişdirmək imkanı verir.

## USD fayl formatı

USD faylları ikili formata (həmçinin Crate faylları kimi tanınır) və ya ASCII dəstəkli fayllara malik ola bilər. Bu fayl formatlarının hər ikisi bir-birini əvəz edə bilər, burada istinadlar mənbələri dəyişdirmədən .usd aktivləri ilə əlaqələndirilə bilər. USD fayl formatı skript üçün Python bağlamaları olan bir sıra C++ kitabxanalarından ibarətdir. O, tətbiqdən tətbiqə ötürmək üçün virtual dəstlər, səhnələr və kadrlar kimi istənilən sayda 3D səhnə elementlərinin yığılmasına və təşkilinə imkan verir.

### USD Məlumat Növləri

USD fayl formatı tərəfindən dəstəklənən əsas məlumat növləri aşağıdakı cədvəldə verilmişdir.

|Dəyər tipi işarəsi |C++ növü |Təsvir|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit işarəsiz tam|
|int|int32_t|32 bit işarəli tam ədəd|
|uint|uint32_t|32 bit işarəsiz tam|
|int64|int64_t|64 bit işarəli tam ədəd|
|uint64|uint64_t|64 bit işarəsiz tam|
|yarım|GfHalf|16 bitlik üzən nöqtə|
|float|float|32 bit üzən nöqtə|
|double|double|64 bit floating point|
|timecode|SdfTimeCode|həll edilə bilən vaxtı təmsil edən ikiqat|
|string|std::string|stl string|
|token|TfToken|sürətli müqayisə və hashing ilə interned sətir|
|asset|SdfAssetPath|başqa aktivə həll edilə bilən yolu təmsil edir|
|matrix2d|GfMatrix2d|2x2 cütlərin matrisi|
|matrix3d|GfMatrix3d|3x3 cütlərin matrisi|
|matrix4d|GfMatrix4d|4x4 cütlərin matrisi|
|quatd|GfQuatd|ikiqat dəqiqlikli quaternion|
|quatf|GfQuatf|tək dəqiqlikli quaternion|
|quath|GfQuath|yarı dəqiqlikli quaternion|
|double2|GfVec2d|2 cütün vektoru|
|float2|GfVec2f|2 float vektoru|
|yarım2|GfVec2h|2 yarımın vektoru|
|int2|GfVec2i|2 ints vektoru|
|double3|GfVec3d|3 cütün vektoru|
|float3|GfVec3f|3 üzmə vektoru|
|yarım3|GfVec3h|3 yarımın vektoru|
|int3|GfVec3i|3 ints vektoru|
|double4|GfVec4d|4 cütün vektoru|
|float4|GfVec4f|4 üzən vektor|
|yarım4|GfVec4h|4 yarımın vektoru|
|int4|GfVec4i|4 ints vektoru|

## ABŞ dolları nümunəsi

Düz ASCII fayl formatında USD faylının nümunəsi aşağıdakı kimidir.

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
## İstinadlar ##

* [USD-yə giriş](https://openusd.org/release/intro.html)

* [USD API Referansı](https://openusd.org/release/apiDocs.html)


