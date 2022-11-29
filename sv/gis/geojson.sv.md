{
  "date" : "2019-10-11",
  "keywords" :[ "geojson fil", "vad är en geojson fil", "fil", "geojson exempel", "geojson filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - JSON-baserat geografiskt filformat",
  "description":"Läs mer om GeoJSON-filformat och API:er som kan skapa och öppna GeoJSON-filer.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en GeoJSON fil?

GeoJSON är ett JSON-baserat format designat för att representera de geografiska egenskaperna med deras icke-spatiala attribut. Det här formatet definierar olika JSON-objekt (JavaScript Object Notation) och deras sätt att sammanfoga dem. JSON-formatet representerar en samlad information om de geografiska funktionerna, deras rumsliga omfattning och egenskaper. Ett objekt i denna fil kan indikera en geometri (Point, LineString, Polygon), en egenskap eller en samling av funktioner. Funktionerna återspeglar adresser och platser som punktens gator, huvudvägar och gränser som linjesträngar och länder, provinser och landområden som polygoner. Med hjälp av GeoJSON kan olika mobila routing- och navigeringsapplikationer indikera täckningen för deras tjänster. En förlängning av GeoJSON är TopoJSON som är mindre i storlek och kodar för geospatial topologi.

## Kortfattad bakgrund ##

Internet Engineering Task Force (IETF), i samarbete med formatförfattarna, formade en [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) för att släppa GeoJSON i april 2015. Ersätter 2008 GeoJSON-specifikation, [RFC 7946](https://tools.ietf.org/html/rfc7946), den nya standardspecifikationen för GeoJSON-formatet publicerad i augusti 2016.

## GeoJSON filformat ##

### Samordna ###

Koordinat är grundelementet i alla geografiska data. Detta är en enstaka dimension (longitud, latitud) som representerar ett enda tal (decimalformat) och ibland registrerar även en koordinat för höjd. Tid är också en dimension men dess komplexitet gör det svårt att registrera den som koordinat. Koordinater i båda JSON GeoJSON är formaterade som siffror.

### Position ###

En ordnad matris av koordinater representerar [positionen](http://geojson.org/geojson-spec.html#positions). Detta är den minsta enheten som kan indikera en punkt på jorden.

`[Longitud, latitud, höjd]`

Innan den nuvarande specifikationen släpptes tillät GeoJSON att spela in tre koordinater per position men tillåts inte av den nya specifikationen.

### Geometri ###

Geometrier är enkla former (punkter, kurvor och ytor) i GeoJSON som består av en typ och en samling koordinater. Punkt är den enklaste geometrin som representerar en enda position

`{ "type": "Punkt", "koordinater": [0, 0] }`

### LineStrings ###

Minst två sammankopplade platser används för att representera en linje.

`{ "type": "Linsträng", "koordinater": [[10, 30], [10, 10]] }`

Punkt- och linjesträngar är de två enklaste kategorierna av geometri. Båda typerna av geometri stör inte många geometriska regler. En punkt kan representeras på en plats var som helst, och en linje kan ha mer än en punkt, även om punkterna är självkorsande.

### Polygoner ###

GeoJSON-geometrier verkar betydligt mer komplexa i polygoner. Polygoner har områden på insidan och utsidan och kan ha hål på insidan.

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

Jämfört med LineStrings, i polygoner, är koordinatlistan ytterligare en nivå kapslad och kan ha utskärningar som munkar.

### Koordinatnivå ###

I GeoJSON-format, för koordinategenskapen, finns det fyra nivåer av djup.

### Funktioner ###

Geometrier är den centrala delen av GeoJSON, därför är den verkliga världens data mer än dessa enkla former med identitet och attribut. Funktioner registrerar geometrin såväl som deras egenskaper.

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

En egenskapsegenskaper kan vara en typ av [JSON](http://json.org/)-objekt som innehåller nyckelvärdesmappningar på ett djup.

### FeatureCollection ###

På den översta nivån av GeoJSON-filer är FeatureCollection det vanligaste som ser ut så här:

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

Många kart- och GIS-mjukvarupaket stöder GeoJSON inklusive programvaran GeoDjango, OpenLayers och Geoforge. Den är även kompatibel med PostGIS och Mapnik. API-tjänsterna från Google, Yahoo och Bing maps stöder också GeoJSON.

## Referenser ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - av Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

