{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODTTF ファイル - 難読化された OpenType フォント ファイル形式",
  "description":"ODTTF ファイル形式と,ODTTF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## .ODTTF ファイルとは何ですか?

ODTTF ファイルは、[.XPS](/ja/page-description-language/xps/) および Microsoft Office 2007 ファイル形式で使用されるフォント ファイル形式です。難読化された OpenType フォントが含まれており、フォントのデザイン情報の抽出やフォントのソース コードのリバース エンジニアリングを困難にするために変更されています。 ODTTF は、元のドキュメントで使用されているフォントに基づいていますが、プレーン フォーマットではなく、フォント データを抽出するためにサードパーティ ソフトウェアで読み取れない場合があります。

Pagemark XpsViewer、Pagemark XpsPlugin を使用した Apple Safari、Pagemark XpsPlugin を使用した Mozilla Firefox を使用して ODTTF ファイルを開くことができます。
NiXPS ビュー、および NiXPS 編集。

## ODTTF ファイル形式

ODTTF ファイル形式の内部ファイル形式構造は、難読化された埋め込み形式として格納されているため不明です。これらは、.PDF や .DOCX などのデジタル ドキュメントに埋め込むことができます。

## 参考文献
* [マイクロソフトによる OpenType フォント仕様](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType の概要](https://learn.microsoft.com/en-us/typography/truetype/)

