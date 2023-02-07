{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZST ファイル - Zstandard 圧縮ファイル形式",
  "description":"ZST ファイル形式と,ZST ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## .ZSTファイルとは何ですか?

ZST ファイルは、Zstandard (zstd) 圧縮アルゴリズムで生成された圧縮ファイルです。アルゴリズムによる可逆圧縮で作成された圧縮ファイルです。 ZST ファイルは、データベース、ファイル システム、ネットワーク、ゲームなど、さまざまな種類のファイルを圧縮するために使用できます。 Zstandard は、[RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) によって管理されており、全体的な圧縮メカニズム、メディア タイプ、およびコンテンツ エンコーディングが記述されています。

## ZST ファイル形式

ZST ファイルは圧縮ファイル形式でディスクに保存されます。圧縮メカニズムは、RFC 8478 を廃止する RFC 8878 で説明されているとおりです。

## ZST フレーム

ZST ファイルは、1 つまたは複数のフレームで構成されます。各フレームは、Zstandard フレームまたはスキップ可能なフレームのいずれかです。 Zstandard フレームには圧縮データが含まれますが、スキップ可能なフレームにはカスタム ユーザー メタデータが含まれます。

### Z標準フレーム

Zstandard フレームの構造は次のとおりです。

|フィールド|バイト単位のサイズ|
---|---|
|Magic_Number |4 バイト|
|Frame_Header |2 ～ 14 バイト|
|Data_Block |n バイト|
|[さらに Data_Blocks] ||
|[Content_Checksum] |4 バイト|

### スキップ可能なフレーム

スキップ可能なフレームを使用すると、連結されたフレームのフローにユーザー定義のメタデータを挿入できます。スキップ可能なフレームの構造は次のとおりです。

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 バイト |4 バイト |n バイト|

## 参照 ##

* [RFC 8878 Zstandard 圧縮](https://www.rfc-editor.org/rfc/rfc8878)

