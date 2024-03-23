{
  "date" : "2019-10-11",
  "keywords" :["XPS","XML用紙仕様","ファイル","拡張子","ファイル形式","EMF","PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - ページ レイアウト ファイル形式",
  "description":"XPS ファイル形式と,XPS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## .XPS ファイルとは何ですか? ##

XPS ファイルは、Microsoft によって作成された XML Paper Specifications に基づくページ レイアウト ファイルを表します。 EMF ファイル形式の代替として開発されたもので、[PDF](/pdf/) ファイル形式に似ていますが、ドキュメントのレイアウト、外観、および印刷情報に XML を使用します。実際、XPS は PDF に対する試みであると言う方が正当ですが、多くの理由で PDF が所有するほどの人気を得ることができませんでした。 Microsoft は、XPS ファイルを作成するために、Windows 7 以降、デフォルトで XPS Document Writer を提供しています。 XPS ファイルは、ドキュメントの印刷時にプリンターとして「Microsoft XPS Document Writer」を選択することで生成できます。

XPS ビューアは、Windows Vista、Windows 7、Windows 8、および Internet Explorer 6 以降の一部として統合されています。 XPS ファイルは、生成されると読み取り専用になります。これにより、ドキュメントの信頼性について XPS として送信された受信ドキュメントに対するユーザーの信頼が高まります。 XPS ドキュメントには、元のドキュメントから変換された 1 つまたは複数のページを含めることができます。

## 簡単な歴史 ##

Microsoft は、XPS 仕様を Ecma International に提出しました。 2007 年 6 月、OpenXPS Paper Specifications に基づく標準を開発するために、Ecma Technical Committee 46 (TC46) が設立されました。 Ecma International は、2009 年 6 月の第 97 回総会で Ecma Standard (ECMA-388) [XPS 仕様](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) を承認しました。

## XPS ファイル形式 ##

XPS 形式は、ドキュメントの構成と各ページの外観を定義する XML マークアップと、ドキュメントを表示または印刷するためのレンダリング ルールで構成されます。あらゆるシステムでドキュメントを再作成するためのすべての情報を保持するため、そのシステムで利用可能なリソースに依存しません。形式は基本的に ZIP アーカイブであり、ファイル拡張子を ZIP に変更すると、ドキュメント データを含む構成ファイルが表示されます。これらの文書には次のものが含まれます。

* ドキュメント ページ ファイル (.fpage) - ドキュメント コンテンツとドキュメント形式の設定が含まれます。 XPS ドキュメントの各ページには、1 つの FPAGE ファイルがあります。
* ドキュメント設定ファイル (.fdoc) - XPS アーカイブに含まれる設定を保存します。
* ドキュメント フラグメント ファイル (.frag) - 実際の XPS ファイルの設定を定義し、ドキュメント内のすべてのページに独自の .frag ファイルがあります。

{{< figure src="../XPS-1.png" alt="XPS ファイル形式" >}}

これらのファイルは、たとえば、同じフォントがマシンにインストールされていない場合でも、XPS ビューアーがそれらの元のフォントをレンダリングするように、ドキュメントの内容を保持します。これは、それぞれに XML マークアップ ファイルを含めることを意味します。

* ページ
* 文章
* 埋め込みフォント
* ラスター画像
* 2D ベクター グラフィックス
* デジタル著作権管理

XPS ドキュメント形式には、明確に定義されたパーツと関係のセットが含まれており、それぞれがドキュメント内の特定の目的を果たします。この形式は、デジタル署名、サムネイル、インターリーブなどのパッケージ機能も拡張します。

典型的な XPS ドキュメントは次のようになり、XPS ファイル形式 仕様 に照らして分析できます。

{{< figure src="../XPS-2.png" alt="XPS ファイル形式" >}}


## 参照 ##

* [XPSファイル形式仕様](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - ウィキペディアによる](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

