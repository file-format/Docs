{
  "date" : "2021-04-11",
  "keywords" :[ "xapk ファイル", "xapk ファイル形式", "xapk ファイルとは", "ファイル", "xapk の例", "xapk ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - メタ パッケージ ファイル形式",
  "description":"XAPK ファイルの形式と,XAPK ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## .XAPK ファイルとは?

拡張子が .xapk のファイルは、モバイル デバイスに Android アプリをインストールするために使用される圧縮パッケージ ファイルです。これは、インストールに必要な APK と追加の関連ファイルを組み込んだコンテナー ファイル形式です。もう 1 つの関連ファイルは、アプリケーションの実行を維持するために必要なグラフィック、メディア ファイル、アプリ データなどの追加ファイルを格納する OBB ファイルです。 XAPK ファイルは Google Play ではサポートされておらず、サードパーティの Android アプリ ダウンロード Web サイトでの配布にのみ使用されます。これらは、XAPK インストーラーを使用して Android デバイスにインストールできます。

## XAPK ファイル形式

XAPK ファイルは、標準の [ZIP](/compression/zip/) ファイル形式を使用して圧縮されます。これらは、WinZIP などの標準の圧縮/解凍ソフトウェアを使用して抽出できます。 XAPK ファイルがディスクに抽出されると、フォルダー内に次のファイルが含まれます。

* APK - Android デバイスにアプリケーションをインストールするための標準インストール ファイル
* OBB - 関連するリソース ファイルを含む追加ファイル

## 参考文献

* [Android パッケージ ファイル](https://en.wikipedia.org/wiki/Android_application_package)

