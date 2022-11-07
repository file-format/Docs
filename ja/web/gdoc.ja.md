{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC ファイル - Google ドキュメントのショートカット",
  "description":"GDOC ファイルとは何か,および GDOC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## .GDOC オプション番号

GDOC ファイルは、クラウドベースのドキュメント ストレージ サービスである Google ドライブにあるファイルを指すショートカット ファイルです。 Google ドライブ クライアントがコンピューターにインストールされ、その中にドキュメントが作成されると、ドライブはオンライン クラウド ストレージにドキュメントを作成し、このドキュメントの [URL](/web/url/) をローカル Google の GDOC ファイルに書き込みます。ドライブ フォルダ。このショートカット ファイルをダブルクリックすると、デフォルトの Web ブラウザーが [URL](/web/url/) の場所からドキュメントを開きます。このショートカット ファイルをこのフォルダの外に移動すると、オンライン ドキュメントへのリンクが壊れます。

## GDOC ファイル形式 - 詳細情報

GDOC ファイルには、[JSON](/web/json/) ファイル形式で記述されたオンライン ドキュメントへのショートカットが含まれています。ユーザーがドキュメントが保存されているこの Google アカウントにログインしている場合、GDOC ファイルを開くブラウザは URL 情報を読み取り、リンクされたドキュメントを開いて表示します。 GDOC ファイルには、ドキュメントの内容は含まれていません。

### GDOC ファイルの例

GDOC ファイルはテキスト エディターで開くことができ、その内容は次のようになります。

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

ご覧のとおり、コンテンツは、ドキュメントの URL と関連するドキュメント ID を持つ JSON でフォーマットされています。

## 参考文献

* [Google ドキュメントで gdoc ファイルも docx ファイルも開かない](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

