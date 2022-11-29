{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Report Definition Language File",
  "keywords" :[ "rdl", "rapportdefinitionsspråk", "XmlTextWriter", "XSD", "RDL-element"],
  "description":"Läs mer om RDL-filformat som är en XML-representation av en rapportdefinition för SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Vad är en RDL fil? ##

RDL (Report Definition Language) är ett riktmärke som satts av Microsoft för att definiera rapporter. En RDL-fil består av ett eller flera RDL-element. Medan ett RDL-element består av dess datatyp och kardinalitet. Ett element kan vara enkelt eller komplext. Det enkla elementet har inga underordnade element eller attribut, medan ett komplext element har underordnade och valfria attribut.

## RDL XML Schema Definition
En XML Schema Definition-fil (XSD) validerar RDL-filen. Schemat definierar reglerna för var RDL-element kan förekomma i en .rdl-fil. Ett RDL-element kan vara enkelt eller komplext. Ett enkelt element har inte underordnade element eller attribut och ett komplext element har underordnade element och eventuellt attribut.

## Skapar RDL
Eftersom RDL är öppet och utbyggbart till sin natur kan många applikationer och verktyg byggas som genererar RDL-filer baserat på dess XML-schema. Ett av de enklaste sätten att skapa RDL från ett program är att använda Microsoft .NET Framework-klasserna i namnutrymmet **System.Xml** och System.Linq-namnutrymmet. Speciellt klassen **XmlTextWriter** kan användas för att skriva RDL. Du kan generera en komplett rapportdefinition från början till slut i alla .NET Framework-program genom att använda **XmlTextWriter**. Utvecklare kan också lägga till anpassade rapportobjekt med anpassade egenskaper för att utöka RDL.

## RDL-typer
Följande tabell listar de typer och attribut som används i RDL-element.

|Typ|Beskrivning|
---|---|
|Binär |En egenskap med ett bas-64-kodat binärt värde.|
|Boolesk| En egenskap med sant eller falskt som värdet på objektet. Om inget annat anges är värdet på ett utelämnat valfritt booleskt objekt False.|
|Datum |En egenskap med ett fullständigt angivet datum- eller datetime-värde specificerat i ISO8601-datumformat: ÅÅÅÅ-MM-DD[THH:MM[:SS[.S]]].|
|Enum |En egenskap med ett strängtextvärde som måste vara ett av en lista med angivna värden.|
|Flott |En fastighet med ett flytande värde. En punkt (.) används som valfri decimalavgränsare.|
|Heltal |En egenskap med ett heltalsvärde (int32).|
|Språk |En egenskap med ett textvärde som innehåller en språk- och kulturkod, till exempel "en-us" för amerikansk engelska. Värdet måste antingen vara ett specifikt språk eller ett neutralt språk för vilket ett standardspråk är definierat i Microsoft .NET Framework.|
|Namn |En egenskap med ett strängtextvärde. Namn måste vara unika inom namnområdet för objektet. Om det inte anges är namnutrymmet för ett objekt det innersta innehållande objektet som har ett namn.|
|NormalizedString |En egenskap med ett strängtextvärde som har normaliserats.|
|Size |Ett storlekselement måste innehålla ett tal (med ett punkttecken som används som valfri decimalavgränsare). Numret måste följas av en beteckning för en CSS-längdenhet som cm, mm, in, pt eller pc. Ett mellanslag mellan numret och beteckningen är valfritt. För mer information om storleksbeteckningar, se CSS-värden och enhetsreferens. I RDL är maxvärdet för storlek 160 tum. Minsta storlek är 0 tum.|
|String |En egenskap med ett strängtextvärde.|
|UnsignedInt |En egenskap med ett osignerat heltalsvärde (uint32).|
|Variant |En egenskap med valfri enkel XML-typ.|

## RDL-datatyper
I RDL definierar DataType Enumeration datatypen för ett attribut, uttryck eller parameter. Följande tabell visar hur CLR-datatyper motsvarar RDL-datatyper.

|CLR-typ(er) |Motsvarande datatyp|
---|---|
|Boolesk| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Heltal|
|Singel, Dubbel |Flytande|
|String, Char, GUID, Timespan |String|


## Referenser ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

