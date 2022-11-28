{
  "date" : "2021-08-13",
  "keywords" :[ "файл sdi", "формат файла sdi", "что такое файл sdi", "файл", "пример sdi", "расширение файла sdi", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Узнайте о формате файла SDI и API-интерфейсах, которые могут создавать и открывать файлы SDI.",
  "title" :"SDI — файл образа развертывания системы Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## .SDI вариант №
Файл с расширением .sdi содержит большой двоичный объект загрузки, двоичный объект загрузки и большой двоичный объект части; обычно используется Windows Embedded Studio для создания RAM-дисков или загрузочных дисков для загрузки и установки Windows. SDI является аббревиатурой от System Deployment Image. Windows Embedded Studio — это программа, используемая для создания образов дисков для Windows. На самом деле эта программа содержит программу SDI File Manager и инструмент командной строки под названием **sdimgr.exe**, которые можно использовать для загрузки, создания и редактирования изображений SDI.

## Формат SDI-файла
Формат файла SDI широко используется для обеспечения возможности использования виртуального диска для загрузки системы. Некоторые версии Microsoft Windows допускают **загрузку из RAM**, что важно для загрузки SDI-файла в память и последующей загрузки из него. Формат файла SDI также обеспечивает загрузку по сети с использованием PXE (среда выполнения предварительной загрузки). Он также используется для создания образов жестких дисков.
### Разделы файла SDI
Сам файл SDI можно разделить на следующие разделы:
- **Boot BLOB**: содержит саму загрузочную программу STARTROM.COM. Это аналог загрузочного сектора жесткого диска.
- **Загрузить BLOB**: обычно содержит NTLDR и запускается загрузочным BLOB.
- **Part BLOB**: содержит фактическую среду выполнения загрузки; также включает файлы boot.ini и ntdetect.com, которые должны находиться в корневом каталоге среды выполнения.
- **Disk BLOB**: это плоский образ жесткого диска, начинающийся с MBR. Он используется для создания образа жесткого диска вместо загрузки. Кроме того, с помощью утилит Microsoft можно монтировать только Disk BLOB.


## использованная литература

* [Образ развертывания системы — из Википедии] (https://en.wikipedia.org/wiki/System_Deployment_Image)

