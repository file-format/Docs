{
  "date" : "2020-08-20",
  "keywords" :[ "cff ファイル", "cff ファイル形式", "cff ファイルとは", "ファイル", "cff の例", "cff ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - コンパクト フォント ファイル形式",
  "description":"CFF ファイル形式と,CFF ファイルを作成して開くための API について学びます。",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .CFF オプション番号

拡張子が .cff のファイルはコンパクト フォント形式であり、PostScript Type 1 または CIDFont とも呼ばれます。 CFF は、FontSet と呼ばれる 1 つのユニットに複数のフォントをまとめて格納するコンテナーとして機能します。 CFF フォントの設計により、PostScript 言語コードを埋め込むことができるため、プリンター環境で使用するためのフォーマットの柔軟性と拡張性がさらに向上します。 CFF フォント ファイルは、[Aspose.Font](https://products.aspose.com/font) などの API を使用して開いたり変換したりできます。

## CFF ファイル形式

CFF ファイルは、構造化されたデータ レイアウトを含むバイナリ ファイルであり、データ型、ヘッダー、グリフ構成、およびテーブル ディクショナリが定義されています。これらの詳細については、[コンパクト フォント形式の仕様](https://docs.microsoft.com/en-us/typography/opentype/spec/cff) を参照してください。

### データレイアウト
CFFファイル形式のデータ配置は以下の通りです。

|エントリー|コメント|
---|---|
|ヘッダー|–|
|NameINDEX|–|
|トップ DICT インデックス|–|
|文字列インデックス|–|
|グローバルサブインデックス|–|
|エンコーディング–文字セット|–|
|FDSelect|CIDFonts のみ|
|CharStrings INDEX|フォントごと|
|フォント DICT INDEX|フォントごと、CIDFonts のみ|
|プライベート DICT|フォントごと|
|Local Subr INDEX|フォントごとまたは CIDFonts のプライベート DICT|
|著作権および商標に関する通知|–|

### データ型

CFF のデータ型は次の表のとおりです。

|名前|範囲|説明|
---|---|---|
|Card8|0 –255|1 バイトの符号なし数値|
|Card16|0 – 65535|2 バイトの符号なし数値|
|オフセット|変化します|1、2、3、または 4 バイトのオフセット (OffSize フィールドで指定)|
|OffSize|1 ～ 4|1 バイトの符号なし数値は、1 つまたは複数のオフセット フィールドのサイズを指定します|
|SID|0 ～ 64999|2 バイトの文字列識別子|

### ヘッダー

バイナリ データは、次の表に示す形式のヘッダーで始まります。

|タイプ|名前|説明|
---|---|---|
|Card8|major|フォーマット メジャー バージョン (1 から始まる)|
|Card8|minor|フォーマット マイナー バージョン (0 から始まる)|
|Card8|hdrSize|ヘッダー サイズ (バイト)|
|OffSize|offSize|絶対オフセット (0) サイズ|

## 参考文献

* [コンパクト フォント フォーマット表](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
※【CFFファイル形式】(https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 チャートセット](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

