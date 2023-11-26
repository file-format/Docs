{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DXL ファイル形式と,DTSX ファイルを作成して開くことができる API について学びます。",
  "title" :"DXL ファイル形式 - Domino XML 言語ファイル形式",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## .DXLファイルとは何ですか?

DXL ファイルは、エンタープライズ レベルのビジネス コラボレーション ソフトウェアである Lotus Domino 用に作成された XML ベースのデータ ストレージ ファイルです。これには、スキーマ、設計要素、ビュー、フォーム、ドキュメント、データベース データ自体など、Lotus Domino データベースに関連するデータが含まれています。 [XML](/ja/web/xml/) は、あらゆるプログラミング言語で書かれたソフトウェア アプリケーションで読み取ることができる汎用ファイル形式です。また、人間が判読できる形式であり、任意のテキスト エディタで開くことができます。このため、DXL ファイルには、交換可能なファイル形式でデータをエクスポートする機能が備わっています。

## DXL ファイル形式

DXL ファイルは XML ファイル形式で保存され、任意のプログラミング言語で作成されたアプリケーションで簡単に読み取ることができます。これらのファイルは、データと設定を XML タグに保存し、データを分類し、適切な順序で配置します。

### DXL 出力例

以下は、Notes ドキュメントの出力テキストの抜粋です。

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## 参考文献

* [DXL 形式 - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

