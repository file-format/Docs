{
  "date": "2021-02-01",
  "keywords": [
"usd",
"usd fails",
"usd faila formātā",
"faila formātā",
"failu",
"pagarinājumu",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD — universāls ainas apraksta formāts",
  "description": "Uzziniet par USD failu formātu un API, kas var atvērt un izveidot USD failus.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-lvd"
}
},
  "lastmod": "2021-02-01"
}

## Kas ir USD fails?

Fails ar paplašinājumu .usd ir universāla ainas apraksta faila formāts, kas kodē datus datu apmaiņai un papildināšanai starp digitālā satura izveides lietojumprogrammām. Pixar izstrādātā [USD](https://openusd.org/release/intro.html) nodrošina iespēju apmainīties ar elementāriem līdzekļiem (piemēram, modeļiem) vai animāciju.

## USD faila formāts

USD failiem var būt binārais formāts (pazīstams arī kā Crate faili) vai ASCII faili. Abi šie failu formāti ir savstarpēji aizvietojami, ja atsauces var saistīt ar .usd līdzekļiem, nemainot avotus. USD faila formāts sastāv no C++ bibliotēku kopas ar Python saitēm skriptu veidošanai. Tas ļauj montēt un organizēt jebkādu skaitu 3D ainas elementu, piemēram, virtuālās kopas, ainas un kadrus, lai tos pārsūtītu no vienas lietojumprogrammas uz programmu.

### USD datu tipi

Pamatdatu tipi, ko atbalsta USD faila formāts, ir norādīti šajā tabulā.

|Vērtības tipa marķieris |C++ tips |Apraksts|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bitu neparakstīts vesels skaitlis|
|int|int32_t|32 bitu vesels skaitlis|
|uint|uint32_t|32 bitu neparakstīts vesels skaitlis|
|int64|int64_t|64 bitu vesels skaitlis|
|uint64|uint64_t|64 bitu neparakstīts vesels skaitlis|
|half|GfHalf|16 bitu peldošā komata|
|peldēt|peldēt|32 bitu peldošais punkts|
|double|double|64 bitu peldošā komata|
|timecode|SdfTimeCode|dubults, kas attēlo atrisināmu laiku|
|string|std::string|stl string|
|token|TfToken|internēta virkne ar ātru salīdzināšanu un jaukšanu|
|asset|SdfAssetPath|apzīmē atrisināmu ceļu uz citu līdzekli|
|matrica2d|GfMatrix2d|2x2 dubultnieku matrica|
|matrix3d|GfMatrix3d|3x3 dubultnieku matrica|
|matrix4d|GfMatrix4d|4x4 dubultnieku matrica|
|quatd|GfQuatd|dubultās precizitātes kvaternions|
|quatf|GfQuatf|vienas precizitātes quaternion|
|quath|GfQuath|pusprecizitātes quaternion|
|double2|GfVec2d|vektors no 2 dubultspēlēm|
|float2|GfVec2f|vektors no 2 pludiņiem|
|puse2|GfVec2h|vektors no 2 pusēm|
|int2|GfVec2i|vektors no 2 ints|
|double3|GfVec3d|vektors no 3 dubultspēlēm|
|float3|GfVec3f|vektors no 3 pludiņiem|
|puse3|GfVec3h|vektors no 3 pusēm|
|int3|GfVec3i|vektors no 3 ints|
|double4|GfVec4d|vektors no 4 dubultspēlēm|
|float4|GfVec4f|vektors no 4 pludiņiem|
|puse4|GfVec4h|vektors no 4 pusēm|
|int4|GfVec4i|vektors no 4 ints|

## USD piemērs

USD faila piemērs vienkāršā ASCII faila formātā ir šāds.

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
## Atsauces Nr.

* [Ievads par USD](https://openusd.org/release/intro.html)

* [USD API atsauce](https://openusd.org/release/apiDocs.html)


