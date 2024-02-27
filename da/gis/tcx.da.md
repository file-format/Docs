{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX-filformat- Training Center XML-fil",
  "description":"Lær om TCX-filformat og API'er, der kan oprette og åbne TCX-filer.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-da",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Hvad er en TCX fil?

En TCX-fil (Training Center XML) er et dataudvekslingsformat, der bruges til at dele data mellem fitnessenheder. Det blev introduceret i 2008 med Garmins Training Center-produkt. Træningsdata såsom puls, løbekadence, cykelkadence, kalorier og omgangstid gemmes i formatet [XML](/web/xml/) i TCX-filen. Derudover er oversigtsdata om træningssporet også inkluderet i TCX-filen. TCX-filer ligner [FIT](/gis/fit/)-filer, der er oprettet med Garmin-sportsbærbare enheder.

## TCX-filformat - Mere information

TCX-filer gemmes på disken som XML-filer med hver post gemt som en aktivitet. En aktivitet omfatter alle data for en træning, såsom tid, omgangstid, id, puls, intensitet, kadence og sporoplysninger, der indeholder positionsparrene sammen med tidsstemplet for den lat-lange position svarende til [GPX](/gis/gpx/) filer.

### TCX filformatversioner

Der er to versioner af dette format med deres egne XML-skemaer hostet af Garmin. Følgende er nogle af dem:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX dataprotokol

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referencer ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


