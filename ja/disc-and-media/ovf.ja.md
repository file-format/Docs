{
  "date" : "2021-08-10",
  "keywords" :[".ovf ファイル","ファイル形式",".ovf ファイルとは","ファイル","ファイル拡張子"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :".ovf ファイル形式とは何か,および OVF ファイルを作成して開くことができる API について学びます。",
  "title" :"OVF ファイル形式 - 仮想化ファイルを開く",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## .OVF オプション番号

OVF ファイルは、仮想マシンで実行されるソフトウェアのパッケージ化と配布に関する情報を含むテキスト ファイルです。 [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) に従ってフォーマットされており、仮想マシンでアプリケーションを実行するためのすべての要件 (セキュリティ、移植性、効率、拡張性など) が記述されています。国際標準化機構 (ISO) は、OVF を ISO 17203 標準として採用しました。

## OVF ファイル形式の歴史

OVF ファイル形式は、オープンな管理性標準を作成する DMTF (Distributed Management Task Force) によって導入されました。これは、特定のハイパーバイザーまたは命令セット アーキテクチャから独立しています。 OVF パッケージには 1 つ以上の仮想システムが含まれており、それぞれを仮想マシンにデプロイできます。

## OVF ファイル形式 - 詳細情報

OVF パッケージは、1 つのディレクトリに配置された複数のファイルで構成されます。これらのうち、[XML](/web/xml/) ファイル形式で格納されている OVF 記述子 (拡張子は .ovf) ファイルを 1 つだけ含んでいます。パッケージ化された仮想マシン情報と、OVF パッケージに関する次のようなメタデータ情報について説明します。

* 名前
* ハードウェア要件
* OVF パッケージ内の他のファイルへの参照、および
* 人間が読める説明

OVF パッケージに含まれるその他のファイルには、1 つ以上のディスク イメージと、オプションで証明書ファイルおよびその他の補助ファイルが含まれます。

## 参考文献

* [オープン仮想化フォーマット - DMTF](https://www.dmtf.org/standards/ovf)
※【OVFファイル形式仕様書】(https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

