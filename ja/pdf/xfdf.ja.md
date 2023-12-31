{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF ファイル形式 - XFDF ファイルとは?",
  "description":"XFDF ファイルと,XFDF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## XFDF ファイルとは?

拡張子が .xfdf のファイルは、Adobe Acrobat ソフトウェアで生成される XML フォーム データ形式です。 [FDF](/pdf/fdf/) と同様に、XFDF にはフォーム要素の説明とその値が XML 形式で含まれています。これには、PDF フォームのテキスト フィールドの名前と値を含めることができます。 XFDF は人間が読める形式で保存され、C# などのプログラミング言語を使用してプログラムで読み取ることができます。

## XFDF ファイル形式 - 詳細情報

XFDF ファイルは、データのインポートとエクスポートに使用される汎用形式である XML ファイル形式で保存されます。 XFDF ファイル構造は、以下に示すように、ヘッダー、それに続くフィールド値、および要素データで構成されます。

|要素|属性|コンテンツ|
---|---|---|
|\<XFDF> ||最上位の要素|
|\<fields> ||このテンプレートのすべてのフィールド値|
| |<field (T)> |名前 |フィールド名|
| |<value (V)> |値 |フィールド値|

## 参考文献

* [Acrobat による FDF 形式のサポート](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [アドビ開発者向けリソース](https://opensource.adobe.com/)

