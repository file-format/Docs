{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor NUPKG - soubor balíčku NuGet",
  "description":"Další informace o formátu souboru NUPKG a rozhraních API, která mohou vytvářet a otevírat soubory NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Co je soubor NUPKG?

Soubor NUPKG je soubor balíčku, který obsahuje zdrojový kód, který má software NuGet použít k vytváření balíčků pro použití v projektech .NET. Komponenta NuGet Package Manager je nainstalována jako součást Microsoft Visual Studio pro načítání balíčků z online úložiště balíčků hostujících. Soubory NUPKG pomáhají vývojářům načíst nejnovější balíčky z [Nuget.org](https://nuget.org) pomocí NuGet Package Manager namísto ručního stahování a instalace vývojových balíčků. Soubory NUPKG jsou sestaveny ze souborů NUSPEC a po načtení nainstalují balíček do uživatelského systému.

## Formát souboru NUPKG

Soubory NUPKG jsou archivy [ZIP](/cs/compression/zip/), které obsahují zabalené knihovny. Po stažení jej lze přejmenovat na .zip a extrahovat pomocí libovolných standardních nástrojů zip, jako jsou WinZIP, 7-Zip a Apple Archive Utility.

## Odkaz

* [Nuget.org](https://nuget.org)
* [Rychlý start: Nainstalujte a použijte balíček ve Visual Studiu (pouze Windows)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- studio)
* [Jak vytvořit a publikovat balíček Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

