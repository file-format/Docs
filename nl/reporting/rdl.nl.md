{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Rapportdefinitie taalbestand",
  "keywords" :[ "rdl", "rapportdefinitietaal", "XmlTextWriter", "XSD", "RDL-element"],
  "description":"Meer informatie over de RDL-bestandsindeling die een XML-weergave is van een SQL Server Reporting Services-rapportdefinitie.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Wat is een RDL-bestand? ##

De RDL (Report Definition Language) is een benchmark die door Microsoft is ingesteld voor het definiëren van rapporten. Een RDL-bestand bestaat uit één of meerdere RDL-elementen. Terwijl een RDL-element bestaat uit het gegevenstype en de kardinaliteit. Een element kan eenvoudig of complex zijn. Het eenvoudige element heeft geen onderliggende elementen of attributen, terwijl een complex element wel kinderen en optionele attributen heeft.

## RDL XML-schemadefinitie
Een XML Schema Definition (XSD)-bestand valideert het RDL-bestand. Het schema definieert de regels voor waar RDL-elementen kunnen voorkomen in een .rdl-bestand. Een RDL-element kan eenvoudig of complex zijn. Een eenvoudig element heeft geen onderliggende elementen of attributen en een complex element heeft wel kinderen en optioneel attributen.

## RDL maken
Omdat RDL open en uitbreidbaar van aard is, kunnen veel toepassingen en tools worden gebouwd die RDL-bestanden genereren op basis van het XML-schema. Een van de eenvoudigste manieren om RDL van een toepassing te maken, is door de Microsoft .NET Framework-klassen van de naamruimte **System.Xml** en System.Linq te gebruiken. Met name de klasse **XmlTextWriter** kan worden gebruikt om RDL te schrijven. U kunt een volledige rapportdefinitie van begin tot eind genereren in elke .NET Framework-toepassing door **XmlTextWriter** te gebruiken. Ontwikkelaars kunnen ook aangepaste rapportitems met aangepaste eigenschappen toevoegen om de RDL uit te breiden.

## RDL-typen
In de volgende tabel worden de typen en attributen vermeld die in RDL-elementen worden gebruikt.

|Type|Beschrijving|
---|---|
|Binair |Een eigenschap met een base-64 gecodeerde binaire waarde.|
|Booleaans| Een eigenschap met waar of onwaar als de waarde van het object. Tenzij anders aangegeven, is de waarde van een weggelaten optioneel Booleaans object False.|
|Datum |Een eigenschap met een volledig gespecificeerde datum- of datetime-waarde gespecificeerd in ISO8601-datumnotatie: JJJJ-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Een eigenschap met een tekenreekstekstwaarde die moet behoren tot een lijst met aangewezen waarden.|
|Float |Een eigenschap met een float-waarde. Een punt (.) wordt gebruikt als het optionele decimaalteken.|
|Integer |Een eigenschap met een integer (int32) waarde.|
|Taal |Een eigenschap met een tekstwaarde die een taal- en cultuurcode bevat, zoals "en-us" voor Amerikaans Engels. De waarde moet een specifieke taal zijn of een neutrale taal waarvoor een standaardtaal is gedefinieerd in het Microsoft .NET Framework.|
|Name |Een eigenschap met een tekenreekstekstwaarde. Namen moeten uniek zijn binnen de naamruimte van het item. Indien niet gespecificeerd, is de naamruimte voor een item het binnenste bevattende object dat een naam heeft.|
|NormalizedString |Een eigenschap met een tekenreekstekstwaarde die is genormaliseerd.|
|Size |Een size-element moet een getal bevatten (met een punt als optioneel decimaalteken). Het nummer moet worden gevolgd door een aanduiding voor een CSS-lengte-eenheid, zoals cm, mm, in, pt of pc. Een spatie tussen het nummer en de aanduiding is optioneel. Zie CSS-waarden en eenhedenreferentie voor meer informatie over maataanduidingen. In RDL is de maximumwaarde voor Grootte 160 inch. De minimumgrootte is 0 inch.|
|String |Een eigenschap met een tekenreekstekstwaarde.|
|UnsignedInt |Een eigenschap met een unsigned integer (uint32) waarde.|
|Variant |Een eigenschap met elk eenvoudig XML-type.|

## RDL-gegevenstypen
In RDL definieert de DataType Enumeration het gegevenstype van een attribuut, expressie of parameter. De volgende tabel laat zien hoe CLR-gegevenstypen overeenkomen met RDL-gegevenstypen.

|CLR-type(s) |Overeenkomstig gegevenstype|
---|---|
|Booleaans| Booleaans|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Geheel getal|
|Enkel, Dubbel |Float|
|String, Char, GUID, Tijdspanne |String|


## Referenties ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

