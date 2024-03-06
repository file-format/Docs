{
  "date": "2021-07-29",
  "keywords": [
"gpkg failu",
"gpkg faila formātā",
"kas ir gpkg fails",
"failu",
"gpkg piemērs",
"gpkg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG — ģeogrāfiskās pakotnes formāta faili",
  "description": "Uzziniet par GPKG faila formātu un API, kas var izveidot un atvērt GPKG failus.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## Kas ir GPKG fails?
Fails ar paplašinājumu .gpkg sastāv no ģeogrāfiskās informācijas sistēmas, kas ieviesta kā SQLite datu bāzes konteiners, kurā ir datu un metadatu tabulas ar tipiskām definīcijām, formātu ierobežojumiem, integritātes apgalvojumiem un satura ierobežojumiem. Tas tika publicēts 2014. gadā; ASV militāro spēku vārdā noteicis OGC (Open Geospatial Consortium). Dažādas valdības, komerciālas un atvērtā pirmkoda organizācijas plaši atbalsta ĢeoPackage.

## GPKG faila formāts
GeoPackage ir izveidots kā paplašināts SQLite 3 datu bāzes fails; standarts definē noteikumu kopumu (vajadzīgās konvencijas):
- Flīžu matricu attēlu kopu glabāšana
- Vektoru funkcijas
- Rastra kartes dažādos mērogos
- Metadati un shēma

Ģeopaku var paplašināt, izmantojot paplašinājuma noteikumus, kas definēti standarta 2.3. punktā. GeoPackage izstrādes mērķis bija pēc iespējas izveidot vieglu datubāzi un iekļaut to lietošanai gatavā vienā failā. Tas padara to ideāli piemērotu mobilajām lietojumprogrammām bezsaistes režīmā un ātrai kopīgošanai mākoņkrātuvē vai USB atmiņas ierīcēs utt.

### GPKG saturs
Ģeopaketes, tāpat kā citas relāciju datu bāzes, satur vairākas tabulas. Šīs tabulas var būt lietotāja definētas vai metadatu tabulas. GeoPackages sastāv no divām obligātajām metadatu tabulām:

#### gpkg_contents
Geopackage satura rādītājs. Šīs tabulas obligātās slejas ir:

- **table_name**: lietotāja definētās datu tabulas faktiskais nosaukums;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x un max_y**: satura telpiskais apjoms. ;
- **srs_id**: telpiskā atsauces sistēma .

#### gpkg_spatial_ref_sys
Telpiskajam atsauces saturam; tostarp, bet ne tikai, elementi un elementi, katrai satura rindai jāatsaucas uz koordinātu atskaites sistēmu; tiek saglabāti tabulā **gpkg_spatial_ref_sys**. Šīs tabulas obligātās slejas ir:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-lve;
- **organizācija**: definējošās organizācijas nosaukums bez reģistrjutīga.
- **organization_coordsys_id**: organizācijas piešķirtais VID ciparu ID;
- **definīcija**: labi zināma VID teksta definīcija.


## Atsauces

* [GeoPackage — Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)

* [Getting Started with GeoPackage](http://www.geopackage.org/guidance/getting-started.html)


