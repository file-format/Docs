{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "wat is een cd-bestand", "hoe een cd-bestand te openen", "extensie", "bestand", "cd-bestand", "cd-bestandsformaat", "cd-bestandsextensie" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio Class Diagram-bestand",
  "description":"Meer informatie over cd-bestandsindeling en API's die cd-bestanden kunnen maken en openen.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Wat is een CD-bestand?

Een bestand met de extensie .cd is een Visual Studio-klassediagrambestand dat informatie geeft over de structuur en relatie tussen alle klassen in de huidige oplossing. Een Visual Studio-oplossing (weergegeven door [.sln](/nl/programming/sln/)) kan een of meer projecten bevatten, elk met meerdere verschillende klassen. Het klassendiagrambestand kan worden gegenereerd door met de rechtermuisknop op het project te klikken en de optie klassendiagram te selecteren.

## Klassendiagram (.cd) Bestandsformaat - Meer informatie

Een klassediagrambestand wordt opgeslagen in een standaard XML-bestandsformaat dat klassen in een project vertegenwoordigt als XML-knooppunten. Als Visual Studio niet beschikbaar is, kunnen deze klassendiagrambestanden worden geopend in elk toepassingsprogramma dat het openen van XML-bestanden ondersteunt.

### Klassendiagrammen toevoegen aan Visual Studio Project

Open in Visual Studio de oplossing/het project waarvoor u het klassendiagram wilt toevoegen. Klik vervolgens met de rechtermuisknop op het projectknooppunt en kies vervolgens Toevoegen > Nieuw item. Of druk op Ctrl+Shift+A.

* Het dialoogvenster Nieuw item toevoegen wordt geopend.

* Vouw Algemene items > Algemeen uit en selecteer vervolgens Klassediagram in de lijst met sjablonen. Kijk voor Visual C++-projecten in de categorie Hulpprogramma's om de sjabloon voor klassendiagrammen te vinden.

### Klassendiagrammen (CD) exporteren naar afbeeldingen

Visual Studio maakt het mogelijk om klassendiagrammen te converteren/exporteren naar afbeeldingen zoals [PNG](/nl/image/png/), [JPEG](/nl/image/jpeg/) en [BMP](/nl/image/bmp/). Deze geëxporteerde klassendiagrambestanden kunnen worden gebruikt voor het bijhouden van documentatie en technische datapakketten (TDP). Om een klassendiagram naar een afbeelding te converteren, kunnen de volgende stappen worden gebruikt vanuit Microsoft Visual Studio.

1. Open uw klassendiagrambestand (.cd).
1. Kies in het menu Klassendiagram of het snelmenu voor diagramoppervlak de optie Diagram exporteren als afbeelding.
1. Selecteer een diagram.
1. Selecteer het gewenste formaat.
1. Kies Exporteren om het exporteren te voltooien.

## Referenties

* [Ontwerplessen in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

