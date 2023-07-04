{
  "date" : "2021-02-01",
  "keywords" :["usd", "fichier usd", "format de fichier usd", "format de fichier", "fichier","extension", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Format universel de description de scène",
  "description":"En savoir plus sur le format de fichier USD et les API qui peuvent ouvrir et créer des fichiers USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Qu'est-ce qu'un fichier USD ?

Un fichier avec l'extension .usd est un format de fichier Universal Scene Description qui encode les données dans le but d'échanger et d'augmenter les données entre les applications de création de contenu numérique. Développé par Pixar, [USD](https://openusd.org/release/intro.html) offre la possibilité d'échanger des actifs élémentaires (tels que des modèles) ou des animations.

## Format de fichier USD

Les fichiers USD peuvent avoir un format binaire (également appelé fichiers Crate) ou des fichiers sauvegardés en ASCII. Ces deux formats de fichiers sont interchangeables où les références peuvent être liées à des actifs .usd sans changer les sources. Le format de fichier USD consiste en un ensemble de bibliothèques C++ avec des liaisons Python pour les scripts. Il permet l'assemblage et l'organisation d'un nombre quelconque d'éléments de scène 3D tels que des décors virtuels, des scènes et des prises de vue pour les transmettre d'une application à l'autre.

### Types de données USD

Les types de données fondamentaux pris en charge par le format de fichier USD sont répertoriés dans le tableau suivant.

|Jeton de type valeur |Type C++ |Description|
---|---|---|
|bool|bool||
|uchar|uint8_t|Entier non signé 8 bits|
|int|int32_t|Entier signé 32 bits|
|uint|uint32_t|Entier non signé 32 bits|
|int64|int64_t|Entier signé 64 bits|
|uint64|uint64_t|Entier non signé 64 bits|
|half|GfHalf|virgule flottante 16 bits|
|float|float|virgule flottante 32 bits|
|double|double|virgule flottante 64 bits|
|timecode|SdfTimeCode|double représentant un temps résoluble|
|chaîne|std::chaîne|chaîne stl|
|token|TfToken|chaîne interne avec comparaison rapide et hachage|
|asset|SdfAssetPath|représente un chemin résoluble vers un autre actif|
|matrix2d|GfMatrix2d|matrice 2x2 de doubles|
|matrix3d|GfMatrix3d|matrice 3x3 de doubles|
|matrix4d|GfMatrix4d|matrice 4x4 de doubles|
|quatd|GfQuatd|quaternion double précision|
|quatf|GfQuatf|quaternion simple précision|
|quath|GfQuath|quaternion demi-précision|
|double2|GfVec2d|vecteur de 2 doubles|
|float2|GfVec2f|vecteur de 2 flottants|
|half2|GfVec2h|vecteur de 2 half's|
|int2|GfVec2i|vecteur de 2 entiers|
|double3|GfVec3d|vecteur de 3 doubles|
|float3|GfVec3f|vecteur de 3 flottants|
|half3|GfVec3h|vecteur de 3 half's|
|int3|GfVec3i|vecteur de 3 entiers|
|double4|GfVec4d|vecteur de 4 doubles|
|float4|GfVec4f|vecteur de 4 flottants|
|half4|GfVec4h|vecteur de 4 half's|
|int4|GfVec4i|vecteur de 4 entiers|

## Exemple en USD

Un exemple de fichier USD au format de fichier ASCII simple est le suivant.

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
## Références ##

* [Introduction à l'USD](https://openusd.org/release/intro.html)
* [Référence API USD](https://openusd.org/release/apiDocs.html)

