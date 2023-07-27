{
  "date" : "2019-10-11",
  "keywords" :[ "geojson-bestand", "wat is een geojson-bestand", "bestand", "voorbeeld geojson", "geojson-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - op JSON gebaseerd geografisch bestandsformaat",
  "description":"Meer informatie over GeoJSON-bestandsindelingen en API's die GeoJSON-bestanden kunnen maken en openen.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GeoJSON-bestand?

GeoJSON is een op JSON gebaseerd formaat dat is ontworpen om de geografische kenmerken met hun niet-ruimtelijke kenmerken weer te geven. Dit formaat definieert verschillende JSON-objecten (JavaScript Object Notation) en hun verbindingswijze. JSON-indeling vertegenwoordigt een collectieve informatie over de geografische kenmerken, hun ruimtelijke begrenzingen en eigenschappen. Een object van dit bestand kan een geometrie (Punt, LineString, Polygoon), een feature of een verzameling features aangeven. De functies weerspiegelen adressen en plaatsen als straten van punten, hoofdwegen en grenzen als lijnreeksen en landen, provincies en landregio's als polygonen. Met behulp van de GeoJSON kunnen verschillende mobiele routerings- en navigatietoepassingen de dekking van hun diensten aangeven. Een uitbreiding van GeoJSON is TopoJSON die kleiner is en geospatiale topologie codeert.

## Korte geschiedenis ##

De Internet Engineering Task Force (IETF) heeft in samenwerking met de auteurs van het formaat een [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) gevormd om GeoJSON in april 2015 uit te brengen. GeoJSON-specificatie, [RFC 7946](https://tools.ietf.org/html/rfc7946), de nieuwe standaardspecificatie van het GeoJSON-formaat gepubliceerd in augustus 2016.

## GeoJSON-bestandsindeling ##

### Coördinaat ###

Coördinaat is het basiselement van alle geografische gegevens. Dit is een enkele dimensie (lengtegraad, breedtegraad) die een enkel getal (decimaal formaat) vertegenwoordigt en soms ook een coördinaat voor hoogte opneemt. Tijd is ook een dimensie, maar de complexiteit ervan maakt het moeilijk om het als coördinaat vast te leggen. Coördinaten in beide JSON GeoJSON zijn opgemaakt als getallen.

### Positie ###

Een geordende reeks coördinaten vertegenwoordigt de [positie](https://geojson.org/geojson-spec.html#positions). Dit is de kleinste eenheid die een punt op aarde kan aangeven.

`[Lengtegraad, breedtegraad, hoogte]`

Vóór de release van de huidige specificatie stond GeoJSON toe om drie coördinaten per positie vast te leggen, maar dit is niet toegestaan door de nieuwe specificatie.

### Geometrie ###

Geometrieën zijn eenvoudige vormen (punten, krommen en oppervlakken) in GeoJSON die bestaan uit een type en een verzameling coördinaten. Punt is de eenvoudigste geometrie die een enkele positie vertegenwoordigt

`{ "type": "Punt", "coördinaten": [0, 0] }`

### Lijnstrings ###

Er worden ten minste twee verbonden plaatsen gebruikt om een lijn weer te geven.

`{ "type": "LineString", "coördinaten": [[10, 30], [10, 10]] }`

Punt- en lijnstrings zijn de twee eenvoudigste categorieën van geometrie. Beide soorten geometrie storen niet veel geometrische regels. Een punt kan overal op een plaats worden weergegeven en een lijn kan meer dan één punt hebben, zelfs als de punten elkaar kruisen.

### Veelhoeken ###

GeoJSON-geometrieën lijken aanzienlijk complexer in Polygons. Veelhoeken hebben binnen- en buitengebieden en kunnen daar gaten in hebben.

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

In vergelijking met LineStrings, in polygonen, is de lijst met coördinaten nog een niveau genest en kan uitsnijdingen zoals donuts hebben.

### Coördinatenniveau ###

In GeoJSON-indeling zijn er voor de coördinaateigenschap vier diepteniveaus.

### Functies ###

Geometrieën vormen het centrale onderdeel van GeoJSON, daarom zijn de gegevens uit de echte wereld meer dan deze eenvoudige vormen met identiteit en attributen. Kenmerken registreert zowel de geometrie als hun eigenschappen.

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

Eigenschappen van een kenmerk kunnen een type [JSON](http://json.org/)-object zijn dat sleutelwaardetoewijzingen met een enkele diepte bevat.

### FeatureCollection ###

Op het hoogste niveau van GeoJSON-bestanden is FeatureCollection het meest voorkomende dat eruitziet als:

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

Veel kaart- en GIS-softwarepakketten ondersteunen GeoJSON, waaronder GeoDjango-, OpenLayers- en Geoforge-software. Het is ook compatibel met PostGIS en Mapnik. De API-services van Google, Yahoo en Bing Maps ondersteunen ook GeoJSON.

## Referenties ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Door Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

