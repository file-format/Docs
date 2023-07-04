{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd file", "usd file format", "file format", "file", "extension", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD – univerzális jelenetleíró formátum",
  "description":"További információ az USD fájlformátumról és az API-król, amelyek USD-fájlokat nyithatnak meg és hozhatnak létre.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Mi az az USD fájl?

Az .usd kiterjesztésű fájl egy univerzális jelenetleíró fájlformátum, amely adatokat kódol a digitális tartalomkészítő alkalmazások közötti adatcsere és -kiegészítés céljából. A Pixar által kifejlesztett [USD](https://openusd.org/release/intro.html) lehetőséget biztosít elemi eszközök (például modellek) vagy animációk cseréjére.

## USD fájlformátum

Az USD-fájlok bináris formátumúak (más néven Crate-fájlok) vagy ASCII-alapú fájlok lehetnek. Mindkét fájlformátum felcserélhető, ahol a hivatkozások .usd eszközökhöz kapcsolhatók a forrás megváltoztatása nélkül. Az USD fájlformátum C++-könyvtárakból áll, amelyek Python-kötésekkel rendelkeznek a szkriptek írásához. Lehetővé teszi tetszőleges számú 3D-s jelenetelem összeállítását és rendszerezését, például virtuális szetteket, jeleneteket és felvételeket, hogy alkalmazásról alkalmazásra továbbítsa őket.

### USD adattípusok

Az USD fájlformátum által támogatott alapvető adattípusokat a következő táblázat sorolja fel.

|Értéktípus token |C++ típusú |Leírás|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bites előjel nélküli egész szám|
|int|int32_t|32 bites előjelű egész szám|
|uint|uint32_t|32 bites előjel nélküli egész szám|
|int64|int64_t|64 bites előjelű egész szám|
|uint64|uint64_t|64 bites előjel nélküli egész szám|
|fél|GfHalf|16 bites lebegőpontos|
|float|float|32 bites lebegőpontos|
|dupla|dupla|64 bites lebegőpontos|
|timecode|SdfTimeCode|feloldható időt képviselő kettős|
|string|std::string|stl string|
|token|TfToken|internált karakterlánc gyors összehasonlítással és hash-el|
|asset|SdfAssetPath|egy másik eszköz feloldható elérési útja|
|mátrix2d|GfMatrix2d|2x2 kettős mátrix|
|mátrix3d|GfMatrix3d|3x3-as kettős mátrix|
|mátrix4d|GfMatrix4d|4x4-es kettősmátrix|
|quatd|GfQuatd|kettős pontosságú kvaternió|
|quatf|GfQuatf|egy pontosságú kvaternió|
|quath|GfQuath|félpontos kvaternió|
|double2|GfVec2d|2 kettős vektora|
|float2|GfVec2f|2 float vektora|
|fél2|GfVec2h|2 felének vektora|
|int2|GfVec2i|2 int vektora|
|double3|GfVec3d|3 kettős vektora|
|float3|GfVec3f|3 lebegésből álló vektor|
|fél3|GfVec3h|3 felének vektora|
|int3|GfVec3i|3 int vektora|
|double4|GfVec4d|4 kettős vektora|
|float4|GfVec4f|4 úszóból álló vektor|
|fél4|GfVec4h|4 felének vektora|
|int4|GfVec4i|4 int vektora|

## USD példa

A következő példa egy egyszerű ASCII fájlformátumú USD-fájlra.

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
## Hivatkozások ##

* [Bevezetés az USD-be](https://openusd.org/release/intro.html)
* [USD API-referencia](https://openusd.org/release/apiDocs.html)

