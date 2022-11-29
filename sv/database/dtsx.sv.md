{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DTSX-filformat och API:er som kan skapa och öppna DTSX-filer.",
  "title" :"DTSX File Format - SQL Server DTS Settings File",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Vad är en DTSX fil?

En fil med tillägget .dtsx (Data Transformation Services Package XML) är en Data Transformation Services-fil (DTS) som används av Microsoft SQL för att referera till datamigreringssteg/regler för överföring av data från en databas till en annan. Detta inkluderar transformationerna och eventuella valfria bearbetningssteg som kan krävas under dataöverföringen mellan ursprungs- och destinationspunkten. SQL Server Integration Services (SSIS), en komponent i Microsoft SQL Server, använder DTSX-filerna för att identifiera stegen för bearbetning av data mellan databasservrar. DTSX-filer kan öppnas med Microsoft SQL Server 2019.

## DTSX filformat

Dataöverföring mellan databasservrar kräver regler och bearbetningssteg för att säkerställa dataintegriteten under denna operation. SSIS säkerställer att alla dessa aktiviteter, för att flytta och anpassa data från olika källor i ett företag, sker bekvämt. Det är där DTSX kommer som definierar strukturerna som ska användas av SSIS för att fastställa stegen där data kan behandlas som den följer genom dessa steg.

Dataflödet som beskrivs av DTSX är som visas i följande bild.

{{< figure src="../DataFlowDTSX.png" alt="Dataflöde DTSX" >}}

DTSX är [XML](/sv/web/xml/)-baserat och är dokumenterat i [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). Den förbättrade refactoring av DTSX XML är DTSX 2.0 som inkluderar nya attribut till strukturerna, ersättning av namngivna egenskaper som överordnade XML-attribut, specificerar standardvärden för de flesta attributvärden och placering av upprepade element inuti ett överordnat element. DTSX-strukturer beskrivs med dessa [XML-scheman](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) och är det strukturella formatet celar-text XML.

## Referenser

* [DTSX-format – Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2-format – av Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

