{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER-bestand - ASP.NET Master Page-bestandsindeling",
  "description" :"Leer meer over het MASTER-bestandsformaat en API's om MASTER-bestanden te maken en te openen.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Wat is een MASTER-bestand?

Een MASTER-bestand is een hoofdwebpaginasjabloonbestand gemaakt met ASP.NET. Het wordt gebruikt als uitgangspunt voor het maken van meerdere pagina's met dezelfde lay-out en instellingen als het MASTER-bestand. Het sjabloon MASTER-bestand bevat instellingen voor koptekst, navigatiemenu's, voettekst, lettertype en stijlinformatie. Met behulp van een MASTER-bestand kunt u snel meerdere webpagina's maken.

U kunt een MASTER-bestand openen met Microsoft Visual Studio 2022 en hoger.

## MASTER-bestandsindeling - Meer informatie

Een MASTER-bestand wordt gemaakt en opgeslagen in HTML-bestandsindeling en is vergelijkbaar met elk ander webpaginabestand. Het is verdeeld in bewerkbare en niet-bewerkbare secties. De bewerkbare secties zijn de secties die kunnen worden aangepast om aan de vereisten van de gebruiker te voldoen. De niet-bewerkbare secties worden grijs weergegeven wanneer het MASTER-bestand wordt geopend in Microsoft Visual Studio.

Basispagina's bestaan uit twee delen, namelijk de basispagina zelf en een of meer inhoudspagina's.

### HOOFDpagina

De masterpagina heeft de extensie .master en is gemaakt in ASP.NET. Het heeft een vooraf gedefinieerde lay-out die bestaat uit statische tekst, HTML-tags en bedieningselementen aan de serverzijde. Op gewone .aspx-pagina's wordt de @ Page-richtlijn gebruikt. In het geval van .master-bestanden wordt dit vervangen door de @Master-richtlijn.

### Inhoudspagina's

Een inhoudspagina vertegenwoordigt de inhoud voor de tijdelijke aanduidingen van de stramienpagina. Dit zijn .aspx-pagina's die feitelijk de code achter de hoofdpagina vormen. Inhoudspagina's worden gekoppeld met behulp van de @ Page-richtlijn door een MasterPageFile-attribuut op te nemen dat verwijst naar de te gebruiken stramienpagina, zoals hieronder weergegeven.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referenties

* [Overzicht ASP.NET-basispagina's](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

