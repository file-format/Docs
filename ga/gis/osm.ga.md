{
  "date": "2019-10-11",
  "keywords": [
"comhad osm",
"cad is comhad osm ann",
"comhad",
"sampla osm",
"síneadh comhad osm",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM - Formáid Chomhaid OpenStreetMap",
  "description": "Foghlaim faoi fhormáid comhaid OSM agus APIs is féidir comhaid OSM a chruthú agus a oscailt.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-gam"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad OSM ann?

Is éard atá i OpenStreetMap (OSM) ná bailiúchán ollmhór de stórtha faisnéise geografaí deonacha i gcineálacha éagsúla comhaid, ag baint úsáide as scéimeanna ionchódaithe éagsúla chun na sonraí seo a thiontú ina giotáin agus ina mbearta. Is comhiarracht é OSM chun léarscáil den domhan saor in aisce a chruthú ar féidir eagarthóireacht a dhéanamh air. Is é príomh-aschur na comhiarrachta seo ná sonraí geografacha seachas an léarscáil féin. Spreagann na srianta ar úsáid nó ar infhaighteacht faisnéise geografaí ar fud cuid mhór den domhan an gá atá le OSM a chruthú.

Tá na sonraí atá ar fáil ó OSM réidh le cur in ionad Google Maps d’fheidhmchláir chlasaiceacha (Facebook, Craigslist srl.) agus sonraí réamhshocraithe d’fheidhmchláir ghlacadóra GPS. Cé go bhfuil cáilíocht sonraí éagsúil ar fud an domhain fós is féidir sonraí OpenStreetMap a chur i gcomparáid go háisiúil le foinsí sonraí paitinne.

## Stair Achomair ar Formáid Chomhaid OSM

Spreagtha ag rathúlacht Vicipéid, in 2004, fiontraí Briotánach Steve Coast, a chruthaigh an tionscadal mapála domhanda pobalbhunaithe seo sa RA. Dhírigh sé ar dtús ar an Ríocht Aontaithe a mhapáil. Bunaíodh Fondúireacht OpenStreetMap den chéad uair i mí Aibreáin 2006 chun tacú le héabhlóid, leathnú agus scaipeadh geospásála saor in aisce do dhuine ar bith. I mí na Nollag 2006, chabhraigh Yahoo le OpenStreetMap lena ghrianghrafadóireacht ón aer le haghaidh táirgeadh léarscáileanna.

Chuir Automotive Navigation Data (AND) sonraí bóithre iomlána don Ísiltír agus sonraí trunk bóithre don India agus don tSín le OSM i mí Aibreáin 2007. I mí na Nollag 2007, bhí Ollscoil Oxford ar an eagraíocht ba shuntasaí a chomhtháthaigh sonraí OpenStreetMap laistigh dá bpríomhshuíomh Gréasáin. Ó shin i leith, cuireann breis agus 2 mhilliún úsáideoir cláraithe sonraí leis an tionscadal seo trí úsáid a bhaint as gléasanna GPS, aerghrianghrafadóireacht agus suirbhéanna láimhe. Cuirtear na sonraí seo a chuir an pobal ar fáil faoin gCeadúnas Bunachar Sonraí Oscailte. Choinnigh eagraíocht neamhbhrabúis chláraithe Shasana OpenStreetMap Foundation an suíomh OSM.

## Formáid Comhaid OSM

Tá go leor bealaí agus formáidí comhaid ann chun sonraí geografacha a stóráil ach tá formáid comhaid **OSM** teoranta do OpenStreetMap. Tá OSM deartha go háirithe i bhformáid chaighdeánach a bheartaítear a iompar go héasca ar fud an Idirlín. Comhad .osm is ea formáid struchtúrtha ordaithe, códaithe in XML. In OpenStreetMap tá ceithre eilimint mhaighdeogacha chun struchtúr sonraí topological a stóráil:

{{< figure src="../OSM.png" alt="Formáid Comhaid OSM" >}}


|Nóid|Bealaí|Caidreamh|Clibeanna
---|---|---|---|
|<ul><li> Léiríonn sé suíomh geografach arna stóráil mar phéirí domhanleithead agus domhanfhad.</li><li> Úsáidtear é chun gnéithe léarscáile gan méid a léiriú, mar bheanna sléibhe.</li></ul> |<ul><li> Liostaí nóid curtha in eagar, rud a chiallaíonn polyline, nó polagán</li><li> Déan ionadaíocht ar ghnéithe líneacha ar nós bóithre agus aibhneacha, agus criosanna, mar limistéir pháirceála dufair, agus páirceanna.</li></ul> |<ul><li> Léiríonn liostaí sórtáilte nóid agus bealaí a ngaol cosúil le bacainní agus u casadh ar bhóithre, trasnaíonn mótarbhealaí bealaí éagsúla atá ann cheana féin agus limistéir le poill.</li></ul> |<ul><li> Stóráil meiteashonraí faoi oibiachtaí na léarscáile.* Ceangailte i gcónaí le haon nód, bealach nó gaol</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

Úsáideann OSM trí chineál comhaid chun a phríomhshonraí a stóráil.

Láimhseálann OSM na comhaid seo go léir leis an bhfaisnéis faoina sonraí formáidithe. Ach is iad na comhaid seo a tháirgtear na rudaí inmheánacha céanna. Maidir le comhaid sonraí tá an bhratach infheicthe ar oibiachtaí OSM fíor i gcónaí, rud nach bhfuil fíor i gcás na staire agus comhaid athraithe.

In úsáid go coitianta, tá éagsúlacht i bhformáidí comhaid OSM. Sainmhíníonn formáidí comhaid an t-ábhar a ionchódú ar dhiosca nó ar shreang i giotáin agus bearta. Tá OSM in ann na formáidí seo a léamh agus a scríobh ar a mhéad.

**XML**

Tá an bhunfhormáid OSM bunaithe ar XML. Tá sonraí tuairisceáin phríomhbhunachar sonraí OSM API i bhformáid XML.

**PBF**

Seasann ionchódú Maoláin Phrótacail ar fhormáid dhénártha agus ar cheann de na formáidí is dlúithe.

**O5M/O5C**

Formáid dhénártha bunaithe ar fhormáid níos simplí ach níos lú úsáide a bhaint as. Is féidir le OSM an fhormáid seo a léamh ach ní féidir leis a scríobh.

**OPL**

Formáid shimplí atá beartaithe le húsáid le huirlisí caighdeánacha ordú UNIX. In aice le comhaid CSV, ceadaítear aonán OSM amháin ar líne amháin.

**DEBUG**

Formáid téacs-bhunaithe atá ceaptha a chruthú le haghaidh dífhabhtaithe. Is féidir leis an OSM an fhormáid seo a scríobh ach ní féidir leis a léamh.

**POLL DUBH**

Formáid chaochadán a dhiúscraíonn na sonraí go léir. Is féidir leis an OSM an fhormáid seo a scríobh ach ní féidir leis a léamh.

## Stóráil Sonraí OSM ##

Coinníonn príomhbhunachar sonraí **PostgreSQL** OSM an phríomhchóip de shonraí OSM le síneadh PostGIS. I gcás gach primitive sonraí, coinníonn an príomhbhunachar sonraí tábla a bhfuil a sraitheanna a stóráil rudaí aonair. Déanann gach eagarthóireacht an bunachar sonraí seo a nuashonrú agus cruthaítear gach formáid eile leis an mbunachar sonraí seo. Cruthaítear go leor comhthiomsaithe bunachar sonraí is féidir a íoslódáil chun sonraí a aistriú ó áit amháin go háit eile. Sainmhíníonn dhá fhormáid, ceann ag baint úsáide as XML agus ceann eile ag baint úsáide as Formáid Dénártha Maolán Prótacail (PBF) na linnte seo. Stóráiltear na sonraí iomlána i gcomhad ar a dtugtar planet.osm

## Comhbhrú i gComhaid OSM ##

Úsáideann formáidí téacsbhunaithe (XML, OPL, agus Debug) comhbhrú gzip nó bzip2 go roghnach.

## Tagairtí ##

* [Lámhleabhar Formáidí Comhaid OSM](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://ga.wikipedia.org/wiki/OpenStreetMap#History)

* [Foghlaim OSM](https://learnosm.org/ga/osm-data/getting-data/)


