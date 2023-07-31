{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX ファイル形式と,DTSX ファイルを作成して開くことができる API について学びます。",
  "title" :"DTSX ファイル形式 - SQL Server DTS 設定ファイル",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .DTSX オプション番号

.dtsx (Data Transformation Services Package XML) 拡張子を持つファイルは、あるデータベースから別のデータベースにデータを転送するためのデータ移行手順/ルールを参照するために Microsoft SQL によって使用される Data Transformation Services (DTS) ファイルです。これには、変換と、発信元ポイントと宛先ポイント間のデータ転送中に必要になる可能性のあるオプションの処理手順が含まれます。 Microsoft SQL Server のコンポーネントである SQL Server Integration Services (SSIS) は、DTSX ファイルを使用して、データベース サーバー間のデータ処理手順を識別します。 DTSX ファイルは、Microsoft SQL Server 2019 で開くことができます。

## DTSX ファイル形式

データベース サーバー間のデータ移動には、この操作中にデータの整合性を確保するためのルールと処理手順が必要です。 SSIS を使用すると、企業内のさまざまなソースからデータを移動および調整するためのこれらすべてのアクティビティを簡単に実行できます。そこで、SSIS が使用する構造を定義する DTSX を使用して、これらの手順に従ってデータを処理できる手順を確立します。

DTSX で記述されたデータ フローは、次の図のようになります。

{{< figure src="../DataFlowDTSX.png" alt="データ フロー DTSX" >}}

DTSX は [XML](/web/xml/) ベースであり、[MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd)。 DTSX XML の強化されたリファクタリングは DTSX 2.0 であり、構造に対する新しい属性、親 XML 属性としての名前付きプロパティの置き換え、ほとんどの属性値の既定値の指定、および親要素内の繰り返し要素の配置が含まれています。 DTSX 構造は、これらの [XML スキーマ](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) を使用して記述され、構造形式は次のとおりです。セラーテキスト XML。

## 参考文献

* [DTSX 形式 - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2 形式 - Microsoft による](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

