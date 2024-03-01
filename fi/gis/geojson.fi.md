{
  "date": "2019-10-11",
  "keywords": [
"geojson tiedosto",
"mikä on geojson-tiedosto",
"tiedosto",
"geojson esimerkki",
"geojson tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON – JSON-pohjainen maantieteellinen tiedostomuoto",
  "description": "Opi GeoJSON-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GeoJSON-tiedostoja.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-fin"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GeoJSON-tiedosto?

GeoJSON on JSON-pohjainen muoto, joka on suunniteltu edustamaan maantieteellisiä piirteitä niiden ei-tilaominaisuuksilla. Tämä muoto määrittelee erilaiset JSON-objektit (JavaScript Object Notation) ja niiden liitostavat. JSON-muoto edustaa kollektiivista tietoa maantieteellisistä ominaisuuksista, niiden alueellisista ulottuvuuksista ja ominaisuuksista. Tämän tiedoston objekti voi osoittaa geometrian (piste, viivajono, monikulmio), ominaisuuden tai piirteiden kokoelman. Ominaisuudet heijastavat osoitteita ja paikkoja pisteen katuina, pääteitä ja rajoja viivajonoina ja maat, maakunnat ja maa-alueet polygoneina. GeoJSONin avulla erilaiset mobiilireititys- ja navigointisovellukset voivat ilmoittaa palveluidensa kattavuuden. GeoJSONin laajennus on TopoJSON, joka on kooltaan pienempi ja joka koodaa geospatiaalista topologiaa.

## Lyhyt historia ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON-tiedostomuoto ##

### Koordinaatit ###

Koordinaatti on minkä tahansa maantieteellisen tiedon peruselementti. Tämä on yksittäinen mitta (pituusaste, leveysaste), joka edustaa yhtä numeroa (desimaalimuoto) ja tallentaa joskus myös korkeuden koordinaatin. Aika on myös ulottuvuus, mutta sen monimutkaisuus vaikeuttaa sen tallentamista koordinaatiksi. Molempien JSON GeoJSONin koordinaatit on muotoiltu numeroiksi.

### Asema ###

Järjestetty koordinaattijoukko edustaa {{HYPERLINKKI}}. Tämä on pienin yksikkö, joka voi osoittaa pisteen maan päällä.

[Pituusaste, leveysaste, korkeus].

Ennen nykyisen määrityksen julkaisua GeoJSON salli kolmen koordinaatin tallentamisen sijaintia kohti, mutta uusi spesifikaatio ei salli sitä.

### Geometria ###

Geometriat ovat yksinkertaisia muotoja (pisteitä, käyriä ja pintoja) GeoJSONissa, jotka koostuvat tyypistä ja joukosta koordinaatteja. Piste on yksinkertaisin geometria, joka edustaa yhtä sijaintia

`{ tyyppi: Piste, koordinaatit: [0, 0] }`

### LineStrings ###

Vähintään kahta yhdistettyä kohtaa käytetään edustamaan viivaa.

`{ tyyppi: LineString, koordinaatit: [[10, 30], [10, 10]] }`

Piste- ja viivajonot ovat kaksi yksinkertaisinta geometrian luokkaa. Molemmat geometriatyypit eivät häiritse monia geometrisia sääntöjä. Piste voidaan esittää missä tahansa paikassa, ja suoralla voi olla useampi kuin yksi piste, vaikka pisteet ylittäisivät itsensä.

### Monikulmiot ###

GeoJSON-geometriat näyttävät huomattavasti monimutkaisemmilta polygoneissa. Monikulmioilla on sisä- ja ulkoalueet, ja niissä voi olla reikiä.

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

Verrattuna LineStringsiin, monikulmioissa koordinaattiluettelo on yhden tason sisäkkäisempi, ja siinä voi olla leikkauksia, kuten munkkeja.

### Koordinaattitaso ###

GeoJSON-muodossa koordinaattiominaisuutta varten on neljä syvyystasoa.

### Ominaisuudet ###

Geometriat ovat GeoJSONin keskeinen osa, joten reaalimaailman data on enemmän kuin yksinkertaisia muotoja, joilla on identiteetti ja attribuutit. Ominaisuudet tallentavat geometrian sekä niiden ominaisuudet.

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

Ominaisuuden ominaisuudet voivat olla tyyppi [JSON](http://json.org/), joka sisältää yhden syvyysavaimen arvomappauksia.

### FeatureCollection ###

GeoJSON-tiedostojen ylimmällä tasolla FeatureCollection on yleisin asia, joka näyttää tältä:

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

Monet kartoitus- ja GIS-ohjelmistopaketit tukevat GeoJSONia, mukaan lukien GeoDjango-, OpenLayers- ja Geoforge-ohjelmistot. Se on myös yhteensopiva PostGIS:n ja Mapnikin kanssa. Myös Googlen, yahoo- ja Bing-karttojen API-palvelut tukevat GeoJSONia.

## Viitteet ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON – Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)


