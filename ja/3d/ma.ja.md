{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma ファイル", "ma ファイル形式", "ファイル形式", "3d","ma ファイル ダウンロード", ".ma ファイル", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"MA ファイル形式と,MA ファイルを開いて作成できる API について学びます。",
  "title" :"MAファイル形式",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## .MA オプション番号

拡張子が .ma のファイルは、Autodesk Maya アプリケーションで作成された 3D プロジェクト ファイルです。ファイルに関する情報を指定するためのテキストコマンドの大きなリストが含まれています。 **.ma ファイル**は、任意のテキスト エディターで開いて編集し、ファイルが破損した場合にコマンドの問題を修正することができます。これらのファイルには、ジオメトリ、照明、アニメーション、レンダリングなどの 3D シーン情報を定義するための情報が含まれています。

## MA ファイル形式

MA ファイルは、バイナリ ファイル形式でディスクに保存される MB ファイルとは異なり、ASCII テキスト形式でディスクに保存されます。 MA ファイル フォーマットの詳細なリファレンスは、[Autodesk Maya ドキュメント](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)にあり、参照できます。開発者の参考のために。

### MA ファイルのヘッダー

MA ファイルのヘッダーは、ファイルの作成情報と変更日を示すコメントのセクションで始まります。このブロックは情報提供のみを目的として使用されるため、Maya ファイル リーダはこのブロックを無視します。ただし、ヘッダーは「//Maya」のように最初の 6 文字で始まる必要があります。

ASCII ファイルのヘッダーは次のようになります。

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### ファイル参照

.ma ファイルのファイル参照セクションには、このファイルで参照されている他のすべての Maya ファイルに関する情報が含まれています。各参照ファイルは、同じファイルに含まれる単一のファイル コマンドを使用して読み取ることができます。参照に使用する場合の file コマンドの構文は次のとおりです。

```
file -r -rpr prefixString fileName;
```
また

```
file -r -ns nameSpace fileName
```
文字列の例を次に示します。

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
この例は、ファイル「solar」に含まれる太陽オブジェクトが、「solar_sun」という名前を使用してこのファイルでアクセスできることを示しています。

＃＃＃ 要件

.ma ファイルの Requirements セクションは、一連の必須コマンドで構成され、ファイルの読み取りに必要なバージョンやプラグイン情報などの May の情報を伝えます。要件セクションの例は次のとおりです。

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


次のセクションでは、要件を指定します。これは、一連の require コマンドで構成されます。ファイルのこのセクションは、ファイルを適切にロードするために必要なソフトウェアを Maya に通知します。具体的には、Maya のバージョンとプラグインです。

## MAファイルのダウンロード
3D モデルの MA ファイルを見つけてダウンロードするのは少し難しいです。したがって、サンプルの MA ファイルは次の場所からダウンロードできます。

- [Sample.ma](../sample.ma)


## 参考文献

* [Maya ASCII ファイルの構成 - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

