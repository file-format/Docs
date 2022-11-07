{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL ファイル形式 - Web サービス記述言語ファイル",
  "description":"WSDL ファイルとは何か,および WSDL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## .WSDL ファイルとは?

WSDL ファイルは、Web サービスを記述するために XML 言語で記述された Web サービス記述言語ファイルです。これには、外部世界への接続用のエンドポイントまたはインターフェイスに関する情報が、広く受け入れられている形式で含まれています。 [WSDL ファイル形式の仕様](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (W3C.org が管理) は、データ交換のためにデータ フィードを公開するための条件を定義しています。ポートおよびエンドポイントを介したリモート アプリケーション アクセス。

## WSDL ファイル形式 - 詳細情報

WSDL ファイルは、人間が判読できる XML ファイルとして保存され、任意のテキスト エディターで開いて内容を表示できます。

## WSDL サービスの説明

WSDL 2.0 ファイル形式の仕様では、WSDL サービスは次の 2 つの段階で構成されると説明されています。

- 抽象ステージ
- コンクリートステージ

説明と独立した関心事の設計の再利用性は、Web サービスによって管理されます。これは、型 (データ型の定義)、メッセージ (通信されるデータ)、操作 (アクション)、サービスで使用されるプロトコルなど、いくつかの異なる型の要素を使用して実現されます。これらはすべて抽象レベルで管理されます。トランスポートのバインディングとワイヤ形式の詳細は、エンドポイントをグループ化して共通のインターフェイスを実装するバインディングによって指定されます。

### WSDL サービスとのインターフェースにはどのような技術を使用できますか?

ASP.NET、C/C++、Java アプリケーションなどの WSDL サービスとのインターフェイスには、いくつかの異なるテクノロジを使用できます。

## WSDL の例

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

この例では、portType "glossaryTerms" は "setTerm" という一方向操作を定義します。

## 参考文献

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
※【WSDLファイルフォーマット仕様】(https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

