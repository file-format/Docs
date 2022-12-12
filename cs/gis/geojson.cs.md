{
  "date" : "2019-10-11",
  "keywords" :[ "soubor geojson", "co je soubor geojson", "soubor", "příklad geojson", "přípona souboru geojson","přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON – formát geografického souboru založený na JSON",
  "description":"Další informace o formátu souborů GeoJSON a rozhraních API, která mohou vytvářet a otevírat soubory GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GeoJSON?

GeoJSON je formát založený na JSON navržený tak, aby reprezentoval geografické prvky s jejich neprostorovými atributy. Tento formát definuje různé objekty JSON (JavaScript Object Notation) a způsob jejich spojování. Formát JSON představuje souhrnné informace o geografických prvcích, jejich prostorovém rozsahu a vlastnostech. Objekt tohoto souboru může označovat geometrii (Bod, LineString, Polygon), prvek nebo kolekci prvků. Prvky odrážejí adresy a místa jako ulice bodů, hlavní silnice a hranice jako řetězce čar a země, provincie a zemské oblasti jako polygony. Pomocí GeoJSON mohou různé mobilní směrovací a navigační aplikace indikovat pokrytí jejich služeb. Rozšířením GeoJSON je TopoJSON, který je menší velikosti a kóduje geoprostorovou topologii.

## Stručná historie ##

The Internet Engineering Task Force (IETF) ve spolupráci s autory formátu vytvořila [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/), aby vydala GeoJSON v dubnu 2015. Nahrazuje 2008 Specifikace GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), nová standardní specifikace formátu GeoJSON zveřejněná v srpnu 2016.

## Formát souboru GeoJSON ##

### Souřadnice ###

Souřadnice jsou základním prvkem všech geografických dat. Jedná se o jeden rozměr (zeměpisná délka, zeměpisná šířka) představující jedno číslo (desetinný formát) a někdy zaznamenává i souřadnice pro nadmořskou výšku. Čas je také dimenze, ale kvůli jeho složitosti je obtížné jej zaznamenat jako souřadnice. Souřadnice v obou JSON GeoJSON jsou formátovány jako čísla.

### Pozice ###

Uspořádané pole souřadnic představuje [pozice](http://geojson.org/geojson-spec.html#positions). Jedná se o nejmenší jednotku, která může označovat bod na Zemi.

`[Zeměpisná délka, šířka, nadmořská výška]`

Před vydáním aktuální specifikace umožňoval GeoJSON zaznamenávat tři souřadnice na pozici, ale nová specifikace to neumožňuje.

### Geometrie ###

Geometrie jsou jednoduché tvary (body, křivky a povrchy) v GeoJSON, které se skládají z typu a kolekce souřadnic. Bod je nejjednodušší geometrie, která představuje jednu pozici

`{ "type": "Bod", "souřadnice": [0, 0] }`

### LineStrings ###

Pro znázornění čáry se používají alespoň dvě spojená místa.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Bodové a čárové řetězce jsou dvě nejjednodušší kategorie geometrie. Oba typy geometrie mnoho geometrických pravidel netrápí. Bod může být reprezentován na místě kdekoli a čára může mít více než jeden bod, i když se body kříží.

### Polygony ###

Geometrie GeoJSON se v Polygonech zdají výrazně složitější. Polygony mají vnitřní a vnější oblasti a mohou mít v nich díry.

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

Ve srovnání s LineStrings je v polygonech seznam souřadnic vnořený o jednu úroveň navíc a může mít výřezy jako koblihy.

### Úroveň souřadnic ###

Ve formátu GeoJSON jsou pro vlastnost souřadnic čtyři úrovně hloubky.

### Funkce ###

Geometrie jsou ústřední částí GeoJSON, proto jsou data v reálném světě více než tyto jednoduché tvary s identitou a atributy. Prvky zaznamenávají geometrii i jejich vlastnosti.

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

Vlastnosti prvku mohou být typu objektu [JSON](http://json.org/) obsahujícího mapování hodnot klíče s jednou hloubkou.

### FeatureCollection ###

Na nejvyšší úrovni souborů GeoJSON je FeatureCollection nejběžnější věc, která vypadá takto:

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

Mnoho mapových a GIS softwarových balíků podporuje GeoJSON včetně GeoDjango, OpenLayers a Geoforge. Je také kompatibilní s PostGIS a Mapnik. API služby Google, yahoo a mapy Bing také podporují GeoJSON.

## Reference ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON – z Wikipedie](https://en.wikipedia.org/wiki/GeoJSON)

