{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SDF ファイル - 空間データ形式ファイル",
  "description":"SDF ファイル形式と,SDF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## .SDF ファイルとは?

空間データ ファイル (SDF) は、オートデスクが開発したジオデータベース ファイル形式です。地理空間データを格納し、Autodesk GIS プログラム MapGuide および AutoCAD Map 3D で使用されます。 SDF ファイル形式は、単一ファイル データベース ファイル形式 SQLite3 に基づいています。これは、空間情報の大規模なデータセット用に最適化されたファイル形式と見なされます。

Autodesk AutoCAD Map 3D 2022 および Autodesk AutoCAD Civil 3D 2023 を使用して SDF ファイルを開くことができます。

## SDF ファイル形式 - 詳細情報

SDF ファイル形式は、バイナリ ファイルとしてディスクに保存されます。これは、データのバイナリ シリアル化に低レベルのストレージ コンポーネントを利用する SQLite データベースに基づいています。 SDF ファイルには、ファイルごとに複数のフィーチャ クラスと、各フィーチャ クラスの複数のジオメトリ プロパティが含まれています。 R ツリーを使用した各ジオメトリ プロパティのインデックス付けにより、SDF ファイル内のデータに高速にアクセスできます。

## 参考文献

* [自衛隊データ形式](https://en.wikipedia.org/wiki/Spatial_Data_File)
* [Autodesk SDF の読み込み](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)

