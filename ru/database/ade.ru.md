{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "расширение", "файл", "формат файла", "Тип файла базы данных", "Формат файла базы данных", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла ADE и API-интерфейсах, которые могут создавать и открывать файлы ADE.",
  "title" :"ADE — доступ к файлу расширения проекта",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## .ADE вариант №

Файл с расширением .ade — это файл проекта Microsoft Access, который содержит скомпилированный вывод информации, содержащейся в файле проекта Microsoft Access ADP. Информация в файле проекта Access, отличная от Visual Basic для приложений (VBA), доступна в скомпилированном виде в файлах ADE. Данные в этих файлах хранятся в сжатом формате, чтобы уменьшить размер файла и повысить производительность в Access. Поскольку ADE представляет собой скомпилированный вывод файла проекта Access, любой исходный код VBA, являющийся частью проекта, остается защищенным, поскольку он не может быть частью вывода. Файлы ADE можно открывать в Microsoft Access 365.

## Формат файла ADE — дополнительная информация

ADE — это скомпилированные файлы базы данных Access, которые хранятся на диске в виде двоичных файлов. Внутренняя файловая структура этих файлов не известна.

Файлы ADE могут создавать проблемы при открытии в зависимости от версии Microsoft Access, которая использовалась для создания этих файлов. Базы данных Access, использующие 64-разрядную версию Microsoft Access 2010 и скомпилированные как файлы MDE, [ACCDE](/ru/database/accde/) или ADE, необходимо перекомпилировать в Microsoft Access 2021 с пакетом обновления 1 (SP1) для корректно работать с Access 2010 SP1. Эта проблема возникает из-за того, что Access 2010 с пакетом обновления 1 (SP1) использует более новую версию файла VBE7.dll (версия 7.00.1619).

## использованная литература

* [Проблема с доступом к файлам ADE] (https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Какие форматы файлов доступа использовать] (https://support.microsoft.com/en-us/office/what-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
