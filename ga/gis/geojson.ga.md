{
  "date": "2019-10-11",
  "keywords": [
"comhad geojson",
"cad is comhad geojson ann",
"comhad",
"sampla geojson",
"síneadh comhad geojson",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON - Formáid Chomhaid Geografach bunaithe ar JSON",
  "description": "Foghlaim faoi fhormáid comhaid GeoJSON agus APIanna ar féidir leo comhaid GeoJSON a chruthú agus a oscailt.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-gan"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GeoJSON ann?

Is formáid JSON é GeoJSON atá deartha chun na gnéithe geografacha lena dtréithe neamhspásúla a léiriú. Sainmhíníonn an fhormáid seo oibiachtaí éagsúla JSON (Notaireacht Oibiachta JavaScript) agus a mbealach le chéile. Léiríonn formáid JSON faisnéis chomhchoiteann faoi na gnéithe Geografacha, a fairsinge spáis, agus a n-airíonna. Féadfaidh réad den chomhad seo céimseata (Point, LineString, Polagán), gné nó bailiúchán gnéithe a léiriú. Léiríonn na gnéithe seoltaí agus áiteanna mar shráideanna pointe, príomhbhóithre agus teorainneacha mar theaghráin líne agus tíortha, cúigí, agus réigiúin talún mar pholagáin. Trí úsáid a bhaint as GeoJSON, is féidir le feidhmchláir ródúcháin agus loingseoireachta éagsúla soghluaiste clúdach a gcuid seirbhísí a léiriú. Is síneadh de GeoJSON é TopoJSON atá níos lú i méid agus a ionchódaíonn topology geospásúil.

## Stair Ghearr ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## Formáid Chomhaid GeoJSON ##

### Comhordú ###

Is é Comhordanáid an ghné bhunúsach d'aon sonraí geografacha. Toise singil é seo (Domhanfhad, domhanleithead) a léiríonn uimhir shingil (formáid dheachúil) agus uaireanta taifeadann sé comhordanáid don ingearchló freisin. Is gné é an t-am freisin ach fágann castacht na hoibre sin go bhfuil sé deacair é a thaifeadadh mar chomhordanáidí. Déantar comhordanáidí sa dá JSON GeoJSON a fhormáidiú cosúil le huimhreacha.

### Post ###

Léiríonn sraith ordaithe comhordanáidí an [position](https://geojson.org/geojson-spec.html#positions). Is é seo an t-aonad is lú ar féidir pointe ar domhan a chur in iúl.

`[domhanfhad, domhanleithead, ingearchló]`

Sular scaoileadh an tsonraíocht reatha, cheadaigh GeoJSON trí chomhordanáidí a thaifeadadh in aghaidh an tsuímh ach níl sé ceadaithe ag an tsonraíocht nua.

### Céimseata ###

Is cruthanna simplí (pointí, cuair, agus dromchlaí) iad céimseata i GeoJSON atá comhdhéanta de chineál agus de bhailiúchán comhordanáidí. Is é pointe an chéimseata is simplí a sheasann do shuíomh amháin

`{ cineál: Pointe, comhordanáidí: [0, 0] }`

### LineStrings ###

Úsáidtear ar a laghad dhá áit nasctha chun líne a léiriú.

`{ cineál: LineString, comhordanáidí: [[10, 30], [10, 10]] }`

Is iad teaghráin phointe agus línte an dá chatagóir céimseata is simplí. Ní bhacann an dá chineál céimseata mórán rialacha geoiméadracha. Is féidir pointe a léiriú in áit ar bith, agus is féidir níos mó ná pointe amháin a bheith ag líne, fiú má tá na pointí féin-thrasnaithe.

### Polagáin ###

Is cosúil go bhfuil céimseataí GeoJSON i bhfad níos casta i Polagáin. Tá limistéir laistigh agus lasmuigh ag polagáin agus is féidir leo poill a bheith acu laistigh den taobh istigh.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

I gcomparáid le LineStrings, i bpolagáin, tá leibhéal amháin eile neadaithe sa liosta comhordanáidí agus is féidir go mbeadh gearrtha amach cosúil le donuts.

### Leibhéal Comhordaithe ###

I bhformáid GeoJSON, tá ceithre leibhéal doimhneachta ann don airí comhordanáidí.

### Gnéithe ###

Is cuid lárnach de GeoJSON iad céimseataí, dá bhrí sin, tá níos mó i gceist le sonraí an fhíorshaoil ná na cruthanna simplí seo a bhfuil féiniúlacht agus tréithe acu. Taifeadann gnéithe an chéimseata chomh maith lena n-airíonna.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Is féidir le hairíonna gné a bheith ina gcineál réad [JSON](http://json.org/) ina bhfuil mapálacha aon-doimhneachta eochairluacha.

###FeatureCollection ###

Ag an leibhéal is airde de chomhaid GeoJSON, is é FeatureCollection an rud is coitianta ar nós:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
  },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Tacaíonn go leor pacáistí bogearraí mapála agus GIS le GeoJSON lena n-áirítear bogearraí GeoDjango, OpenLayers, agus Geoforge. Tá sé comhoiriúnach freisin le PostGIS agus Mapnik. Tacaíonn seirbhísí API léarscáileanna Google, Yahoo agus Bing le GeoJSON freisin.

## Tagairtí ##

* [macwright.org]( https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON - Le Vicipéid]( https://en.wikipedia.org/wiki/GeoJSON)


