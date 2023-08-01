{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл NUPKG - файл пакета NuGet",
  "description":"Дізнайтеся про формат файлу NUPKG та API, які можуть створювати та відкривати файли NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Що таке файл NUPKG?

Файл NUPKG — це файл пакета, який містить вихідний код, який буде використовуватися програмним забезпеченням NuGet для створення пакетів для використання в проектах .NET. Компонент NuGet Package Manager встановлюється як частина Microsoft Visual Studio для отримання пакетів із онлайнового сховища пакетів. Файли NUPKG допомагають розробникам отримувати найновіші пакети з [Nuget.org](https://nuget.org) за допомогою диспетчера пакетів NuGet замість ручного завантаження та встановлення пакетів розробки. Файли NUPKG створені з файлів NUSPEC і після отримання встановлюють пакет у системі користувача.

## Формат файлу NUPKG

Файли NUPKG — це архіви [ZIP](/uk/compression/zip/), які містять запаковані бібліотеки всередині. Після завантаження його можна перейменувати на .zip і розпакувати будь-якими стандартними утилітами для zip-архіву, такими як WinZIP, 7-Zip і Apple Archive Utility.

## довідка

* [Nuget.org](https://nuget.org)
* [Швидкий старт: установіть і використовуйте пакет у Visual Studio (тільки для Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [Як створити та опублікувати пакет Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

