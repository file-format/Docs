
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML-fil - Microsoft Assistance Markup Language File",
  "description":"Lær om, hvad en AML-fil og API'er er, der kan oprette og åbne AML-filer.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft Assistance Markup Language File

## Hvad er en AML fil?

En AML-fil (Assistance Markup Language) er en XML-fil, der er genereret med Microsoft Assistance Markup Language (MAML). Det blev udviklet af Microsoft for at give online hjælp til Microsoft Windows OS. Før dette var Windows-hjælp tilgængelig i det kompilerede HTML-filformat [CHM](/web/chm/). AML-filer giver et struktureret dokument, der lader applikationen oprette kildekode og understøttende hjælpesider. Dette gør det muligt at definere dokumenter og deres bestanddele ud fra deres kontekst. AML-hjælpefilerne udgives online og kan konfigureres til at blive opdateret fra de pakkeopdateringer, der er tilgængelige online.

## MAML filstruktur

AML-filer, der er genereret ved hjælp af MAML, gemmes som [XML](/web/xml/)-filer, der kan bruges til at udtrykke en bred vifte af aktive koncepter. Det kan også give guidet hjælp (guiden til aktivt indhold), der gør hjælpefilen interaktiv for brugeren med en trin-for-trin guide.

An AML file generated using the MAML follows its authoring structure that can be divided into segments like:

 * Konceptuel
 * FAQ
 * Ordliste
 * Procedure
 * Reference
 * Genanvendeligt indhold
 * Opgave
 * Fejlfinding, og
 * Tutorial

## Hvordan opretter man MAML-filer?

MAML-filer kan oprettes ved hjælp af en af følgende metoder:

 * Brug af Sandcastle - Bruger en række skemaer og programeksekverbare filer til at generere hjælpefilen. Dette værktøj er dog udgået.
 * Brug af DocProject - Et Microsoft Visual Studio-plugin, der kan udføres fra Microsoft Visual Studio til generering af hjælpeindholdet.

MAML-filer kan oprettes ved hjælp af Sandcastle, en suite af .XSL-skemaer og eksekverbare programmer. De kan også oprettes ved hjælp af DocProject, et tilføjelsesprogram til Microsoft Visual Studio-hjælpeværktøj.

## Referencer

 * [Opret XML-baseret hjælp ved hjælp af PlatyPS](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
 * [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc Macro Language File

## Hvad er en ARC Macro AML-fil?

En AML-fil (ARC Macro Language) er en scriptfil, der er genereret med ArcInfo Workstation GIS-applikationen. Det er skrevet i ARC Macro Language, som er et proprietært algoritmisk sprog på højt niveau til oprettelse af GIS-applikationer i ArcInfo. AML blev designet af ESRI i 1986 og tjente det formål at skabe applikationer fra deres kommandolinje ARCINFO GIS-system. Som scripting-fil kan AML-filer indeholde script-kommandoer til at udføre en række opgaver, såsom oprettelse af brugergrænsefladekomponenter og manipulation af kortdata.

## AML-filformat - flere oplysninger

AML, som er scriptfiler, gemmer oplysningerne på disken som almindelige tekstfiler. Det følger AML-syntaksen, der var baseret på CPL-skalsproget i PRIMOS-operativsystemet. AML-sproget er blevet erstattet af ESRIs geoprocessing-ramme, der er en del af ArcGIS-pakken og bruger ArcObjects til at levere programmeringsunderstøttelse via VBA eller Python.

## Referencer

 * [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
 * [Brug af AML med scriptværktøjer](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

