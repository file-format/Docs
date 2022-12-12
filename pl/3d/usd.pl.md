{
  "date" : "2021-02-01",
  "keywords" :["usd", "plik usd", "format pliku usd", "format pliku", "plik","rozszerzenie", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - uniwersalny format opisu sceny",
  "description":"Dowiedz się o formacie pliku USD i interfejsach API, które mogą otwierać i tworzyć pliki USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Czym jest plik USD?

Plik z rozszerzeniem .usd to format pliku Universal Scene Description, który koduje dane w celu wymiany i rozszerzania danych między aplikacjami do tworzenia treści cyfrowych. Opracowana przez firmę Pixar usługa [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) umożliwia wymianę podstawowych zasobów (takich jak modele) lub animacji.

## Format pliku USD

Pliki USD mogą mieć format binarny (znany również jako pliki Crate) lub pliki z obsługą ASCII. Oba te formaty plików są wymienne, a odniesienia można łączyć z zasobami .usd bez zmiany źródeł. Format pliku USD składa się z zestawu bibliotek C++ z powiązaniami Pythona do skryptowania. Umożliwia składanie i porządkowanie dowolnej liczby elementów sceny 3D, takich jak wirtualne plany zdjęciowe, sceny i ujęcia w celu przesyłania ich z aplikacji do aplikacji.

### Typy danych USD

Podstawowe typy danych obsługiwane przez format pliku USD są wymienione w poniższej tabeli.

|Token typu wartości |Typ C++ |Opis|
---|---|---|
|bool|bool||
|uchar|uint8_t|8-bitowa liczba całkowita bez znaku|
|int|int32_t|32-bitowa liczba całkowita ze znakiem|
|uint|uint32_t|32-bitowa liczba całkowita bez znaku|
|int64|int64_t|64-bitowa liczba całkowita ze znakiem|
|uint64|uint64_t|64-bitowa liczba całkowita bez znaku|
|half|GfHalf|16 bitów zmiennoprzecinkowych|
|float|float|32 bity zmiennoprzecinkowe|
|podwójne|podwójne|64 bity zmiennoprzecinkowe|
|timecode|SdfTimeCode|podwójna reprezentacja czasu, który można rozwiązać|
|string|std::string|stl string|
|token|TfToken|ciąg znaków internowany z szybkim porównaniem i haszowaniem|
|zasób|SdfAssetPath|reprezentuje możliwą do rozwiązania ścieżkę do innego zasobu|
|macierz2d|GfMatrix2d|macierz podwójnych 2x2|
|matrix3d|GfMatrix3d|macierz podwójnych 3x3|
|macierz4d|GfMatrix4d|macierz podwójnych 4x4|
|quatd|GfQuatd|kwaternion podwójnej precyzji|
|quatf|GfQuatf|kwaternion pojedynczej precyzji|
|quath|GfQuath|kwaternion o połowie precyzji|
|podwójne2|GfVec2d|wektor 2 podwójnych|
|float2|GfVec2f|wektor 2 pływaków|
|half2|GfVec2h|wektor 2 połówek|
|int2|GfVec2i|wektor 2 int|
|podwójne3|GfVec3d|wektor 3 podwójnych|
|float3|GfVec3f|wektor 3 pływaków|
|half3|GfVec3h|wektor 3 połówek|
|int3|GfVec3i|wektor 3 int|
|podwójne4|GfVec4d|wektor 4 podwójnych|
|float4|GfVec4f|wektor 4 pływaków|
|half4|GfVec4h|wektor 4 połówek|
|int4|GfVec4i|wektor 4 int|

## Przykład USD

Przykład pliku USD w zwykłym formacie pliku ASCII jest następujący.

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
## Bibliografia ##

* [Wprowadzenie do USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Odniesienie do API USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

