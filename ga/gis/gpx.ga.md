{
  "date": "2019-10-11",
  "keywords": [
"comhad gpx",
"Cad is comhad gpx ann",
"comhad",
"sampla gpx",
"Síneadh comhad gpx",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX - Formáid Chomhaid Mhalartaithe GPX",
  "description": "Foghlaim faoi fhormáid comhaid GPX agus APIanna ar féidir leo comhaid GPX a chruthú agus a oscailt.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad GPX ann?

Is ionann comhaid le síneadh GPX agus formáid GPS Exchange chun sonraí GPS a idirmhalartú idir feidhmchláir agus seirbhísí gréasáin ar an idirlíon. Is formáid comhaid XML éadrom-mheáchan é ina bhfuil sonraí GPS ie pointí bealaigh, bealaí agus rianta le hiompórtáil agus dearg le cláir iolracha. Tá formáid comhaid GPX oscailte agus tacaithe ag feidhmchláir éagsúla agus gléasanna GPS. Is féidir sonraí GPS ó chomhaid den sórt sin a luchtú lena thaispeáint ar fheidhmchláir mhapála chun críocha geospásúla.

## Formáid Chomhaid GPX ##

Tá comhad GPX comhdhéanta de shonraí suímh domhanleithead agus domhanfhad, luachanna ardaithe agus faisnéis thuairisciúil eile a d’fhéadfadh a bheith ann. Cuirtear sonraí suímh in iúl mar chéimeanna deachúla agus cuirtear an t-ingearchló in iúl i méadair. Tá an t-am i gcomhad GPX san Am Comhordaithe Uilíoch (UTC) ag baint úsáide as formáid ISO 8601. Seo a leanas na buntáistí a bhaineann le comhad GPX a úsáid:

* Ligeann GPX duit sonraí a mhalartú le liosta clár atá ag dul i méid do Windows, MacOS, Linux, Palm, agus PocketPC.

* Is féidir GPX a chlaochlú go formáidí comhaid eile trí úsáid a bhaint as leathanach gréasáin simplí nó clár tiontaire.

* Tá GPX bunaithe ar an gcaighdeán XML, mar sin is féidir le go leor de na cláir nua a úsáideann tú (Microsoft Excel, mar shampla) comhaid GPX a léamh.

* Déanann GPX éasca é do dhuine ar bith ar an ngréasán gnéithe nua a fhorbairt a oibreoidh láithreach leis na cláir is fearr leat.


Taispeánann an [GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) an léiriú do fhormáid comhaid GPX le haghaidh tagartha.

### Sonraí Riachtanach ###

Seo a leanas sonraí riachtanacha atá mar chuid de chomhad GPX chun sonraí GPS a léiriú.

* **Pointe bealaigh**: Is ionann bealachphointe agus comhordanáidí WGS84 (GPS) de phointe agus seasann sé do shraith gnéithe den chineál OGR wkbPoint

* **Bealaí**: Léiríonn sraith gnéithe de chineál OGR wkbLineString. Cuimsíonn sé liosta de rianphointí, ar pointí bealaigh iad a thaispeánann cas nó pointí céime a leanann ceann scríbe

* ** Rianta**: Is ionann rianta agus sraith gnéithe de chineál OGR wkbMultiLineString. Tá sé déanta de mhír amháin ar a laghad ina bhfuil pointí bealaigh i liosta ordaithe pointí a chuireann síos ar chosán. Is éard atá ann liosta pointí rian a léiríonn rian leanúnach GPS.


### Comhad Samplach GPX ###

Taispeánann an comhad GPX seo a leanas eagrú sonraí GPS i gcomhad GPX agus féadann sé smaoineamh maith a thabhairt ar a bhfuil i gcomhad GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Tagairtí ##

* [Formáid Comhaid GPX](https://www.topografix.com/gpx.asp)

* [GPX - Le Vicipéid](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


