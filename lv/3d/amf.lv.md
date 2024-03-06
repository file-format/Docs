{
  "date": "2019-10-11",
  "keywords": [
"amf",
"amf fails",
"amf faila formāts",
"faila formātā",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par AMF failu formātu un API, kas var atvērt un izveidot AMF failus.",
  "title": "AMF — piedevu ražošanas fails",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir AMF fails?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF faila formāts

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### AMF faila elementi

Pieci augstākā līmeņa elementi, kas definēti ar<AMF> tagi ir norādīti tālāk. Viena objekta elementa klātbūtne ir obligāta pilnībā funkcionējošam AMF failam.

`<object> ` — objekta elements definē materiāla apjomu vai apjomus, no kuriem katrs ir saistīts ar materiāla ID drukāšanai. Failā ir jābūt vismaz vienam objekta elementam. Papildu objekti nav obligāti.

`<material> ` — izvēles materiāla elements definē vienu vai vairākus materiālus drukāšanai ar saistīto materiāla ID. Ja nav iekļauts neviens materiāla elements, tiek pieņemts viens noklusējuma materiāls.

`<texture> ` — izvēles faktūras elements nosaka vienu vai vairākus attēlus vai faktūras krāsu vai faktūras kartēšanai, katram no kuriem ir saistīts faktūras ID.

`<constellation> ` — izvēles konstelācijas elements hierarhiski apvieno objektus un citus konstelācijas relatīvā drukāšanas paraugā.

`<metadata> ` — neobligātais metadatu elements norāda papildu informāciju par failā ietverto(-ajiem) objektu(-iem) un elementiem.

## AMF piemērs

Tālāk ir sniegts AMF faila piemērs, ko var kopēt [text](/word-processing/txt/) failā un saglabāt kā saspiestu [zip](/compression/zip/) failu atvēršanai.
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
## Atsauces

 * [AMF — Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [AMF specifikācijas uz ISO](https://www.iso.org/standard/67472.html)

