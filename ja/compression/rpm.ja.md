{
  "date" : "2021-04-08",
  "keywords" :["rpmファイル","rpmファイル形式","rpmファイルとは","ファイル","rpm例","rpmファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager ファイル",
  "description":"RPM ファイルのフォーマットと,RPM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## .RPM ファイルとは?

拡張子が .rpm のファイルは、Linux システムにプログラムをインストールするための Red Hat Linux オペレーティング システム パッケージです。 Red Hat Package Manager は RPM ファイル形式を使用する無料のオープンソース パッケージ管理システムです。プログラムのインストールにはRPMファイルをそのまま使用することもできますが、AlienというDebianプログラムを使用して[DEB](/compression/deb/)などの別のパッケージ形式に変換することができます。

## RPM ファイル形式

RPM ファイルは、一連のファイルを含むことができるバイナリです。ほとんどの場合、RPM ファイルはソフトウェアのコンパイル済み実行可能ファイルである「バイナリ RPM」です。 RPM ファイルには、ソース コードからパッケージをビルドするために使用できるソース RPM (SRPM) を含めることができます。 RPM ファイル形式は 4 つのセクションで構成されています。

* リード - ファイルを RPM ファイルとして識別します
* 署名 - 完全性および/または真正性を保証するために使用できます
* ヘッダー - パッケージ名、バージョン、アーキテクチャ、ファイル リストなどのメタデータが含まれます。
* ファイル アーカイブ - ペイロードとも呼ばれ、通常は [GZIP](/compression/gz/) で圧縮された cpio 形式です。

## 参考文献

* [RPM - ウィキペディア](https://rpm.org)
* [RPM ドキュメント](https://rpm.org/documentation.html)

