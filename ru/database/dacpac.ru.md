{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "расширение", "файл", "формат файла", "Тип файла базы данных", "Формат файла базы данных", "Пакет приложения уровня данных" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла DACPAC и API-интерфейсах, которые могут создавать и открывать файлы DACPAC.",
  "title" :"DACPAC — Пакет приложений уровня данных",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## .DACPAC вариант №

Файл с расширением .dacpac (расшифровывается как Data Tier AppliCation Package) — это файл базы данных, созданный с помощью приложения уровня данных Microsoft SQL Server, который содержит модель базы данных для представления объектов базы данных. Поскольку он содержит полную модель базы данных, он используется для восстановления базы данных из сведений, доступных в модели. Файлы DACPAC обычно передаются группам развертывания для установки на территории заказчика для восстановления базы данных. Их можно открыть с помощью
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Формат файла DACPAC — дополнительная информация

Файлы пакета данных DACPAC на самом деле представляют собой сжатые ZIP-файлы, содержащие несколько файлов [XML](/ru/web/xml/), содержащих информацию о модели базы данных, такую как таблицы и представления, используемые для восстановления базы данных. Чтобы просмотреть содержимое файлов DACPAC, переименуйте файлы из .dacpac в [.zip](/ru/compression/zip/) и распакуйте zip-архив с помощью любой утилиты распаковки.

Ниже приведены несколько файлов, которые находятся внутри файла DACPAC.

* [Типы_содержимого].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Происхождение.xml

* модель.xml

Следует отметить, что DACPAC не содержит DATA и других объектов уровня сервера. Файл может содержать все типы объектов, которые могут храниться в проекте SSDT.

## использованная литература

* [Приложения уровня данных — преимущества](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Развертывание приложения уровня данных — Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Как создать файл DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

