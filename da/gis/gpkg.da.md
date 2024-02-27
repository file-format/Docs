{
  "date": "2021-07-29",
  "keywords": [
"gpkg fil",
"gpkg filformat",
"hvad er en gpkg fil",
"fil",
"gpkg eksempel",
"gpkg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG - GeoPackage Format Filer",
  "description": "Lær om GPKG filformat og API'er, der kan oprette og åbne GPKG filer.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## Hvad er en GPKG fil?
En fil med filtypenavnet .gpkg består af et geografisk informationssystem implementeret som en SQLite-databasecontainer, der indeholder data- og metadatatabeller med typiske definitioner, formatbegrænsninger, integritetspåstande og indholdsbegrænsninger. Den blev udgivet i 2014; defineret af OGC (Open Geospatial Consortium) på vegne af det amerikanske militær. Forskellige regeringer, kommercielle og open source-organisationer støtter i vid udstrækning GeoPackage.

## GPKG filformat
En GeoPackage er lavet som en udvidet SQLite 3-databasefil; en standard definerer et sæt regler (påkrævede konventioner) for:
- Lagring af billedmateriale til matrixsæt
- Vektorfunktioner
- Rasterkort i forskellige skalaer
- Metadata og skema

Du kan udvide en GeoPackage ved at bruge udvidelsesreglerne som defineret i paragraf 2.3 i standarden. Formålet med at designe en GeoPackage var at lave en letvægtsdatabase så meget som muligt og inkludere den i en klar-til-brug enkelt fil. Dette gør den ideel til mobile applikationer i offline-tilstand og hurtig deling på skylager eller USB-lagerenheder osv.

### GPKG-indhold
GeoPackages indeholder en række tabeller, ligesom andre relationelle databaser. Disse tabeller kan enten være brugerdefinerede eller metadatatabeller. GeoPackages består af to obligatoriske metadatatabeller:

#### gpkg_contents
En indholdsfortegnelse for en GeoPackage. De obligatoriske kolonner i denne tabel er:

- **table_name**: det faktiske navn på den brugerdefinerede datatabel;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x og max_y**: indholdets rumlige udstrækning. ;
- **srs_id**: rumligt referencesystem .

#### gpkg_spatial_ref_sys
For rumligt referenceindhold; inklusive, men ikke begrænset til fliser og funktioner, skal hver række i indholdet referere til et koordinatreferencesystem; gemt i tabellen **gpkg_spatial_ref_sys**. De obligatoriske kolonner i denne tabel er:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-dae;
- **organisation**: Navn på den definerende organisation, der ikke skelner mellem store og små bogstaver.
- **organization_coordsys_id**: Numerisk ID for SRS tildelt af organisationen;
- **definition**: Velkendt tekstdefinition af SRS.


## Referencer

* [GeoPackage - af Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)

* [Kom godt i gang med GeoPackage](http://www.geopackage.org/guidance/getting-started.html)


