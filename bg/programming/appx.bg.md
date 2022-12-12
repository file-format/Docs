{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Какво е APPX файл?",
  "description":"Научете за файловия формат APPX и API, които могат да създават и отварят APPX файлове.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Какво е APPX файл?

APPX файлът е файлов формат на пакет за разпространение, който се използва за разпространение и инсталиране на приложение. Беше представен с Windows 8, за да бъде публикуван в Microsoft Windows Store. Той съдържа всички файлове, необходими за инсталиране на Windows приложение. Те включват метаданни, файлове и информация за идентификационни данни. По-модерен файлов формат за пакетиране е MSIX, който в момента се използва по-често в сравнение с APPX.

## APPX файлов формат - повече информация

APPX файловете се записват като компресирани файлове във файлов формат [ZIP](/bg/компресия/zip/). Това прави целия пакет като архивен файл с намален размер на файла, който лесно се качва в Microsoft Store.

## Как да преглеждате файлове в APPX файл?

За да видите съдържанието или файловете в APPX файл, трябва да следвате следните стъпки.

1. Тъй като APPX файловете се съхраняват като компресирани ZIP файлове, преименувайте файла на разширение .zip
1. Използвайте всеки инструмент за декомпресия като 7-Zip, WinZip или WinRAR, за да извлечете файловете, съдържащи се във файла APPX

## Как да създадете APPX файл?

Има два метода, които могат да се използват за създаване на APPX файлове.

1. Използване на MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) се използва за създаване на двете пакети с приложения (.msix или .appx) и файлове с пакети с приложения .msixbundle или .appxbundle). Освен това може да извлича файлове от пакет на приложение. MakeApp.exe се предлага с Windows 10 SDK и може да се използва от командния ред.
1. Използване на Microsoft Visual Studio – Разработчиците обикновено [създават APPX файлове](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) с помощта на Microsoft Visual Studio. След като разработката на приложението приключи и приложението е готово за публикуване, файлът на пакета APPX може да бъде създаден чрез публикуването му от Visual Studio.

## Препратки

* [Създайте MSIX пакет или пакет с MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Създайте APPX файлове с помощта на Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

