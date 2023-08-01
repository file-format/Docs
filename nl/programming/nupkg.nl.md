{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG-bestand - NuGet-pakketbestand",
  "description":"Meer informatie over NUPKG-bestandsindelingen en API's die NUPKG-bestanden kunnen maken en openen.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Wat is een NUPKG-bestand?

Een NUPKG-bestand is een pakketbestand dat de broncode bevat die door NuGet-software moet worden gebruikt voor het maken van pakketten voor gebruik in .NET-projecten. Het NuGet Package Manager-onderdeel wordt geïnstalleerd als onderdeel van Microsoft Visual Studio voor het ophalen van pakketten van online pakketten die een repository hosten. Met NUPKG-bestanden kunnen ontwikkelaars de nieuwste pakketten ophalen van [Nuget.org](https://nuget.org) met behulp van NuGet Package Manager in plaats van de ontwikkelingspakketten handmatig te downloaden en te installeren. NUPKG-bestanden zijn opgebouwd uit NUSPEC-bestanden en, wanneer ze worden opgehaald, installeren ze het pakket op het gebruikerssysteem.

## NUPKG-bestandsindeling

NUPKG-bestanden zijn [ZIP](/nl/compression/zip/)-archieven die de verpakte bibliotheken erin bevatten. Wanneer het is gedownload, kan het worden hernoemd naar .zip en worden uitgepakt met alle standaard zip-hulpprogramma's zoals WinZIP, 7-Zip en Apple Archive Utility.

## Referentie

* [Nuget.org](https://nuget.org)
* [Snelstart: een pakket installeren en gebruiken in Visual Studio (alleen Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [Een Nuget-pakket maken en publiceren](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

