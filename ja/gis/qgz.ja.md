{
  "date" : "2021-03-18",
  "keywords" :["qgzファイル","qgzファイル形式","qgzファイルとは","ファイル","qgz例","qgzファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - 量子 GIS 圧縮プロジェクト",
  "description":"圧縮された QGS である QGZ ファイル形式と,QGZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## .QGZ ファイルとは何ですか?

**QGZ** ファイル形式は、[QGS](https://docs.fileformat.com/gis/qgs/) ファイルと QGD ファイルを含む圧縮アーカイブです。一方、QGD ファイルは、プロジェクトの補助データで構成される qgis プロジェクトの sqlite データベースです。補助データがない場合、QGD ファイルは空のままになります。

## QGZ ファイル形式の詳細

QGZ は、**QGIS 3 プロジェクト ファイル形式**の新しいバリアントとして導入されました。この形式は、QGS xml ファイルの圧縮コンテナーです。ユーザーがオプションの形式である QGD を選択した場合、この場合、コンテナーは補助記憶域データベースを格納するのに役立ちます。

クラシック モードでは、補助データベースは xml ファイルに沿って .qgd 拡張子を持つファイルとして保存されます。圧縮されたコンテナーを選択すると、.qgd ファイルが .qgz に含まれます。ユーザーは問題なく簡単に使用できます。ユーザーは、プロジェクト ファイルを共有するときにそれを削除したり、コピーするのを忘れたりすることはありません!


## 参考文献

* [QGZ – QGIS の新しいデフォルト プロジェクト ファイル形式](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS ファイル形式](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

