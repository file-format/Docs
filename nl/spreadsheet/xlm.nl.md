{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "bestand", "extensie", "bestandsindeling", "Microsoft Excel-macrobestand", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een XLM-macrobestand is en API's die XLM-bestanden kunnen maken en openen.",
  "title" :"Wat is een XLM-bestand?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een XLM-bestand?

XLM, voor Excel Macro, is een soort spreadsheetbestanden die worden gebruikt om macro's op te slaan. Vanuit het oogpunt van de toepassing is een macro een set instructies die worden gebruikt voor het automatiseren van processen. Een macro wordt gebruikt om de stappen vast te leggen die herhaaldelijk worden uitgevoerd voor de bestandsindeling [XLS](/nl/spreadsheet/xls/) en vergemakkelijkt het uitvoeren van de acties door de macro opnieuw uit te voeren. Macro's worden geprogrammeerd met Microsoft's Visual Basic for Applications (VBA) vanuit de Excel-werkmap met behulp van de Visual Basic Editor en kunnen direct vanaf daar worden uitgevoerd/foutopsporing.

## Korte geschiedenis ##

Microsoft Excel ondersteunde het programmeren van macro's sinds de eerste openbare lancering. De functies van macro's bleven hetzelfde door latere versies van Excel met extensie volgens nieuwe functies. XLM was de standaard macrotaal voor Excel tot en met Excel 4.0. Excel 5.0 nam macro's standaard op in VBA, maar met versie 5.0 was XLM-opname nog steeds als optie toegestaan. Na versie 5.0 werd die optie stopgezet. Alle versies van Excel, inclusief Excel 2010 kunnen een XLM-macro uitvoeren, hoewel Microsoft het gebruik ervan ontmoedigt.

## Een macro opnemen in XLM ##

Excel biedt eenvoudig te gebruiken stappen voor het opnemen van een macro. Het vereist dat u ontwikkelaarstools hebt geïnstalleerd om met macro's te kunnen werken. Zodra een macro-opname aan de gang is, wordt elke gebruikersactie opgenomen om later af te spelen. Macro-opname omvat eigenlijk alle stappen die een gebruiker uitvoert nadat de opname is gestart. Dus als u de inhoud van een cel vet of cursief maakt en de tekstuitvulling instelt nadat een macro-opname is gestart, worden al deze opdrachten opgenomen. Aan elke opgenomen macro kan ook een snelkoppeling worden toegewezen om later snel af te spelen. Macro-opname genereert VBA-code in de vorm van een macro die kan worden bewerkt met behulp van de Visual Basic Editor (VBE).

## Excel-objectmodel ##

Macro's gebruiken VBA-routines op hun rug en volgen hiervoor het [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Dit model identificeert de objecten van een spreadsheet voor interactie met de spreadsheet via door de gebruiker gedefinieerde opdrachtwerkbalken, opdrachtbalken of berichtenvensters. Toegang tot de eigenschappen van de werkmap wordt bijvoorbeeld verleend met het object Workbook. Evenzo is er een werkbladobject in het model om programmatisch met de werkbladen van de werkmap te werken.

## Macro's en beveiliging ##

VBA geeft toegang tot alle toepassingsgebieden en het bestandssysteem en kan ook gevaarlijk zijn. Dit geeft aanleiding tot bezorgdheid bij het delen van een werkmap met iemand die het bestand aan zijn kant kan uitvoeren. Dat wil zeggen dat Microsoft Excel waarschuwt voor het openen van zo'n bestand. Macro's kunnen worden gecertificeerd met een digitale handtekening zodat andere gebruikers kunnen controleren of deze betrouwbaar zijn. Zo kunnen macro's worden ingeschakeld na verificatie van hun bron.

## Referenties ##

* [[MS-XLS] - Excel binaire bestandsindelingsstructuur](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Macro-programmering](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

