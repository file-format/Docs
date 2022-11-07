{
  "date" : "2019-10-11",
  "keywords" :[ "adr",".adr ファイル", "ファイル形式", "ファイルの種類", "adr ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADR - Opera ブックマーク ファイル形式",
  "description" :"ADR ファイルとは何か,ADR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ADR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-06"
}

## .ADR オプション番号

ADR ファイル (.adr 拡張子で保存) は、Opera Web ブラウザーによって作成されたブックマークのリストです。このリストは、ユーザーが Web URL をブックマークし続けると入力されます。これらのブックマークは、必要に応じてバックアップおよび復元できる ADR ファイルに保存されます。 Chrome や Firefox などのほとんどのブラウザでは、ブックマークは [HTML](/web/html/) 形式で保存されるため、これらを ADR ファイル形式に変換して Opera ブラウザにインポートすることができます。 ADR ファイルは Opera ブラウザで開くことができます。

## ADR ファイル形式 - 詳細情報

ADR ファイルの内部ファイル形式の詳細は不明です。ただし、異なるバージョンの Opera でエクスポートされた ADR ファイル形式には違いがあります。これにより、[ADR ファイルのマージ](https://superuser.com/questions/471959/how-do-i-merge-several-opera-adr-bookmark-files-to-one-single-file) の生成が困難になります。さまざまなバージョンの Opera で。ただし、一部の外部ツールを使用してこれらをマージできます。

## 参考文献

* [ADR ファイルのマージ](https://superuser.com/questions/471959/how-do-i-merge-several-opera-adr-bookmark-files-to-one-single-file)

