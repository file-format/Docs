{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"fil",
"udvidelse",
"filformat",
"Microsoft Excel makrofil",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en XLM-makrofil og API'er er, der kan oprette og åbne XLM-filer.",
  "title": "Hvad er en XLM fil?",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-dam"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en XLM fil?

XLM, for Excel Macro, er en type regnearksfiler, der bruges til at gemme makroer. Fra applikationssynspunkt er en makro et sæt instruktioner, der bruges til at automatisere processer. En makro bruges til at registrere de trin, der udføres gentagne gange for filformatet [XLS](/spreadsheet/xls/) og letter udførelsen af handlingerne ved at køre makroen igen. Makroer programmeres med Microsofts Visual Basic for Applications (VBA) fra Excel-projektmappen ved hjælp af Visual Basic Editor og kan køres/fejlfindes direkte derfra.

## Kort historie ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 optog makroer i VBA som standard, men med version 5.0 var XLM-optagelse stadig tilladt som en mulighed. Efter version 5.0 blev denne mulighed afbrudt. Alle versioner af Excel, inklusive Excel 2010, er i stand til at køre en XLM-makro, selvom Microsoft fraråder deres brug.

## Optagelse af en makro i XLM ##

Excel giver brugervenlige trin til optagelse af en makro. Det kræver, at du har udviklerværktøjer installeret for at kunne arbejde med makroer. Når først en makrooptagelse er i gang, optager den hver brugerhandling for at blive afspillet senere. Makrooptagelse involverer faktisk alle de trin, en bruger udfører, efter at optagelsen starter. Således, hvis du gør en celles indhold fed, kursiv og indstiller dens tekstbegrundelse, efter at en makrooptagelse er startet, vil alle disse kommandoer blive optaget. Hver optaget makro kan også tildeles en genvej til hurtig afspilning senere. Makrooptagelse genererer VBA-kode i form af en makro, der kan redigeres ved hjælp af Visual Basic Editor (VBE).

## Excel-objektmodel ##

Makroer bruger VBA-rutiner på bagsiden og følger [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) til dette formål. Denne model identificerer objekterne i et regneark til interaktion med regnearket gennem brugerdefinerede kommandoværktøjslinjer, kommandolinjer eller meddelelsesbokse. For eksempel gives adgang til projektmappens egenskaber med projektmappeobjektet. På samme måde er der et regnearksobjekt i modellen til at arbejde med regnearkene i projektmappen programmatisk.

## Makroer og sikkerhed ##

VBA giver adgang til alle applikationsområder såvel som filsystemer og kan også være farligt. Dette giver anledning til bekymring, når du deler projektmappe med en person, der kan køre filen i sin ende. Det vil sige, at Microsoft Excel advarer om at åbne sådan en fil. Makroer kan certificeres med en digital signatur, så andre brugere kan verificere, at disse er troværdige. Makroer kan således aktiveres efter verificering af deres kilde.

## Referencer ##

* [[MS-XLS] - Excel Binær filformatstruktur](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [Makroprogrammering](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)


