{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg-bestand", "gpkg-bestandsformaat", "wat is een gpkg-bestand", "bestand", "gpkg-voorbeeld", "gpkg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Bestanden in GeoPackage-indeling",
  "description":"Meer informatie over GPKG-bestandsindelingen en API's die GPKG-bestanden kunnen maken en openen.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Wat is een GPKG-bestand?
Een bestand met de extensie .gpkg bestaat uit een geografisch informatiesysteem dat is geïmplementeerd als een SQLite-databasecontainer met gegevens- en metadatatabellen met typische definities, formaatbeperkingen, integriteitsverklaringen en inhoudsbeperkingen. Het werd gepubliceerd in 2014; gedefinieerd door het OGC (Open Geospatial Consortium) namens het Amerikaanse leger. Diverse overheden, commerciële en open source organisaties ondersteunen het GeoPackage breed.

## GPKG-bestandsindeling
Een GeoPackage is samengesteld als een uitgebreid SQLite 3-databasebestand; een standaard definieert een reeks regels (vereiste conventies) voor:
- Opslaan van tegelmatrixsets met afbeeldingen
- Vectorfuncties
- Rasterkaarten op verschillende schalen
- Metadata en schema

U kunt een GeoPackage uitbreiden door gebruik te maken van de uitbreidingsregels zoals gedefinieerd in artikel 2.3 van de standaard. Het doel van het ontwerpen van een GeoPackage was om zoveel mogelijk een lichtgewicht database te maken en deze in een kant-en-klaar enkelvoudig bestand op te nemen. Dit maakt het ideaal voor mobiele toepassingen in offline modus en snel delen op cloudopslag of USB-opslagapparaten, enz.

### GPKG-inhoud
De GeoPackages bevatten, net als andere relationele databases, een aantal tabellen. Deze tabellen kunnen door de gebruiker gedefinieerde tabellen of metagegevenstabellen zijn. GeoPackages bestaan uit twee verplichte metadatatabellen:

#### gpkg_contents
Een inhoudsopgave voor een GeoPackage. De verplichte kolommen in deze tabel zijn:

- **tabelnaam**: de werkelijke naam van de door de gebruiker gedefinieerde gegevenstabel;
- **data_type**: het datatype, bijv. titels, kenmerken en attributen;
- **identificatie en omschrijving**: door mensen leesbare tekst;
- **last_change**: de informatieve datum van de laatste wijziging, in ISO 8601-formaat;
- **min_x, min_y, max_x en max_y**: de ruimtelijke omvang van de inhoud. ;
- **srs_id**: ruimtelijk referentiesysteem.

#### gpkg_spatial_ref_sys
Voor ruimtelijke referentie-inhoud; inclusief maar niet beperkt tot tegels en elementen, moet elke rij in de inhoud verwijzen naar een coördinatenreferentiesysteem; opgeslagen in de tabel **gpkg_spatial_ref_sys**. De verplichte kolommen in deze tabel zijn:

- **srs_name, description**: een voor mensen leesbare naam en beschrijving voor de SRS;
- **srs_id**: een unieke identificatie voor de SRS; ook de primaire sleutel voor de tabel;
- **organisatie**: hoofdletterongevoelige naam van de definiërende organisatie.
- **organization_coordsys_id**: numerieke ID van de SRS die door de organisatie is toegewezen;
- **definitie**: bekende tekstdefinitie van de SRS.


## Referenties

* [GeoPackage - door Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Aan de slag met GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

