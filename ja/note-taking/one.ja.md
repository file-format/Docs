{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote ファイル形式",
  "description":"ONE ファイル形式と,ONE ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## .ONE ファイルとは何ですか? ##

.ONE 拡張子で表されるファイルは、Microsoft OneNote アプリケーションによって作成されます。 OneNote を使用すると、下書きパッドを使用してメモを取っているかのように、アプリケーションを使用して情報を収集できます。 OneNote ファイルには、ドキュメント ページの固定されていない場所に配置できるさまざまな要素を含めることができます。これらの要素には、テキスト、デジタル化された手書き、および画像、描画、マルチメディア (オーディオ/ビデオ) クリップなど、他のアプリケーションからコピーされたオブジェクトが含まれる場合があります。 Microsoft は現在、Office365 の一部として OneNote のオンライン バージョンを提供しており、インターネット経由で他の OneNote ユーザーと Notes を共有できます。

## .ONE ファイル形式の仕様 ##

OneNote ファイル形式は、デジタル ノートをセクションとページの階層セットとして表現する効果的な方法を提供します。各ページには、ファイル形式のドキュメント オブジェクト モデル (DOM) で表現するために、特定の構造でユーザー定義のコンテンツが含まれています。この形式の のデータ モデルは次の図のようになります。

### 構造の概要 ###

OneNote ファイル形式のデータ モデルに示されているように、OneNote ドキュメントはさまざまな要素で構成されています。

＃＃＃＃ セクション ＃＃＃＃

セクションは、次のようなさまざまな要素をさらに含む OneNote ファイルの最上位のコンテナーです。

* ページ
* メタデータ
* プロパティ

メタデータとプロパティには、セクション名、セクションに含まれるページの識別、およびそれらのページが表示される順序が含まれます。 「セクション」という用語は、セクション内のすべてのページと、.one ファイル名拡張子を持つ OneNote® リビジョン ストア ファイル内のそのデータの表現を指します。

#### ページ ####

OneNote ドキュメントのユーザー定義コンテンツは、ページ内に含まれています。ページ情報には、テキスト、リスト、表、ページ タイトル、画像、メモ タグが含まれます。ページは、含まれているほとんどのオブジェクトが追加されたアウトライン オブジェクトで構成されます。各ページには意味のある表現の名前を割り当てることができ、オブジェクトをページに直接追加することもできます。ページには、階層システムのサブページをさらに含めることができます。

#### プロパティとプロパティ セット ####

OneNote のコンテンツは、プロパティ、プロパティ セット、およびファイル データ オブジェクトで構成されます。プロパティ セットは、ある種のコンテンツを表すプロパティのコレクションです。ファイル データ オブジェクトは、画像、埋め込みファイル、またはオーディオ/ビデオ コンテンツを含むバイナリ データのブロックです。

#### OneNote ノートブック ####

ノートブックは、同じディレクトリに格納されているセクション ファイルのコレクションです。プロパティのコレクションを使用して、ノートブック内のセクションの順序やノートブックの色などの設定を指定します。

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

|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 バイト):` 符号なし整数。このファイルのファイル形式に応じて、次の表の値のいずれかでなければなりません。

|ファイル形式|値
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 バイト):` 「fcrZero」の値を持たなければならない **FileChunkReference32** 構造。

`fcrLegacyTransactionLog (8 バイト):` 「fcrNil」でなければならない **FileChunkReference32** 構造。

`cTransactionsInLog (4 バイト):` トランザクション ログ内のトランザクション数を指定する符号なし整数。ゼロであってはなりません。

`cbLegacyExpectedFileLength (4 bytes):`ゼロでなければならず、無視されなければならない符号なし整数。

`rgbPlaceholder (8 バイト):` ゼロでなければならず、無視されなければならない符号なし整数。

