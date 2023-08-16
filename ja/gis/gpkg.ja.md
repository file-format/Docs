{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg ファイル", "gpkg ファイル形式", "gpkg ファイルとは", "ファイル", "gpkg の例", "gpkg ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage フォーマット ファイル",
  "description":"GPKG ファイル形式と,GPKG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## .GPKG ファイルとは?
拡張子が .gpkg のファイルは、一般的な定義、形式の制限、整合性アサーション、およびコンテンツの制約を含むデータ テーブルとメタデータ テーブルを含む SQLite データベース コンテナーとして実装された地理情報システムで構成されます。 2014年に出版されました。米軍に代わって OGC (Open Geospatial Consortium) によって定義されました。さまざまな政府機関、商業組織、およびオープン ソース組織が、GeoPackage を広くサポートしています。

## GPKG ファイル形式
GeoPackage は、拡張された SQLite 3 データベース ファイルとして構成されます。標準は、次の一連の規則 (必要な規則) を定義します。
- 画像のタイル マトリックス セットの保存
- ベクトル機能
- さまざまな縮尺のラスター マップ
- メタデータとスキーマ

標準の 2.3 節で定義されている拡張ルールを使用して、GeoPackage を拡張できます。 GeoPackage を設計する目的は、可能な限り軽量のデータベースを作成し、すぐに使用できる単一のファイルに含めることでした。これにより、オフライン モードでのモバイル アプリケーションや、クラウド ストレージや USB ストレージ デバイスなどでの高速共有に最適です。

### GPKG の内容
GeoPackages には、他のリレーショナル データベースと同様に、多数のテーブルが含まれています。これらのテーブルは、ユーザー定義テーブルまたはメタデータ テーブルのいずれかです。 GeoPackages は、2 つの必須のメタデータ テーブルで構成されます。

#### gpkg_contents
GeoPackage の目次。この表の必須列は次のとおりです。

- **table_name**: ユーザー定義データ テーブルの実際の名前。
- **data_type**: タイトル、機能、属性などのデータ型。
- **識別子と説明**: 人間が読めるテキスト。
- **last_change**: ISO 8601 形式での最終変更の情報日付。
- **min_x、min_y、max_x、および max_y**: コンテンツの空間範囲。 ;
- **srs_id**: 空間参照系。

#### gpkg_spatial_ref_sys
空間参照コンテンツ用。タイルやフィーチャを含むがこれらに限定されないコンテンツの各行は、座標参照系を参照する必要があります。 **gpkg_spatial_ref_sys** テーブルに格納されます。この表の必須列は次のとおりです。

- **srs_name, description**: 人間が読める SRS の名前と説明。
- **srs_id**: SRS の一意の識別子。テーブルの主キーでもあります。
- **組織**: 定義する組織の大文字と小文字を区別しない名前。
- **organization_coordsys_id**: 組織によって割り当てられた SRS の数値 ID。
- **定義**: SRS の Well Known Text 定義。


## 参考文献

* [GeoPackage - ウィキペディアによる](https://en.wikipedia.org/wiki/GeoPackage)
* [GeoPackage を始める](http://www.geopackage.org/guidance/getting-started.html)

