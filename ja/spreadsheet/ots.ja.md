{
  "date" : "2019-12-16",
  "keywords" :["OTS","ファイル","拡張子","ファイル形式","Excel","スプレッドシート"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"OTS ファイル形式と,OTS ファイルを作成して開くことができる API について学びます。",
  "title" :"OTS - OpenDocument スプレッドシート テンプレート ファイル形式",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## .OTS ファイルとは?

拡張子が .ots のファイルは、Apache OpenOffice に含まれる Calc アプリケーション ソフトウェアで作成された OpenDocument スプレッドシート テンプレート ファイルです。 Calc アプリケーション ソフトウェアは、Microsoft Office で利用できる Excel に似ています。 OTS ファイル形式は、スタイル、フォント、データ、スプレッドシートのレイアウト、および書式設定に関連する定義済みの設定を含むテンプレートを作成するために使用されます。 OTF ファイルには `mime-type application/vnd.oasis.opendocument.spreadsheet-template` があります。これらのテンプレート ファイルは、[ODS ファイル形式](/spreadsheet/ods/) で保存される実際のデータ ファイルを生成および保存するための出発点として使用できます。 OTS ファイルは、OpenOffice や LibreOffice などのアプリケーションで使用できます。

## OTS ファイル形式

OTS ファイルは OASIS の OpenDocument XML ベースのファイル形式で保存され、[ZIP](/compression/zip/) アーカイブとしてパッケージを含む複数のサブドキュメントのコレクションで構成されます。各 zip アーカイブにはドキュメント全体の一部が格納され、各サブドキュメントにはドキュメントの特定の側面が格納されます。たとえば、あるサブドキュメントにはスタイル情報が含まれ、別のサブドキュメントにはドキュメントのコンテンツが含まれます。一般的な ODF ドキュメントには、次のコンポーネントがあります。

### OTS Content.xml

content.xml ファイルには、ドキュメントの実際のコンテンツが含まれています。ただし、これには画像などのバイナリ データは含まれません。
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS ファイル形式の Styles.xml

styles.xml ファイルにはスタイル情報が含まれており、書式設定とレイアウトに頻繁に使用されます。スタイルの種類は次のとおりです。

* 段落スタイル
* ページのスタイル
* 文字スタイル
* フレームスタイル
*リストスタイル

### メタ.xml

meta.xml ファイルには、作成者、最終更新日など、ファイルのメタデータに関する情報が含まれています。
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

`settings.xml` ファイルには、ズーム倍率やカーソル位置などのドキュメント レベルの設定が含まれています。

## 参照 ##

* [OpenDocument 1.2 仕様](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - ウィキペディアによる](https://en.wikipedia.org/wiki/OpenDocument)

