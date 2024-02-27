{
  "date": "2022-03-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "NUPKG-fil - NuGet-pakkefil",
  "description": "Lær om NUPKG filformat og API'er, der kan oprette og åbne NUPKG filer.",
  "linktitle": "NUPKG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nupk-dag"
}
},
  "lastmod": "2022-03-09"
}

## Hvad er en NUPKG fil?

En NUPKG-fil er en pakkefil, der indeholder kildekode, der skal bruges af NuGet-software til at oprette pakker, der skal bruges i .NET-projekter. NuGet Package Manager-komponent er installeret som en del af Microsoft Visual Studio til at hente pakker fra online-pakkehosting-lager. NUPKG-filer hjælper udviklere med at hente de seneste pakker fra [Nuget.org](https://nuget.org) ved hjælp af NuGet Package Manager i stedet for manuelt at downloade og installere udviklingspakkerne. NUPKG-filer er bygget ud fra NUSPEC-filer, og når de hentes, installeres pakken på brugersystemet.

## NUPKG filformat

NUPKG-filer er [ZIP](/compression/zip/)-arkiver, der indeholder de pakkede biblioteker i det. Når den er downloadet, kan den omdøbes til .zip og udpakkes med alle standard zip-værktøjer som WinZIP, 7-Zip og Apple Archive Utility.

## Reference

* [Nuget.org](https://nuget.org)

* [Hurtigstart: Installer og brug en pakke i Visual Studio (kun Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studie)

* [Sådan opretter og udgiver du en Nuget-pakke](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)


