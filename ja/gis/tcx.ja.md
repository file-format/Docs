{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX ファイル形式 - Training Center XML ファイル",
  "description":"TCX ファイル形式と,TCX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## .TCX オプション番号

TCX (Training Center XML) ファイルは、フィットネス デバイス間でデータを共有するために使用されるデータ交換形式です。 2008 年に Garmin の Training Center 製品で導入されました。心拍数、ランニングケイデンス、自転車ケイデンス、カロリー、ラップタイムなどのワークアウトデータは、TCX ファイル内に [XML](/web/xml/) 形式で保存されます。さらに、ワークアウト トラックに関する概要データも TCX ファイルに含まれています。 TCX ファイルは、Garmin スポーツ ウェアラブル デバイスで作成された [FIT](/gis/fit/) ファイルに似ています。

## TCX ファイル形式 - 詳細情報

TCX ファイルは XML ファイルとしてディスクに保存され、各レコードはアクティビティとして保存されます。アクティビティは、時間、ラップタイム、ID、心拍数、強度、ケイデンス、トラック情報などのワークアウトのすべてのデータで構成され、位置のペアと [GPX] に似た緯度と経度の位置のタイムスタンプが含まれます。 (/gis/gpx/) ファイル。

### TCX ファイル形式のバージョン

この形式には、Garmin がホストする独自の XML スキーマを持つ 2 つのバージョンがあります。それらのいくつかを次に示します。

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX データ プロトコル

TCX XML 形式の迅速なバージョンは、Github で [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol) として入手できます。

## 参照 ##

* [トレーニング センター XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX ビューアー](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

