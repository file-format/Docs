{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BCP ファイル形式と,BCP ファイルを作成して開くことができる API について学びます。",
  "title" :"BCP - SQL Server 一括コピー ファイル形式",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .BCP オプション番号

BCP (バルク コピー フォーマット) は、Microsoft SQL Server の技術的なデータ フォーマットであり、データ構造を定義して、インポート/エクスポート用のさまざまなデータベース データ型の値を格納します。この形式は、データ ファイルで指定された一連の値を読み取ることができるように、各データ列の解釈を完全に定義します。 [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) ユーティリティは、BCP ファイル形式を使用して読み取りますそのようなファイルからデータを取得し、それを識別します。


## BCP ファイル形式

BCP フォーマット ファイルは、列の順序、名前、およびデータ型を定義する XML ドキュメントです。ユーザーは、これらのフィールドを指定して、データ ファイルから大量のデータをインポート/エクスポートできます。これは、データ ファイルからデータ値を一括インポートする場合に役立ちます。データ ファイル内のデータ フィールドの数と順序は、宛先テーブルの列のものとは異なる場合があります。これは、データをインポートするための列の順序とタイプを指定することにより、BCP データ形式ファイルが役立つ場合です。

フォーマットファイルの構造は、次の形式で表されます。

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP データ型

|データ型|範囲|表現|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) から 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|バイナリ|1 ～ 8000 バイト|16 進数でエンコードされた Unicode 文字列形式 `バイナリ = 32000OCTET`|
|ビット|0 または 1|単純な Unicode 文字列 ビット = "0" / "1"|
|文字|1 ～ 8000|Unicode 文字列形式、文字 = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET with n = 4 x (2,147,483,647)|
|日付|0001-01-01 から 9999-12-31|YYYY-MM-DD 文字列形式|
|日時|1753-01-01 00:00:00.000 から 9999-12-31 23:59:59.997| Unicode YYYY-MM-DD hh:mm:ss[.nnn] 文字列形式|
|DateTime2|0001-01-01 00:00:00.0000000 ～ 9999-12-31 23:59:59.9999999.| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] 文字列形式|
|DateTimeOffset|0001-01-01 00:00:00.0000000 ～ 9999-12-31 23:59:59.9999999 (協定世界時 (UTC) タイム ゾーン)| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] 文字列形式|
|Decimal|-1038 + 1 ～ 1038 – 1|Unicode 文字列形式 `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|フロート|-1.79E+308 ～ -2.23E-308; 0; 2.23E-308 から 1.79E+308 まで|Unicode 文字列形式|
|画像|0 ～ 231 – 1 (2,147,483,647) の範囲のバイトのシーケンス|16 進数でエンコードされた Unicode 文字列形式|
|Int|-231 (-2,147,483,648) ～ 231 – 1 (2,147,483,647)|Unicode 文字列形式|

## 参考文献

* [BCP 形式 - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

