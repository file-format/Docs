{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote ファイル形式",
  "description":"ONETOC2 ファイル形式と,ONETOC2 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ONETOC2とは？ ##

[Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) アプリケーションを使用したことがある方は、ノートブック フォルダーに .onetoc2 ファイルが存在することに気付いたかもしれません。 Microsoft OneNote は、ノートブック内のさまざまなメモ作成セクションの順序に関するインデックスを保持するための目次としてバイナリ .onetoc2 ファイルを作成します。ノートブックは、同じディレクトリに格納されているセクション ファイルのコレクションです。 .onetoc2 ファイルは、一連のプロパティを使用して、ノートブック内のセクションの順序やノートブックの色などの設定を指定します。

OneNote 2016 でノートブックを作成すると、新しい 2010-2016 ファイル形式で自動的に保存されます。数式やリンクされたノートなど、OneNote 2016 のすべての機能を正しく動作させるには、この形式が必要です。

## ONETOC2 ファイル形式 ##

.onetoc2 ファイル形式は、OneNote リビジョン ストア ファイル形式として表され、相互参照されたオブジェクト スペースに編成されたリビジョン ストアを指定する構造のコレクションであり、プロパティ セットを持つオブジェクトを含み、トランザクション ログを含み、非同期全体でファイルの整合性を確保します。書いています。 .onetoc2 ファイル形式の完全な仕様は [オンライン] (https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) で入手でき、アプリケーションの開発に参照できます。 .

### ファイル構造 ###

リビジョン ストア ファイルは **Header** 構造で始まる必要があります。ファイルの残りの部分は、バイトのブロックに分割されます。各ブロックのサイズと構造は、それを参照するフィールドによって指定されます。 **Header** 構造によって参照されている場合、または別の到達可能なブロックのフィールドによって参照されている場合、ブロックは到達可能です。 **Header** 構造外のデータと到達可能なブロックは無視する必要があります。

すべての構造体は、1 バイト境界で位置合わせされます。特に指定のない限り、すべての整数は符号付きです。特に指定がない限り、すべてのフィールドは [リトル エンディアン](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) です。

#### ヘッダー ####

.ONE ファイルのヘッダーは、次のようにファイル情報を表現するためのさまざまな一意の ID とフィールドを含むチャンクで構成されます。

`guidFileType (16 バイト):` リビジョン ストア ファイルのタイプを指定する GUID。次の表のいずれかの値でなければなりません。

|ファイル形式|値
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 バイト):` このリビジョン ストア ファイルの ID を指定する GUID。グローバルに一意であるべきです。

`guidLegacyFileVersion (16 バイト):` 「{00000000-0000-0000-0000-000000000000}」でなければならず、無視しなければなりません。

`guidFileFormat (16 バイト):` ファイルがリビジョン ストア ファイルであることを指定する GUID。 「{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}」でなければなりません。

`ffvLastCodeThatWroteToThisFile (4 バイト):` 符号なし整数。ファイルの種類に応じて、次の表の値のいずれかでなければなりません。

|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 バイト):` 符号なし整数。このファイルのファイル形式に応じて、次の表の値のいずれかでなければなりません。


|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 バイト):` 符号なし整数。このファイルのファイル形式に応じて、次の表の値のいずれかでなければなりません。
:


|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 バイト):` 符号なし整数。このファイルのファイル形式に応じて、次の表の値のいずれかでなければなりません。


|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## 参照 ##

* [[MS-ONESTORE] - OneNote ファイル形式](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - ウィキペディア](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

