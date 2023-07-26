{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell スクリプト ファイル形式",
  "description":"HS ファイル形式とは何か,および HS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet ファイル形式

## Java HS ファイルとは何ですか?

Java プログラミング言語の .hs 拡張子を持つファイルは、アプリケーションによってアクティブ化されたときに JavaHelp システムによって使用されるヘルプ ドキュメント ファイルです。これは、インストールされた特定のアプリケーションのヘルプセットを定義し、アプリケーションのシステム ヘルプの一部として複数のサブセットで構成されます。 Java プログラムは、名前が .hs 拡張子で終わるヘルプセット ファイルを見つけることができなければなりません。

## Java ヘルプセット情報

.hs ファイルには、次の情報が含まれる場合があります。

|情報|説明|
---|---|
|マップ ファイル|マップ ファイルは、トピック ID をハイパーテキスト マークアップ言語トピック ファイルのパス名またはユニフォーム リソース ロケーターに関連付けるために使用されます。|
|ビュー情報|ヘルプセット内で使用されているナビゲーターを説明する情報。品質ナビゲーターは、目次、索引、および全文検索です。追加のナビゲーターには、グロスとお気に入りのナビゲーターが含まれます。カスタムナビゲーターに関するデータは、ここにさらに含まれています.|
<html>|ヘルプセットのタイトル|\<title>ヘルプセット (.hs) ファイル内で概説されています。このタイトルは、ヘルプセット ファイルで概説されているほとんどのウィンドウとセカンダリ ウィンドウの最上位に表示されます。| </html>
|ホーム ID|アシスタンス ウォッチャーが ID を示さずに呼び出されたときに表示される (既定の) ID のタイトル。
|プレゼンテーション|支援対象を表示するウィンドウ。これは、JavaHelp 2 コンピュータ プログラムの最新のインクルードである可能性があり、\<presentation> .|
|サブヘルプセット|この任意領域は、タグを利用して他のヘルプセットを静的に組み込みます。このタグで表示されるヘルプセットは、タグを含むヘルプセットに自然に結合されます。ブレンディングに関するその他の興味深い点は、ブレンディング ヘルプセットで見つけることができます。|
|実装|この裁量セグメントは、HelpSet.createHelpBroker メソッド内で使用する HelpBroker クラスを特徴付けるキー情報マッピングを提供するレジストリを作成します。さらにレジストリは、指定されたエミュレート ソートのサブスタンス ビューアーをクライアントに決定します。|

## Java HS ファイル形式

Java HS ファイルは XML ファイル形式であり、World Wide Web Consortium (W3C) Extended Markiup Language 提案の勧告 [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208)。これは、Java HS ファイルが人間が判読できる XML ファイル形式であり、任意の XML リーダー アプリケーションで開くことができることを意味します。

### Java HS ファイル形式の例

以下は、[Oracle Helpset ドキュメント](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)からのヘルプセット ファイルの例です。

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## 参考文献
* [Oracle Java Helpset ファイル](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell スクリプト ファイル形式

## .HS オプション番号

拡張子が .hs のファイルは、[Haskell](https://wiki.haskell.org/Haskell) で記述された Haskell スクリプト ファイルであり、高度な純粋関数型オープン ソース プログラミング言語です。 HS ファイルに記述されたコードは、[C](/programming/c/)、[C++](/programming/cpp/) などとは異なり、堅牢で簡潔なソフトウェアの迅速な開発の原則に従う純粋な関数に基づいています。 Haskell は、柔軟で高品質なアプリケーションを作成するために、豊富な API、プロファイラー、およびデバッガーと共に組み込みの並行性と並列処理を提供します。

## HSファイル形式

他のプログラミング言語と同様に、HS ファイルは人間が読めるプレーン テキスト形式で記述されます。これらは、使用可能なテキスト ツールを使用して作成、編集、および表示できます。 .hs ソース コード ファイルは Haskell コンパイラでコンパイルされ、実行可能なバイナリ ファイルが生成されます。

### HS ファイル形式の例

コードは .hs ファイルに記述し、[GHC](https://haskell.org/ghc) などの Haskell コンパイラを使用してコンパイルできます。次のサンプルに示すように、次のコード行は `HelloWorld.hs` として保存されます。

```
main = putStrLn "Hello, World!"
```

これは、次のコマンドを使用してコンパイルされます。

```
$ ghc -o hello hello.hs
```
結果の実行可能ファイルは次のように実行できます。

```
$ ./hello
```
これにより、「Hello, World!」が出力されます。出力へのステートメント。

## 参考文献

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell の 5 つの簡単なステップ](https://wiki.haskell.org/Haskell_in_5_steps)

