{
  "date" : "2021-02-01",
  "keywords" :["usd", "file usd", "formato file usd", "formato file", "file", "estensione", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Formato descrizione scena universale",
  "description":"Scopri il formato di file USD e le API che possono aprire e creare file USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Che cos'è un file USD?

Un file con estensione .usd è un formato di file Universal Scene Description che codifica i dati allo scopo di scambiare e aumentare i dati tra le applicazioni di creazione di contenuti digitali. Sviluppato da Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) offre la possibilità di scambiare risorse elementari (come modelli) o animazioni.

## Formato file USD

I file USD possono avere un formato binario (noto anche come file Crate) o file supportati da ASCII. Entrambi questi formati di file sono intercambiabili in cui i riferimenti possono essere collegati a risorse .usd senza modificare le fonti. Il formato di file USD è costituito da un set di librerie C++ con collegamenti Python per lo scripting. Consente l'assemblaggio e l'organizzazione di un numero qualsiasi di elementi di scene 3D come set virtuali, scene e riprese per trasmetterli da un'applicazione all'altra.

### Tipi di dati USD

I tipi di dati fondamentali supportati dal formato di file USD sono elencati nella tabella seguente.

|Tipo valore token |Tipo C++ |Descrizione|
---|---|---|
|bool|bool||
|uchar|uint8_t|Intero senza segno a 8 bit|
|int|int32_t|Intero con segno a 32 bit|
|uint|uint32_t|Intero senza segno a 32 bit|
|int64|int64_t|Intero con segno a 64 bit|
|uint64|uint64_t|Intero senza segno a 64 bit|
|metà|GfHalf|virgola mobile a 16 bit|
|float|float|virgola mobile a 32 bit|
|doppio|doppio|virgola mobile a 64 bit|
|timecode|SdfTimeCode|doppio che rappresenta un tempo risolvibile|
|stringa|std::stringa|stringa stl|
|token|TfToken|stringa interna con confronto veloce e hash|
|asset|SdfAssetPath|rappresenta un percorso risolvibile verso un altro asset|
|matrix2d|GfMatrix2d|Matrice 2x2 di doppi|
|matrix3d|GfMatrix3d|Matrice 3x3 di doppi|
|matrix4d|GfMatrix4d|matrice 4x4 di doppi|
|quatd|GfQuatd|quaternione a doppia precisione|
|quatf|GfQuatf|quaternione a precisione singola|
|quath|GfQuath|quaternione a mezza precisione|
|double2|GfVec2d|vettore di 2 doppi|
|float2|GfVec2f|vettore di 2 float|
|half2|GfVec2h|vettore di 2 metà|
|int2|GfVec2i|vettore di 2 int|
|double3|GfVec3d|vettore di 3 doppi|
|float3|GfVec3f|vettore di 3 float|
|half3|GfVec3h|vettore di 3 metà|
|int3|GfVec3i|vettore di 3 int|
|double4|GfVec4d|vettore di 4 doppi|
|float4|GfVec4f|vettore di 4 float|
|half4|GfVec4h|vettore di 4 metà|
|int4|GfVec4i|vettore di 4 int|

## Esempio di USD

Un esempio di un file USD in un semplice formato di file ASCII è il seguente.

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
## Riferimenti ##

* [Introduzione a USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Riferimento API USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

