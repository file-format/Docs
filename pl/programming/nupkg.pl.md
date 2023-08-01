{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik NUPKG - Plik pakietu NuGet",
  "description":"Poznaj format pliku NUPKG i interfejsy API, które mogą tworzyć i otwierać pliki NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Czym jest plik NUPKG?

Plik NUPKG to plik pakietu zawierający kod źródłowy, który ma być używany przez oprogramowanie NuGet do tworzenia pakietów do wykorzystania w projektach .NET. Komponent NuGet Package Manager jest instalowany jako część Microsoft Visual Studio do pobierania pakietów z repozytorium hostującego pakiety online. Pliki NUPKG pomagają programistom pobierać najnowsze pakiety z [Nuget.org](https://nuget.org) przy użyciu Menedżera pakietów NuGet zamiast ręcznego pobierania i instalowania pakietów programistycznych. Pliki NUPKG są zbudowane z plików NUSPEC i po pobraniu instalują pakiet w systemie użytkownika.

## Format pliku NUPKG

Pliki NUPKG to archiwa [ZIP](/pl/compression/zip/), które zawierają spakowane biblioteki. Po pobraniu można zmienić jego nazwę na .zip i rozpakować za pomocą dowolnych standardowych narzędzi zip, takich jak WinZIP, 7-Zip i Apple Archive Utility.

## Odniesienie

* [Nuget.org](https://nuget.org)
* [Szybki start: instalacja i używanie pakietu w programie Visual Studio (tylko Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [Jak utworzyć i opublikować pakiet Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

