{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"comhad",
"síneadh",
"formáid comhaid",
"Suíomh GPS",
"Bealachbhealach"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC - Formáid Chomhaid Suíomh GPS",
  "description": "Foghlaim faoi fhormáid comhaid LOC agus APIs ar féidir leo comhaid LOC a chruthú agus a oscailt.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-gac"
}
},
  "lastmod": "2021-07-18"
}

## Cad is comhad LOC ann?

Comhad suímh GPS é comhad a bhfuil síneadh .loc aige ina bhfuil suíomhanna geospásúla mar phointí bealaigh. Péire luachanna domhanleithead-leithead is ea pointe bealaigh a thagraíonn do shuíomh a úsáideann feidhmchláir an Chórais Faisnéise Geografaí (GIS). Úsáideann cláir léarscáilithe GPS, mar DeLorme Topo, comhaid LOC chun faisnéis atá sna comhaid LOC seo a léamh agus a thaispeáint mar shraitheanna in-roghnaithe ag úsáideoirí deiridh. Ina theannta sin, úsáidtear iad seo chun sonraí GPS a mhalartú idir feidhmchláir. Is féidir comhaid LOC a oscailt trí úsáid a bhaint as feidhmchláir ar nós [TopoGrafix EasyGPS](https://www.easygps.com/) a thaispeánann inneachar na gcomhad sin mar shraitheanna agus sonraí a breacadh ar an léarscáil ag geolocation faoi seach.

## Formáid Chomhaid LOC - Tuilleadh Eolais

Tá cosúlachtaí idir comhaid LOC agus comhaid [GPX](/gis/gpx/) ach déantar iad a shábháil i bhformáid éagsúil. Déantar iad seo a shábháil mar chomhaid [XML](/web/xml/) ina bhfuil inneachar na pointí bealaigh agus an fhaisnéis ghaolmhar i gclibeanna struchtúrtha. Toisc gur teanga ghinearálaithe é XML chun sonraí a mhalartú idir feidhmchláir éagsúla, éascaíonn sé seo malartú sonraí LOC le feidhmchláir eile.

## Formáid Comhaid LOC - Sampla

Seo a leanas ceanntásc agus téacs pointe bealaigh amháin ó chomhad LOC. Mar is léir, tá foinse suímh na sonraí san eolas ceanntásca. Tá faisnéis ar nós an `ID` agus sonraí inneachair ghaolmhara a bhaineann leis an bpointe bealaigh sa phointe bealaigh. Ar deireadh, is bailiúchán de luachanna domhanleithead agus domhanleithead é an pointe bealaigh agus an téacs a bhaineann leis an bpointe bealaigh áirithe seo.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Tagairtí

* [TopGraphic EasyGPS](https://www.easygps.com/)


