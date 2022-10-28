{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DTSX-Dateiformat und APIs, die DTSX-Dateien erstellen und öffnen können.",
  "title" :"DTSX-Dateiformat - SQL Server DTS-Einstellungsdatei",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine DTSX-Datei?

Eine Datei mit der Erweiterung .dtsx (Data Transformation Services Package XML) ist eine Data Transformation Services (DTS)-Datei, die von Microsoft SQL verwendet wird, um auf Datenmigrationsschritte/-regeln für die Übertragung von Daten von einer Datenbank in eine andere zu verweisen. Dies umfasst die Transformationen und alle optionalen Verarbeitungsschritte, die während der Datenübertragung zwischen den Ursprungs- und Zielpunkten erforderlich sein können. SQL Server Integration Services (SSIS), eine Komponente von Microsoft SQL Server, verwendet die DTSX-Dateien, um die Schritte zur Verarbeitung von Daten zwischen Datenbankservern zu identifizieren. DTSX-Dateien können mit Microsoft SQL Server 2019 geöffnet werden.

## DTSX-Dateiformat

Die Datenbewegung zwischen Datenbankservern erfordert Regeln und Verarbeitungsschritte, um die Integrität der Daten während dieses Vorgangs sicherzustellen. SSIS stellt sicher, dass all diese Aktivitäten zum Verschieben und Angleichen von Daten aus verschiedenen Quellen in einem Unternehmen bequem stattfinden. An dieser Stelle kommt DTSX, das die von SSIS zu verwendenden Strukturen definiert, um die Schritte festzulegen, in denen die Daten verarbeitet werden können, während diese Schritte durchlaufen werden.

Der von DTSX beschriebene Datenfluss ist wie in der folgenden Abbildung dargestellt.

{{< figure src="../DataFlowDTSX.png" alt="Datenfluss DTSX" >}}

DTSX basiert auf [XML](/de/web/xml/) und ist dokumentiert in [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). Das erweiterte Refactoring von DTSX XML ist DTSX 2.0, das neue Attribute für die Strukturen, das Ersetzen benannter Eigenschaften als übergeordnete XML-Attribute, das Festlegen von Standardwerten für die meisten Attributwerte und das Platzieren wiederholter Elemente innerhalb eines übergeordneten Elements enthält. DTSX-Strukturen werden unter Verwendung dieser [XML-Schemas](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) beschrieben, und das Strukturformat ist Celar-Text-XML.

## Verweise

* [DTSX-Format – Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2-Format – von Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

