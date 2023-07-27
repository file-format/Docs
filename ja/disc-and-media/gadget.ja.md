{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"GADGET ファイルの形式と,GADGET ファイルを作成して開くことができる API について学びます。",
  "title" :"ガジェット - 仮想 CD ファイル",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## ガジェット ファイルとは何ですか?

ガジェット ファイルは、Windows Vista または Windows 7 のサイドバー内で実行される小さなソフトウェア プログラムで構成されています。複数の Web ベースのファイルを圧縮し、ファイルは [.html](/web/html/)、[.css](/web/css)、または [.js](/web/js/) ファイルで構成される場合があります。他の Web ファイル。 GADGET ファイルは、検索ツール、ニュース フィード、システム ユーティリティ、小さなゲームなどの小さなコンポーネントに使用されます。ガジェットはサイドバーによってホストされますが、サイドバー領域に固有のものではありません。これらはドッキングを解除して、必要に応じてデスクトップに移動できます。

## ガジェットファイル形式

GADGET ファイルは、名前が変更された [ZIP](/compression/zip/) アーカイブで、HTML、XML、JScript、および CSS (Cascading Style Sheets) ファイルのコレクションが含まれています。インストールには、.gadget ファイルのダウンロードとダウンロード プロセスの有効化によるコンポーネントのインストール、または .gadget ファイルのローカル システムへの保存とダブルクリックによるインストール プロセスの開始が含まれます。

基本的に、ガジェットには次の 2 つのファイルが含まれます。

1. **Gadget.xml**: マニフェスト。ガジェットの一般的なプレゼンテーションと構成情報で構成される XML ファイル。
2. **name.html**: HTML ファイル。<name>関連するガジェット マニフェストのタグ。ガジェット UI のラッパーを提供し、ガジェットのコア機能を構成します。

GADGET ファイルの複数のインスタンスを同時に実行できます。たとえば、さまざまなタイム ゾーンの時刻を知りたい場合は、各時計を特定のタイム ゾーンに設定することで、時計ガジェットの複数のインスタンスを実行できます。

### ガジェットの廃止

Windows 7 の Windows サイドバー プラットフォームには重大な脆弱性があるため、Microsoft の公式 Web サイトでガジェットを利用できなくなりました。その後、Microsoft は Windows の新しいリリースでこの機能を廃止しました。 GADGET は、いつでもコンピュータのファイルにアクセスしたり、コンピュータに損害を与えたり、不快なコンテンツを明らかにしたり、動作を変更したりするために悪用される可能性があります。

## 参考文献

* [Windows サイドバー - Microsoft による](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Windows サイドバー用ガジェットの開発パート 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

