{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :["QGD","QGIS プロジェクトの Sqlite データベース","拡張子","フォーマット","QGIS","補助データベース","QGD ファイルとは"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - QGIS プロジェクトの Sqlite データベース",
  "description":"QGIS プロジェクトの sqlite データベースである QGD と,QGD ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## .QGD オプション番号

拡張子が .QGD のファイルは、実際には、プロジェクトの補助データを収容する **QGIS** プロジェクトに関連付けられた sqlite データベースです。プロジェクトの補助データがない場合、QGD ファイルは空のままになります。

## QGD ファイル形式の詳細

クラシック モードでは、補助データベースは xml ファイルに沿って .qgd 拡張子を持つファイルとして保存されます。 **補助データベース** システムでは、別の方法としてシステム内のデータを読み書きできます。圧縮されたコンテナである QGZ を作成すると、.qgd ファイルが .qgz にインクルードされます。

## 補助データベースとは
補助データベースは、実際には、ターゲット データベースの複製の応答として作成されるスタンバイ データベース システムです。補助データベースは、実際には複製データベースの場合であり、複製先のデータベースになります。たとえば、複製データベースを使用してスタンバイ データベースをセットアップする場合、ソース データベースはターゲットになり、スタンバイ データベースは補助データベースと呼ばれます。


## 参考文献

* [QGZ – QGIS の新しいデフォルト プロジェクト ファイル形式](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS ファイル形式](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

