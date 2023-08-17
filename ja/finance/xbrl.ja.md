{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl ファイル", "xbrl ファイル形式", "xbrl ファイルの種類", "ファイル", "種類", "xbrl ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - ビジネスおよび財務報告ファイル形式",
  "description":"XBRL ファイル形式と,XBRL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## .XBRL ファイルとは何ですか?

拡張子が .xbrl (eXtensible Business Reporting Language) のファイルは、ビジネス情報を交換するための自由に利用できるグローバルなフレームワークです。現在では、古い紙ベースのレポートをより有用で正確なデジタル記録に置き換えた標準形式の 1 つとして広く使用されています。 XBRL ファイルを使用して交換されるデータには、元帳、財務の詳細、貸借対照表が含まれます。あらゆる業務情報の準備から分析段階までのデータ処理を可能にするデータタグに対応しています。 XBRL ファイルは、Rivet Software Dragon View XBRL Viewer などのソフトウェアと [Aspose.Finance](https://products.aspose.com/finance/) などの API を使用して開くことができます。

## XBRL ファイル形式

XBRL は、世界中で広く使用されているデジタル ビジネス レポートのオープンな国際標準です。 [XML](/web/xml/) ベースの言語であり、タグと呼ばれる XBRL 要素を使用してビジネス データの各項目を記述し、レポートの並べ替えと分析用のデータを作成します。 XBRL ファイル形式の仕様は、現在 [XBRL バージョン 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) を使用して、XBRL International, Inc によって開発および公開されています。ユーザーが利用できます。

### XBRL ドキュメントの構造

[XBRL 2.1 タグ] に関する完全な情報 (https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) は、プログラマーがこのファイル形式を操作するためのアプリケーションを作成するために参照できます。 XBRL は、XBRL インスタンスとタクソノミーのコレクションで構成されます。

**`XBRL インスタンス`** - XBRL インスタンスは<xbrl>ルート要素。大きな XML ドキュメントには、複数の XBRL インスタンスが埋め込まれている場合があります。

**`XBRL タクソノミー`** - [XBRL タクソノミー](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5) は、XML スキーマ構造および直接参照される外部リンク要素のセットとして定義されています。リンクベース参照を示すスケーラブルな分類スキーマは次のとおりです。

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## 参照 ##

* [XBRL - ウィキペディアによる](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+修正済み- errata-2013-02-20.html)

