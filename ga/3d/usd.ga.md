{
  "date": "2021-02-01",
  "keywords": [
"USD",
"comhad usd",
"formáid comhaid usd",
"formáid comhaid",
"comhad",
"síneadh",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USD - Formáid Cur Síos ar an Radharc Uilíoch",
  "description": "Foghlaim faoi fhormáid comhaid USD agus APIs is féidir comhaid USD a oscailt agus a chruthú.",
  "linktitle": "USD",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-us-gad"
}
},
  "lastmod": "2021-02-01"
}

## Cad is comhad USD ann?

Is formáid comhaid Tuairisc ar Radharc Uilíoch é comhad le síneadh .usd a ionchódaíonn sonraí chun críche sonraí a idirmhalartú agus a mhéadú idir feidhmchláir chruthaithe ábhair dhigitigh. Arna fhorbairt ag Pixar, soláthraíonn [USD](https://openusd.org/release/intro.html) an cumas sócmhainní eiliminteacha (amhail samhlacha) nó beochan a idirmhalartú.

## Formáid Comhaid USD

Is féidir formáid dhénártha (ar a dtugtar comhaid Crate freisin) nó comhaid le tacaíocht ASCII a bheith ag comhaid USD. Tá an dá fhormáid comhaid seo idirmhalartaithe nuair is féidir na tagairtí a nascadh le sócmhainní .usd gan na foinsí a athrú. Tá formáid comhaid USD comhdhéanta de shraith leabharlanna C ++ le ceangail Python le haghaidh scriptithe. Cuireann sé ar chumas líon ar bith d’eilimintí radharc 3D a thionól agus a eagrú, mar thacair fhíorúla, radhairc agus seatanna chun iad a tharchur ó fheidhm go feidhmchlár.

### Cineálacha Sonraí USD

Tá na cineálacha sonraí bunúsacha a dtacaíonn formáid comhaid USD leo liostaithe sa tábla seo a leanas.

|Cineál luacha comhartha |Cineál C++ |Cur síos|
---|---|---|
|bool|bool||
|uchar|uint8_t| slánuimhir 8 ghiotán gan síniú|
|int|int32_t| slánuimhir sínithe 32 giotán|
|uint|uint32_t| slánuimhir 32 ghiotán gan síniú|
|int64|int64_t| slánuimhir sínithe 64 giotán|
|uint64|uint64_t| slánuimhir 64 ghiotán gan síniú |
|leath|GfHalf|Snámhphointe 16 ghiotán|
|snámhphointe | snámhphointe | snámhphointe 32 giotán |
|dúbailte | dúbailte | snámhphointe 64 giotán |
|cód ama|Cód SdfTime|dúbailte a léiríonn am inréite |
| teaghrán | std:: teaghrán | stl teaghrán |
|token|TfToken|teaghrán inmheánach le comparáid tapa agus hashing|
|sócmhainn|SdfAssetPath|is ionann é agus cosán inréitithe chuig sócmhainn eile|
|maitrís2d|GfMatrix2d|maitrís dúbailte 2x2|
|maitrís3d|GfMatrix3d|maitrís 3x3 na dúbailtí |
|maitrís4d|GfMatrix4d|maitrís dúbailte 4x4|
|quatd|GfQuatd|ceathrú cruinneas dúbailte|
|quatf|GfQuatf|ceathrú aonchruinneas|
|quath|GfQuath|ceathrú leathchruinneas|
|dúbailte2|GfVec2d|veicteoir 2 dhúbailte|
|snámh2|GfVec2f|veicteoir 2 shnámhán|
|leath2|GfVec2h|veicteoir 2 leath|
|int2|GfVec2i|veicteoir 2 int|
|dúbailte3|GfVec3d|veicteoir 3 dhúbailte |
|snámh3|GfVec3f|veicteoir 3 shnámhán|
|leath3|GfVec3h|veicteoir 3 leath|
|int3|GfVec3i|veicteoir 3 int|
|dúbailte4|GfVec4d|veicteoir 4 dhúbailte |
|snámh4|GfVec4f|veicteoir 4 shnámhán|
|leath4|GfVec4h|veicteoir 4 leath|
|int4|GfVec4i|veicteoir 4 int|

## Sampla USD

Seo a leanas sampla de chomhad USD i bhformáid ghnáthchomhaid ASCII.

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
## Tagairtí ##

* [Réamhrá ar USD](https://openusd.org/release/intro.html)

* [Tagairt API USD](https://openusd.org/release/apiDocs.html)


