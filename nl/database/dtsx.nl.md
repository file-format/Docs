{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DTSX-bestandsindelingen en API's die DTSX-bestanden kunnen maken en openen.",
  "title" :"DTSX-bestandsindeling - SQL Server DTS-instellingenbestand",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Wat is een DTSX-bestand?

Een bestand met de extensie .dtsx (Data Transformation Services Package XML) is een Data Transformation Services (DTS)-bestand dat door Microsoft SQL wordt gebruikt om te verwijzen naar stappen/regels voor gegevensmigratie voor de overdracht van gegevens van de ene database naar de andere. Dit omvat de transformaties en eventuele optionele verwerkingsstappen die nodig kunnen zijn tijdens de gegevensoverdracht tussen de herkomst- en bestemmingspunten. SQL Server Integration Services (SSIS), een onderdeel van Microsoft SQL Server, gebruikt de DTSX-bestanden om de stappen voor het verwerken van gegevens tussen databaseservers te identificeren. DTSX-bestanden kunnen worden geopend met Microsoft SQL Server 2019.

## DTSX-bestandsindeling

Het verplaatsen van gegevens tussen databaseservers vereist regels en verwerkingsstappen om de integriteit van gegevens tijdens deze bewerking te waarborgen. SSIS zorgt ervoor dat al deze activiteiten, om gegevens uit verschillende bronnen in een onderneming te verplaatsen en te conformeren, gemakkelijk kunnen plaatsvinden. Dat is waar DTSX komt dat de structuren definieert die door SSIS moeten worden gebruikt om de stappen vast te stellen waar de gegevens kunnen worden verwerkt, zoals door deze stappen wordt gevolgd.

De gegevensstroom die door DTSX wordt beschreven, is zoals weergegeven in de volgende afbeelding.

{{< figure src="../DataFlowDTSX.png" alt="Gegevensstroom DTSX" >}}

DTSX is gebaseerd op [XML](/nl/web/xml/) en is gedocumenteerd in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). De verbeterde refactoring van DTSX XML is DTSX 2.0 dat nieuwe attributen voor de structuren omvat, vervanging van benoemde eigenschappen als bovenliggende XML-attributen, standaardwaarden specificeert voor de meeste attribuutwaarden en plaatsing van herhaalde elementen binnen een bovenliggend element. DTSX-structuren worden beschreven met behulp van deze [XML-schema's](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) en het structurele formaat is celar-tekst XML.

## Referenties

* [DTSX-indeling - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2-indeling - door Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

