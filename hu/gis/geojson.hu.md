{
  "date" : "2019-10-11",
  "keywords" :[ "geojson fájl", "mi az a geojson fájl", "fájl", "geojson példa", "geojson fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON – JSON alapú földrajzi fájlformátum",
  "description":"További információ a GeoJSON fájlformátumról és az API-król, amelyek képesek létrehozni és megnyitni GeoJSON fájlokat.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GeoJSON fájl?

A GeoJSON egy JSON-alapú formátum, amelyet a földrajzi jellemzők nem térbeli attribútumainak megjelenítésére terveztek. Ez a formátum különböző JSON (JavaScript Object Notation) objektumokat és azok összekapcsolási módját határozza meg. A JSON-formátum a földrajzi jellemzőkről, azok térbeli kiterjedéséről és tulajdonságairól szóló kollektív információt képvisel. Ennek a fájlnak egy objektuma jelezhet geometriát (pont, vonallánc, sokszög), jellemzőt vagy jellemzők gyűjteményét. A funkciók a címeket és helyeket pontok utcáiként, a főutakat és a határokat vonalláncként, az országokat, tartományokat és szárazföldi régiókat pedig sokszögként tükrözik. A GeoJSON használatával különböző mobil útválasztó és navigációs alkalmazások jelezhetik szolgáltatásaik lefedettségét. A GeoJSON kiterjesztése a TopoJSON, amely kisebb méretű és térinformatikai topológiát kódol.

## Rövid története ##

Az Internet Engineering Task Force (IETF) a formátum szerzőivel együttműködve egy [GeoJSON WG-t](https://datatracker.ietf.org/wg/geojson/charter/) alakított ki a GeoJSON 2015 áprilisában történő kiadására. A 2008. GeoJSON specifikáció, [RFC 7946](https://tools.ietf.org/html/rfc7946), a GeoJSON formátum 2016 augusztusában közzétett új szabványos specifikációja.

## GeoJSON fájlformátum ##

### Koordináta ###

A koordináta minden földrajzi adat alapeleme. Ez egyetlen dimenzió (hosszúság, szélesség), amely egyetlen számot jelent (tizedes formátum), és néha a magassági koordinátákat is rögzíti. Az idő is dimenzió, de bonyolultsága megnehezíti a koordinátaként való rögzítését. Mindkét JSON GeoJSON koordinátái számokként vannak formázva.

### Pozíció ###

A koordináták rendezett tömbje képviseli a [pozíciót](http://geojson.org/geojson-spec.html#positions). Ez a legkisebb egység, amely egy pontot jelezhet a Földön.

"[Hosszúsági fok, szélesség, magasság]".

A jelenlegi specifikáció kiadása előtt a GeoJSON pozíciónként három koordinátát rögzített, de az új specifikáció nem teszi lehetővé.

### Geometria ###

A geometriák egyszerű formák (pontok, görbék és felületek) a GeoJSON-ban, amelyek egy típusból és koordináták gyűjteményéből állnak. A pont a legegyszerűbb geometria, amely egyetlen pozíciót reprezentál

`{ "típus": "Pont", "koordináták": [0, 0] }`

### Vonalláncok ###

Egy vonal ábrázolására legalább két összekapcsolt helyet használnak.

`{ "type": "LineString", "koordináták": [[10, 30], [10, 10]] }`

A pont- és vonalláncok a geometria két legegyszerűbb kategóriája. Mindkét típusú geometria nem zavar sok geometriai szabályt. Egy pont bárhol ábrázolható egy helyen, és egy egyenesnek több pontja is lehet, még akkor is, ha a pontok egymást keresztezik.

### Sokszögek ###

A GeoJSON geometriák sokkal összetettebbnek tűnnek a sokszögekben. A sokszögeknek belső és külső területei vannak, és ezeken belül lyukak lehetnek.

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

A LineStrings-hez képest a sokszögekben a koordináták listája még egy szinttel van beágyazva, és lehetnek kivágások, például fánkok.

### Koordináta szint ###

GeoJSON formátumban a koordináta tulajdonság négy mélységi szinttel rendelkezik.

### Jellemzők ###

A geometriák a GeoJSON központi részét képezik, ezért a valós világ adatai többek, mint identitásokkal és attribútumokkal rendelkező egyszerű alakzatok. A jellemzők rögzítik a geometriát és azok tulajdonságait.

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

A jellemző tulajdonságok lehetnek egy típusú [JSON](http://json.org/) objektumok, amelyek egymélységű kulcsérték-leképezéseket tartalmazhatnak.

### FeatureCollection ###

A GeoJSON-fájlok legfelső szintjén a FeatureCollection a leggyakoribb dolog, amely így néz ki:

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

Sok térkép- és térinformatikai szoftvercsomag támogatja a GeoJSON-t, beleértve a GeoDjango-t, az OpenLayers-t és a Geoforge szoftvert. Kompatibilis a PostGIS és a Mapnik programmal is. A Google, a yahoo és a Bing maps API-szolgáltatásai is támogatják a GeoJSON-t.

## Referenciák ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON – a Wikipedia által](https://en.wikipedia.org/wiki/GeoJSON)

