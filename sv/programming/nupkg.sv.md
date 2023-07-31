{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG-fil - NuGet-paketfil",
  "description":"Läs mer om NUPKG-filformat och API:er som kan skapa och öppna NUPKG-filer.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Vad är NUPKG fil?

En NUPKG-fil är en paketfil som innehåller källkod som ska användas av NuGet-programvaran för att skapa paket som ska användas i .NET-projekt. NuGet Package Manager-komponenten är installerad som en del av Microsoft Visual Studio för att hämta paket från onlinepaket som är värdlager. NUPKG-filer hjälper utvecklare att hämta de senaste paketen från [Nuget.org](https://nuget.org) med NuGet Package Manager istället för att manuellt ladda ner och installera utvecklingspaketen. NUPKG-filer är byggda från NUSPEC-filer och, när de hämtas, installera paketet på användarsystemet.

## NUPKG filformat

NUPKG-filer är [ZIP](/sv/compression/zip/)-arkiv som innehåller de paketerade biblioteken i den. När den har laddats ner kan den döpas om till .zip och extraheras med alla vanliga zip-verktyg som WinZIP, 7-Zip och Apple Archive Utility.

## Referens

* [Nuget.org](https://nuget.org)
* [Snabbstart: Installera och använd ett paket i Visual Studio (endast Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studio)
* [Hur man skapar och publicerar ett Nuget-paket](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

