{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "файл usd", "формат файла usd", "формат файла", "файл", "расширение", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD — универсальный формат описания сцены",
  "description":"Узнайте о формате файла USD и API, которые могут открывать и создавать файлы USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## .USD вариант №

Файл с расширением .usd представляет собой формат универсального описания сцены, который кодирует данные для обмена данными и дополнения между приложениями для создания цифрового контента. Разработанный Pixar, [USD](https://openusd.org/release/intro.html) обеспечивает возможность обмена элементарными активами (например, моделями) или анимацией.

## Формат файла в долларах США

Файлы USD могут иметь двоичный формат (также известный как файлы Crate) или файлы с поддержкой ASCII. Оба эти формата файлов являются взаимозаменяемыми, где ссылки могут быть связаны с активами .usd без изменения источников. Формат файла USD состоит из набора библиотек C++ с привязками Python для сценариев. Он позволяет собирать и организовывать любое количество элементов 3D-сцены, таких как виртуальные наборы, сцены и кадры, для передачи их из приложения в приложение.

### Типы данных в долларах США

Основные типы данных, поддерживаемые форматом файла USD, перечислены в следующей таблице.

|Токен типа значения |Тип C++ |Описание|
---|---|---|
|логическое значение | логическое значение ||
|uchar|uint8_t|8-битное целое число без знака|
|int|int32_t|32-битное целое число со знаком|
|uint|uint32_t|32-битное целое число без знака|
|int64|int64_t|64-битное целое число со знаком|
|uint64|uint64_t|64-битное целое число без знака|
|half|GfHalf|16-битная плавающая точка|
|с плавающей точкой|с плавающей запятой|32-битная плавающая точка|
|двойной|двойной|64-битная с плавающей запятой|
|timecode|SdfTimeCode|double, представляющий разрешаемое время|
|строка|std::string|строка stl|
|token|TfToken|интернированная строка с быстрым сравнением и хешированием|
|asset|SdfAssetPath|представляет разрешимый путь к другому активу|
|matrix2d|GfMatrix2d|матрица двойников 2x2|
|matrix3d|GfMatrix3d|3x3 двойная матрица|
|matrix4d|GfMatrix4d|матрица двойников 4x4|
|quatd|GfQuatd|кватернион двойной точности|
|quatf|GfQuatf|кватернион одинарной точности|
|quath|GfQuath|кватернион половинной точности|
|double2|GfVec2d|вектор из 2 двойников|
|float2|GfVec2f|вектор из 2 поплавков|
|half2|GfVec2h|вектор из двух половинок|
|int2|GfVec2i|вектор из 2 целых чисел|
|double3|GfVec3d|вектор из 3 двойников|
|float3|GfVec3f|вектор из 3 поплавков|
|half3|GfVec3h|вектор из 3 половин|
|int3|GfVec3i|вектор из 3 целых чисел|
|double4|GfVec4d|вектор из 4 двойников|
|float4|GfVec4f|вектор из 4 поплавков|
|half4|GfVec4h|вектор из 4 половин|
|int4|GfVec4i|вектор из 4 целых чисел|

## Пример доллара США

Ниже приведен пример файла USD в формате простого файла ASCII.

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
## Использованная литература ##

* [Знакомство с долларом США](https://openusd.org/release/intro.html)
* [Справочник по API USD](https://openusd.org/release/apiDocs.html)

