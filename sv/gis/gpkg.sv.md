{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg fil", "gpkg filformat", "vad är en gpkg fil", "fil", "gpkg exempel", "gpkg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage Format Files",
  "description":"Läs mer om GPKG-filformat och API:er som kan skapa och öppna GPKG-filer.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Vad är en GPKG fil?
En fil med filtillägget .gpkg består av ett geografiskt informationssystem implementerat som en SQLite-databasbehållare som innehåller data- och metadatatabeller med typiska definitioner, formatbegränsningar, integritetskrav och innehållsbegränsningar. Den publicerades 2014; definieras av OGC (Open Geospatial Consortium) på uppdrag av den amerikanska militären. Olika regeringar, kommersiella organisationer och organisationer med öppen källkod stöder GeoPackage i stor utsträckning.

## GPKG filformat
Ett GeoPackage är uppbyggt som en utökad SQLite 3-databasfil; en standard definierar en uppsättning regler (obligatoriska konventioner) för:
- Lagring av kakelmatrisuppsättningar av bilder
- Vektorfunktioner
- Rasterkartor i olika skalor
- Metadata och schema

Du kan utöka ett GeoPackage genom att använda förlängningsreglerna som definieras i paragraf 2.3 i standarden. Syftet med att designa ett GeoPackage var att göra en lättviktsdatabas så mycket som möjligt och inkludera den i en färdig att använda enskild fil. Detta gör den idealisk för mobila applikationer i offline-läge och snabb delning på molnlagring eller USB-lagringsenheter, etc.

### GPKG-innehåll
Geopaketen innehåller ett antal tabeller, liksom andra relationsdatabaser. Dessa tabeller kan vara antingen användardefinierade eller metadatatabeller. GeoPackages består av två obligatoriska metadatatabeller:

#### gpkg_contents
En innehållsförteckning för ett GeoPackage. De obligatoriska kolumnerna i denna tabell är:

- **tabellnamn**: det faktiska namnet på den användardefinierade datatabellen;
- **data_type**: datatypen, t.ex. titlar, funktioner och attribut;
- **identifierare och beskrivning**: text som kan läsas av människor;
- **senaste_ändring**: informationsdatumet för senaste ändringen, i ISO 8601-format;
- **min_x, min_y, max_x och max_y**: innehållets rumsliga omfattning. ;
- **srs_id**: rumsligt referenssystem .

#### gpkg_spatial_ref_sys
För rumsligt referensinnehåll; inklusive men inte begränsat till brickor och funktioner, varje rad i innehållet måste referera till ett koordinatreferenssystem; lagras i tabellen **gpkg_spatial_ref_sys**. De obligatoriska kolumnerna i denna tabell är:

- **srs_name, description**: ett mänskligt läsbart namn och beskrivning för SRS;,
- **srs_id**: en unik identifierare för SRS; även den primära nyckeln för tabellen;
- **organisation**: Skiftlägesokänsligt namn på den definierande organisationen.
- **organisation_coordsys_id**: Numeriskt ID för SRS tilldelat av organisationen;
- **definition**: Välkänd textdefinition av SRS.


## Referenser

* [GeoPackage - av Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Komma igång med GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

