{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extension", "format", "eBook", "file", "Adobe Digital Editions" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Adobe による ACSM ファイル形式と,ACSM ファイルを作成して開くことができる API について学びます。",
  "title" :"ACSM - Adobe Content Server メッセージ ファイル形式",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## .ACSM オプション番号

拡張子が .acsm のファイルは、Adobe Content Server Message ファイルと呼ばれます。これらのファイルは、Adobe DRM で保護されたコンテンツを有効にしてダウンロードするために **Adobe Digital Editions** によって使用されます。実際、ACSM ファイルは eBook ファイルではありません。他の電子ブック (PDF など) のように開いて読むことはできません。電子ブックをアクティブにしてダウンロードするためのデータのみが含まれています。これは、ACSM ファイルがアドビのサーバーと通信する情報のみで構成されていることを意味します。 Digital Editions ユーザーは、eBook をダウンロードする場合は ACSM ファイルを見ることができますが、ダウンロードは何らかの理由で停止します。ユーザーは、.acsm ファイルをダブルクリックしてダウンロードを再開できます。

## ACSM ファイルのしくみ

Adobe Content Server は、電子書籍やその他のデジタルコンテンツを保護する役割を担っているためです。購入後、コンテンツは購入者の Adobe ID に自動的にリンクされます。 ID は非公開であり、他人に譲渡することはできません。ユーザーは、アドビのコピー保護付きのドキュメントを購入する前に、それを設定する必要があります。顧客は、Adobe ID をバックグラウンドで実行されている Adobe サーバー アプリケーションに渡さない限り、コピー防止されたドキュメントにアクセスできません。

顧客が購入するとき、最初にダウンロードできるファイルは ACSM だけです。 ACSM ファイルを開くには、システムに Adobe Digital Editions ソフトウェアをインストールし、それを Adobe ID にリンクしている必要があります。 Adobe Digital Editions は、ACSM ファイルを変換する権限の ID を確認します。認証された場合、ユーザーは自分の eBook を [EPUB](/ebook/epub/) または [PDF](/pdf/) 形式でダウンロードできます。また、Adobe Digital Editions は、ACSM ファイルを使用してダウンロード ディレクトリを認識します。

## 参考文献

* [Adobe Content Server - ウィキペディアによる](https://en.wikipedia.org/wiki/Adobe_Content_Server)


