{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX — Что такое файл APPX?",
  "description":"Узнайте о формате файла APPX и API-интерфейсах, которые могут создавать и открывать файлы APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## .APPX вариант №

Файл APPX — это формат файла распространяемого пакета, который используется для распространения и установки приложения. Он был представлен в Windows 8 для публикации в Microsoft Windows Store. Он содержит все файлы, необходимые для установки приложения Windows. К ним относятся метаданные, файлы и учетные данные. Более современный формат файла упаковки — MSIX, который в настоящее время используется чаще, чем APPX.

## Формат файла APPX — дополнительная информация

Файлы APPX сохраняются в виде сжатых файлов в формате [ZIP](/ru/compression/zip/). Это превращает весь пакет в архивный файл с уменьшенным размером файла, который легко загрузить в Microsoft Store.

## Как просмотреть файлы в файле APPX?

Чтобы просмотреть содержимое или файлы внутри файла APPX, необходимо выполнить следующие шаги.

1. Поскольку файлы APPX хранятся в виде сжатых ZIP-файлов, переименуйте файл в расширение .zip.
1. Используйте любой инструмент распаковки, такой как 7-Zip, WinZip или WinRAR, чтобы извлечь файлы, содержащиеся в файле APPX.

## Как создать файл APPX?

Существует два метода, которые можно использовать для создания файлов APPX.

1. Использование MakeApp.exe — [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) пакеты приложений (.msix или .appx) и файлы пакетов пакетов приложений .msixbundle или .appxbundle). Кроме того, он может извлекать файлы из пакета приложения. MakeApp.exe доступен с Windows 10 SDK и может использоваться из командной строки.
1. Использование Microsoft Visual Studio. Разработчики обычно [создают файлы APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) с помощью Microsoft Visual Studio. Когда разработка приложения завершена и приложение готово к публикации, файл пакета APPX можно создать, опубликовав его в Visual Studio.

## использованная литература

* [Создайте пакет или пакет MSIX с помощью MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Создание файлов APPX с помощью Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

