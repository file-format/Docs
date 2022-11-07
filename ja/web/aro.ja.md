{
  "date" : "2021-12-09",
  "keywords" :[ "aro",".aro ファイル", "aro ファイル形式", "ファイルの種類", "ファイル", "種類", ".aro ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AROファイル形式 - SteelArrow Webアプリケーションファイル",
  "description" :"ARO ファイルとは何か,および ARO ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## .ARO ファイルとは何ですか?

ARO ファイルは、SteelArrow Web アプリケーションで生成されるサーバー側の Web ページ ファイルです。 [HTML](/web/html/) と SteelArrow タグとスクリプトが含まれています。これらはサーバー上で実行され、ユーザーのブラウザーに送信する前に完全な応答ページを生成します。 ARO ファイルにはほぼ 95% の HTML コンテンツが含まれ、残りは SteelArrow コードで構成されています。 ARO ファイルが機能するためには、SteelArrow Web アプリケーション サーバーがインストールされ、Web サーバー マシンで実行されている必要があります。

## ARO ファイル形式

ARO ファイルは、JavaScript コードと Java アプレットが埋め込まれた HTML マークアップ言語ファイルで記述されています。 [SteelArrow タグ](http://www.steelarrow.com/docs/basics1.aro) は、Web ページを開発するための基本的な構成要素です。これらはページの表示を変更しませんが、ページをデータで埋めるために使用されます。さらに、条件付きステートメントで出力を制御するためにも使用できます。

### ARO タグの例

の<SAOUTPUT>ARO タグを使用すると、開発者はスクリプト内の任意の場所でデータ値を出力できます。たとえば、PARAM テーブルの出力を取得するために使用できます。<SAOUTPUT VALUE=PARAM[]> HTML内に表示できる<BODY>鬼ごっこ。

## 参考文献

* [SteelArrow タグ](http://www.steelarrow.com/docs/basics.aro)

