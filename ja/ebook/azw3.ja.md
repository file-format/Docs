{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extension", "file", "format", "eBook", "Kindle File Format", "AZW3 File Structure" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AZW3 ファイル形式と,AZW3 ファイルを作成して開くことができる API について学びます。",
  "title" :"AZW3 ファイルとは何ですか?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## AZW3 ファイルとは何ですか?

AZW3 は、Kindle フォーマット 8 (**KF8**) とも呼ばれ、Amazon Kindle デバイス用に開発された [AZW](/ebook/azw/) 電子ブック デジタル ファイル形式の修正版です。この形式は古い AZW ファイルを拡張したもので、Kindle Fire デバイスでのみ使用され、元のファイル形式、つまり [MOBI](/ebook/mobi/) および AZW との下位互換性があります。 Amazon は、最新の Kindle デバイスで使用されている KF8 の後に KFX (KF バージョン 10) 形式を導入しました。 AZW3 ファイルのインターネット メディア タイプは、application/vnd.amazon.mobi8-ebook です。 AZW3 ファイルは、[PDF](/pdf/)、[EPUB](/ebook/epub/)、[AZW](/ebook/azw/)、[DOCX](/ word-processing/docx/)、および [RTF](/word-processing/rtf/)。

## AZ3/KF8 ファイル形式 ##

KF8 ファイルは本質的にバイナリであり、MOBI ファイル形式の構造を PDB ファイルとして保持します。前述のように、KF8 ファイルは MOBI と EPUB の新しい KF8 バージョンの両方で構成される場合があります。フォーマットの内部詳細は、[Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) によってデコードされています。これは、最終的にコンパイルされたデータベースを解析し、そこから MOBI または AZW ソース ファイルを抽出する Python スクリプトです。 AZW3 (KF8) ファイルは、EPUB の下位互換性を持つ EPUB3 バージョンも対象としています。 KF8 は EPUB ファイルをコンパイルし、PDB ファイル形式に基づいてバイナリ構造を生成します。

## 参照 ##

* [KF8 - ウィキペディアによる](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle アンパック](https://github.com/kevinhendricks/KindleUnpack)

