
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML-fil - Microsoft Assistance Markup Language File",
  "description":"Läs mer om vad som är en AML-fil och API:er som kan skapa och öppna AML-filer.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft Assistance Markup Language File

## Vad är AML fil?

En AML-fil (Assistance Markup Language) är en XML-fil som genereras med Microsoft Assistance Markup Language (MAML). Det utvecklades av Microsoft för att tillhandahålla onlinehjälp för Microsoft Windows OS. Innan detta var Windows-hjälpen tillgänglig i det kompilerade HTML-filformatet [CHM](/sv/web/chm/). AML-filer tillhandahåller ett strukturerat dokument som låter programmet skapa källkod och stödjande hjälpsidor. Detta gör det möjligt att definiera dokument och deras beståndsdelar utifrån deras sammanhang. AML-hjälpfilerna publiceras online och kan konfigureras för att uppdateras från de paketuppdateringar som finns tillgängliga online.

## MAML-filstruktur

AML-filer som genereras med MAML sparas som [XML](/sv/web/xml/)-filer som kan användas för att uttrycka ett brett utbud av aktiva koncept. Den kan också ge guidad hjälp (guiden för aktivt innehåll) som gör hjälpfilen interaktiv för användaren med en steg-för-steg-guide.

En AML-fil som genereras med MAML följer dess författarstruktur som kan delas in i segment som:

* Konceptuell
* FAQ
* Ordlista
* Procedur
* Referens
* Återanvändbart innehåll
* Uppgift
* Felsökning och
* Handledning

## Hur skapar man MAML-filer?

MAML-filer kan skapas med någon av följande metoder:

* Använda Sandcastle - Använder en uppsättning scheman och programkörbara filer för att generera hjälpfilen. Detta verktyg har dock upphört.
* Använda DocProject - Ett Microsoft Visual Studio-plugin som kan köras inifrån Microsoft Visual Studio för att generera hjälpinnehållet.

MAML-filer kan skapas med Sandcastle, en svit av .XSL-scheman och programkörbara filer. De kan också skapas med hjälp av DocProject, ett Microsoft Visual Studio-hjälpförfattarverktyg.

## Referenser

* [Skapa XML-baserad hjälp med PlatyPS
](https://docs.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc Macro Language File

## Vad är en ARC Macro AML-fil?

En AML-fil (ARC Macro Language) är en skriptfil som genereras med ArcInfo Workstation GIS-applikationen. Det är skrivet i ARC Macro Language, som är ett proprietärt algoritmiskt språk på hög nivå för att skapa GIS-applikationer i ArcInfo. AML designades av ESRI 1986 och tjänade syftet att skapa applikationer från deras kommandorads ARCINFO GIS-system. Som skriptfil kan AML-filer innehålla skriptkommandon för att utföra ett antal uppgifter som att skapa användargränssnittskomponenter och manipulera kartdata.

## AML-filformat - Mer information

AML, som är skriptfiler, sparar informationen på skivan som vanliga textfiler. Den följer AML-syntaxen som baserades på CPL-skalspråket i PRIMOS-operativsystemet. AML-språket har ersatts av ESRI:s geoprocessing-ramverk som är en del av ArcGIS-sviten och använder ArcObjects för att tillhandahålla programmeringsstöd via VBA eller Python.

## Referenser

* [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [Använda AML med skriptverktyg](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

