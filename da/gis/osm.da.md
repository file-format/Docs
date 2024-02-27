{
  "date": "2019-10-11",
  "keywords": [
"osm fil",
"hvad er en osm fil",
"fil",
"osm eksempel",
"osm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM - OpenStreetMap-filformat",
  "description": "Lær om OSM-filformat og API'er, der kan oprette og åbne OSM-filer.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-dam"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en OSM fil?

OpenStreetMap (OSM) er en enorm samling af frivillige geografiske informationslagre i forskellige typer filer, der bruger forskellige kodningsskemaer til at konvertere disse data til bits og bytes. OSM er en fælles indsats for at skabe et gratis redigerbart kort over verden. Det primære resultat af denne samarbejdsindsats er geografiske data snarere end selve kortet. Begrænsningerne for brugen eller tilgængeligheden af geografisk information i store dele af verden udløser behovet for at oprette et OSM.

De tilgængelige data fra OSM er klar til at erstatte Google Maps for klassiske applikationer (Facebook, Craigslist osv.) og standarddata til GPS-modtagerens applikationer. Selvom datakvaliteten er forskellig i hele verden, kan OpenStreetMap-data nemt sammenlignes med patentdatakilder.

## Kort historie om OSM-filformat

Inspireret af Wikipedias succes skabte Steve Coast, en britisk iværksætter, i 2004 dette samfundsbaserede verdenskortlægningsprojekt i Storbritannien. Han fokuserede oprindeligt på at kortlægge Storbritannien. OpenStreetMap Foundation blev først etableret i april 2006 for at støtte udviklingen, udvidelsen og cirkulationen af gratis geospatial for enhver. I december 2006 hjalp Yahoo OpenStreetMap med dets luftfotografering til kortproduktion.

Fuldstændige vejdata for Holland og hovedvejsdata for Indien og Kina blev bidraget til OSM i april 2007 af Automotive Navigation Data (AND). I december 2007 var Oxford University den mest fremtrædende organisation, der integrerede OpenStreetMap-data på deres hovedwebsted. Siden da har over 2 millioner registrerede brugere bidraget med data i dette projekt ved hjælp af GPS-enheder, luftfotografering og manuelle undersøgelser. Disse fællesskabsbidragede data er gjort tilgængelige under Open Database-licensen. En England-registreret, non-profit organisation OpenStreetMap Foundation vedligeholdt OSM-webstedet.

## OSM filformat

Der er mange måder og filformater til at gemme geografiske data, men **OSM** filformat er begrænset til OpenStreetMap. OSM er specielt designet standardformat beregnet til at blive transporteret nemt over internettet. Et struktureret ordnet format, kodet i XML, udgør en .osm-fil. I OpenStreetMap er der fire pivotelementer til lagring af topologisk datastruktur:

{{< figure src="../OSM.png" alt="OSM filformat" >}}


|Noder|Vejder|Relationer|Tags
---|---|---|---|
|<ul><li> Repræsenterer geografisk position gemt som par af en breddegrad og en længdegrad.</li><li> Bruges til at repræsentere kortfunktioner uden en størrelse, såsom bjergtoppe.</li></ul> |<ul><li> Sorterede lister over noder, der angiver en polylinje eller en polygon</li><li> Repræsenterer lineære funktioner såsom veje og floder og zoner som parkeringsområders jungler og parker.</li></ul> |<ul><li> Sorterede lister over knudepunkter og veje repræsenterer deres relation som barrierer og u-sving på veje, motorveje spænder over forskellige eksisterende veje og områder med huller.</li></ul> |<ul><li> Gem metadata om kortobjekterne.* Altid knyttet til enhver node, måde eller en relation</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

Tre typer filer bruges af OSM til at gemme dets hoveddata.

OSM håndterer alle disse filer med oplysningerne om deres formateringsdetaljer. Men de samme interne objekter produceres af disse filer. For datafiler er det synlige flag på OSM-objekter altid sandt, hvilket ikke er tilfældet for historik- og ændringsfiler.

I almindelig brug er der en mangfoldighed i OSM-filformater. Filformater definerer indholdskodningen på disk eller ledning i bits og bytes. OSM er i stand til at læse og skrive maksimalt af disse formater.

**XML**

Det originale OSM-format er XML-baseret. Returdataene for OSM-databasens hoved-API er i XML-format.

**PBF**

Protokolbuffere-kodning står på binært format og et af de mest kompakte formater.

**O5M/O5C**

Binært format baseret på enklere format, men relativt mindre brugt. OSM kan læse, men kan ikke skrive dette format.

**OPL**

Et simpelt format foreslået til brug med standard UNIX kommandolinjeværktøjer. Tæt på CSV-filer, tillader én OSM-entitet på én linje.

**FEJLFINDE**

Et tekstbaseret format beregnet til at skabe til fejlretning. OSM kan skrive dette format, men kan ikke læse.

**SORT HUL**

Et dummy-format, der bortskaffer alle data. OSM kan skrive dette format, men kan ikke læse.

## OSM-datalager ##

OSM's vigtigste **PostgreSQL**-database opbevarer hovedkopien af OSM-dataene med PostGIS-udvidelsen. For hver primitiv data vedligeholder hoveddatabasen en tabel, hvis rækker gemmer individuelle objekter. Alle redigeringer opdaterer denne database, og alle andre formater dannes ved hjælp af denne database. Adskillige databasepuljer, der kan downloades, oprettes til at overføre data fra et sted til et andet. To formater, et der bruger XML og et andet der bruger Protocol Buffer Binary Format (PBF) definerer disse puljer. De komplette data gemmes i en fil kaldet planet.osm

## Komprimering i OSM-filer ##

Tekstbaserede formater (XML, OPL og Debug) bruger valgfrit gzip- eller bzip2-komprimering.

## Referencer ##

* [Manual til OSM-filformater](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)

* [Lær OSM](https://learnosm.org/en/osm-data/getting-data/)


