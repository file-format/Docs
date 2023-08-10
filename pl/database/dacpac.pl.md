{
  "date" : "2021-09-06",
  "keywords" :["dacpac", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pakiet aplikacji warstwy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku DACPAC i interfejsy API, które mogą tworzyć i otwierać pliki DACPAC.",
  "title" :"DACPAC – pakiet aplikacji warstwy danych",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Czym jest plik DACPAC?

Plik z rozszerzeniem .dacpac (skrót od Data Tier Application Package) to plik bazy danych utworzony za pomocą aplikacji warstwy danych Microsoft SQL Server, który zawiera model bazy danych do reprezentacji obiektów bazy danych. Ponieważ zawiera pełny model bazy danych, służy do odtwarzania bazy danych ze szczegółów dostępnych w modelu. Pliki DACPAC są zwykle przekazywane zespołom wdrożeniowym do instalacji w siedzibie klienta w celu przywrócenia bazy danych. Można je otworzyć za pomocą
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Format pliku DACPAC — więcej informacji

Pliki pakietu danych DACPAC to w rzeczywistości skompresowane pliki ZIP, które zawierają kilka plików [XML](/pl/web/xml/) zawierających informacje o modelu bazy danych, takie jak tabele i widoki, używane do przywracania bazy danych. Aby wyświetlić zawartość plików DACPAC, zmień nazwę plików z .dacpac na [.zip](/pl/compression/zip/) i rozpakuj archiwum zip za pomocą dowolnego narzędzia do dekompresji.

Poniżej przedstawiono kilka plików, które znajdują się w pliku DACPAC.

* [Typy_zawartości].xml
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
* Pochodzenie.xml

* model.xml

Należy zauważyć, że DACPAC nie zawiera DANYCH ani innych obiektów na poziomie serwera. Plik może zawierać wszystkie typy obiektów, które mogą być przechowywane w projekcie SSDT.

## Bibliografia

* [Aplikacje warstwy danych — korzyści](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Wdrażanie aplikacji warstwy danych — Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Jak utworzyć plik DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

