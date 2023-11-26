{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM ファイル - Adobe Edge Animate ウィジェット ファイル形式",
  "description" :"OAM ファイルとは何か,および OAM ファイルを作成して開くことができる API について説明します。",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## .OAM ファイルとは何ですか?

.oam ファイルは、Adobe Edge Animate Widget からエクスポートされたアニメーション ウィジェット ファイルです。 OAM ウィジェット ファイル形式としてエクスポートされたアニメーションは、InDesign ドキュメント ([INDD ファイル](/ja/page-description- language/indd/)、Dreamweaver、Muse など) の他の Adobe アプリケーションに挿入できます。OAM ファイルは、すぐに使用できる展開パッケージのようなものです。他の Adobe のプロジェクトに挿入して利用できます。OAM ファイルには、アニメーションのアセット、動作、アクション スクリプト コードに関する情報が含まれています。OAM ファイルは、Adobe Animate プロジェクト [.AN ファイル](/ja/web/an/) を公開することで作成できます。 。
ユーザーは、Edge Animate プロジェクト (.AN ファイル) から公開することで OAM ファイルを作成できます。

## OAM ファイル形式

OAM ファイルは、圧縮された [ZIP](/ja/compression/zip/) アーカイブとしてディスクに保存されます。これは、ファイル拡張子の名前を .zip に変更し、WinZIP や WinRAR などの圧縮ユーティリティで抽出できることを意味します。ファイル サイズが小さくなったことで、インターネット経由でアニメーションを転送したり、他のユーザーと共有したりすることが容易になります。

### OAM ファイル構造

.oam ファイルの内部ファイル構造は独自のものであり、Adobe によって公的に文書化されていません。ただし、.oam ファイルには、単一のファイルにパッケージ化されたファイルとリソース (グラフィックス、オーディオ、ActionScript コードなど) のコレクションが含まれていることが知られています。 .oam ファイルの内容には、[XML](/ja/web/xml/) ファイル、SWF ファイル、およびその他のリソース ファイルが含まれる場合があります。 .oam ファイルの正確な構造は、ファイルの作成に使用された Adobe Animate の特定のバージョン、およびファイルに含まれるアニメーションとアセットの種類によって異なります。

OAM ファイルには次の情報が含まれています。

`Assets:` アニメーションで使用されるグラフィック、オーディオ、およびビデオ アセットに関する情報。

`Behaviors:` アニメーション内で発生するアクションとインタラクションの説明。

`ActionScript コード:` アニメーションの動作と対話性を制御するために使用されるコード。

`パブリッシュ設定:` HTML5 や AIR など、アニメーションがパブリッシュされるプラットフォームと形式に関する情報。

`メタデータ:` アニメーションの作成者、作成日、バージョン番号などの追加情報。

## OAMファイルを開くには?

次のアプリケーションを使用して OAM ファイルを開くことができます。

* Adobe Edge Animate CC (販売終了)
* Adobe Animate 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## 参考文献

* [OAM パブリッシング](https://helpx.adobe.com/animate/using/OAM-publishing.html)

