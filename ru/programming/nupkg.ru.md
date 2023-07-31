{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл NUPKG — файл пакета NuGet",
  "description":"Узнайте о формате файла NUPKG и API-интерфейсах, которые могут создавать и открывать файлы NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## .NUKG вариант №

Файл NUPKG — это файл пакета, содержащий исходный код, который будет использоваться программным обеспечением NuGet для создания пакетов, которые будут использоваться в проектах .NET. Компонент NuGet Package Manager устанавливается как часть Microsoft Visual Studio для получения пакетов из онлайн-репозитория пакетов. Файлы NUPKG помогают разработчикам получать последние пакеты с [Nuget.org](https://nuget.org) с помощью диспетчера пакетов NuGet, а не загружать и устанавливать пакеты разработки вручную. Файлы NUPKG создаются из файлов NUSPEC и при получении устанавливают пакет в пользовательской системе.

## Формат файла NUPKG

Файлы NUPKG представляют собой архивы [ZIP](/ru/compression/zip/), содержащие внутри упакованные библиотеки. После загрузки его можно переименовать в .zip и распаковать любыми стандартными zip-утилитами, такими как WinZIP, 7-Zip и Apple Archive Utility.

## Ссылка

* [Nuget.org](https://nuget.org)
* [Быстрый старт: установка и использование пакета в Visual Studio (только для Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [Как создать и опубликовать пакет Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)
