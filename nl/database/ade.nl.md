{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Microsoft Access"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over ADE-bestandsindelingen en API's die ADE-bestanden kunnen maken en openen.",
  "title" :"ADE - Toegang tot projectextensiebestand",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Wat is een ADE-bestand?

Een bestand met de extensie .ade is een Microsoft Access Project-bestand dat de gecompileerde uitvoer bevat van de informatie in het Microsoft Access ADP-projectbestand. Informatie in het Access-projectbestand, anders dan Visual Basic for Applications (VBA), is in gecompileerde vorm beschikbaar in ADE-bestanden. Gegevens worden in deze bestanden in gecomprimeerde indeling opgeslagen om de bestandsgrootte te verkleinen en de prestaties in Access te verbeteren. Aangezien ADE de gecompileerde uitvoer is van het Access-projectbestand, blijft elke VBA-broncode die deel uitmaakt van het project beschermd door deze geen deel te laten uitmaken van de uitvoer. ADE-bestanden kunnen worden geopend in Microsoft Access 365.

## ADE-bestandsindeling - Meer informatie

ADE zijn gecompileerde Access Database-bestanden die als binaire bestanden op schijf worden opgeslagen. De interne bestandsstructuur van deze bestanden is niet bekend.

De ADE-bestanden kunnen problemen veroorzaken bij het openen op basis van de versie van Microsoft Access die is gebruikt om deze bestanden te maken. Access-databases die gebruikmaken van de 64-bits versie van Microsoft Access 2010 en die zijn gecompileerd als MDE-, [ACCDE](/nl/database/accde/)- of ADE-bestanden, moeten opnieuw worden gecompileerd in Microsoft Access 2021 Service Pack 1 (SP1) om correct werken met Access 2010 SP1. Dit probleem treedt op omdat Access 2010 SP1 een nieuwere versie van het bestand VBE7.dll (versie 7.00.1619) gebruikt.

## Referenties

* [Probleem met Access ADE-bestanden](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Welke toegangsbestandsindelingen moeten worden gebruikt](https://support.microsoft.com/en-us/office/who-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

