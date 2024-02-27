{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DTSX filformat og API'er, der kan oprette og åbne DTSX filer.",
  "title": "DTSX-filformat - SQL Server DTS-indstillingsfil",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-dax"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er en DTSX fil?

En fil med .dtsx (Data Transformation Services Package XML) filtypenavn er en Data Transformation Services (DTS) fil, der bruges af Microsoft SQL til at henvise til datamigreringstrin/regler for overførsel af data fra en database til en anden. Dette inkluderer transformationerne og eventuelle valgfri behandlingstrin, der kan være nødvendige under dataoverførslen mellem oprindelses- og destinationspunktet. SQL Server Integration Services (SSIS), en komponent i Microsoft SQL Server, bruger DTSX-filerne til at identificere trinene til behandling af data mellem databaseservere. DTSX-filer kan åbnes med Microsoft SQL Server 2019.

## DTSX filformat

Databevægelse mellem databaseservere kræver regler og behandlingstrin for at sikre dataintegriteten under denne operation. SSIS sikrer, at alle disse aktiviteter, for at flytte og tilpasse data fra forskellige kilder i en virksomhed, finder sted bekvemt. Det er her DTSX kommer, der definerer de strukturer, der skal bruges af SSIS til at etablere de trin, hvor dataene kan behandles, som de følger gennem disse trin.

Datastrømmen beskrevet af DTSX er som vist i det følgende billede.

{{< figure src="../DataFlowDTSX.png" alt="Dataflow DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## Referencer

 * [DTSX-format - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2-format - af Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

