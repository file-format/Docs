{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "разширение", "файл", "файлов формат", "Тип файл на база данни", "Файлов формат на база данни", "Пакет за приложение на ниво данни" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат DACPAC и API, които могат да създават и отварят DACPAC файлове.",
  "title" :"DACPAC – Пакет за приложение на ниво данни",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Какво е DACPAC файл?

Файл с разширение .dacpac (съкращение от Data Tier AppliCation Package) е файл на база данни, създаден с приложение за ниво на данни на Microsoft SQL Server, който съдържа модела на базата данни за представяне на обекти на база данни. Тъй като съдържа пълния модел на базата данни, той се използва за възстановяване на база данни от детайлите, налични в модела. DACPAC файловете обикновено се предават на екипите за внедряване за инсталиране в помещенията на клиента за възстановяване на база данни. Те могат да се отварят с
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC файлов формат - повече информация

Пакетните файлове DACPAC всъщност са компресирани ZIP файлове, които съдържат няколко [XML](/bg/web/xml/) файла, съдържащи информация за модела на базата данни, като например таблици и изгледи, използвани за възстановяване на база данни. За да видите съдържанието на DACPAC файловете, преименувайте файловете от .dacpac на [.zip](/bg/compression/zip/) и извлечете zip архива с помощта на която и да е помощна програма за декомпресия.

Следват няколко файла, които се намират в DACPAC файл.

* [Типове_съдържание].xml
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
* Origin.xml

* model.xml

Трябва да се отбележи, че DACPAC не съдържа DATA и други обекти на ниво сървър. Файлът може да съдържа всички типове обекти, които могат да се съхраняват в проекта SSDT.

## Препратки

* [Приложения от ниво на данни - предимства](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Внедряване на приложение от ниво данни - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Как да създадете DACPAC файл?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

