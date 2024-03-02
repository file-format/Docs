{
  "date": "2019-10-11",
  "keywords": [
"shp comhad",
"formáid comhaid shp",
"cad is comhad shp ann",
"comhad",
"shp shampla",
"shp síneadh comhad",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP - Cruthchomhad ESRI",
  "description": "Foghlaim faoi fhormáid comhaid SHP agus APIs ar féidir leo comhaid SHP a chruthú agus a oscailt.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-gap"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad SHP ann?

Is é SHP an síneadh comhad do cheann de na príomhchineálacha comhaid a úsáidtear chun Cruth an ESRI a léiriú. Léiríonn sé faisnéis gheospásúil i bhfoirm sonraí veicteora atá le húsáid ag feidhmchláir Chórais Faisnéise Geografaí (GIS). Forbraíodh an fhormáid mar shonraíochtaí oscailte chun idir-inoibritheacht a éascú idir ESRI agus táirgí bogearraí eile.

## Léiriú Sonraí

Mar a luadh, cuireann formáid cruthchomhaid síos ar fhaisnéis geospásúil de thacar sonraí mar ghnéithe veicteora. Áirítear ar na gnéithe veicteoir seo:

* pointí

* línte

* polagáin


Is féidir leis na gnéithe seo i dteannta a chéile ionadaíocht a dhéanamh ar chruthanna de chineál ar bith ar nós toibreacha uisce, teorainneacha tíre, pointí spásúlachta, sreabhadh aibhneacha, lochanna, etc. Is féidir tréithe a bheith ag gach gné veicteoir a shainíonn cuspóir na gné sin. Mar shampla, is féidir ainm cathrach agus teocht a bheith ag cruthchomhad ina bhfuil cathracha Los Angeles mar thréithe a thugann léiriú brí do na sonraí spásúlachta.

## Comhaid Ghaolmhara

Ní féidir le feidhmchláir bogearraí comhad shp aonair a úsáid chun brí a bhaint as na sonraí atá ann. Chun ciall a bhaint as an bhfaisnéis atá i gcomhad den sórt sin, baineann cruthchomhad úsáid as na comhaid éigeantacha breise seo a leanas.

* comhad shx - comhad innéacs

* comhad dbf - comhad dBASE a stórálann tréithe uile na gcruthanna sa phríomhchomhad

* prj file - stórálann sé faisnéis tionscadail an chomhaid


Is féidir comhaid roghnacha eile a bheith ann freisin a roinneann an t-ainm céanna leis an bpríomhchomhad.

## Sonraíochtaí Formáid Comhaid SHP

Tá sonraíochtaí oscailte cruthchomhaid ar fáil ar líne ón ESRI i bhfoirm [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) agus mionléiríonn siad struchtúr iomlán an chomhaid go mion. Is éard atá san fhaisnéis atá sa phríomhchomhad .shp ná ceanntásca agus taifid. Tar éis an ceanntásc comhaid ar fhad sheasta tá taifid ar fhad inathraithe ina bhfuil gach taifead comhdhéanta de cheanntásc taifid ar fhad sheasta agus ina dhiaidh sin tá inneachar taifead ar fhad inathraithe.

### Príomhcheanntásc Comhad SHP

Tosaíonn an príomhcheanntásc Comhad ó thús an chomhaid agus tá sé 100 beart ar fad. Tá eagrú an phríomhcheannteidil seo mar aon le suíomh beart, luach, cineál agus ord beart mar a thaispeántar sa tábla seo a leanas.


| Beart | Réimse | Luach | Cineál | Ordú Beart
---|---|---|---|---|
|0-3|Cód Comhaid|9994|Slánuimhir | Endian Mór
|4-23|Neamhúsáidte|0|Slánuimhir|Eideann Mór
|24-27|Fad an Chomhaid|Fad an Chomhaid|Slánuimhir| Endian Mór
|28-31|Leagan|1000|Slánuimhir|Aondach Beag
|32-35|Cineál Cruth|Cineál Cruth|Slánuimhir|Indian Beag
|36-67|Dronuilleog Theoranta Íosta|Xmin, Ymin, Xmax agus Ymax|dúbailte | Endian Beag
|68-83|Bosca Teorann | Zmin, Zmax | dúbailte | Endian Beag
|84-99|Bosca Teorann|Mmin, Mmax|dúbailte|

Ní mór a thabhairt faoi deara gurb é luach fad comhaid fad iomlán an chomhaid i bhfocal 16-ghiotán a áiríonn freisin na caoga focal 16-ghiotán atá sa cheanntásc.

#### Cineálacha Cruth

Is iad seo a leanas luachanna na gcineálacha cruthanna sa tábla thuas:


|Luach|Cineál Cruth
---|---|
|0|Cruth Neamhní
|1|Pointe
|3|Paillíne
|5|Polagán
|8|Ilphointe
|11|PointeZ
|13|PolaiLíneZ
|15|PolygonZ
|18|MultiPointZ
|21|PointeM
|23|PolailíneM
|25|PolygonM
|28|IlphointeM
|31|Ilphaiste

### Taifid Sonraí ###

Tar éis an phríomhcheannteidil comhaid tá taifid ar fhad athraitheach ina bhfuil ceanntásc ar fhad sheasta i ngach taifead agus ina dhiaidh sin tá inneachar taifid ar fhad inathraithe.

#### Ceanntásc Taifead ####

Tá eolas i gceanntásc taifead faoi uimhir thaifid agus fad ábhair an taifid i fad seasta 8 mbeart. Tá eagrú an chinnteidil taifid mar a thaispeántar thíos:


| Beart | Réimse | Luach | Cineál | Ordú Beart
---|---|---|---|---|
|0-3|Uimhir Thaifid|Uimhir Thaifid|Slánuimhir|Mór
|4-7|Fad Taifid|Fad Taifid|Slánuimhir|Mór

#### Taifead na nÁbhar ####

Is éard atá i dtaifead comhaid crutha ná cineál crutha agus na sonraí geoiméadracha don chruth sin ina dhiaidh sin. Seasann cineál cruth 0 do chruth nialasach nach bhfuil aon sonraí geoiméadracha ann don chruth. Is ionann fad na n-ábhar taifid agus frithchaitheamh na gcodanna crutha agus na rinn. Glacaimid sampla de chineál Pointe Cruth chun an chaoi a bhfuil faisnéis faoi chineál cruth dá leithéid i dtaifead a mhionsaothrú.

Seasann pointe do shuíomh geografach áirithe san ord X,Y, áit a léirítear gach comhordanáid le luach débheachtais. Taispeánann an tábla seo a leanas an leagan amach de chineál cruth Pointe.


|Biotáil|Cineál Cruth|Luach|Cineál|Uimhir|Ordú Beart
---|---|---|---|---|---|
|0-3|Cineál Cruth|1|Slánuimhir|1|Beag
|4-11|X|X|dúbailte|1|Beag
|12-19|Y|Y|dúbailte|1|Beag

Examples of other shape types can be found the ESRI technical description document.

## Tagairtí ##

* [Cur Síos Teicniúil Shapefile ESRI](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) ag an ESRI


