{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Пакет програми рівня даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу DACPAC та API, які можуть створювати та відкривати файли DACPAC.",
  "title" :"DACPAC - пакет прикладних програм рівня даних",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Що таке файл DACPAC?

Файл із розширенням .dacpac (розшифровується як Data Tier AppliCation Package) — це файл бази даних, створений за допомогою програми рівня даних Microsoft SQL Server, який містить модель бази даних для представлення об’єктів бази даних. Оскільки він містить повну модель бази даних, він використовується для відновлення бази даних з деталей, доступних у моделі. Файли DACPAC зазвичай передаються групам розгортання для встановлення в приміщеннях клієнта для відновлення бази даних. Їх можна відкрити за допомогою
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Формат файлу DACPAC – додаткова інформація

Файли пакетів даних DACPAC — це фактично стислі ZIP-файли, які містять кілька файлів [XML](/uk/web/xml/), що містять інформацію про модель бази даних, наприклад таблиці та подання, які використовуються для відновлення бази даних. Щоб переглянути вміст файлів DACPAC, перейменуйте файли з .dacpac на [.zip](/uk/compression/zip/) і розпакуйте архів zip за допомогою будь-якої утиліти декомпресії.

Нижче наведено кілька файлів, які містяться у файлі DACPAC.

* [Content_Types].xml
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

Слід зазначити, що DACPAC не містить DATA та інших об’єктів рівня сервера. Файл може містити всі типи об’єктів, які можуть зберігатися в проекті SSDT.

## Список літератури

* [Програми рівня даних – переваги](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Розгортання програми рівня даних – Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Як створити файл DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

