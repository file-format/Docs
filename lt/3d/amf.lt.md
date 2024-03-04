{
  "date": "2019-10-11",
  "keywords": [
"amf",
"amf failą",
"amf failo formatas",
"Dokumento formatas",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie AMF failo formatą ir API, kurios gali atidaryti ir kurti AMF failus.",
  "title": "AMF – priedų gamybos failas",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra AMF failas?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF failo formatas

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### AMF failo elementai

Penki aukščiausio lygio elementai, apibrėžti su<AMF> žymos yra tokios, kaip nurodyta toliau. Norint, kad AMF failas veiktų visiškai, būtina turėti vieną objekto elementą.

`<object> ` – objekto elementas apibrėžia medžiagos tūrį ar tūrius, kurių kiekvienas yra susietas su medžiagos ID spausdinimui. Faile turi būti bent vienas objekto elementas. Papildomi objektai yra neprivalomi.

`<material> ` – pasirenkamas medžiagos elementas apibrėžia vieną ar daugiau medžiagų, skirtų spausdinti su susijusiu medžiagos ID. Jei neįtrauktas joks materialus elementas, daroma prielaida, kad yra viena numatytoji medžiaga.

`<texture> ` – pasirenkamas tekstūros elementas apibrėžia vieną ar daugiau vaizdų arba tekstūrų, skirtų spalvų ar tekstūrų atvaizdavimui, kiekvienas su susietu tekstūros ID.

`<constellation> ` – pasirenkamas žvaigždyno elementas hierarchiškai sujungia objektus ir kitus žvaigždynus į santykinį spausdinimo šabloną.

`<metadata> ` – pasirenkamas metaduomenų elementas nurodo papildomą informaciją apie objektą (-us) ir elementus, esančius faile.

## AMF pavyzdys

Toliau pateikiamas AMF failo pavyzdys, kurį galima nukopijuoti į [text](/word-processing/txt/) failą ir išsaugoti kaip suspaustą [zip](/compression/zip/) failą, kad jį būtų galima atidaryti.
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
## Nuorodos

 * [AMF – Vikipedija](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [AMF specifikacijos ISO](https://www.iso.org/standard/67472.html)

