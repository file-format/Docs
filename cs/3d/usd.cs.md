{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd soubor", "formát souboru usd", "formát souboru", "soubor", "přípona", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Univerzální formát popisu scény",
  "description":"Další informace o formátu souboru USD a rozhraních API, která mohou otevírat a vytvářet soubory USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Co je soubor USD?

Soubor s příponou .usd je formát souboru Universal Scene Description, který kóduje data za účelem výměny a rozšiřování dat mezi aplikacemi pro vytváření digitálního obsahu. [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html), vyvinutý společností Pixar, poskytuje možnost vyměňovat si základní prvky (jako jsou modely) nebo animace.

## Formát souboru USD

Soubory USD mohou mít binární formát (také známý jako soubory Crate) nebo soubory zálohované ASCII. Oba tyto formáty souborů jsou zaměnitelné, kde lze odkazy propojit s aktivy .usd bez změny zdrojů. Formát souboru USD se skládá ze sady knihoven C++ s vazbami Python pro skriptování. Umožňuje sestavení a organizaci libovolného počtu prvků 3D scény, jako jsou virtuální sady, scény a záběry, za účelem jejich přenosu z aplikace do aplikace.

### Typy dat USD

Základní datové typy podporované formátem souboru USD jsou uvedeny v následující tabulce.

|Token typu hodnoty |Typ C++ |Popis|
---|---|---|
|bool|bool||
|uchar|uint8_t|8bitové celé číslo bez znaménka|
|int|int32_t|32bitové celé číslo se znaménkem|
|uint|uint32_t|32bitové celé číslo bez znaménka|
|int64|int64_t|64bitové celé číslo se znaménkem|
|uint64|uint64_t|64bitové celé číslo bez znaménka|
|polovina|GfHalf|16 bitů s plovoucí desetinnou čárkou|
|float|float|32bitová plovoucí desetinná čárka|
|double|double|64 bit s plovoucí desetinnou čárkou|
|timecode|SdfTimeCode|dvojitý představující rozlišitelný čas|
|string|std::string|stl řetězec|
|token|TfToken|internovaný řetězec s rychlým porovnáním a hashováním|
|asset|SdfAssetPath|představuje řešitelnou cestu k jinému aktivu|
|matrix2d|GfMatrix2d|2x2 matice dvojic|
|matrix3d|GfMatrix3d|3x3 matice dvojic|
|matice4d|GfMatrix4d|matice 4x4 dvojic|
|quatd|GfQuatd|čtveřice s dvojitou přesností|
|quatf|GfQuatf|čtveřice s jednoduchou přesností|
|quath|GfQuath|čtveřice s poloviční přesností|
|double2|GfVec2d|vektor 2 dvojic|
|float2|GfVec2f|vektor 2 plováků|
|polovina2|GfVec2h|vektor 2 polovičních|
|int2|GfVec2i|vektor 2 ints|
|double3|GfVec3d|vektor 3 dvojic|
|float3|GfVec3f|vektor 3 plováků|
|polovina3|GfVec3h|vektor 3 polovičních|
|int3|GfVec3i|vektor 3 ints|
|double4|GfVec4d|vektor 4 dvojic|
|float4|GfVec4f|vektor 4 plováků|
|polovina4|GfVec4h|vektor 4 polovičních|
|int4|GfVec4i|vektor 4 ints|

## Příklad USD

Příklad souboru USD v prostém formátu souboru ASCII je následující.

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
## Reference ##

* [Úvod do USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Reference USD API](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

