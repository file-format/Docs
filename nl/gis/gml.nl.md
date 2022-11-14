{
  "date" : "2019-10-11",
  "keywords" :[ "gml-bestand", "wat is een gml-bestand", "bestand", "gml-voorbeeld", "gml-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Geografie Markup Language File Format",
  "description":"Meer informatie over de GML-bestandsindeling en API's die GML-bestanden kunnen maken en openen.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GML-bestand?

GML staat voor Geography Markup Language en is gebaseerd op XML-specificaties die zijn ontwikkeld door het Open Geospatial Consortium (OGC). Het formaat wordt gebruikt om geografische gegevenskenmerken op te slaan voor uitwisseling tussen verschillende bestandsindelingen. Het dient als een modelleertaal voor geografische systemen en als een open uitwisselingsformaat voor geografische transacties op internet.

## GML-bestandsindeling ##

Zoals bij de meeste op XML gebaseerde grammatica's, bestaat de grammatica uit twee delen: het schema dat het document beschrijft en het instantiedocument dat de feitelijke gegevens bevat. Een GML-document wordt beschreven met behulp van een GML-schema. Hierdoor kunnen gebruikers en ontwikkelaars generieke geografische datasets beschrijven die punten, lijnen en polygonen bevatten. Met toepassingsschema's kunnen gebruikers verwijzen naar wegen, snelwegen en bruggen in plaats van naar punten, lijnen en polygonen.

Het is vermeldenswaard dat GML niet moet worden geïnterpreteerd voor de weergave van ruimtelijke gegevens op kaarten. De weergave van GML-inhoud is anders dan het doel waarvoor GML is gemaakt. Kort gezegd, GML is vergelijkbaar met XML in die zin dat het alleen wordt gebruikt voor het bewaren van de ruimtelijke inhoud die kan worden gebruikt door toewijzingstoepassingen voor weergavedoeleinden.

### Inhoudsvorming in GML ###

GML vertegenwoordigt ruimtelijke gegevens met behulp van functies, een lijst met eigenschappen en geometrieën. Een Property heeft een naam, type en waardebeschrijving. Geometrieën zijn samengesteld uit basisgeometrie-bouwstenen, zoals:

* punten
* lijnen
* bochten
* oppervlakten en
* veelhoeken

De toekomstige versies van GML zijn gepland om zowel 3D-geometrie als topologische relaties tussen objecten te ondersteunen.

GML-codering maakt al behoorlijk complexe functies mogelijk. Een kenmerk kan bijvoorbeeld zijn samengesteld uit andere kenmerken. Een enkel kenmerk, zoals een luchthaven, kan dus worden samengesteld uit andere kenmerken, zoals taxibanen, start- en landingsbanen, hangers en luchthaventerminals. De geometrie van een geografisch kenmerk kan ook uit vele geometrische elementen bestaan. Een geometrisch complex kenmerk kan dus bestaan uit een mix van soorten geometrie, waaronder punten, lijnstrings en polygonen.

### Voorbeelden ###

GML 1.0 en 2.0 coderen objecten Polygons, Points en LineString als volgt:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referenties ##

* [GML-specificaties](http://www.opengeospatial.org/standards/gml)
* [GML - Door Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

