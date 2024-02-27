{
  "date": "2021-02-01",
  "keywords": [
"usd",
"usd fil",
"usd filformat",
"filformat",
"fil",
"udvidelse",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD - Universal Scene Description Format",
  "description": "Lær om USD-filformat og API'er, der kan åbne og oprette USD-filer.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-dad"
}
},
  "lastmod": "2021-02-01"
}

## Hvad er en USD fil?

En fil med filtypenavnet .usd er et Universal Scene Description-filformat, der koder data med det formål at udveksle og udvide data mellem applikationer til oprettelse af digitalt indhold. Udviklet af Pixar, [USD](https://openusd.org/release/intro.html) giver mulighed for at udveksle elementære aktiver (såsom modeller) eller animation.

## USD filformat

USD-filer kan have binært format (også kendt som Crate-filer) eller ASCII-støttede filer. Begge disse filformater er udskiftelige, hvor referencerne kan linkes til .usd-aktiver uden at ændre kilderne. USD-filformatet består af et sæt C++-biblioteker med Python-bindinger til scripting. Det gør det muligt at samle og organisere et vilkårligt antal 3D-sceneelementer såsom virtuelle sæt, scener og billeder for at overføre dem fra applikation til applikation.

### USD-datatyper

De grundlæggende datatyper, der understøttes af filformatet USD, er angivet i følgende tabel.

|Værditypetoken |C++ type |Beskrivelse|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit usigneret heltal|
|int|int32_t|32 bit fortegnet heltal|
|uint|uint32_t|32 bit usigneret heltal|
|int64|int64_t|64 bit fortegnet heltal|
|uint64|uint64_t|64 bit usigneret heltal|
|halv|GfHalv|16 bit flydende komma|
|float|float|32 bit flydende komma|
|dobbelt|dobbelt|64 bit flydende komma|
|timecode|SdfTimeCode|dobbelt repræsenterer en opløselig tid|
|streng|std::streng|stl streng|
|token|TfToken|internet streng med hurtig sammenligning og hashing|
|asset|SdfAssetPath|repræsenterer en sti, der kan løses til et andet aktiv|
|matrix2d|GfMatrix2d|2x2 matrix af doubler|
|matrix3d|GfMatrix3d|3x3 matrix af doubler|
|matrix4d|GfMatrix4d|4x4 matrix af doubler|
|quatd|GfQuatd|dobbelt-præcision quaternion|
|quatf|GfQuatf|single-precision quaternion|
|quath|GfQuath|halvpræcision quaternion|
|double2|GfVec2d|vektor af 2 doubler|
|float2|GfVec2f|vektor af 2 flydere|
|half2|GfVec2h|vektor af 2 halvdele|
|int2|GfVec2i|vektor af 2 ints|
|double3|GfVec3d|vektor af 3 doubler|
|float3|GfVec3f|vektor af 3 flydere|
|half3|GfVec3h|vektor af 3 halvdele|
|int3|GfVec3i|vektor af 3 ints|
|double4|GfVec4d|vektor af 4 doubler|
|float4|GfVec4f|vektor af 4 flydere|
|half4|GfVec4h|vektor af 4 halvdele|
|int4|GfVec4i|vektor på 4 ints|

## USD eksempel

Et eksempel på en USD-fil i almindeligt ASCII-filformat er som følger.

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
## Referencer ##

* [Introduktion til USD](https://openusd.org/release/intro.html)

* [USD API-reference](https://openusd.org/release/apiDocs.html)