`fcrLegacyFileNodeListRoot (8 バイト):` 「fcrNil」でなければならない **FileChunkReference32** 構造。

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):`ゼロでなければならず、無視されなければならない符号なし整数。

`fNeedsDefrag (1 バイト):` は無視する必要があります。

`fRepairedFile (1 バイト):` は無視する必要があります。

`fNeedsGarbageCollect (1 バイト):` は無視する必要があります。

`fHasNoEmbeddedFileObjects (1 byte):`ゼロでなければならず、無視されなければならない符号なし整数。

`guidAncestor (16 バイト):` 目次ファイルの **Header.guidFile** フィールドを指定する GUID。次の表で指定します。


|目次ファイル形式|目次ファイルの場所
--- | --- |
|セクション ファイル - .One|目次ファイルは、このファイルと同じディレクトリにあります。
|目次ファイル - .onetoc2|目次ファイルは、このファイルの親ディレクトリにあります。

GUID が {00000000-0000-0000-0000-000000000000} の場合、このフィールドは目次ファイルを参照しません。

`crcName (4 バイト):` このリビジョン ストア ファイルの名前の CRC 値を指定する符号なし整数。名前は、ファイル名の Unicode 表現であり、拡張子と最後に追加のヌル文字が含まれています。この CRC は、このリビジョン ストア ファイル形式に関係なく、常に .one ファイルの CRC アルゴリズムを使用して計算されます。

`fcrHashedChunkList (12 バイト):` ハッシュされたチャンク リストの最初の **FileNodeListFragment** への参照を指定する **FileChunkReference64x32** 構造。 **FileChunkReference64x32** 構造体の値が "fcrZero" または "fcrNil" の場合、ハッシュされたチャンク リストは存在しません。

`fcrTransactionLog (12 バイト):` トランザクション ログの最初の **TransactionLogFragment** 構造への参照を指定する **FileChunkReference64x32** 構造。 **fcrTransactionLog** フィールドの値は、「fcrZero」であってはならず、「fcrNil」であってはなりません。

`fcrFileNodeListRoot (12 バイト):` ルート ファイル ノード リストへの参照を指定する **FileChunkReference64x32** 構造。 **fcrFileNodeListRoot** フィールドの値は、「fcrZero」であってはならず、「fcrNil」であってはなりません。

`fcrFreeChunkList (12 バイト):` 最初の **FreeChunkListFragment** 構造への参照を指定する **FileChunkReference64x32** 構造。 **FileChunkReference64x32** 構造体の値が「fcrZero」または「fcrNil」の場合、フリー チャンク リストは存在しません。

`cbExpectedFileLength (8 バイト):` このリビジョン ストア ファイルのサイズをバイト単位で指定する符号なし整数。

`cbFreeSpaceInFreeChunkList (8 bytes):` フリー チャンク リストで指定されたフリー スペースのサイズをバイト単位で指定する必要がある符号なし整数。

`guidFileVersion (16 バイト):` GUID。 **cTransactionsInLog** フィールドまたは **guidDenyReadFileVersion** フィールドの値が変更されている場合、**guidFileVersion** を新しい GUID に変更する必要があります。

`nFileVersionGeneration (8 バイト):` ファイルが変更された回数を指定する符号なし整数。 **guidFileVersion** フィールドが変更されたときにインクリメントする必要があります。

`guidDenyReadFileVersion (16 バイト):` GUID。ファイルの **Header** 構造と未使用のストレージ ブロックを除いて、ファイルの既存の内容を変更する場合、**guidDenyReadFileVersion** を新しい GUID に変更する必要があります。

`grfDebugLogFlags (4 バイト):` ゼロでなければなりません。無視しなければなりません。

`fcrDebugLog (12 バイト):` 値 "fcrZero" を持たなければならない **FileChunkReference64x32** 構造。無視しなければなりません。

`fcrAllocVerificationFreeChunkList (12 バイト):` 「fcrZero」でなければならない **FileChunkReference64x32** 構造。無視しなければなりません。

`bnCreated (4 バイト):` このリビジョン ストア ファイルを作成したアプリケーションのビルド番号を指定する符号なし整数。無視すべきです。

`bnLastWroteToThisFile (4 バイト):` このリビジョン ストア ファイルに最後に書き込んだアプリケーションのビルド番号を指定する符号なし整数。無視すべきです。

`bnOldestWritten (4 バイト):` このリビジョン ストア ファイルに書き込んだ最も古いアプリケーションのビルド番号を指定する符号なし整数。無視すべきです。

`bnNewestWritten (4 バイト):` このリビジョン ストア ファイルに書き込んだ最新のアプリケーションのビルド番号を指定する符号なし整数。無視すべきです。

`rgbReserved (728 バイト):` ゼロでなければなりません。無視しなければなりません。

## 参照 ##

* [[MS-ONESTORE] - OneNote ファイル形式](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - ウィキペディア](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

