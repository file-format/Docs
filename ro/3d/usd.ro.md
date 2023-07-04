{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "fișier usd", "format fișier usd", "format fișier", "fișier", "extensie", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Format universal de descriere a scenei",
  "description":"Aflați despre formatul de fișier USD și despre API-urile care pot deschide și crea fișiere USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Ce este un fișier USD?

Un fișier cu extensia .usd este un format de fișier Universal Scene Description care codifică date în scopul schimbului de date și al creșterii între aplicațiile de creare de conținut digital. Dezvoltat de Pixar, [USD](https://openusd.org/release/intro.html) oferă posibilitatea de a schimba elemente elementare (cum ar fi modele) sau animație.

## Format de fișier USD

Fișierele USD pot avea format binar (cunoscut și ca fișiere Crate) sau fișiere susținute de ASCII. Ambele formate de fișiere sunt interschimbabile, unde referințele pot fi legate la active .usd fără a schimba sursele. Formatul de fișier USD constă dintr-un set de biblioteci C++ cu legături Python pentru scripting. Permite asamblarea și organizarea oricărui număr de elemente de scenă 3D, cum ar fi decoruri virtuale, scene și fotografii, pentru a le transmite de la aplicație la aplicație.

### Tipuri de date USD

Tipurile de date fundamentale acceptate de formatul de fișier USD sunt enumerate în tabelul următor.

|Jeton de tipul valorii |Tipul C++ |Descriere|
---|---|---|
|bool|bool||
|uchar|uint8_t|întreg fără semn de 8 biți|
|int|int32_t|întreg cu semn de 32 de biți|
|uint|uint32_t|întreg fără semn pe 32 de biți|
|int64|int64_t|întreg cu semn de 64 de biți|
|uint64|uint64_t|întreg fără semn pe 64 de biți|
|jumătate|GfJumătate|virgula mobilă de 16 biți|
|float|float|virgula mobilă de 32 de biți|
|dublu|dublu|virgula mobilă pe 64 de biți|
|timecode|SdfTimeCode|dublu reprezentând un timp rezolvabil|
|șir|std::șir|șir stl|
|token|TfToken|șir intern cu comparație rapidă și hashing|
|activ|SdfAssetPath|reprezintă o cale rezolvabilă către un alt activ|
|matrice2d|GfMatrix2d|matricea dublelor 2x2|
|matrice3d|GfMatrix3d|matricea dublelor 3x3|
|matrice4d|GfMatrix4d|matrice 4x4 a dublelor|
|quatd|GfQuatd|cuaternion cu precizie dublă|
|quatf|GfQuatf|cuaternion cu o singură precizie|
|quath|GfQuath|cuaternion cu jumătate de precizie|
|double2|GfVec2d|vector de 2 duble|
|float2|GfVec2f|vector de 2 flotoare|
|half2|GfVec2h|vector a 2 jumătăți|
|int2|GfVec2i|vector de 2 int|
|double3|GfVec3d|vector de 3 duble|
|float3|GfVec3f|vector de 3 flotoare|
|half3|GfVec3h|vector de 3 jumătăți|
|int3|GfVec3i|vector de 3 int|
|double4|GfVec4d|vector de 4 duble|
|float4|GfVec4f|vector de 4 flotoare|
|half4|GfVec4h|vector de 4 jumătăți|
|int4|GfVec4i|vector de 4 inti|

## Exemplu USD

Un exemplu de fișier USD în format simplu de fișier ASCII este următorul.

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
## Referințe ##

* [Introducere în USD](https://openusd.org/release/intro.html)
* [USD API Reference](https://openusd.org/release/apiDocs.html)

