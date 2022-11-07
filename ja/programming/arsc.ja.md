{
  "date" : "2019-10-11",
  "keywords" :[ "arsc",".arsc","arscファイルとは","arscファイルの開き方","拡張子","ファイル","arscファイル","arscファイル形式","arscファイル拡張子" ,"arsc ファイルの例"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android パッケージ リソース テーブル ファイル",
  "description":"ARSC ファイル形式と,ARSC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## .ARSC オプション番号

ARSC ファイルは、アプリケーションのリソースのリストをテーブル形式で含む Android リソース テーブル ファイルです。これには、リソース名、プロパティ、ID などの情報が含まれます。 ARSC ファイルは、これらの Android アプリのインストールに使用される APK パッケージの一部です。 Android アプリケーションの画像、レイアウト、スタイル、文字列などのすべてのリソースは、APK ファイルの生成時にバイナリ ファイルに変換されます。 ARSC ファイルも同時に生成され、すべてのプログラムのコンパイル済みリソースとその ID のリストが含まれます。

## ARSC ファイル形式

.arsc 拡張ファイルは、ANT (Eclipse) や Gradle (AS) などのコンパイラが Android アプリケーション コードをコンパイルして [APK](/compression/apk/) ファイルを生成した後に生成されるバイナリ ファイルです。 WinZip などのアーカイブ ユーティリティを使用して APK ファイルを抽出し、コンパイル済みの Java クラス ファイル、つまり classes.dex であるその内容を表示できます。これらに加えて、次のメタ情報を含むこの ARSC ファイルも含まれています。

* XML ノード
*属性
* リソース ID

APK ファイル内のリソースはリソース ID によって参照されますが、属性は実行時に値に解決されます。 Android aapt ツールは、ビルド時にファイルで定義されたすべてのリソースを収集し、それらにリソース ID を割り当てます。コンパイルされたリソースに識別子が割り当てられると、ソース コードと resources.arsc から R.java ファイルが生成されます。

## 参考文献

* [バイナリ リソース テーブル構造](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

