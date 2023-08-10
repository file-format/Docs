{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DACPAC ファイル形式と,DACPAC ファイルを作成して開くことができる API について学びます。",
  "title" :"DACPAC - データ層アプリケーション パッケージ",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## .DACPAC ファイルとは?

.dacpac (Data Tier AppliCation Package の略) 拡張子を持つファイルは、Microsoft SQL Server データ層アプリケーションで作成されたデータベース ファイルで、データベース オブジェクトを表現するためのデータベース モデルが含まれています。データベースの完全なモデルが含まれているため、モデルで使用可能な詳細からデータベースを復元するために使用されます。 DACPAC ファイルは、通常、お客様の施設にインストールしてデータベースを復元するために、展開チームに引き渡されます。これらはで開くことができます
[マイクロソフト SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC ファイル形式 - 詳細情報

DACPAC データ パッケージ ファイルは、実際には、データベースの復元に使用されるテーブルやビューなどのデータベース モデルに関する情報を含む複数の [XML](/web/xml/) ファイルを含む圧縮 ZIP ファイルです。 DACPAC ファイルの内容を表示するには、ファイルの名前を .dacpac から [.zip](/compression/zip/) に変更し、解凍ユーティリティを使用して zip アーカイブを抽出します。

以下は、DACPAC ファイル内にあるいくつかのファイルです。

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

* モデル.xml

DACPAC には DATA やその他のサーバー レベルのオブジェクトが含まれていないことに注意してください。このファイルには、SSDT プロジェクトに保持される可能性のあるすべてのオブジェクト タイプを含めることができます。

## 参考文献

* [データ層アプリケーション - 利点](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [データ層アプリケーションのデプロイ - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
※【DACPACファイルの作り方】(https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

