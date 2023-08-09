{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FDF ファイル形式 - FDF ファイルとは?",
  "description":"FDF ファイル形式と,FDF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## .FDF オプション番号

FDF (**Forms Data Format**) ファイルは、[PDF](/pdf/) ファイルのフォーム フィールドからデータをエクスポートすることによって生成されるテキスト ドキュメントです。 PDF ファイルで使用可能なフォーム フィールドから抽出されたテキスト フィールド データのみが含まれます。エクスポートされたデータにはフォーム自体が含まれていないため、これにより比較的小さなデータ ファイルが作成されます。 Adobe Acrobat は、アプリケーション メニューの [フォーム データのエクスポート] オプションを使用して、フォーム フィールド データをエクスポートする機能を提供します。

## FDF ファイル形式 - 詳細情報

FDF はプレーン テキスト形式であり、Portable Document Format の [ISO 32000 標準](https://www.iso.org/standard/51502.html) の一部として含まれています。これは、Acrobat Forms または AcroForms からのデータのインポートおよびエクスポートを可能にするために Adobe によって開発されました。

FDF ファイルには次の 2 種類があります。

• `Classic FDF` – 既存の静的フォームに入力するデータを提供します。

• `Template FDF` – 指定された PDF ファイル内のテンプレートに基づいて新しい PDF を構築します。新しいドキュメント内のフォームは、データを提供することによって入力されます。

## Adobe Acrobat を使用した FDF の作成

Adobe の [FDF ツールキット](https://opensource.adobe.com/dc-acrobat-sdk-docs/) を使用すると、テキスト データから FDF ファイルを作成できます。

## 参照 ##

* [Acrobat による FDF 形式のサポート](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [アドビ開発者向けリソース](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

