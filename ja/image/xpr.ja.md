{
  "date" : "2022-03-21",
  "keywords" :[ "xpr ファイル", "xpr ファイル形式", "xpr ファイルとは", "ファイル", "xpr の例", "xpr ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPR ファイル形式 - Microsoft Expression Design グラフィック ファイル",
  "description":"XPR ファイル形式と,XPR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## .XPR ファイルとは何ですか?

XPR ファイルは、廃止された Microsoft Expression Graphics (EGD) ソフトウェアで作成されたベクター画像ファイルです。ユーザー インターフェイスのモックアップとして使用できるグラフィック情報が含まれています。 XPR ファイルは、後に Microsoft Expression Design の .design ファイルに置き換えられました。 XPR ファイルは、かなり前に廃止された Microsoft Expression Studio で開くことができました。

## XPR ファイル形式の脆弱性

XPR ファイルは、Microsoft Expression Design の脆弱性を利用してリモート コードの実行を可能にすることが確認されました。報告された問題では、ダイナミック リンク ライブラリ (DLL) ファイルと共にネットワーク ディレクトリに配置されている正当な .xpr ファイルをユーザーが開いた場合、Microsoft Expression Design は DLL ファイルをロードし、そこに含まれるコードを実行しようとする可能性があります。これは、後にマイクロソフトのセキュリティ アップデートで修正されました。

## 参考文献

* [式の設計の脆弱性により、リモートでコードが実行される (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

