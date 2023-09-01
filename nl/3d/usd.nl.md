{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd-bestand", "usd-bestandsindeling", "bestandsindeling", "bestand", "extensie", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Universal Scene Description Format",
  "description":"Meer informatie over USD-bestandsindelingen en API's die USD-bestanden kunnen openen en maken.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Wat is een USD-bestand?

Een bestand met de extensie .usd is een Universal Scene Description-bestandsindeling die gegevens codeert met als doel gegevens uit te wisselen en te vergroten tussen toepassingen voor het maken van digitale inhoud. [USD](https://openusd.org/release/intro.html) is ontwikkeld door Pixar en biedt de mogelijkheid om elementaire activa (zoals modellen) of animatie uit te wisselen.

## USD-bestandsindeling

USD-bestanden kunnen een binair formaat hebben (ook bekend als Crate-bestanden) of ASCII-bestanden. Beide bestandsindelingen zijn onderling uitwisselbaar, waarbij de verwijzingen kunnen worden gekoppeld aan .usd-activa zonder de bronnen te wijzigen. Het USD-bestandsformaat bestaat uit een set C++-bibliotheken met Python-bindingen voor scripting. Het maakt assemblage en organisatie van een willekeurig aantal 3D-scène-elementen mogelijk, zoals virtuele sets, scènes en opnamen, om ze van toepassing naar toepassing te verzenden.

### USD-gegevenstypen

De fundamentele gegevenstypen die door het USD-bestandsformaat worden ondersteund, staan in de volgende tabel.

|Waardetype token |C++ type |Beschrijving|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit geheel getal zonder teken|
|int|int32_t|32-bits geheel getal met teken|
|uint|uint32_t|32 bit geheel getal zonder teken|
|int64|int64_t|64-bits geheel getal met teken|
|uint64|uint64_t|64 bit geheel getal zonder teken|
|half|GfHalf|16 bit drijvende komma|
|float|float|32 bit drijvende komma|
|double|double|64 bit drijvende komma|
|timecode|SdfTimeCode|double staat voor een oplosbare tijd|
|string|std::string|stl string|
|token|TfToken|interned string met snelle vergelijking en hashing|
|asset|SdfAssetPath|vertegenwoordigt een oplosbaar pad naar een ander activum|
|matrix2d|GfMatrix2d|2x2 matrix van dubbels|
|matrix3d|GfMatrix3d|3x3 matrix van dubbels|
|matrix4d|GfMatrix4d|4x4 matrix van dubbels|
|quatd|GfQuatd|quaternion met dubbele precisie|
|quatf|GfQuatf|quaternion met enkele precisie|
|quath|GfQuath|half-precisie quaternion|
|double2|GfVec2d|vector van 2 doubles|
|float2|GfVec2f|vector van 2 drijvers|
|half2|GfVec2h|vector van 2 helften|
|int2|GfVec2i|vector van 2 ints|
|double3|GfVec3d|vector van 3 doubles|
|float3|GfVec3f|vector van 3 drijvers|
|half3|GfVec3h|vector van 3 helften|
|int3|GfVec3i|vector van 3 ints|
|double4|GfVec4d|vector van 4 doubles|
|float4|GfVec4f|vector van 4 drijvers|
|half4|GfVec4h|vector van 4 helften|
|int4|GfVec4i|vector van 4 ints|

## USD voorbeeld

Een voorbeeld van een USD-bestand in gewoon ASCII-bestandsformaat is als volgt.

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
## Referenties ##

* [Inleiding tot USD](https://openusd.org/release/intro.html)
* [USD API-referentie](https://openusd.org/release/apiDocs.html)

