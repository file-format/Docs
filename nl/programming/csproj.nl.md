{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Meer informatie over CSPROJ-bestandsindeling en API's die CSPROJ-bestanden kunnen maken en openen.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Wat is een CSProj-bestand?
Bestanden met de extensie CSPROJ vertegenwoordigen een C#-projectbestand dat de lijst met bestanden bevat die in een project zijn opgenomen, samen met de verwijzingen naar systeemassemblages. Wanneer een nieuw project wordt gestart in Microsoft VIiual Studio, krijgt u één .csproj-bestand samen met het hoofdoplossingsbestand ([.sln](/nl/programming/sln/)). Als er meer dan één assemblage in een project is, zal er ook een gelijk aantal projectbestanden zijn waar het .sln-bestand ze allemaal samenbindt als onderdeel van het project. De inhoud van dit bestand definieert alle vereisten die nodig zijn om het project te bouwen, zoals de inhoud die moet worden opgenomen, de platformvereisten, versie-informatie, webserver- of databaseserverinstellingen en de taken die moeten worden uitgevoerd. De inhoud van een projectbestand is gerangschikt in XML-bestandsformaat en kan in elke teksteditor worden geopend om te bewerken en te bekijken. Het geeft ook een logisch overzicht van de projectbestanden voor een goede ordening.

## CSPROJ-bestandsindeling #

Ontwikkelaars kunnen zelf projectbestanden maken en het [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx) respecteren. Door de open en transparante structuur van projectbestanden kunnen applicatieontwikkelaars geavanceerde en fijnmazige controle opleggen over hoe de projecten worden gebouwd en geïmplementeerd. De inhoud van zo'n projectdossier heeft een heel duidelijke onderlinge relatie. De volgende figuur toont de belangrijkste elementen en de relatie daartussen voor een dergelijk projectdossier.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

De volgende paragrafen werken de bestandsformaatelementen voor een projectbestand uit.

### Projectelement ###

Het element [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) is het hoofdelement van elk projectbestand. Het identificeert het XML-schema voor het projectbestand en kan attributen bevatten om de toegangspunten voor het bouwproces te specificeren.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Eigenschappen en voorwaarden

Eigenschappen vertegenwoordigen de nodige informatie die nodig is om een project te bouwen. Dergelijke eigenschappen worden gedefinieerd in een [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) element. Deze eigenschappen bestaan uit sleutel-waardeparen waarbij de naam van het eigenschapselement de eigenschapssleutel definieert en de inhoud van het element de eigenschapswaarde definieert. U kunt bijvoorbeeld eigenschappen met de naam ServerName en ConnectionString definiëren om een statische servernaam en verbindingsreeks op te slaan.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Via elementen kunnen voorwaarden worden gespecificeerd om de criteria voor de beoordeling van het element te specificeren. Dit wordt gespecificeerd door het voorwaardewoord bij het definiëren van de eigenschap zoals hieronder weergegeven:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Wanneer MSBuild deze eigenschapsdefinitie verwerkt, wordt eerst gecontroleerd of een **$(OutputRoot)** eigenschapswaarde beschikbaar is. Als de eigenschapswaarde leeg is, met andere woorden, de gebruiker heeft geen waarde voor deze eigenschap opgegeven, wordt de voorwaarde geëvalueerd als **true** en wordt de eigenschapswaarde ingesteld op **..\Publish\Out.**

### Artikelen en Artikelgroepen

Een projectbestand definieert invoer voor het bouwproces die in feite verschillende bestandstypen zijn. In de MSBuild-nomenclatuur worden deze invoer vertegenwoordigd door Item-elementen en gedefinieerd in een [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) -element. Net als **Property**-elementen, kunt u een **Item**-element een naam geven zoals u dat wilt. U moet echter een **Include**-kenmerk opgeven om het bestand of jokerteken te identificeren dat het item vertegenwoordigt.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Doelen en taken

Een [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) element vertegenwoordigt een individuele bouwinstructie (of taak). MSBuild bevat een groot aantal vooraf gedefinieerde taken. Bijvoorbeeld:

* De taak **Kopiëren** kopieert bestanden naar een nieuwe locatie.
* De **Csc**-taak roept de Visual C#-compiler aan.
* De taak **Vbc** roept de Visual Basic-compiler op.
* De **Exec** taak voert een gespecificeerd programma uit.
* De taak **Bericht** schrijft een bericht naar een logger.

Taken moeten altijd binnen [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elementen vallen. Een **Target**-element is een set van een of meer taken die opeenvolgend worden uitgevoerd, en een projectbestand kan meerdere doelen bevatten.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referenties

* [Het projectbestand begrijpen - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

