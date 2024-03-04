{
  "date": "2021-02-01",
  "keywords": [
"USD",
"usd failą",
"usd failo formatas",
"Dokumento formatas",
"failą",
"pratęsimas",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD – universalus scenos aprašymo formatas",
  "description": "Sužinokite apie USD failo formatą ir API, kurios gali atidaryti ir kurti USD failus.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-ltd"
}
},
  "lastmod": "2021-02-01"
}

## Kas yra USD failas?

Failas su plėtiniu .usd yra universalaus scenos aprašo failo formatas, koduojantis duomenis, kad būtų galima keistis duomenimis ir papildyti skaitmeninio turinio kūrimo programas. Pixar sukurta [USD](https://openusd.org/release/intro.html) suteikia galimybę keistis elementariais ištekliais (pvz., modeliais) arba animacija.

## USD failo formatas

USD failai gali būti dvejetainio formato (taip pat žinomi kaip Crate failai) arba ASCII failai. Abu šie failų formatai yra keičiami, kai nuorodos gali būti susietos su .usd ištekliais nekeičiant šaltinių. USD failo formatą sudaro C++ bibliotekų rinkinys su Python įrišimais scenarijui kurti. Tai leidžia surinkti ir organizuoti bet kokį 3D scenos elementų skaičių, pavyzdžiui, virtualius rinkinius, scenas ir kadrus, kad būtų galima perduoti juos iš vienos programos į kitą.

### USD duomenų tipai

Pagrindiniai duomenų tipai, kuriuos palaiko USD failo formatas, yra išvardyti šioje lentelėje.

|Vertės tipo raktas |C++ tipas |Aprašymas|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bitų beženklis sveikasis skaičius|
|int|int32_t|32 bitais pasirašytas sveikasis skaičius|
|uint|uint32_t|32 bitų beženklis sveikasis skaičius|
|int64|int64_t|64 bitais pasirašytas sveikasis skaičius|
|uint64|uint64_t|64 bitų beženklis sveikasis skaičius|
|pusė|GfHalf|16 bitų slankusis kablelis|
|plūduriuoti|plaukioti|32 bitų slankiojo kablelio|
|dvigubas|dvigubas|64 bitų slankusis kablelis|
|timecode|SdfTimeCode|dvigubas, reiškiantis išsprendžiamą laiką|
|string|std::string|stl string|
|token|TfToken|internuota eilutė su greitu palyginimu ir maiša|
|turtas|SdfAssetPath|reiškia išsprendžiamą kelią iki kito turto|
|matrica2d|GfMatrix2d|2x2 dvigubų matrica|
|matrica3d|GfMatrix3d|3x3 dvigubų matrica|
|matrica4d|GfMatrix4d|4x4 dvigubų matrica|
|quatd|GfQuatd|dvigubo tikslumo kvaternionas|
|quatf|GfQuatf|vieno tikslumo kvaternionas|
|quath|GfQuath|pusės tikslumo kvaternionas|
|double2|GfVec2d|vektorius iš 2 dublių|
|float2|GfVec2f|vektorius iš 2 plūdurių|
|pusė2|GfVec2h|vektorius iš 2 puselių|
|int2|GfVec2i|vektorius iš 2 int|
|double3|GfVec3d|vektorius iš 3 dublių|
|float3|GfVec3f|vektorius iš 3 plūdurių|
|pusė3|GfVec3h|vektorius iš 3 puselių|
|int3|GfVec3i|vektorius iš 3 int|
|double4|GfVec4d|vektorius iš 4 dublių|
|float4|GfVec4f|vektorius iš 4 plūdurių|
|pusė4|GfVec4h|vektorius iš 4 puselių|
|int4|GfVec4i|vektorius iš 4 int|

## USD pavyzdys

USD failo paprasto ASCII formato pavyzdys yra toks.

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
## Nuorodos Nr.

* [Įvadas į USD](https://openusd.org/release/intro.html)

* [USD API nuoroda](https://openusd.org/release/apiDocs.html)


