{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "bestand", "extensie", "bestandsformaat", "VB-projectbestand", "Programmeergids"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Meer informatie over VBPROJ-bestandsindelingen en API's die VBPROJ-bestanden kunnen maken en openen.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een VBPROJ-bestand?

Een bestand met de extensie .vbproj is een Microsoft Visual Basic-projectbestand dat door de MSBuild-engine van Microsoft wordt gebruikt om de projecten binnen een Visual Studio-oplossing te bouwen. Het is vergelijkbaar met het [CSPROJ](/nl/programming/csproj/)-bestand voor .NET-projecten geschreven in [C#](/nl/programming/cs/). De MSBuild-engine leest informatie in verschillende groepen uit de VBPROJ-bestanden en genereert het uitvoerbestand. Een VBPROJ-bestand kan informatie bevatten met betrekking tot globale id's, klassen en eigenschappen die het project definiëren. VBPROJ-bestanden kunnen worden geopend en bewerkt met Microsoft Visual Studio en elke gewone teksteditor zoals Kladblok op Windows- en MacOS-besturingssystemen.

## VBPROJ-bestandsindeling - Meer informatie

VBPROJ-bestanden zijn tekstbestanden die zijn geschreven in de bestandsindeling [XML](/nl/web/xml/) op basis van het [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). Een VBPROJ-bestand bevat informatie in de vorm van XML-tags die informatie definiëren met betrekking tot die specifieke groep instellingen. Het wordt ten zeerste aanbevolen om deze instellingsbestanden te openen en te bewerken in Microsoft Visual Studio IDE.

### VBPROJ-elementen

De samenstellende elementen van een VB-instellingenbestand zijn zoals weergegeven in de volgende afbeelding.

{{< figure src="../vbproj.png" alt="VBPROJ-bestandsindeling" >}}

De volgende tabel geeft een korte beschrijving van deze elementen.

|Element|Beschrijving|
---|---|
|Project| Rootelement van elk projectbestand en kan attributen bevatten om de toegangspunten voor het bouwproces te specificeren, naast het identificeren van XML-schema voor het projectbestand |
|Eigenschappen en voorwaarden| Eigenschappen bestaan uit sleutel-waardeparen en worden gedefinieerd met een PropertyGroup-element. De naam van het eigenschapselement vertegenwoordigt de eigenschapssleutel en de inhoud van het element definieert de eigenschapswaarde.|
|Items en ItemGroups|Items in een projectbestand zijn invoer voor het bouwproces, zoals bestanden-codebestanden, configuratiebestanden, opdrachtbestanden en andere die nodig zijn als onderdeel van het bouwproces. Items zijn en moeten worden gedefinieerd binnen een ItemGroup-element.|
|Doelen en taken| Een taakelement vertegenwoordigt een individuele bouwinstructie (of taak). MSBuild bevat een groot aantal vooraf gedefinieerde taken zoals kopiëren, CSC, VBC, Exec. Taken moeten altijd zijn opgenomen in een `Target` Element dat een set van een of meer taken is die opeenvolgend worden uitgevoerd, en een projectbestand kan meerdere doelen bevatten.|

## Referenties

* [Het projectbestand begrijpen](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild-schema-elementen](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

