{
  "date": "2019-10-11",
  "keywords": [
"amf",
"amf tiedosto",
"amf tiedostomuoto",
"tiedosto muoto",
"3d"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi AMF-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda AMF-tiedostoja.",
  "title": "AMF - lisäainevalmistustiedosto",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on AMF-tiedosto?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF tiedostomuoto

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### AMF-tiedoston elementit

Viisi ylimmän tason elementtiä, jotka on määritelty<AMF> tunnisteet ovat alla kuvatun mukaisesti. Yksittäisen objektielementin läsnäolo on välttämätöntä täysin toimivalle AMF-tiedostolle.

`<object> ` - Objektielementti määrittää materiaalin määrän tai tilavuuksia, joista jokaiseen on liitetty materiaalitunnus tulostusta varten. Tiedostossa on oltava vähintään yksi objektielementti. Lisäobjektit ovat valinnaisia.

`<material> ` - Valinnainen materiaalielementti määrittää yhden tai useamman tulostettavan materiaalin ja siihen liittyvän materiaalitunnuksen. Jos materiaalielementtiä ei sisällytetä, oletuksena on yksi oletusmateriaali.

`<texture> ` - Valinnainen pintakuvioelementti määrittelee yhden tai useamman kuvan tai pintakuvion väri- tai pintakuviokartoittamista varten, joista jokaiselle on liitetty pintakuviotunnus.

`<constellation> ` - Valinnainen tähdistöelementti yhdistää hierarkkisesti objektit ja muut konstellaatiot suhteelliseksi kuvioksi tulostusta varten.

`<metadata> ` - Valinnainen metatieto-elementti määrittää lisätietoja tiedoston sisältämistä objekteista ja elementeistä.

## AMF esimerkki

Seuraavassa on esimerkki AMF-tiedostosta, joka voidaan kopioida [text](/word-processing/txt/)-tiedostoon ja tallentaa pakattuna [zip](/compression/zip/)-tiedostona avaamista varten.
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
## Viitteet

 * [AMF – Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [AMF:n tekniset tiedot ISO:lla](https://www.iso.org/standard/67472.html)

