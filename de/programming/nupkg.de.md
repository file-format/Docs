{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG-Datei - NuGet-Paketdatei",
  "description":"Erfahren Sie mehr über das NUPKG-Dateiformat und APIs, die NUPKG-Dateien erstellen und öffnen können.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Was ist eine NUPKG-Datei?

Eine NUPKG-Datei ist eine Paketdatei, die Quellcode enthält, der von der NuGet-Software zum Erstellen von Paketen verwendet wird, die in .NET-Projekten verwendet werden sollen. Die NuGet Package Manager-Komponente wird als Teil von Microsoft Visual Studio zum Abrufen von Paketen aus dem Onlinepaket-Hosting-Repository installiert. NUPKG-Dateien helfen Entwicklern, die neuesten Pakete von [Nuget.org](https://nuget.org) mithilfe des NuGet-Paket-Managers abzurufen, anstatt die Entwicklungspakete manuell herunterzuladen und zu installieren. NUPKG-Dateien werden aus NUSPEC-Dateien erstellt und installieren das Paket beim Abrufen auf dem Benutzersystem.

## NUPKG-Dateiformat

NUPKG-Dateien sind [ZIP](/de/compression/zip/)-Archive, die die darin enthaltenen gepackten Bibliotheken enthalten. Nach dem Herunterladen kann es in .zip umbenannt und mit allen Standard-Zip-Dienstprogrammen wie WinZIP, 7-Zip und Apple Archive Utility extrahiert werden.

## Bezug

* [Nuget.org](https://nuget.org)
* [Schnellstart: Installieren und Verwenden eines Pakets in Visual Studio (nur Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- Studio)
* [So erstellen und veröffentlichen Sie ein Nuget-Paket](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- CLI)

