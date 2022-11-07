{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","vdw ファイル", "vdw ファイル形式", "vdw ファイルの種類", "ファイル", "種類", "vdw ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio Graphics Service ファイル形式",
  "description":"VDW ファイル形式と,VDW ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## .VDW オプション番号

VDW は、Web 図面のレンダリングに必要なストリームとストレージを指定する Visio Graphics Service ファイル形式です。 Web 図面は、ベクターまたはラスター図面としてレンダリングできる図面ページ、図形、フォント、画像、データ接続、および図の更新情報のコレクションです。 VDW ファイルは Microsoft Visio でも開くことができますが、主に Web 上で使用するために保存されます。 Microsoft Visio は、Visio ファイルを [PNG](/Image/PNG/)、[BMP](/Image/BMP/)、[PDF](/pdf/) などのさまざまなファイル形式に変換する機能を提供します。

## **VDW** ファイル形式

VDW ファイル形式の技術仕様は、[Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) によってオンラインで入手でき、開発者が参照して作成することができます。アプリケーション。この技術文書では、ストレージとストリームを含む複合ファイルに含まれるデータについて説明しています。 Web 図面の表現は、VisioServerData という名前のストリームと ZIP アーカイブを介して可能になります。アーカイブ内の ShapGraphic XML パーツは、Web 図面に表示されるグラフィック要素を記述し、Extensible Application Markup Language (XAML) で表現されます。 ZIP アーカイブ内の XML パーツのコレクションには、Web 図面のデータ接続、その形状に関する情報、および図の更新ロジックが記述されています。これらの部分は XML として表現されます。 DataGraphic XML 部分は、Web 図面のデータがデータ ソースから更新された後に評価される、再計算されたプロパティを記述します。 ZIP アーカイブ内の追加アイテムには、Web 図面で使用されるフォントとイメージの情報が含まれています。

|![可能なファイルの実装](/web/vdw.png "可能なファイルの実装")

## 参考文献

* [[MS-VGSFF]: Visio Graphics Service (.vdw) ファイル形式](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

