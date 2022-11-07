{
  "date" : "2019-10-11",
  "keywords" :[ "fodg ファイル", "fodg ファイル形式", "fodg ファイルとは", "ファイル", "fodg の例", "fodg ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument 図面ファイル形式",
  "description":"FODG ファイル形式と,FODG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .FODG オプション番号

拡張子が .fodg のファイルは、描画要素を格納するための Apache OpenOffice Drawing ファイル形式です。これは、Advancement of Structural Information Standards (OASIS) によって概説されているファイル形式の仕様に基づいています。 OpenOffice グラフィックスの別の同様のファイル形式は [ODG](/image/odg/) で、描画要素をベクター画像として保存します。 FODG ファイルは、OpenOffice と LibreOffice で開くことができます。 OpenOffice でサポートされているその他のファイル形式には、[ODT](/word-processing/odt/)、ODF、[ODP](/presentation/odp/)、[ODS](/spreadsheet/ods/) などがあります。

## FODG ファイル形式

FODG は、OASIS OpenDocument Format ISO/IEC 26300 に準拠する OpenDocument の XML ファイル形式に基づいています。これには、インターネット メディア タイプ application/vnd.oasis.opendocument.graphics があり、org.oasis-open.opendocument public.composite-content にも準拠しています。 . XML 構造は、スプレッドシート、図面ファイル、テキスト ドキュメントなど、すべてのドキュメント タイプに共通です。 OpenOffice ドキュメントは、コンテンツ、スタイル、メタデータ、およびアプリケーション設定を 4 つの個別の XML ファイルに分離することにより、関心の分離を利用します。

`<office:document-content> ` - ドキュメント コンテンツとコンテンツで使用される自動スタイル。
`<office:document-styles> ` - ドキュメント コンテンツで使用されるスタイルと、スタイル自体で使用される自動スタイル。
`<office:document-meta> ` - 作成者や最後の保存アクションの時刻などのメタ情報を文書化します。
`<office:document-settings> ` - ウィンドウ サイズやプリンター情報など、アプリケーション固有の設定。

## 参照 ##
* [v 1.3 標準化の将来仕様](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument 形式 - ウィキペディア](https://en.wikipedia.org/wiki/OpenDocument)

