{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG файл – NuGet пакетен файл",
  "description":"Научете за файловия формат NUPKG и API, които могат да създават и отварят NUPKG файлове.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Какво е NUPKG файл?

NUPKG файлът е пакетен файл, който съдържа изходен код, който да се използва от софтуера NuGet за създаване на пакети, които да се използват в .NET проекти. Компонентът NuGet Package Manager е инсталиран като част от Microsoft Visual Studio за извличане на пакети от онлайн хранилище за хостване на пакети. NUPKG файловете помагат на разработчиците да извлекат най-новите пакети от [Nuget.org](https://nuget.org) с помощта на NuGet Package Manager вместо ръчно изтегляне и инсталиране на пакетите за разработка. NUPKG файловете са изградени от NUSPEC файлове и, когато бъдат извлечени, инсталират пакета в потребителската система.

## NUPKG файлов формат

NUPKG файловете са [ZIP](/bg/компресия/zip/) архиви, които съдържат пакетираните библиотеки вътре в тях. Когато бъде изтеглен, той може да бъде преименуван на .zip и извлечен с всякакви стандартни помощни програми за zip като WinZIP, 7-Zip и Apple Archive Utility.

## справка

* [Nuget.org](https://nuget.org)
* [Бърз старт: Инсталирайте и използвайте пакет във Visual Studio (само за Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- студио)
* [Как да създадете и публикувате пакет Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

