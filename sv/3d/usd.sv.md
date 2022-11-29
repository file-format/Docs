{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd-fil", "usd-filformat", "filformat", "fil", "tillägg", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Universal Scene Description Format",
  "description":"Läs mer om USD-filformat och API:er som kan öppna och skapa USD-filer.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Vad är en USD-fil?

En fil med filtillägget .usd är ett Universal Scene Description-filformat som kodar data i syfte att datautbyte och utöka mellan applikationer för digitalt innehåll. Utvecklat av Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) ger möjligheten att byta ut elementära tillgångar (som modeller) eller animationer.

## USD filformat

USD-filer kan ha binärt format (även känd som Crate-filer) eller ASCII-stödda filer. Båda dessa filformat är utbytbara där referenserna kan länkas till .usd-tillgångar utan att ändra källorna. USD-filformatet består av en uppsättning C++-bibliotek med Python-bindningar för skript. Det möjliggör montering och organisering av valfritt antal 3D-scenelement som virtuella uppsättningar, scener och bilder för att överföra dem från applikation till applikation.

### USD-datatyper

De grundläggande datatyperna som stöds av filformatet USD listas i följande tabell.

|Värdetypstoken |C++ typ |Beskrivning|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bitar osignerat heltal|
|int|int32_t|32-bitars signerat heltal|
|uint|uint32_t|32-bitars heltal utan tecken|
|int64|int64_t|64 bitars signerat heltal|
|uint64|uint64_t|64 bitar utan tecken heltal|
|halv|GfHalv|16 bitars flyttal|
|float|float|32 bitars flyttal|
|dubbel|dubbel|64 bitars flyttal|
|timecode|SdfTimeCode|dubbel som representerar en lösbar tid|
|string|std::string|stl-sträng|
|token|TfToken|internerad sträng med snabb jämförelse och hash|
|asset|SdfAssetPath|representerar en lösbar sökväg till en annan tillgång|
|matrix2d|GfMatrix2d|2x2 matris av dubblar|
|matrix3d|GfMatrix3d|3x3 matris av dubblar|
|matrix4d|GfMatrix4d|4x4 matris av dubblar|
|quatd|GfQuatd|dubbel precision quaternion|
|quatf|GfQuatf|single-precision quaternion|
|quath|GfQuath|halvprecision quaternion|
|double2|GfVec2d|vektor av 2 dubblar|
|float2|GfVec2f|vektor av 2 flottörer|
|half2|GfVec2h|vektor av 2 halvor|
|int2|GfVec2i|vektor med 2 ints|
|double3|GfVec3d|vektor med 3 dubblar|
|float3|GfVec3f|vektor av 3 flottörer|
|half3|GfVec3h|vektor av 3 halvor|
|int3|GfVec3i|vektor med 3 ints|
|double4|GfVec4d|vektor av 4 dubblar|
|float4|GfVec4f|vektor av 4 flottörer|
|half4|GfVec4h|vektor av 4 halvor|
|int4|GfVec4i|vektor med 4 ints|

## USD Exempel

Ett exempel på en USD-fil i vanligt ASCII-filformat är följande.

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
## Referenser ##

* [Introduktion till USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD API Reference](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

