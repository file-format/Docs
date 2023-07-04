{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd файл", "usd файл формат", "формат файлу", "файл", "розширення", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - універсальний формат опису сцени",
  "description":"Дізнайтеся про формат файлу USD і API, які можуть відкривати та створювати файли USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Що таке файл USD?

Файл із розширенням .usd — це формат файлу універсального опису сцени, який кодує дані з метою обміну даними та доповнення між програмами для створення цифрового вмісту. Розроблений Pixar, [USD](https://openusd.org/release/intro.html) надає можливість обмінюватися елементарними ресурсами (наприклад, моделями) або анімацією.

## Формат файлу USD

Файли USD можуть мати двійковий формат (також відомий як файли Crate) або файли з підтримкою ASCII. Обидва ці формати файлів є взаємозамінними, де посилання можуть бути пов’язані з активами .usd без зміни джерел. Формат файлу USD складається з набору бібліотек C++ із прив’язками Python для створення сценаріїв. Це дозволяє збирати та організовувати будь-яку кількість елементів 3D-сцени, таких як віртуальні набори, сцени та кадри, для передачі їх із програми в програму.

### Типи даних USD

Основні типи даних, які підтримує формат файлу USD, перераховані в наведеній нижче таблиці.

|Тип значення |Тип C++ |Опис|
---|---|---|
|буль|буль||
|uchar|uint8_t|8-розрядне ціле число без знака|
|int|int32_t|32-розрядне ціле число|
|uint|uint32_t|32-розрядне ціле число без знака|
|int64|int64_t|64-розрядне ціле число|
|uint64|uint64_t|64-розрядне ціле число без знака|
|half|GfHalf|16 біт з плаваючою точкою|
|float|float|32-бітове число з плаваючою комою|
|double|double|64 біт з плаваючою комою|
|timecode|SdfTimeCode|double представляє час, який можна розв’язати|
|рядок|std::рядок|рядок stl|
|токен|TfToken|вбудований рядок із швидким порівнянням і хешуванням|
|asset|SdfAssetPath|представляє розв’язаний шлях до іншого активу|
|matrix2d|GfMatrix2d|2x2 матриця подвійних|
|matrix3d|GfMatrix3d|матриця подвійних 3x3|
|matrix4d|GfMatrix4d|матриця подвійних 4x4|
|quatd|GfQuatd|кватерніон подвійної точності|
|quatf|GfQuatf|кватерніон одинарної точності|
|quath|GfQuath|кватерніон половинної точності|
|double2|GfVec2d|вектор із 2 подвійних|
|float2|GfVec2f|вектор із 2-х плаваючих елементів|
|half2|GfVec2h|вектор 2 половинок|
|int2|GfVec2i|вектор з 2 ints|
|double3|GfVec3d|вектор з 3 подвійних|
|float3|GfVec3f|вектор із 3 поплавками|
|half3|GfVec3h|вектор із 3 половинок|
|int3|GfVec3i|вектор з 3 ints|
|double4|GfVec4d|вектор із 4 подвійних|
|float4|GfVec4f|вектор із 4-х плаваючих елементів|
|half4|GfVec4h|вектор із 4 половинок|
|int4|GfVec4i|вектор із 4 ints|

## USD Приклад

Нижче наведено приклад файлу USD у простому форматі ASCII.

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
## Посилання ##

* [Знайомство з доларами США](https://openusd.org/release/intro.html)
* [Довідка щодо API USD](https://openusd.org/release/apiDocs.html)

