{
  "date" : "2021-04-08",
  "keywords" :[ "deb ファイル", "deb ファイル形式", "deb ファイルとは", "ファイル", "deb 例", "deb ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip圧縮タールアーカイブ",
  "description":"DEB ファイル形式と,DEB ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## .DEB オプション番号

拡張子が .deb のファイルは、Linux OS でのソフトウェア パッケージの配布に使用できる Debian バイナリ パッケージ ファイル形式です。 2 つの [TAR](/compression/tar/) アーカイブ ファイルで構成されます。 DPKG は、DEB パッケージを読み取ってインストールするメカニズムを提供します。 DEB パッケージは、APT パッケージ ソフトウェア管理インターフェイスを使用してインストールできます。 DEB ファイルの Internet Media Type は「application/vnd.debian.binary-package」です。

## DEB ファイル形式

DEB ファイルは、2 つの [TAR](/compression/tar/) アーカイブ ファイルで構成されます。 1 つのアーカイブには制御情報が含まれ、別のアーカイブにはインストール可能なデータが含まれます。

### パッケージ構成

DEB ファイルは、魔法の値 `!' を持つ **ar** アーカイブ ファイルです。<arch> `。 Debian 0.93 以降、DEB ファイルのアーカイブ メカニズムには、特定の順序で 3 つのファイルが含まれています。

1. `Debian Binary` - 改行で区切られた一連の行を持つ予定です。現在、バージョン番号を記述する行は 1 行だけです。現在のバージョン番号は 2.0 です。
1. `Control Archive` - パッケージ名、バージョン、依存関係、メンテナーなどのパッケージに関するメンテナー スクリプトとメタ情報を含む control.tar アーカイブが含まれています。
1. 「データ アーカイブ」 - data.tar という名前の tar アーカイブで、実際のインストール可能なメディア ファイルが含まれています。アーカイブは gz、bz2、lzma、または xz で圧縮でき、それに応じてデータ アーカイブのファイル拡張子が変わります。

### アーカイブの管理

コントロール アーカイブには、次のようなコンテンツを含めることができます。

* `control` - パッケージの簡単な説明と、依存関係などのその他の情報が含まれています。
* `md5sums` - 破損または不完全なファイルを検出するために、パッケージ内のすべてのファイルの MD5 チェックサムが含まれています。
* `conffiles` - 構成ファイルとして扱われるべきパッケージのファイルを一覧表示します。指定されていない限り、構成ファイルは更新中に上書きされません。
* `preinst`、postinst、prerm、および postrm - パッケージのインストールまたは削除の前後に実行されるオプションのスクリプト
* `config` は、debconf 設定メカニズムをサポートするオプションのスクリプトです。
* `shlibs` - 共有ライブラリの依存関係のリストです。

## 参考文献

* [DEB - ウィキペディア](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian バイナリ パッケージ形式](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

