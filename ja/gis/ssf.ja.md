{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - Trimble Standard Storage Format File",
  "description":"SSF ファイル形式と,SSF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## .SSF ファイルとは何ですか?

.ssf ファイルを含むファイルは、[Trimble](https://www.trimble.com) Navigation GIS ソフトウェア アプリケーションで使用される地理空間データ ストレージ ファイル形式です。 Trimble デバイスを使用してフィールドから記録された GPS データを保存します。 GPS ログは、Trimble アプリケーション スイートのアプリケーションの 1 つにインポートされます。 SSF に含まれる GPS ログは、カスタム座標系を作成するために使用されます。 SSF ファイルは、[Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/products-and-solutions/ssf-and-ddf-data-format-extensions-fme)、Trimble Navigation GPS Pathfinder Tools SDK、ESRI ArcGIS for Desktop で開くことができます。 Trimble GPS Analyst プラグイン。

## SSF ファイル形式 - 詳細情報

GPS データが後処理のために Trimble デバイスからコンピュータに転送されると、これらのファイルはすべて 1 つの .ssf ファイルに結合されます。この生の未処理ファイルは、後処理ソフトウェアによって修正を行い、データ管理を支援するために使用されます。

SSF ファイルは、Trimble 独自のファイル形式としてディスクに保存され、その詳細な仕様は公開されていません。これは Trimble デバイスに固有のもので、GPS ユニットのデータを表します。今日まで、SSF ファイルを読み取ったり変換したりするための非商用の無料ソリューションはありません。

## 参考文献

* [Trimbleニュースリリース](https://www.trimble.com/news/release.aspx?id=050510b)

