{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - レポート定義言語ファイル",
  "keywords" :["rdl","レポート定義言語","XmlTextWriter","XSD","RDL要素"],
  "description":"SQL Server Reporting Services レポート定義の XML 表現である RDL ファイル形式について学びます。",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## .RDL オプション番号##

RDL (Report Definition Language) は、レポートを定義するために Microsoft によって設定されたベンチマークです。 RDL ファイルは、1 つまたは複数の RDL 要素で構成されます。一方、RDL 要素はデータ型とカーディナリティで構成されます。要素は、単純または複雑にすることができます。単純な要素には子要素や属性がありませんが、複雑な要素には子要素とオプションの属性があります。

## RDL XML スキーマ定義
XML スキーマ定義 (XSD) ファイルは、RDL ファイルを検証します。スキーマは、RDL 要素を .rdl ファイル内で使用できる場所に関する規則を定義します。 RDL 要素は、単純または複雑にすることができます。単純な要素には子要素または属性がありませんが、複雑な要素には子要素とオプションの属性があります。

## RDL の作成
RDL は本質的にオープンで拡張可能であるため、XML スキーマに基づいて RDL ファイルを生成する多くのアプリケーションとツールを構築できます。アプリケーションから RDL を作成する最も簡単な方法の 1 つは、**System.Xml** 名前空間と System.Linq 名前空間の Microsoft .NET Framework クラスを使用することです。特に、**XmlTextWriter** クラスを使用して RDL を記述できます。**XmlTextWriter** を使用すると、任意の .NET Framework アプリケーションで最初から最後まで完全なレポート定義を生成できます。開発者は、カスタム プロパティを含むカスタム レポート アイテムを追加して、RDL を拡張することもできます。

## RDL タイプ
次の表に、RDL 要素で使用される型と属性を示します。

|タイプ|説明|
---|---|
|バイナリ |base-64 でエンコードされたバイナリ値を持つプロパティ。|
|ブール値|オブジェクトの値として true または false を持つプロパティ。特に指定しない限り、省略されたオプションの Boolean オブジェクトの値は False です。|
|日付 |ISO8601 日付形式で指定された完全に指定された日付または日時値を持つプロパティー: YYYY-MM-DD[THH:MM[:SS[.S]]]。|
|列挙 |指定された値のリストの 1 つである必要がある文字列テキスト値を持つプロパティ。|
|Float |float 値を持つプロパティ。ピリオド (.) は、オプションの小数点記号として使用されます。|
||Integer |整数 (int32) 値を持つプロパティ。|
|Language |米国英語の「en-us」など、言語とカルチャ コードを含むテキスト値を持つプロパティ。値は、Microsoft .NET Framework で既定の言語が定義されている特定の言語またはニュートラル言語のいずれかである必要があります。|
|名前 |文字列テキスト値を持つプロパティ。名前は、アイテムの名前空間内で一意である必要があります。指定されていない場合、アイテムの名前空間は名前を持つ最も内側のオブジェクトです。|
|NormalizedString |正規化された文字列テキスト値を持つプロパティ。|
|サイズ |サイズ要素には、数字 (オプションの小数点としてピリオド文字を使用) を含める必要があります。数値の後には、cm、mm、in、pt、pc などの CSS の長さ単位の指定子が続く必要があります。番号と指定子の間のスペースはオプションです。サイズ指示子の詳細については、「CSS の値と単位のリファレンス」を参照してください。RDL では、Size の最大値は 160 インチです。最小サイズは 0 インチです。|
|文字列 |文字列テキスト値を持つプロパティ。|
||UnsignedInt |符号なし整数 (uint32) 値を持つプロパティ。|
|Variant |単純な XML 型のプロパティ。|

## RDL データ型
RDL では、DataType 列挙は、属性、式、またはパラメーターのデータ型を定義します。次の表は、CLR データ型が RDL データ型にどのように対応するかを示しています。

|CLR 型 |対応するデータ型|
---|---|
|ブール値|ブール値|
|DateTime、DateTimeOffset |DateTime|
|Int16、Int32、UInt16、Byte、SByte |Integer|
|シングル、ダブル |フロート|
|文字列、文字、GUID、タイムスパン |文字列|


## 参照 ##

- [レポート定義言語 (ウィキペディア)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [レポート定義言語 (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

