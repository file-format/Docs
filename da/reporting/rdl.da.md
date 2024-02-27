{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL - Report Definition Language File",
  "keywords": [
"rdl",
"rapportdefinitionssprog",
"XmlTextWriter",
"XSD",
"RDL element"
],
  "description": "Lær om RDL-filformat, som er en XML-repræsentation af en SQL Server Reporting Services-rapportdefinition.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-dal"
}
},
  "lastmod": "2021-03-01"
}

## Hvad er en RDL fil? ##

RDL (Report Definition Language) er et benchmark sat af Microsoft til at definere rapporter. En RDL-fil består af et eller flere RDL-elementer. Hvorimod et RDL-element består af dets datatype og kardinalitet. Et element kan være enkelt eller komplekst. Det simple element har ikke nogen underordnet element eller attributter, hvorimod et komplekst element har underordnede og valgfri attributter.

## RDL XML Schema Definition
En XML Schema Definition-fil (XSD) validerer RDL-filen. Skemaet definerer reglerne for, hvor RDL-elementer kan forekomme i en .rdl-fil. Et RDL-element kan være enkelt eller komplekst. Et simpelt element har ikke underordnede elementer eller attributter, og et komplekst element har underordnede elementer og eventuelt attributter.

## Oprettelse af RDL
Da RDL er åben og udvidelsesbar i naturen, kan mange applikationer og værktøjer bygges, der genererer RDL-filer baseret på dets XML-skema. En af de enkleste måder at oprette RDL fra et program på er at bruge Microsoft .NET Framework-klasserne i navneområdet **System.Xml** og System.Linq-navneområdet. Især klassen **XmlTextWriter** kan bruges til at skrive RDL. Du kan generere en komplet rapportdefinition fra start til slut i enhver .NET Framework-applikation ved at bruge **XmlTextWriter**. Udviklere kan også tilføje tilpassede rapportelementer med tilpassede egenskaber for at udvide RDL.

## RDL typer
Følgende tabel viser de typer og attributter, der bruges i RDL-elementer.

|Type|Beskrivelse|
---|---|
|Binær |En egenskab med en base-64-kodet binær værdi.|
|Boolsk| En egenskab med sand eller falsk som værdien af objektet. Medmindre andet er angivet, er værdien af et udeladt valgfrit boolesk objekt False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |En egenskab med en strengtekstværdi, der skal være en af en liste over udpegede værdier.|
|Float |En ejendom med en flydende værdi. Et punktum (.) bruges som valgfri decimalseparator.|
|Heltal |En egenskab med en heltalsværdi (int32).|
|Sprog |En ejendom med en tekstværdi, der indeholder en sprog- og kulturkode, f.eks. en-us for amerikansk engelsk. Værdien skal enten være et specifikt sprog eller et neutralt sprog, for hvilket der er defineret et standardsprog i Microsoft .NET Framework.|
|Navn |En egenskab med en strengtekstværdi. Navne skal være unikke i varens navneområde. Hvis det ikke er angivet, er navneområdet for et element det inderste indeholdende objekt, der har et navn.|
|NormalizedString |En egenskab med en strengtekstværdi, der er blevet normaliseret.|
|Størrelse |Et størrelseselement skal indeholde et tal (med et punktum, der bruges som en valgfri decimalseparator). Tallet skal efterfølges af en betegnelse for en CSS-længdeenhed som cm, mm, in, pt eller pc. Et mellemrum mellem nummeret og betegnelsen er valgfrit. For mere information om størrelsesbetegnelser, se CSS-værdier og enhedsreference. I RDL er den maksimale værdi for størrelse 160 tommer. Minimumsstørrelsen er 0 tommer.|
|String |En egenskab med en strengtekstværdi.|
|UnsignedInt |En egenskab med en værdi uden fortegn (uint32).|
|Variant |En egenskab med enhver simpel XML-type.|

## RDL-datatyper
I RDL definerer DataType Enumeration datatypen for en attribut, et udtryk eller en parameter. Følgende tabel viser, hvordan CLR-datatyper svarer til RDL-datatyper.

|CLR-type(r) |Tilsvarende datatype|
---|---|
|Boolsk| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Heltal|
|Enkelt, Dobbelt |Flåd|
|String, Char, GUID, Timespan |String|


## Referencer ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

