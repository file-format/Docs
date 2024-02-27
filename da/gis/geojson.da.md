{
  "date": "2019-10-11",
  "keywords": [
"geojson fil",
"hvad er en geojson fil",
"fil",
"geojson eksempel",
"geojson filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GeoJSON - JSON-baseret geografisk filformat",
  "description": "Lær om GeoJSON filformat og API'er, der kan oprette og åbne GeoJSON filer.",
  "linktitle": "GeoJSON",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-geojso-dan"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GeoJSON fil?

GeoJSON er et JSON-baseret format designet til at repræsentere de geografiske funktioner med deres ikke-rumlige attributter. Dette format definerer forskellige JSON-objekter (JavaScript Object Notation) og deres sammenføjningsmåde. JSON-format repræsenterer en samlet information om de geografiske funktioner, deres rumlige udstrækning og egenskaber. Et objekt i denne fil kan angive en geometri (Point, LineString, Polygon), en funktion eller en samling af funktioner. Funktionerne afspejler adresser og steder som punkts gader, hovedveje og grænser som linjestrenge og lande, provinser og landområder som polygoner. Ved at bruge GeoJSON kan forskellige mobile routing- og navigationsapplikationer angive dækningen af deres tjenester. En udvidelse af GeoJSON er TopoJSON, der er mindre i størrelse og koder for geospatial topologi.

## Kort historie ##

The Internet Engineering Task Force (IETF), in association with the format authors, shaped a [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) to release GeoJSON in April 2015. Replacing the 2008 GeoJSON specification, [RFC 7946](https://tools.ietf.org/html/rfc7946), the new standard specification of the GeoJSON format published in August 2016.

## GeoJSON filformat ##

### Koordinat ###

Koordinat er det grundlæggende element i alle geografiske data. Dette er en enkelt dimension (længdegrad, breddegrad), der repræsenterer et enkelt tal (decimalformat) og registrerer nogle gange også en koordinat for højden. Tid er også en dimension, men dens kompleksitet gør det vanskeligt at registrere den som koordinat. Koordinater i begge JSON GeoJSON er formateret som tal.

### Position ###

En ordnet matrix af koordinater repræsenterer [position](https://geojson.org/geojson-spec.html#positions). Dette er den mindste enhed, der kan angive et punkt på jorden.

`[Længdegrad, breddegrad, højde]`

Før udgivelsen af den nuværende specifikation tillod GeoJSON at registrere tre koordinater pr. position, men er ikke tilladt af den nye specifikation.

### Geometri ###

Geometrier er simple former (punkter, kurver og overflader) i GeoJSON, som består af en type og en samling koordinater. Punkt er den enkleste geometri, der repræsenterer en enkelt position

`{ type: Punkt, koordinater: [0, 0] }`

### LineStrings ###

Mindst to forbundne steder bruges til at repræsentere en linje.

`{ type: Linjestreng, koordinater: [[10, 30], [10, 10]] }`

Punkt- og linjestrenge er de to enkleste kategorier af geometri. Begge typer geometri generer ikke mange geometriske regler. Et punkt kan være repræsenteret et sted hvor som helst, og en linje kan have mere end ét punkt, selvom punkterne krydser sig selv.

### Polygoner ###

GeoJSON-geometrier virker væsentligt mere komplekse i polygoner. Polygoner har inder- og yderområder og kan have huller i det indvendige.

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

Sammenlignet med LineStrings er listen over koordinater i polygoner et niveau mere indlejret og kan have udskæringer som donuts.

### Koordinatniveau ###

I GeoJSON-format er der fire dybdeniveauer for koordinategenskaben.

### Funktioner ###

Geometrier er den centrale del af GeoJSON, derfor er data fra den virkelige verden mere end disse simple former med identitet og attributter. Features registrerer geometrien såvel som deres egenskaber.

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

En funktionsegenskaber kan være en type [JSON](http://json.org/)-objekt indeholdende enkelt-dybde nøgleværditilknytninger.

### FeatureCollection ###

På det øverste niveau af GeoJSON-filer er FeatureCollection den mest almindelige ting, der ser ud som:

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

En masse kort- og GIS-softwarepakker understøtter GeoJSON inklusive GeoDjango, OpenLayers og Geoforge-software. Den er også kompatibel med PostGIS og Mapnik. API-tjenesterne fra Google, yahoo og Bing maps understøtter også GeoJSON.

## Referencer ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)

* [GeoJSON - af Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)


