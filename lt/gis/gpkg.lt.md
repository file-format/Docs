{
  "date": "2021-07-29",
  "keywords": [
"gpkg failą",
"gpkg failo formatas",
"kas yra gpkg failas",
"failą",
"gpkg pavyzdys",
"gpkg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "GPKG – GeoPackage formato failai",
  "description": "Sužinokite apie GPKG failo formatą ir API, kurios gali kurti ir atidaryti GPKG failus.",
  "linktitle": "GPKG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gpkg"
}
},
  "lastmod": "2021-07-29"
}

## Kas yra GPKG failas?
Failas su plėtiniu .gpkg susideda iš geografinės informacijos sistemos, įdiegtos kaip SQLite duomenų bazės konteineris, kuriame yra duomenų ir metaduomenų lentelės su tipiniais apibrėžimais, formato apribojimais, vientisumo tvirtinimais ir turinio apribojimais. Jis buvo paskelbtas 2014 m.; apibrėžė OGC (Open Geospatial Consortium) JAV kariuomenės vardu. Įvairios vyriausybės, komercinės ir atvirojo kodo organizacijos plačiai palaiko GeoPackage.

## GPKG failo formatas
GeoPackage yra sudarytas kaip išplėstinis SQLite 3 duomenų bazės failas; standartas apibrėžia taisyklių rinkinį (būtinus susitarimus):
- Plytelių matricos vaizdų rinkinių saugojimas
- Vektorinės savybės
- Įvairių mastelių rastriniai žemėlapiai
- Metaduomenys ir schema

GeoPackage galite išplėsti naudodami išplėtimo taisykles, kaip apibrėžta standarto 2.3 punkte. GeoPackage kūrimo tikslas buvo padaryti kuo lengvesnę duomenų bazę ir įtraukti ją į paruoštą naudoti vieną failą. Dėl to jis idealiai tinka mobiliosioms programoms neprisijungus ir greitai bendrinant debesies saugyklą ar USB atmintinę ir kt.

### GPKG turinys
GeoPackages, kaip ir kitose reliacinėse duomenų bazėse, turi daugybę lentelių. Šios lentelės gali būti vartotojo nustatytos arba metaduomenų lentelės. GeoPackages susideda iš dviejų privalomų metaduomenų lentelių:

#### gpkg_contents
GeoPackage turinys. Šios lentelės privalomi stulpeliai:

- **lentelės_pavadinimas**: tikrasis vartotojo apibrėžtos duomenų lentelės pavadinimas;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x ir max_y**: turinio erdviniai mastai. ;
- **srs_id**: erdvinė atskaitos sistema .

#### gpkg_spatial_ref_sys
Erdviniam informaciniam turiniui; įskaitant, bet neapsiribojant, išklotines ir funkcijas, kiekviena turinio eilutė turi nurodyti koordinačių atskaitos sistemą; saugomi **gpkg_spatial_ref_sys** lentelėje. Šios lentelės privalomi stulpeliai:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the tabl-lte;
- **organizacija**: didžiųjų ir mažųjų raidžių neskiriamas organizacijos pavadinimas.
- **organization_coordsys_id**: organizacijos priskirtas skaitmeninis SRS ID;
- **apibrėžimas**: gerai žinomas tekstinis SRS apibrėžimas.


## Nuorodos

* [GeoPackage – Vikipedija](https://en.wikipedia.org/wiki/GeoPackage)

* [Getting Started with GeoPackage](http://www.geopackage.org/guidance/getting-started.html)


