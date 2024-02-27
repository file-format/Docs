{
  "date": "2019-10-11",
  "keywords": [
"amf",
"amf fil",
"amf filformat",
"filformat",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AMF filformat og API'er, der kan åbne og oprette AMF filer.",
  "title": "AMF - Additive Manufacturing File",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er AMF fil?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF filformat

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### Elementer af en AMF-fil

De fem elementer på øverste niveau defineret med<AMF> tags er som beskrevet nedenfor. Tilstedeværelsen af et enkelt objektelement er et must for en fuldt funktionel AMF-fil.

`<object> ` - Objektelementet definerer et eller flere mængder af materiale, som hver er knyttet til et materiale-ID til udskrivning. Mindst ét objektelement skal være til stede i filen. Yderligere objekter er valgfrie.

`<material> ` - Det valgfrie materialeelement definerer et eller flere materialer til udskrivning med et tilknyttet materiale-ID. Hvis der ikke er inkluderet noget materialeelement, antages et enkelt standardmateriale.

`<texture> ` - Det valgfrie teksturelement definerer et eller flere billeder eller teksturer til farve- eller teksturkortlægning, hver med et tilknyttet tekstur-ID.

`<constellation> ` - Det valgfrie konstellationselement kombinerer objekter og andre konstellationer hierarkisk til et relativt mønster til udskrivning.

`<metadata> ` - Det valgfrie metadataelement angiver yderligere information om objektet/objekterne og elementerne i filen.

## Eksempel på AMF

Følgende er et eksempel på AMF-fil, der kan kopieres til en [text](/word-processing/txt/)-fil og gemmes som komprimeret [zip](/compression/zip/)-fil til åbning.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referencer

 * [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [AMF-specifikationer på ISO](https://www.iso.org/standard/67472.html)

