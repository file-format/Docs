{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd файл", "usd файлов формат", "файлов формат", "файл", "разширение", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD – универсален формат за описание на сцена",
  "description":"Научете за файловия формат USD и API, които могат да отварят и създават USD файлове.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Какво е USD файл?

Файлът с разширение .usd е файлов формат за универсално описание на сцена, който кодира данни с цел обмен на данни и разширяване между приложенията за създаване на цифрово съдържание. Разработено от Pixar, [USD](https://openusd.org/release/intro.html) предоставя възможност за обмен на елементарни активи (като модели) или анимация.

## USD файлов формат

USD файловете могат да имат двоичен формат (известен също като Crate файлове) или ASCII-поддържани файлове. И двата файлови формата са взаимозаменяеми, където препратките могат да бъдат свързани с .usd активи, без да се променят източниците. USD файловият формат се състои от набор от C++ библиотеки с обвързвания на Python за скриптове. Той позволява сглобяване и организиране на произволен брой 3D сценични елементи като виртуални комплекти, сцени и кадри, за да ги предава от приложение на приложение.

### Типове данни в USD

Основните типове данни, поддържани от файловия формат USD, са изброени в следващата таблица.

|Тип стойност |Тип C++ |Описание|
---|---|---|
|bool|bool||
|uchar|uint8_t|8-битово цяло число без знак|
|int|int32_t|32-битово цяло число със знак|
|uint|uint32_t|32-битово цяло число без знак|
|int64|int64_t|64-битово цяло число със знак|
|uint64|uint64_t|64-битово цяло число без знак|
|half|GfHalf|16 бита с плаваща запетая|
|float|float|32 бита с плаваща запетая|
|double|double|64 бита с плаваща запетая|
|времеви код|SdfTimeCode|двойно представяне на разрешимо време|
|низ|std::низ|stl низ|
|token|TfToken|вграден низ с бързо сравнение и хеширане|
|asset|SdfAssetPath|представлява разрешим път към друг актив|
|matrix2d|GfMatrix2d|2x2 матрица от удвоени|
|matrix3d|GfMatrix3d|3x3 матрица от удвоени|
|matrix4d|GfMatrix4d|4x4 матрица от двойни|
|quatd|GfQuatd|кватернион с двойна точност|
|quatf|GfQuatf|кватернион с единична точност|
|quath|GfQuath|кватернион с половин точност|
|double2|GfVec2d|вектор от 2 двойни|
|float2|GfVec2f|вектор от 2 float|
|half2|GfVec2h|вектор от 2 половини|
|int2|GfVec2i|вектор от 2 ints|
|double3|GfVec3d|вектор от 3 двойни|
|float3|GfVec3f|вектор от 3 float|
|half3|GfVec3h|вектор от 3 половини|
|int3|GfVec3i|вектор от 3 ints|
|double4|GfVec4d|вектор от 4 двойни|
|float4|GfVec4f|вектор от 4 float|
|half4|GfVec4h|вектор от 4 половини|
|int4|GfVec4i|вектор от 4 ints|

## USD Пример

Пример за USD файл в обикновен ASCII файлов формат е както следва.

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
## Препратки ##

* [Въведение в USD](https://openusd.org/release/intro.html)
* [Справка за API за USD](https://openusd.org/release/apiDocs.html)

