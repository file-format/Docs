{
  "date": "2019-10-11",
  "keywords": [
"amf",
"comhad amf",
"Formáid comhaid amf",
"formáid comhaid",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid AMF agus APIanna ar féidir leo comhaid AMF a oscailt agus a chruthú.",
  "title": "AMF - Comhad Déantúsaíochta Breiseáin",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad AMF ann?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## Formáid Comhaid AMF

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### Eilimintí de Chomhad AMF

Sainmhínítear na cúig ghné barrleibhéil leis an<AMF> Tá na clibeanna mar atá sonraithe thíos. Tá sé riachtanach go mbeadh eilimint oibiachta aonair i láthair i gcomhad AMF atá ag feidhmiú go hiomlán.

`<object> ` - Sainmhíníonn an eilimint oibiachta toirt nó toirteanna ábhair, a bhfuil baint ag gach ceann acu le haitheantas ábhartha le haghaidh priontála. Ní mór dúil oibiachta amháin ar a laghad a bheith i láthair sa chomhad. Tá rudaí breise roghnach.

`<material> ` - Sainmhíníonn an eilimint ábhair roghnach ábhar amháin nó níos mó le priontáil le haitheantas ábhartha ábhartha. Mura n-áirítear aon eilimint ábhartha, glactar leis gur ábhar réamhshocraithe amháin é.

`<texture> ` - Sainmhíníonn an eilimint uigeachta roghnach íomhá nó uigeacht amháin nó níos mó le haghaidh mapála datha nó uigeachta, agus ID uigeachta gaolmhar ag gach ceann acu.

`<constellation> ` - Comhcheanglaíonn eilimint an réaltbhuíon roghnach réada agus réaltbhuíonta eile go hordlathach i bpatrún coibhneasta le haghaidh priontála.

`<metadata> ` - Sonraíonn an eilimint roghnach meiteashonraí faisnéis bhreise faoin oibiacht(eanna) agus faoi na heilimintí atá sa chomhad.

## Sampla AMF

Seo a leanas sampla de chomhad AMF is féidir a chóipeáil go comhad [text](/word-processing/txt/) agus a shábháil mar chomhad comhbhrúite [zip](/compression/zip/) le hoscailt.
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
## Tagairtí

 * [AMF - Vicipéid]( https://ga.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [Sonraíochtaí AMF ar ISO](https://www.iso.org/standard/67472.html)

