
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML fails — Microsoft Assistance iezīmēšanas valodas fails",
  "description":"Uzziniet, kas ir AML fails un API, kas var izveidot un atvērt AML failus.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML — Microsoft Assistance iezīmēšanas valodas fails

## Kas ir AML fails?

AML (Assistance Markup Language) fails ir XML fails, kas ģenerēts, izmantojot Microsoft Assistance Markup Language (MAML). To izstrādāja Microsoft, lai nodrošinātu tiešsaistes palīdzību operētājsistēmai Microsoft Windows. Pirms tam Windows palīdzība bija pieejama kompilētā HTML [CHM](/web/chm/) faila formātā. AML faili nodrošina strukturētu dokumentu, kas ļauj lietojumprogrammai izveidot avota kodu un atbalsta lapas. Tas ļauj definēt dokumentus un to elementus pēc to konteksta. AML palīdzības faili tiek publicēti tiešsaistē, un tos var konfigurēt, lai tie tiktu atjaunināti, izmantojot tiešsaistē pieejamos pakotnes atjauninājumus.

## MAML faila struktūra

AML faili, kas ģenerēti, izmantojot MAML, tiek saglabāti kā [XML](/web/xml/) faili, kurus var izmantot, lai izteiktu plašu aktīvo jēdzienu klāstu. Tas var arī nodrošināt vadītu palīdzību (aktīvo satura vedni), kas padara palīdzības failu interaktīvu lietotājam, izmantojot soli pa solim sniegto vedni.

An AML file generated using the MAML follows its authoring structure that can be divided into segments like:

 * Konceptuāls
 * FAQ
 * Glosārijs
 * Procedūra
 * Atsauce
 * Atkārtoti lietojams saturs
 * Uzdevums
 * Traucējummeklēšana un
 * Apmācība

## Kā izveidot MAML failus?

MAML failus var izveidot, izmantojot vienu no šīm metodēm:

 * Izmantojot Sandcastle — palīdzības faila ģenerēšanai izmanto shēmu un programmu izpildāmo failu komplektu. Tomēr šis rīks ir pārtraukts.
 * DocProject izmantošana — Microsoft Visual Studio spraudnis, ko var izpildīt no Microsoft Visual Studio palīdzības satura ģenerēšanai.

MAML failus var izveidot, izmantojot Sandcastle — .XSL shēmu un programmu izpildāmo failu komplektu. Tos var izveidot arī, izmantojot DocProject — Microsoft Visual Studio palīdzības autorēšanas rīka pievienojumprogrammu.

## Atsauces

 * [Izveidot uz XML balstītu palīdzību, izmantojot PlatyPS](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
 * [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML — loka makro valodas fails

## Kas ir ARC Macro AML fails?

AML (ARC Macro Language) fails ir skriptu fails, kas ģenerēts ar ArcInfo Workstation GIS lietojumprogrammu. Tā ir uzrakstīta ARC Macro Language, kas ir patentēta augsta līmeņa algoritmiskā valoda ĢIS lietojumprogrammu izveidei programmā ArcInfo. AML izstrādāja ESRI 1986. gadā, un tas kalpoja lietojumprogrammu izveidei no komandrindas ARCINFO GIS sistēmas. Kā skriptu fails, AML faili var saturēt skriptu komandas, lai veiktu vairākus uzdevumus, piemēram, izveidotu lietotāja interfeisa komponentus un manipulētu ar kartes datiem.

## AML faila formāts — vairāk informācijas

AML, kas ir skriptu faili, saglabā informāciju diskā kā vienkārša teksta failus. Tas seko AML sintaksei, kas balstījās uz PRIMOS operētājsistēmas CPL čaulas valodu. AML valoda ir aizstāta ar ESRI ģeoapstrādes ietvaru, kas ir daļa no ArcGIS komplekta un izmanto ArcObjects, lai nodrošinātu programmēšanas atbalstu, izmantojot VBA vai Python.

## Atsauces

 * [ARC makro valoda](https://en.wikipedia.org/wiki/ARC_Macro_Language)
 * [AML izmantošana ar skriptu rīkiem](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

