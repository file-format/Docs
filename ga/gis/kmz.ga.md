{
  "date": "2019-10-11",
  "keywords": [
"comhad kmz",
"cad é comhad kmz",
"comhad",
"sampla kmz",
"síneadh comhad kmz",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KMZ - Formáid Chomhaid Zipped KML",
  "description": "Foghlaim faoi fhormáid comhaid KMZ agus APIanna ar féidir leo comhaid KMZ a chruthú agus a oscailt.",
  "linktitle": "KMZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-gaz"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad KMZ ann?

Léiriú é comhad KMZ (KML Zipped) de chomhad [KML](/gis/kml/) zipped ina bhfuil faisnéis gheospásúil atá le feiceáil i bhfeidhmchláir GIS ar nós Google Earth. Léirítear faisnéis faoi áitmharcanna sa chomhad mar dhomhanleithead agus domhanfhad mar aon le hainm saincheaptha. Is féidir an comhad KMZ aonair pacáistithe a roinnt le húsáideoirí eile go héasca. Is féidir sonraí múnla 3D a áireamh i gcomhaid KMZ chomh maith le haghaidh geo-léiriú na samhla. Is féidir comhad KMZ a oscailt in Google Maps ach an comhad a shábháil chuig suíomh ar líne agus ansin an URL a chlóscríobh sa bhosca Cuardaigh Google Maps.

## Struchtúr Comhaid ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. Is féidir leat sonraí a onnmhairiú ó Google Earth ar nós feidhmchláir go díreach chuig formáid comhaid KMZ. Tugtar **doc.kml** ar an bpríomhchomhad KML. Agus comhad KMZ á phacáistiú, is féidir níos mó ná comhad KML amháin a chur leis, ach ní bheidh tairbhe ar bith leis seo toisc go ndéanann Google Earth cuardach don chéad chomhad KML agus an comhad KMZ á oscailt agus á léamh aige. Déanann sé neamhaird ar aon chomhaid KML eile a aimsítear sa chartlann. Chun a bheith cinnte go léifidh Google Earth an comhad KML atá ag teastáil, ní mholtar ach comhad KML amháin a chur laistigh den chomhad KMZ.

Cuirtear na híomhánna, samhlacha, uigeachtaí, comhaid fuaime agus acmhainní eile dá dtagraítear sa chomhad doc.kml i bhfofhillteán eile taobh istigh den phríomhfhillteán. D’fhéadfadh roinnt castachta a bheith i gceist leis seo freisin ag brath ar líon na gcomhad tacaíochta. Is féidir naisc leis na comh-acmhainní seo a thagairt go réasúnta nó trí thagairtí iomlána.

### Tagairt choibhneasta ###

Nuair a chuirtear acmhainní taobh leis an bpríomhdhoic.kml taobh istigh d'fho-fhillteán laistigh den phríomhfhillteán, is féidir leis an tagairt choibhneasta na comhaid tacaíochta seo a chur in iúl mar a thaispeántar sa sampla seo a leanas (le haghaidh deilbhín amháin).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Iomlántagairt ###

Is féidir tagairt iomlán a dhéanamh d'acmhainní freisin. Tá URL iomlán an chomhaid nasctha i dtagairtí iomlána. Nuair a phostáiltear comhaid ar fhreastalaí lárnach, cinntíonn tagairt iomlán go bhfanann siad seo gan athbhrí i gcomparáid le tagairtí coibhneasta. Ní mholtar tagairt iomlán a dhéanamh do chomhad áitiúil mar go mbrisfidh na naisc seo nuair a bhogtar na comhaid go córas nua. Seo a leanas sampla de thagairtí iomlána:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Féach freisin ##

* [GeoJSON](/gis/geojson/)


## Tagairtí ##

* [Comhaid Google Earth agus KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


