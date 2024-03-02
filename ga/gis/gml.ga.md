{
  "date": "2019-10-11",
  "keywords": [
"comhad gml",
"Cad is comhad gml ann",
"comhad",
"sampla gml",
"Síneadh comhad gml",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML - Tíreolaíocht Markup Language File Formáid",
  "description": "Foghlaim faoi fhormáid comhaid GML agus APIanna ar féidir leo comhaid GML a chruthú agus a oscailt.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GML ann?

Seasann GML do Geography Markup Language atá bunaithe ar shonraíochtaí XML arna bhforbairt ag an gCuibhreannas Geospásúil Oscailte (OGC). Úsáidtear an fhormáid chun gnéithe sonraí geografacha a stóráil le haghaidh idirmhalartaithe i bhformáidí éagsúla comhaid. Feidhmíonn sé mar theanga shamhaltaithe do chórais gheografacha chomh maith le formáid idirmhalartaithe oscailte le haghaidh idirbhearta geografacha ar an idirlíon.

## Formáid Chomhaid GML ##

Mar is amhlaidh le formhór na ngramadach atá bunaithe ar XML, tá dhá chuid sa ghramadach – an scéimre a chuireann síos ar an doiciméad agus an doiciméad samplach ina bhfuil na sonraí féin. Déantar cur síos ar dhoiciméad GML ag baint úsáide as Scéimre GML. Ligeann sé seo d’úsáideoirí agus d’fhorbróirí cur síos a dhéanamh ar thacair chineálacha sonraí geografacha ina bhfuil pointí, línte agus polagáin. Trí úsáid a bhaint as scéimre feidhmchlár, is féidir le húsáideoirí tagairt a dhéanamh do bhóithre, do mhórbhealaí agus do dhroichid in ionad pointí, línte agus pholagáin.

Is fiú a thabhairt faoi deara nár cheart GML a léirmhíniú chun sonraí spáis a léiriú ar léarscáileanna. Tá ionadaíocht an ábhair GML difriúil ná an cuspóir ar cruthaíodh GML dó. Go hachomair, tá GML cosúil le XML sa mhéid is nach n-úsáidtear é ach chun an t-inneachar spáis a choinneáil ar féidir le feidhmchláir mhapála a úsáid chun críocha taispeána.

### Foirmiú Ábhair i GML ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* pointí

* línte

* cuair

* sufracáin agus

* polagáin


Tá sé beartaithe na leaganacha amach anseo de GML a thacú le tacú le céimseata 3D chomh maith le gaolmhaireachtaí toipeolaíochta idir gnéithe.

Ceadaíonn ionchódú GML do ghnéithe casta cheana féin. Is féidir gné a bheith comhdhéanta de ghnéithe eile mar shampla. Mar sin d’fhéadfadh gné amháin cosúil le haerfort a bheith comhdhéanta de ghnéithe eile amhail bealaí tacsaithe, rúidbhealaí, crochairí agus aerfoirt. Is féidir le céimseata gné geografach a bheith comhdhéanta de go leor eilimintí céimseata freisin. Mar sin is féidir le gné atá casta go geoiméadrach a bheith comhdhéanta de mheascán de chineálacha céimseata lena n-áirítear pointí, teaghráin línte agus polagáin.

### Samplaí ###

Ionchódaíonn GML 1.0 agus 2.0 Polagán, Pointí agus réada LineString mar a leanas:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Tagairtí ##

* [Sonraíochtaí GML]( https://www.ogc.org/standard/gml/)

* [GML - Le Vicipéid]( https://ga.wikipedia.org/wiki/Geography_Markup_Language)


