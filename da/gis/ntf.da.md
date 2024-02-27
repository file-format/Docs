{
  "date": "2021-07-28",
  "keywords": [
"ntf fil",
"ntf filformat",
"hvad er en ntf-fil",
"fil",
"ntf eksempel",
"ntf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF - National Transfer Format Files",
  "description": "Lær om NTF-filformat og API'er, der kan oprette og åbne NTF-filer.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-daf"
}
},
  "lastmod": "2021-07-28"
}

## Hvad er en NTF fil?
Filerne med filtypenavnet .ntf kaldes **National Transfer Format (NTF)** filer; mest brugt af UK Ordnance Survey (OS); specifikt til overførsel af geospatiale data. Det administreres af British Standards Institution. Det er blevet standardoverførselsformatet for Ordnance Survey digitale data. Det Forenede Kongeriges National Grid-projektion, som er en type Transverse Mercator, indeholder alle de georeferencede oplysninger for NTF-filer.

## NTF filformat
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Dette filformat blev introduceret for at adressere en begrænsning af **PCIDSK** vektorsegment, som kun har ét attributfelt pr. struktur, men der er en række attributter, der kan udtrækkes med vektordata. For at komme rundt er NTF-filformatet konstitueret som to segmenter. Hvert segment består af de samme vektorer, men med forskellige attributter. Det første segment i en NTF-vektorfil indeholder vektorerne med funktionskodenummeret som attribut. Det andet segment indeholder vektorerne med værdien som attribut.

### Koordinatreferencesystem
GDB-biblioteket repræsenterer raster- og vektordata med de passende TM-projektionsegenskaber:

- Referencelængdegrad: 49,0
- Referencebreddegrad: 2.0
- Falsk østing: 400000
- Falsk nording: -100000
- Målestok: 0,9996012717
- Ellipsoide: Airy 1830 (E009)
Ingen support er tilgængelig for opdatering eller skrivning af NTF-filer, og DTM-filerne kan heller ikke linkes til.

### Ogrinfo eksempel
Følgende eksempel bruger **ogrinfo** på en NTF-fil til at hente lagnumre:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referencer

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Web Mapping - Illustreret af Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


