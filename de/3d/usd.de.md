{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd-Datei", "usd-Dateiformat", "Dateiformat", "Datei", "Erweiterung", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Universelles Szenenbeschreibungsformat",
  "description":"Erfahren Sie mehr über das USD-Dateiformat und APIs, die USD-Dateien öffnen und erstellen können.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Was ist eine USD-Datei?

Eine Datei mit der Erweiterung .usd ist ein Universal Scene Description-Dateiformat, das Daten zum Zwecke des Datenaustauschs und der Erweiterung zwischen Anwendungen zur Erstellung digitaler Inhalte codiert. [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) wurde von Pixar entwickelt und bietet die Möglichkeit, elementare Assets (z. B. Modelle) oder Animationen auszutauschen.

## USD-Dateiformat

USD-Dateien können im Binärformat (auch als Crate-Dateien bezeichnet) oder ASCII-gestützte Dateien vorliegen. Diese beiden Dateiformate sind austauschbar, wobei die Referenzen mit .usd-Assets verknüpft werden können, ohne die Quellen zu ändern. Das USD-Dateiformat besteht aus einer Reihe von C++-Bibliotheken mit Python-Bindungen für die Skripterstellung. Es ermöglicht die Zusammenstellung und Organisation einer beliebigen Anzahl von 3D-Szenenelementen wie virtuellen Sets, Szenen und Aufnahmen, um sie von Anwendung zu Anwendung zu übertragen.

### USD-Datentypen

Die vom USD-Dateiformat unterstützten grundlegenden Datentypen sind in der folgenden Tabelle aufgeführt.

|Werttyp-Token |C++-Typ |Beschreibung|
---|---|---|
|bool|bool||
|uchar|uint8_t|8-Bit-Ganzzahl ohne Vorzeichen|
|int|int32_t|32-Bit-Ganzzahl mit Vorzeichen|
|uint|uint32_t|32-Bit-Ganzzahl ohne Vorzeichen|
|int64|int64_t|64-Bit-Ganzzahl mit Vorzeichen|
|uint64|uint64_t|64-Bit-Ganzzahl ohne Vorzeichen|
|half|GfHalf|16-Bit-Gleitkomma|
|float|float|32-Bit-Gleitkomma|
|doppelt|doppelt|64-Bit-Gleitkomma|
|timecode|SdfTimeCode|double repräsentiert eine auflösbare Zeit|
|string|std::string|stl-string|
|token|TfToken|internierter String mit schnellem Vergleich und Hashing|
|asset|SdfAssetPath|stellt einen auflösbaren Pfad zu einem anderen Asset dar|
|matrix2d|GfMatrix2d|2x2 Doppelmatrix|
|matrix3d|GfMatrix3d|3x3 Doppelmatrix|
|matrix4d|GfMatrix4d|4x4 Doppelmatrix|
|quatd|GfQuatd|Quaternion mit doppelter Genauigkeit|
|quatf|GfQuatf|Quaternion mit einfacher Genauigkeit|
|quath|GfQuath|Quaternion mit halber Genauigkeit|
|double2|GfVec2d|Vektor von 2 Doubles|
|float2|GfVec2f|Vektor von 2 Floats|
|half2|GfVec2h|Vektor von 2 Hälften|
|int2|GfVec2i|Vektor von 2 ints|
|double3|GfVec3d|Vektor von 3 Doubles|
|float3|GfVec3f|Vektor von 3 Floats|
|half3|GfVec3h|Vektor von 3 Hälften|
|int3|GfVec3i|Vektor von 3 Ints|
|double4|GfVec4d|Vektor von 4 Doubles|
|float4|GfVec4f|Vektor von 4 Floats|
|half4|GfVec4h|Vektor von 4 Hälften|
|int4|GfVec4i|Vektor von 4 ints|

## USD-Beispiel

Ein Beispiel für eine USD-Datei im reinen ASCII-Dateiformat ist wie folgt.

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
## Verweise ##

* [Einführung in USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD-API-Referenz](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

