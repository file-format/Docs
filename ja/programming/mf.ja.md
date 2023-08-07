{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java マニフェスト ファイル形式",
  "description":"MF ファイル形式と,MF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .MF オプション番号

拡張子が .mf のファイルは、個々の [JAR](/programming/jar/) ファイル エントリに関する情報を含む Java マニフェスト ファイルです。 MF ファイル自体は JAR ファイル内に含まれ、すべての拡張機能とパッケージ関連の定義を提供します。 JAR ファイルを生成して、実行可能ファイルとして使用できます。このような場合、mainfest ファイルは **`public static void main`** ステートメントを含むアプリケーションのメイン クラスを指定します。マニフェスト ファイルは MANIFEST.MF という名前で、Windows、MacOS、および Linux オペレーティング システムの任意のテキスト エディターで開くことができます。

## マニフェストファイル形式の仕様

[マニフェスト ファイル形式の仕様](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) は、Oracle の JAR ファイル形式のガイドで入手できます。マニフェスト ファイルは、個々の JAR ファイル エントリのセクションのリストが続くメイン セクションで構成されます。各セクションは、いくつかの規則と制限に従います。

### 主なセクション

主なセクション:

* JAR ファイルに関するセキュリティと構成に関する情報が含まれています
* JAR ファイルが含まれているアプリケーションまたは拡張機能に関する情報が含まれています。
* 個々のマニフェスト項目ごとに主な属性を定義します

**注**: このセクションの属性に「名前」という名前を付けることはできません。

### 個々のセクション

個々のセクションは、JAR ファイルのパッケージまたはファイルのさまざまな属性を定義します。各セクションは「名前」という名前の属性で始まる必要があり、その値はファイルへの相対パス、またはアーカイブ外のデータを参照する絶対 URL でなければなりません。

### マニフェスト仕様

|属性|説明|
---|---|
|マニフェストファイル|メインセクション改行*個別セクション|
|main-section|バージョン情報改行 *main-attribute|
|version-info|Manifest-Version : バージョン番号|
|バージョン番号|桁+{.桁+}*|
|main-attribute|(正当なメイン属性) newline|
|個別セクション|名前 : 値改行 *perentry-attribute|
|perentry-attribute|(任意の正当な perentry 属性) newline|
|改行|CR LF | LF | CR (後に LF が続かない)|
|桁|{0-9}|

## 参考文献

* [Oracle - JAR ファイル形式](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR ファイル形式](https://en.wikipedia.org/wiki/JAR_(file_format))

