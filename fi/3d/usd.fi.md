{
  "date": "2021-02-01",
  "keywords": [
"USD",
"usd tiedosto",
"usd tiedostomuoto",
"tiedosto muoto",
"tiedosto",
"laajennus",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD - Universal Scene Description Format",
  "description": "Opi USD-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda USD-tiedostoja.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-fid"
}
},
  "lastmod": "2021-02-01"
}

## Mikä on USD-tiedosto?

Tiedosto, jonka pääte on .usd, on Universal Scene Description -tiedostomuoto, joka koodaa tietoja tietojen vaihtamista ja täydentämistä varten digitaalisen sisällön luontisovellusten välillä. Pixarin kehittämä [USD](https://openusd.org/release/intro.html) tarjoaa mahdollisuuden vaihtaa elementtejä (kuten malleja) tai animaatioita.

## USD tiedostomuoto

USD-tiedostot voivat olla binäärimuotoisia (tunnetaan myös Crate-tiedostoina) tai ASCII-tukitiedostoja. Molemmat tiedostomuodot ovat keskenään vaihdettavissa, jos viittaukset voidaan linkittää .usd-sisältöön lähteitä muuttamatta. USD-tiedostomuoto koostuu joukosta C++-kirjastoja Python-sidoksilla komentosarjaa varten. Se mahdollistaa useiden 3D-näkymäelementtien, kuten virtuaalisten sarjojen, kohtausten ja otosten, kokoamisen ja järjestämisen, jotta ne voidaan siirtää sovelluksesta toiseen.

### USD-tietotyypit

USD-tiedostomuodon tukemat perustietotyypit on lueteltu seuraavassa taulukossa.

|Arvotyypin tunnus |C++-tyyppi |Kuvaus|
---|---|---|
|bool|bool||
|uchar|uint8_t|8-bittinen etumerkitön kokonaisluku|
|int|int32_t|32-bittinen etumerkillinen kokonaisluku|
|uint|uint32_t|32-bittinen etumerkitön kokonaisluku|
|int64|int64_t|64-bittinen etumerkillinen kokonaisluku|
|uint64|uint64_t|64-bittinen etumerkitön kokonaisluku|
|half|GfHalf|16 bitin liukuluku|
|float|float|32 bitin liukuluku|
|kaksois|kaksois|64 bitin liukuluku|
|timecode|SdfTimeCode|kaksinkertainen, joka edustaa selvitettävää aikaa|
|merkkijono|std::merkkijono|stl-merkkijono|
|token|TfToken|internoitu merkkijono nopealla vertailulla ja hajautustoiminnolla|
|asset|SdfAssetPath|estää selvitettävän polun toiseen omaisuuteen|
|matriisi2d|GfMatrix2d|2x2 tuplamatriisi|
|matrix3d|GfMatrix3d|3x3 tuplamatriisi|
|matrix4d|GfMatrix4d|4x4 tuplamatriisi|
|quatd|GfQuatd|kaksoistarkkuuden kvaternion|
|quatf|GfQuatf|yksitarkkuus kvaternion|
|quath|GfQuath|puolitarkkuus kvaternion|
|double2|GfVec2d|vektori 2 tuplaa|
|float2|GfVec2f|2 floatin vektori|
|half2|GfVec2h|vektori 2 puolikkaasta|
|int2|GfVec2i|vektori 2 ints|
|double3|GfVec3d|vektori 3 tuplaa|
|float3|GfVec3f|3 floatin vektori|
|half3|GfVec3h|vektori 3 puolikkaasta|
|int3|GfVec3i|vektori 3 ints|
|double4|GfVec4d|vektori 4 tuplaa|
|float4|GfVec4f|4 floatin vektori|
|half4|GfVec4h|vektori 4 puolikkaasta|
|int4|GfVec4i|vektori 4 ints|

## USD esimerkki

Esimerkki USD-tiedostosta tavallisessa ASCII-tiedostomuodossa on seuraava.

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
## Viitteet ##

* [Johdatus USD:hen](https://openusd.org/release/intro.html)

* [USD API-viite](https://openusd.org/release/apiDocs.html)


